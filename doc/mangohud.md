# FPS Limiting with MangoHud

Minecraft's native FPS limit setting cannot be set to any value above 250, and it is generally recommended to avoid unlimited FPS.

On Windows, NVIDIA Control Panel is frequently used to limit Minecraft's FPS instead.

On Linux, MangoHud, a program used to monitor game performance, can be used to limit FPS to any value.

## MangoHud installation

MangoHud is available from the Fedora repos:

```bash
sudo dnf install mangohud
```

If you are using another distro, consult [MangoHud's readme](https://github.com/flightlessmango/MangoHud?tab=readme-ov-file#installation---pre-packaged-binaries)

## Setting Prism Launcher to use MangoHud

- Go to Prism > Instance settings > Performance

- Check `Performance` to enable all options, and then check `Enable MangoHud`

## MangoHud configuration

MangoHud can be configured either with a config file, or by setting environment variables.

### Config file

- Using a config file will configure MangoHud globally, so if you plan to use it in applications other than Minecraft, it may be desirable to use the environment variable instead.

- Create a file at `~/.config/mangohud/mangohud.conf`

- Include the following, replacing `<YOUR_FPS_LIMIT>` with the desired FPS limit:

```
fps_limit=<YOUR_FPS_LIMIT>
no_display
```

### Environment variable

- Go to Prism > Instance settings > Environment variables, and add a new environment variable with the name `MANGOHUD_CONFIG`. Under "Value", enter `fps_limit=<YOUR_FPS_LIMIT>, no_display`, replacing `<YOUR_FPS_LIMIT>` with the desired FPS limit.
