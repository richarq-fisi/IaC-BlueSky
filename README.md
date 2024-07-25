# Proyecto de Infraestructura como Código (IaC) con Terraform y AWS

Este proyecto utiliza [Terraform](https://developer.hashicorp.com/terraform/install) para gestionar e implementar infraestructura en AWS.

## Requisitos previos

Para ejecutar este IaC, necesitarás:
1. Tener [Terraform](https://developer.hashicorp.com/terraform/install) instalado.
2. Configurar el archivo **terraform.tfvars** en cada carpeta del proyecto con las variables de tu cuenta de AWS.

### Variables requeridas

Las siguientes variables deben configurarse en el archivo **terraform.tfvars**:

- `aws_access_key`: Tu clave de acceso a AWS.
- `aws_secret_key`: Tu clave secreta de AWS.
- `key_name`: El nombre del par de claves generado en el servicio EC2.
- `private_key_path`: La ruta al archivo de clave privada del par de claves.

Estas variables se pueden obtener una vez que tengas una [cuenta de AWS](https://aws.amazon.com).

## Pasos para implementar la infraestructura

1. **Inicializar el directorio de trabajo**:

   Inicializa un directorio de trabajo que contiene archivos de configuración de Terraform.

   ```bash
   terraform init
   ```

2. **Desarrollar un plan de ejecución**:

   Genera un plan de ejecución que muestra las acciones que se tomarán para alcanzar el estado deseado de la infraestructura.

   ```bash
   terraform plan
   ```

3. **Aplicar los cambios**:

   Aplica los cambios necesarios para alcanzar el estado deseado de la infraestructura tal como se define en los archivos de configuración.

   ```bash
   terraform apply
   ```

4. **Destruir la infraestructura**:

   Destruye la infraestructura gestionada por Terraform.

   ```bash
   terraform destroy
   ```