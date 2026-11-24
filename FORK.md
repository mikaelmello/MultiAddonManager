# Fork release v1.7.4-fix.1

Upstream v1.7.4 built against mikaelmello/s2sdk `release/cs2-1.42.0.1`: the SDK commit v1.7.4 was
released on (alliedmodders/s2sdk a508eb5) plus alliedmodders/s2sdk#128.

Why: CS2 1.42.0.1 (build 26879581, server version 2000950) inserted one virtual into
`ISource2Server` after `GameCreateNetworkStringTables`. Built on the old layout, the `GameFrame`
hook sits on `ApplyGameSettings(KeyValues *)` and the server crashes at map load.

Exit: an upstream release built against an s2sdk that contains alliedmodders/s2sdk#128 (or an
equivalent change).
