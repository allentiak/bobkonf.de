---
layout: talk
active: bob2020
title: Einführung in F#
speaker: Tim Digel
portrait: tim-digel.jpg
time: 14:30-16:00
type: Tutorial
language: german
head: 2020
---

F# (F Sharp) ist eine von Microsoft entwickelte funktionale
Programmiersprache im _.NET_-Universum. Die Syntax erinnert sehr stark
an _OCaml_.

In diesem Tutorial starten wir bei Null und sehen uns nach vielen
einführenden Anweisungen zusammengesetzte Datentypen (Records,
Listen, etc.), Typisierung, Namensräume, Einrückung, Tests und
Abhängigkeiten an.

Es wird kein Vorwissen vorausgesetzt. Grundideen funktionaler
Programmierung sind hilfreich, aber nicht zwingend erforderlich.

### Vorbereitung

Die Entwicklung findet in der Regel mit _Visual Studio_ unter Windows statt.
Um plattformunabhängig allen
Interessierten die Möglichkeit zu geben, mit zu programmieren,
verwenden wir _Visual Studio **Code**_. Weiter benötigen
wir die _Dotnet-SDK_ (siehe z. B. [für
Ubuntu](https://www.techrepublic.com/article/how-to-install-dotnet-core-on-ubuntu-18-04/)) und _Mono_. Alternativ
lässt sich das komplette Setup unter Linux non-invasiv mit Hilfe von
[Nix](https://nixos.org/nix/download.html) mit diesen Schritten
herstellen:

    # Install Nix Package Manager, see https://nixos.org/nix/download.html
    # Nix is available for Linux &  MacOS
    # Create a playground
     mkdir -p ~/fsharp-tutorial && cd ~/fsharp-tutorial
    # This will download some nix packages and starts a sub shell
    # Unfortunately dotnet-sdk_3 isn't available for MacOS
    NIXPKGS_ALLOW_UNFREE=1 nix-shell -p dotnet-sdk_3 -p vscode -p fsharp -p mono
    
    # Create a new F#-project
    export DOTNET_SKIP_FIRST_TIME_EXPERIENCE=true
    dotnet new console -lang F# -i MyProject
    
    # Start Visual Studio Code
    code .
    # Install Extensions: Ionide-fsharp, C#

In _Visual Studio Code_ benötigen wir dann noch die Erweiterungen
_Ionide-fsharp_ und _C#_.

## Tim Digel

Tim Digel legt viel Wert auf Tests, insbesondere voll automatisierte
Tests. Er entwickelt regelmäßig Automatismen, um Anwendungen zu
testen, zu bauen und im Produktivumfeld einzuspielen.

Tim Digel arbeitet als Softwarearchitekt und DevOps-Spezialist bei der
Active Group GmbH. In diversen Projekten benutzt die Active Group
individuell die besten Techniken und die passendsten funktionalen
Programmiersprachen. Für Anwendungen im Windows-Umfeld ist das
momentan F#.
