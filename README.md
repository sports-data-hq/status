# SportsDataHQ status probe

The independent uptime check behind the status pages of the SportsDataHQ APIs:
[PuckAPI](https://puckapi.com/status), [EndzoneAPI](https://endzoneapi.com/status),
[DunkAPI](https://dunkapi.com/status), [FastballAPI](https://fastballapi.com/status),
[StrikerAPI](https://strikerapi.com/status), [AcesAPI](https://acesapi.com/status),
[BirdieAPI](https://birdieapi.com/status) and [FighterAPI](https://fighterapi.com/status).

Every five minutes, [one GitHub Actions workflow](.github/workflows/status-probe.yml) loads each
brand's website and sends its MCP server an `initialize` request, then records the HTTP status and
response time on that brand's status page. It runs on GitHub's machines, outside the hosting it
measures, and every run and its log are public in the [Actions tab](../../actions).
