# TRMNL plugins

non-exhaustive collection of TRMNL plugin logic. in sharing these assets we intend to provide transparency in how TRMNL manages user data with respect to 3rd party integrations.

## Featured plugins

**native**
- [GitHub Commit Graph](/lib/github_commit_graph)
- [Hacker News](/lib/hacker_news)
- [Lunch Money](/lib/lunch_money)
- [Stock Price](/lib/stock_price)
- [Tempest Weather Station](/lib/tempest_weather_station)

native plugin structure:

1. file `plugin_name.rb` represents an instance of a PluginSetting (user-owned), which belongs to a Plugin (global, immutable)
2. screens are generated by first invoking `Plugins::<PluginName>.new(plugin_setting).locals`
3. the `locals` hash / JSON object contains all the values needed for rendering a screen
4. files inside `/views` interpolate values from `locals` using ERB syntax (`<%= var %>`)
5. views prefixed with `_`, for example `_common`, are called "partials" (or 'components' in other frameworks)
6. shared code is not intended to "just work" but to showcase which values, and how, are extracted from 3rd party apps for TRMNL screen generation

**by the community**
- [(USA) Top 10 College Football Rankings](/lib/usa_college_football_rankings.md) by [@SnarfulSolutionsGroup](https://github.com/SnarfulSolutionsGroup) & [@Sitnik](https://github.com/Sitnik)
- [xkcd comics](https://github.com/SnarfulSolutionsGroup/TRMNL-Plugins/blob/main/TRMNL_Comic.md) by [@SnarfulSolutionsGroup](https://github.com/SnarfulSolutionsGroup)
- [Todoist](https://github.com/Nynir/trmnl-todoist) by [@Nynir](https://github.com/Nynir)
- [Surf reports](https://github.com/pcifaldi/surf_api) by [@pcifaldi](https://github.com/pcifaldi)
- [On This Day (in history)](https://github.com/frethop/TRMNL-thisday) by [@frethop](https://github.com/frethop)
- [Multi-column ICS calendar](https://github.com/jfsso/trmnl-calendar) by [@jfsso](https://github.com/jfsso)
- [WooCommerce](https://github.com/yannicschuller/trmnl-woocommerce) by [@yannicschuller](https://github.com/yannicschuller)
- [Strava goals](https://github.com/vinayak-mehta/trmnl-strava-goals) by [@vinayak-mehta](https://github.com/vinayak-mehta)
- [Valorant Tracker](https://github.com/MarkHopper24/Valorant-Tools) by [@MarkHopper24](https://github.com/MarkHopper24)
- [NASA Deep Space Network](https://github.com/schrockwell/trmnl-dsn) by [@schrockwell](https://github.com/schrockwell)
- [Marvel Character of the Day](https://github.com/MarkHopper24/Marvel-Character-of-the-Day) by [@MarkHopper24](https://github.com/MarkHopper24)
- [Remember The Milk](https://github.com/sejtenik/trmnl-rtm-plugin) by [@sejtenik](https://github.com/sejtenik)
- [Habitify](https://github.com/sejtenik/trmnl-habitify-plugin) by [@sejtenik](https://github.com/sejtenik)
- [Libra](https://github.com/sejtenik/trmnl-libra-cloud-plugin) by [@sejtenik](https://github.com/sejtenik)
- [This Day in History (Wikipedia)](https://github.com/jvivona/TRMNL-recipes/tree/main/thisdayinhistory) by [@jvivona](https://github.com/jvivona)
- [Weekly Goal Tracker](https://github.com/azjgard/trmnl-weekly-goal-tracker) by [@azjgard](https://github.com/azjgard)
- [METAR](https://github.com/schrockwell/trmnl-metar) by [@schrockwell](https://github.com/schrockwell)
- [Block Clock](https://github.com/tyler-dot-earth/trmnl-notblockclock) by [@tyler-dot-earth](https://github.com/tyler-dot-earth)
- [TickTick Calendar](https://github.com/frethop/TRMNL-ticktick) by [@frethop](https://github.com/frethop)

to be featured here, join our developer-only Discord server (link inside TRMNL UI).
