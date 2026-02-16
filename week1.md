# 🟢 Semana 1 --- Git, GitHub y Entorno Local

## ⏱ Duración estimada

5--7 horas

## 🎯 Objetivo de la semana

Al terminar esta semana debes poder:

1.  Usar Git con seguridad.
2.  Crear una rama y abrir un Pull Request en GitHub.
3.  Tener Docker funcionando en WSL.
4.  Levantar Minikube.
5.  Desplegar un nginx en Kubernetes.


------------------------------------------------------------------------

# 🧠 Parte 1 --- Git y GitHub (Fundamentos)

## ¿Qué es un commit?

Un commit es una "foto" de tu código en un momento concreto.

Cada commit: - Tiene un identificador único (SHA). - Guarda quién lo
hizo y cuándo. - Registra los cambios respecto al anterior.

------------------------------------------------------------------------

## ¿Qué es una rama?

Una rama es una línea de trabajo independiente.

En este programa usaremos:

main → rama protegida\
feature/week-1-tuNombre → tu trabajo

Nunca se trabaja directamente sobre `main`.

------------------------------------------------------------------------

## Flujo básico que debes dominar

Siempre seguirás este proceso:

1.  Crear rama\
2.  Hacer cambios\
3.  Commit\
4.  Push\
5.  Abrir Pull Request

Ejemplo:

git checkout -b feature/week-1-ruben\
git add .\
git commit -m "chore: add week-1 deliverable"\
git push origin feature/week-1-ruben

Después vas a GitHub y abres un PR hacia `main`.

------------------------------------------------------------------------

## Merge vs Rebase (explicación simple)

-   Merge → Une ramas y crea un commit adicional.\
-   Rebase → Reorganiza tu rama encima de `main` (historia más limpia).

Por ahora: - Usa merge\
- Entiende que rebase existe

------------------------------------------------------------------------

# 🛠 Parte 2 --- Preparar el Entorno Técnico

Todo debe funcionar dentro de WSL.

------------------------------------------------------------------------

## Herramientas necesarias

Dentro de WSL:

-   Git\
-   Docker Engine\
-   Docker Compose\
-   kubectl\
-   Minikube\
-   Helm

En el sistema principal:

-   VSCode\
-   Extensiones recomendadas:
    -   Docker\
    -   Kubernetes\
    -   GitLens\
    -   YAML

------------------------------------------------------------------------

## Verificaciones obligatorias

Debes poder ejecutar sin errores:

docker ps\
minikube start\
kubectl get nodes\
helm version

Si alguno falla, el entorno no está correctamente configurado.

------------------------------------------------------------------------

# 🧪 Parte 3 --- Primer despliegue en Kubernetes

## Levantar el cluster

minikube start

## Crear un deployment nginx

kubectl create deployment nginx --image=nginx\
kubectl expose deployment nginx --type=NodePort --port=80\
kubectl get pods

Si el pod aparece como Running, el entorno está funcionando
correctamente.

------------------------------------------------------------------------

# 📂 Ejercicio obligatorio

## 1️⃣ Fork del repositorio

Haz fork del repositorio base en tu cuenta de GitHub.

------------------------------------------------------------------------

## 2️⃣ Crear rama

Debe llamarse exactamente:

feature/week-1-tuNombre

------------------------------------------------------------------------

## 3️⃣ Crear archivo obligatorio

Ruta exacta:

deliverables/week-1-tuNombre.md

Debe contener:

-   Tu nombre\
-   Tu objetivo profesional en una frase\
-   3 cosas que aprendiste esta semana\
-   Salida de:
    -   docker ps\
    -   kubectl get nodes

------------------------------------------------------------------------

## 4️⃣ Commit y Push

git add .\
git commit -m "chore: add week-1 deliverable"\
git push origin feature/week-1-tuNombre

------------------------------------------------------------------------

## 5️⃣ Abrir Pull Request

El título debe incluir obligatoriamente:

module:week-1

Si no lo incluyes, el sistema automático no detectará el módulo.

------------------------------------------------------------------------