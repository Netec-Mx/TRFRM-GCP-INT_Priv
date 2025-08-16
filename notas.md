# Ejemplos adicionales de Proyectos en Terraform y Buenas Prácticas de Organización

## **[Lista General](https://netec-mx.github.io/TRFRM-GCP-INT_Priv/)**

## Estructura 1: Proyecto Simple (Monolítico)

### 🔹 Usos: proyectos individuales, pruebas, infraestructura puntual.

```bash
simple-proyecto/
├── main.tf
├── variables.tf
├── outputs.tf
├── terraform.tfvars
├── .gitignore
└── README.md
```

---

## Estructura 2: Por Entornos (`dev`, `test`, `prod`)

### 🔹 Usos: cuando necesitas mantener configuraciones separadas por entorno.

```bash
entornos-proyecto/
├── modules/
│   └── red/
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
├── dev/
│   ├── main.tf
│   ├── terraform.tfvars
│   └── backend.tf
├── test/
│   ├── main.tf
│   ├── terraform.tfvars
│   └── backend.tf
├── prod/
│   ├── main.tf
│   ├── terraform.tfvars
│   └── backend.tf
└── .gitignore
```

---

## Estructura 3: Modular y Escalable (con reuso de módulos)

### 🔹 Usos: para infraestructura compleja, reutilizable o multiplataforma.

```bash
modular-proyecto/
├── modules/
│   ├── network/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   └── compute/
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
├── environments/
│   └── dev/
│       ├── main.tf
│       ├── terraform.tfvars
│       └── backend.tf
├── .gitignore
└── README.md
```

---

## **[Lista General](https://netec-mx.github.io/TRFRM-GCP-INT_Priv/)**