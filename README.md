# Índice    
- [Introducción](#introducción)
- [Objetivos](#objetivos)
  - [Objetivo general](#objetivo-general)
  - [Objetivos específicos](#objetivos-específicos)
- [Proceso unificado de desarrollo (RUP)](#proceso-unificado-de-desarrollo-rup)
- [Modelo del dominio](#modelo-del-dominio)
- [Disciplina de requisitos](#disciplina-de-requisitos)
  - [Actores y casos de uso](#actores-y-casos-de-uso)           
    - [Contexto de casos de uso](#contexto-de-casos-de-uso)
  - [Especificar casos de uso](#especificar-casos-de-uso)
  - [Prototipar la interfaz de usuario](#prototipar-la-interfaz-de-usuario)
- [Disciplina de análisis](#disciplina-de-análisis)
  - [Analizar la arquitectura](#analizar-la-arquitectura)
- [Disciplina de diseño](#disciplina-de-diseño)
  - [Diseñar la arquitectura](#diseñar-la-arquitectura)  
- [Referencias](#referencias)

# Introducción 
Desarrollaremos una aplicación web que permita el intercambio de artículos por artículos en la UNEMI, quiere decir que no se podrá comprar sino que solamente se permitirá el intercambio. Una vez que se acuerde el intercambio, los usuarios podrán acordar un punto de encuentro para llevar a cabo el intercambio de artículos.

# Objetivos

## Objetivo general
Desarrollar una aplicación web que permita a los estudiantes y profesores de la UNEMI intercambiar artículos. 

## Objetivos específicos:
- Implementar funcionalidades de búsqueda y seguimiento de artículos para ofrecer una mejor experiencia de usuario y mantener a los usuarios informados sobre el estado de sus intercambios.
- Permitir a los usuarios evaluar a los intercambiadores para mejorar la confianza en la comunidad de intercambio.
- Proporcionar una vía de retroalimentación y sugerencias para mejorar continuamente la aplicación web. Los usuarios podrán compartir sus opiniones, sugerencias y reportar cualquier problema o incidencia que puedan encontrar durante el uso de la aplicación web.
- Aplicar el proceso de desarrollo Rational Unified Process (RUP) para gestionar el proyecto de manera estructurada y organizada, asegurando la calidad del software resultante.

# Proceso unificado de desarrollo (RUP)
El proceso de desarrollo Rational Unified Process (RUP) es un conjunto de actividades que ayudan a transformar los requisitos de un usuario en un sistema software. Además, RUP también es un marco de trabajo genérico que puede especializarse para una gran variedad de sistemas software.

Los tres aspectos más importantes en RUP son:
 1. Que está dirigido por casos de uso
 2. Está centrado en la arquitectura y 
 3. Es un proceso iterativo incremental. 

Además, se utiliza UML para preparar los esquemas que representan el sistema software. 

Al final un proyecto que hace uso de RUP se ve de la siguiente manera:
![RUP](https://github.com/vfred0/unimart-requirements/blob/main/images/rup/disciplines.png?raw=true)

En dónde se obtiene 5 disciplinas o flujos, los cuales son los modelos de: 
- Casos de uso
- Análisis
- Diseño 
- Despliegue
- Implementación
- Pruebas

y cada disciplina se divide en 4 fases: 
- Inicio
- Elaboración
- Construcción 
- Transición

![RUP](https://github.com/vfred0/unimart-requirements/blob/main/images/rup/phases.png?raw=true)

Al final, no estaré siguiendo al pie de la letra el proceso de desarrollo RUP, pero si tomaré en cuenta los aspectos más importantes.

# Modelo del dominio
Describe los conceptos más importantes del contexto del sistema como son:
- Objetos de negocio
- Objetos del mundo real y conceptos que un sistema necesita hacer un seguimiento
- Eventos que suceden o que sucederán en el sistema

Asimismo nos permite tener un vocabulario común entre los desarrolladores, clientes y usuarios, con la finalidad de evitar malentendidos.

Para el caso de Unimart, el modelo del dominio se ve de la siguiente manera:
![Modelo de dominio](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/0-domain-model/domain-model.svg?raw=true)

# Disciplina de requisitos
Es el flujo de trabajo (realización de casos de uso que incluye roles, actividades y artefactos) cuyo principal propósito es dirigir el desarrollo hacia el sistema correcto describiendo los requisitos del sistema de tal forma que se alcance el acuerdo entre el cliente, usuarios y desarrolladores sobre lo que el sistema debería hacer. (Master EscuelaIT)

## Actores y casos de uso
Los actores son los usuarios que interactúan con el sistema y los casos de uso son las acciones que pueden realizar los actores.

Para el caso de Unimart, los actores serán los usuarios.
Los usuarios podrán realizar las siguientes interacciones:

| Autenticación | Gestión del perfil | 
| --------- | --------- |
| ![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/1-requeriments/1-actors-use-cases/authentication.svg?raw=true) | ![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/1-requeriments/1-actors-use-cases/profile-management.svg?raw=true) |

| Ver detalles, buscar y filtrar | Calificar |
| --------- | --------- | 
| ![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/1-requeriments/1-actors-use-cases/content-interaction/view-search-filter.svg?raw=true) | ![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/1-requeriments/1-actors-use-cases/content-interaction/ratings.svg?raw=true) |


### Contexto de casos de uso

El siguiente diagrama de contexto de casos de uso representa el flujo de interacción entre los diferentes casos de uso del sistema.

![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/1-requeriments/1-actors-use-cases/use-cases-context.svg?raw=true)

## Especificar casos de uso
Detalles de los casos de uso relacionados con la interacción que hace el usuario con el sistema y con la autenticación.

Autenticación

![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/1-requeriments/2-use-cases-specifications/authentication.svg?raw=true)

Interacción con el contenido

![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/1-requeriments/2-use-cases-specifications/content-interaction.svg?raw=true)

Gestión del perfil

![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/1-requeriments/2-use-cases-specifications/profile-management.svg?raw=true)

## Prototipar la interfaz de usuario
Los prototipos se encuentran realizados con figma y se pueden ver en los siguientes enlaces:
- Prototipo Desktop:  https://is.gd/zOKUJ5
- Prototipo Mobile: https://is.gd/SptDMP

## Disciplina de análisis
### Analizar la arquitectura
La estructura de la aplicación será por modelos, vistas y controladores. 
![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/2-analysis/architecture-analysis.svg?raw=true)

## Disciplina de diseño
### Diseñar la arquitectura 
![](https://github.com/vfred0/unimart-requirements/blob/main/images/docs/3-design/architecture.svg?raw=true)

# Referencias
Para llevar a cabo este proyecto, he utilizado como referencia los siguientes proyectos y agradezco a los autores por compartirlos:

- [Gestor de taller mecánico AgrimManager](https://www.notion.so/Gestor-de-taller-mec-nico-AgrimManager-a8d44826c2494e15bcb235fc1019938d#cd3ccf181d9c4a1b9253416cd9b74f57)
- [HalteroCMS](https://github.com/zuldare/mastercloud_pfm_halterocms)
- [Master EscuelaIT](https://github.com/USantaTecla-0-general/3-publicaciones)