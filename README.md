# Julia
Cheatsheet, snippets, resources for Julia.
## Environnement par défaut
Créer une fichier `~/.julia/config/startup.jl`

```julia
println("Greetings!")
using Pkg
if isfile("Project.toml") && isfile("Manifest.toml")
    Pkg.activate(".")
else
    Pkg.activate("/path/to/default/env")
end
```
Lors du lancement de Julia, active l'environnement par défaut si les fichiers `Project.toml` et `Manifest.toml` ne sont pas présents.



