# Led Blink using embedded elixir on a Raspberry 3

## Hardware

- Raspberry 3

## Development

### One time setup

Install erlang, elixir and firmware burning friends. And add `hex` and
`rebar` for elixir dependencies. Install `nerves`, the embedded elixir
framework.

```
❯ brew install erlang
❯ brew install elixir
❯ brew install fwup squashfs coreutils

❯ mix local.hix
❯ mix local.rebar3

❯ mix archive.install \
https://github.com/nerves-project/archives/raw/master/nerves_bootstrap.ez
```

### Day-to-day

Update project dependences:

```
❯ mix deps.get
```

A typical compile loop (build, make release, burn release to attached SD
card):

```
❯ mix compile
❯ mix firmware
❯ mix firmware.burn
```

## Resources

- [https://hexdocs.pm/nerves/installation.html#content](Nerves installation)
- [http://www.carstenblock.org/post/project-blinkenlights/](Led blink blog)
