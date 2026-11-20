# Pinned build sources (ingress-nginx nginx base image)

`images/nginx/rootfs/build.sh` downloads and **sha256-verifies** every source below.
Audited 2026-11-20 (ensembleip): each ref resolved to the commit listed, and each
archive hash equals the recorded sha256. If GitHub re-renders a tarball for the same
commit, the build fails loudly; re-audit and rotate that hash.

| Source | Ref | Commit | sha256 of archive |
|--------|-----|--------|-------------------|
| nginx.org | nginx-1.31.9 source tarball | — | `a11c5eeee2e257f4478f0e649f84b0040787d277d2d3e5233952aa6b6dcb80ad` |
| openresty/ngx_devel_kit | v0.3.6 | `3bd7c5619312` | `e3438a71130b63760ac4accec9f77ac8f91ad8f778e1940b061e9ea83dd62fe7` |
| open-telemetry/opentelemetry-cpp | v1.19.0 | `ced79860f8c8` | `e0330194b72f2fe4c0ce3ece06b02dc4aa0ab491eb75bf42c6f5e283912e468c` |
| open-telemetry/opentelemetry-proto | v1.5.0 | `2bd940b2b77c` | `08f40636adbc5f33d2084bd8e7b64e491dd0239d1a95021dbffbdf1ca8cea454` |
| openresty/set-misc-nginx-module | v0.34 | `35365f29dcba` | `f083e6a68520a9dfa09f0afbeb88ab7539f479cc5af91d8607ae2ab1874f9898` |
| openresty/headers-more-nginx-module | v0.40 | `0bf283ff9201` | `c14cb5e6c998590c209efbf77bd7637ce2cab02332e4192756a8af5b26ba4284` |
| atomx/nginx-http-auth-digest | v1.0.0 | `cd8641886c87` | `f09851e6309560a8ff3e901548405066c83f1f6ff88aa7171e0763bd9514762b` |
| owasp-modsecurity/ModSecurity-nginx | v1.0.4 | `755367a52e7a` | `bb596d146ad0650014168dda9dc8d07c50a070010044c95ed0d167a9a78e63a1` |
| openresty/lua-nginx-module | v0.10.32rc7 | `e672520a9480` | `70e005d3883224a808638154396c65b5e756876e9957c90b244a2f51ca07a843` |
| openresty/stream-lua-nginx-module | v0.0.20rc3 | `7581c68b43e1` | `cbd42d84575be2ca34d58091a519db58b734d9f8ddb9ebb681e0f77e5d9b78f6` |
| openresty/lua-upstream-nginx-module | v0.08 | `ad49f606989f` | `722620a74a8f75ac154691933d2ae4969b2173061476a3d3bf0de2b9891a0e45` |
| openresty/luajit2 | v2.1-20261023 | `5d8d0a27bfa4` | `46ec00b6ba6261890a7d185c48f848e5e6b7a2909fc39ac80f407d1dcbfc74b2` |
| leev/ngx_http_geoip2_module | 445df24ef3781e488cee3dfe8a1e111997fc1dfe | `445df24ef378` | `5e2113ed09cdd710908df8c6d1630616eeacb9216ef8705a06c25733394ddf28` |
| openresty/lua-resty-upload | v0.11 | `03704aee42f7` | `deb4ab1ffb9f3d962c4b4a2c4bdff692b86a209e3835ae71ebdf3b97189e40a9` |
| openresty/lua-resty-string | v0.19 | `282590f58d4c` | `8b3e17e8796f083228b89ddd013bcc688c7d15afcc721c70059fd4a8bf2355dc` |
| openresty/lua-resty-balancer | v0.05 | `1cd4363c0a23` | `8b2ff4edefc240dea0d3adb9dd065a42e8c09e06ba8bb0a188464cf76c9e4d06` |
| openresty/lua-resty-core | v0.1.35rc2 | `873d072635fd` | `fcd84dd01c8d589b0c1f68b11dd54c50d70d9b15d3f6e1a5760e970c4f99b7aa` |
| openresty/lua-cjson | 2.1.0.20 | `5f53e878d044` | `a99fb872aa731274ac70453cd4e6b2e0e8fb978893063d512ca67c7c332510e1` |
| cloudflare/lua-resty-cookie | f418d77082eaef48331302e84330488fdc810ef4 | `f418d77082ea` | `c0217456f4c36bb9ebbf7dbcd733e3d70734330364c88df73e703c4777521ff9` |
| openresty/lua-resty-lrucache | v0.15 | `3ff6300e68b7` | `8cf1a22e0d5b8f35cb0b2e14c58fcb3aa505a8fb6e956817f0cdb1f06593f072` |
| openresty/lua-resty-lock | v0.09 | `9dc550e56b6f` | `b4ddcd47db347e9adf5c1e1491a6279a6ae2a3aff3155ef77ea0a65c998a69c1` |
| openresty/lua-resty-dns | v0.24 | `b68eaecbf799` | `06e08aec4290ee83b505a0b9fa66fa4e9fbe729ce505bc88f3dc2093789223f7` |
| ledgetech/lua-resty-http | v0.17.2 | `183310324026` | `3da18ca8582243eff28302591e36651dc7fab046e77336aa4a6fa718bccce4a2` |
| openresty/lua-resty-memcached | v0.18 | `98bf47d7a481` | `3567144cfa26e63453960ec347137f47403b264af071385d2f16b8434eb3736e` |
| openresty/lua-resty-redis | v0.34 | `0d014dd1c7ca` | `427fde15a4ad2237c947368bee2c443bf8f402e339f64bf3716de324c6afb613` |
| api7/lua-resty-ipmatcher | 3e93c53eb8c9884efe939ef070486a0e507cc5be | `3e93c53eb8c9` | `bf4f89c0c00d1e986260d22180cbccbd2016eb054b5c2adcc1b6ee0ff773032f` |
| microsoft/mimalloc | v2.2.4 | `00d07c4c15a0` | `754a98de5e2912fddbeaf24830f982b4540992f1bab4a0a8796ee118e0752bda` |
| nginx/njs | 1.0.2 | `72e6a980b9bf` | `84a114499fa6878d3ec52b99c1cf2874a91eb0d915408f418a2b1279519f09ae` |
