# Nester Templates

This repository contains the templates used by [**Nester**](https://github.com/fedeegmz/nester), a CLI tool for generating **Kotlin/Ktor** project structures.

## 📜 Template Structure

The templates are written in **Tera**, a templating engine similar to Jinja2 or Handlebars.  
Each template uses **placeholders** that will be dynamically replaced by the Nester CLI.

### 📁 Template Directory

```
tera/
    │── injection.tera
    │── service.tera
    │── routing.tera
    └── ...
```


### 📝 Example Template (`service.tera`)

```tera
package {{ pkg_name }}.{{ module_name }}

import org.koin.core.component.KoinComponent

class {{ module_name_cap }}Service : KoinComponent {}

```

## 🚀 Using Templates in Nester CLI

When you run `nester -g module -n <module_name>`, the templates are rendered with the appropriate values and the corresponding files are generated in your project.

<!-- ## 🔄 Updating Templates

To update the templates on your machine, run:

```sh
nester update-templates
```

This will clone or update this repository in ~/.nester/templates. -->

## 📌 Contributing

If you want to improve the templates or add new ones:

- Fork this repository.
- Modify or add files inside templates/.
- Submit a Pull Request.

## ⚖️ License

This project is licensed under the [MIT License](./LICENSE).
