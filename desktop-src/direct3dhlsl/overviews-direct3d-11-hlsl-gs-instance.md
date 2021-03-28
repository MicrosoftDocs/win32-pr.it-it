---
title: Come eseguire l'istanza di un geometry shader
description: La creazione di istanze di Geometry shader consente l'esecuzione di più esecuzioni dello stesso geometry shader per primitive.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992840"
---
# <a name="how-to-instance-a-geometry-shader"></a>Procedura: eseguire l'istanza di un geometry shader

La creazione di istanze di Geometry shader consente l'esecuzione di più esecuzioni dello stesso geometry shader per primitive. Per eseguire l'istanza di un geometry shader, aggiungere un attributo instance alla funzione shader principale e identificare un parametro di indice dell'istanza nel corpo della funzione shader.

Per l'istanza di un geometry shader:

1.  Aggiungere l' [attributo instance](sm5-attributes-instance.md) alla funzione Main.

    ```
    [instance(24)]
    ```

    

    Definisce il numero di istanze (un massimo di 32) da eseguire per ogni primitiva.

2.  Alleghi il valore del sistema [SV \_ GSInstanceID](sv-gsinstanceid.md) a una variabile nell'elenco dei parametri della funzione che può essere usata per tenere traccia dell'ID dell'istanza in esecuzione.
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  Compilare e creare lo shader Analogamente a qualsiasi altro geometry shader.

Altri dettagli includono:

-   Il numero massimo di istanze è 32.
-   Il numero massimo di vertici è un numero massimo di vertici per istanza.
-   Ogni chiamata di istanza, come qualsiasi chiamata a geometry shader, aumenta il numero di chiamate e genera un RestartStrip implicito ().

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Geometry shader](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




