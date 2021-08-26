---
title: Come creare un'istanza di uno shader geometry
description: L'instancing dello shader geometry consente l'esecuzione di più esecuzioni dello stesso geometry shader per primitiva.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 866b0cedb4de0fe2f8bf9087df6637d3a6340505289b4b773eaccd380fa4b367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067921"
---
# <a name="how-to-instance-a-geometry-shader"></a>Procedura: Creare un'istanza di uno shader Geometry

L'instancing dello shader geometry consente l'esecuzione di più esecuzioni dello stesso geometry shader per primitiva. Per creare un'istanza di uno shader geometry, aggiungere un attributo di istanza alla funzione shader principale e identificare un parametro di indice dell'istanza nel corpo della funzione shader.

Per creare un'istanza di uno shader Geometry:

1.  Aggiungere [l'attributo di](sm5-attributes-instance.md) istanza alla funzione main.

    ```
    [instance(24)]
    ```

    

    Definisce il numero di istanze (un massimo di 32) da eseguire per ogni primitiva.

2.  Collegare il valore di sistema [SV \_ GSInstanceID](sv-gsinstanceid.md) a una variabile nell'elenco dei parametri della funzione che può essere usata per tenere traccia dell'ID dell'istanza in esecuzione.
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  Compilare e creare lo shader esattamente come qualsiasi altro geometry shader.

Altri dettagli includono:

-   Il numero massimo di istanze è 32.
-   Il numero massimo di vertici è un numero massimo di vertici per istanza.
-   Ogni chiamata di istanza (come qualsiasi chiamata geometry shader) aumenta il numero di chiamate e genera un oggetto RestartStrip()implicito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità geometry shader](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




