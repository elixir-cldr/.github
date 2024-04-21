## Localization libraries for Elixir

The [Common Locale Data Repository](https://cldr.unicode.org) maintains the canonical data essential to support localization of applications for the worlds diverse cultures and languages.  The libraries in this organization implement most (but not all) of the CLDR standards and support most (but not all) of the localization data.

The intention behind these libraries is to simplify localization. To make building a localized application as straight forward as one which is not. Indeed it can be argued that all applications are localized since they apply assumptions about the end user by default - even if those defaults are those of the Elixir language.

### Presentations

* ElixirConf EU 2022 [Building Elixir Apps for Global Audiences or an Audience of One](https://www.youtube.com/watch?v=b9BQM40UzEs).
* [Elixir Mix podcast interview](https://topenddevs.com/podcasts/elixir-mix/episodes/the-power-of-cldr-with-kip-cole-emx-244#player1?catid=0&trackid=0)

### Fundamental libraries

The following libraries can be used to support various aspects of localization:

* [ex_cldr](https://hex.pm/packages/ex_cldr) is the base level library that manages language tags and the locale data that supports them. Over 700 locales are supported.
* [ex_cldr_numbers](https://hex.pm/packages/ex_cldr_numbers) which provides localized number formatting and parsing.
* [ex_cldr_currencies](https://hex.pm/packages/ex_cldr_currencies) which provides the data about the world's currencies both current and historic.
* [ex_cldr_dates_times](https://hex.pm/packages/ex_cldr_dates_times) which provides localized date and time formatting (but not parsing)
* [ex_cldr_units](https://hex.pm/packages/ex_cldr_units) which provides localized units-of-measure formatting and parsing.
* [ex_cldr_units_sql](https://hex.pm/packages/ex_cldr_units_sql) which provides a database type and an Ecto type for serializing units-of-measure.
* [ex_cldr_person_names](https://hex.pm/packages/ex_cldr_person_names) which provides localized formatting for peoples' names in a variety of styles and contexts.
* [ex_cldr_messages](https://hex.pm/packages/ex_cldr_messages) implements the [Unicode Message format](https://unicode-org.github.io/icu/userguide/format_parse/messages) for localizing messages. Integrates with `Gettext`.
* [ex_cldr_calendars](https://hex.pm/packages/ex_cldr_calendars) which provides localized calendar implementations of the Proleptic Gregorian calendar, the Julian calendar, the ISO Week calendar and provides a mechanism to define variations of the Gregorian and ISO Week calendars to meet the needs to organizations (like corporations or governments) that use different calendar periods.
* [ex_cldr_lists](https://hex.pm/packages/ex_cldr_lists) implemented localized list formatting.
* [ex_cldr_territories](https://hex.pm/packages/ex_cldr_territories) by @Schultzer provides support for localizing territory (country) information.
* [ex_cldr_languages](https://hex.pm/packages/ex_cldr_languages) by @LostKobrakai which provides support for localizing language names.
* [ex_cldr_collation](https://hex.pm/packages/ex_cldr_collation) which implements the [Unicode Collation Algorithm](https://unicode.org/reports/tr10) although only the [default DUCET](https://unicode.org/reports/tr10/#Default_Unicode_Collation_Element_Table) collation.

### Money

* [ex_money](https://hex.pm/packages/ex_money) provides a full-feature money libraries focusing on correctness and reliability with support for currency specific formatting (in any locale), money parsing, amortization and basic math.
* [ex_money_sql](https://hex.pm/packages/ex_money_sql) provide a database type and an ecto type to simplify serialization of money withoug losing precision or currency tags.  Also includes some aggregate function extensions for the Postgresql database.

### Ecto Integration

* [ex_cldr_trans](https://hex.pm/packages/ex_cldr_trans) provides a mechanism to localized database content. It is based on the fabulous [trans](https://hex.pm/packages/trans) by @crbelaus.
 
### Plug-based applications

In support of Plug-based applications, including Phoenix applications, the following add-on libraries can be used:

* [ex_cldr_plugs](https://hex.pm/packages/ex_cldr_plugs) provides plugs that can extract the requested locale for a user from different parts of the locale or the session.
* [ex_cldr_routes](https://hex.pm/packages/ex_cldr_routes) provides functions to generate and recognize localized routes. Also provides localized route helpers. Does not yet support localized [verified routes](https://github.com/phoenixframework/phoenix/blob/master/guides/routing.md#verified-routes). Verified routes are expected to be supported in March 2023.
* [ex_cldr_html](https://hex.pm/packages/cldr_html) which provides form helpers for selecting currencies, languages and territories. These are static HTML generators. A future `ex_cldr_components` will provide a more complete LiveView localized UI experience. This is not expected before year end 2023.

### Additional Calendars

Additional calendars that full support the Elixir Calendar behaviour are also available.

* [ex_cldr_calendars_lunisolar](https://hex.pm/packages/ex_cldr_calendars_lunisolar) which implements the lunisolar calendars for China, Japan and Korea
* [ex_cldr_calendars_coptic](https://hex.pm/packages/ex_cldr_calendars_coptic)
* [ex_cldr_calendars_persian](https://hex.pm/packages/ex_cldr_calendars_persian)
* [ex_cldr_calendars_ethiopic](https://hex.pm/packages/ex_cldr_calendars_ethiopic)
