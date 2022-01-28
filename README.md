name: krunal timbadiya
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user:krunaltimbadiya
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Calcutta
          plugin_achievements: yes
          plugin_achievements_secrets: yes
          plugin_achievements_threshold: C
          plugin_activity: yes
          plugin_activity_days: 14
          plugin_activity_filter: all
          plugin_activity_limit: 5
          plugin_activity_load: 300
          plugin_activity_visibility: all
          plugin_contributors: yes
          plugin_contributors_head: master
          plugin_contributors_ignored: github-actions[bot], dependabot[bot], dependabot-preview[bot]
          plugin_followup: yes
          plugin_followup_sections: repositories
          plugin_gists: yes
          plugin_habits: yes
          plugin_habits_days: 14
          plugin_habits_facts: yes
          plugin_habits_from: 200
          plugin_introduction: yes
          plugin_introduction_title: yes
          plugin_isocalendar: yes
          plugin_isocalendar_duration: full-year
          plugin_languages: yes
          plugin_languages_colors: github
          plugin_languages_indepth: yes
          plugin_languages_limit: 8
          plugin_languages_recent.days: 14
          plugin_languages_recent.load: 300
          plugin_languages_sections: most-used
          plugin_languages_threshold: 0%
          plugin_licenses: yes
          plugin_licenses_legal: yes
          plugin_licenses_ratio: yes
          plugin_lines: yes
          plugin_pagespeed: yes
          plugin_pagespeed_detailed: yes
          plugin_pagespeed_screenshot: yes
          plugin_pagespeed_url: .user.website
          plugin_people: yes
          plugin_people_identicons: yes
          plugin_people_limit: 24
          plugin_people_shuffle: yes
          plugin_people_size: 28
          plugin_people_types: followers, following
          plugin_posts: yes
          plugin_posts_limit: 4
          plugin_posts_source: hashnode
          plugin_posts_user: .user.login
          plugin_projects: yes
          plugin_projects_descriptions: yes
          plugin_projects_limit: 4
          plugin_skyline: yes
          plugin_skyline_compatibility: yes
          plugin_skyline_frames: 60
          plugin_skyline_quality: 0.5
          plugin_skyline_year: 2020
          plugin_stargazers: yes
          plugin_stars: yes
          plugin_stars_limit: 4
          plugin_support: yes
          plugin_topics: yes
          plugin_topics_limit: 15
          plugin_topics_mode: mastered
          plugin_topics_sort: stars
          plugin_traffic: yes
          plugin_tweets: yes
          plugin_tweets_limit: 2
          repositories_forks: yes


