# env

Useful shell and environment utils

Sourced from `~/.config/fish/config.fish`:

```fish
set ENV_HOME "$HOME/workspace/env"
if test -d $ENV_HOME
    fish_add_path "$ENV_HOME/bin"
    for module in env python
        if test -f "$ENV_HOME/$module.fish"
            source "$ENV_HOME/$module.fish"
        end
    end
end
```
