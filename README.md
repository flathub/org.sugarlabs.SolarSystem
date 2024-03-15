# Solar System Flatpak

The Solar System activity is a tool to encourage children to learn more about the planets and their moons (natural satellites). It is the author's hope that this tool serves as a practical and interactve way to explore astronomy.

To know more refer: https://github.com/sugarlabs/solar-system

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.SolarSystem.git
cd org.sugarlabs.SolarSystem
flatpak -y --user install flathub org.gnome.{Platform,Sdk}//46
flatpak -y --user install org.sugarlabs.BaseApp//24.04
flatpak-builder --user --force-clean --install build org.sugarlabs.SolarSystem.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.SolarSystem
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.SolarSystem.json
```