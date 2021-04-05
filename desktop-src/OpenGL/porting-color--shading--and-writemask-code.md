---
title: Porting di colori, ombreggiatura e codice Writemask
description: Porting di colori, ombreggiatura e codice Writemask
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Porting di IRIS GL, colore
- porting da IRIS GL, color
- porting in OpenGL da IRIS GL, colore
- Porting OpenGL da IRIS GL, colore
- Porting di IRIS GL, ombreggiatura
- porting da IRIS GL, ombreggiatura
- porting in OpenGL da IRIS GL, ombreggiatura
- Porting OpenGL da IRIS GL, ombreggiatura
- Porting di IRIS GL, writemask
- porting da IRIS GL, writemask
- porting in OpenGL da IRIS GL, writemask
- Porting OpenGL da IRIS GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708467"
---
# <a name="porting-color-shading-and-writemask-code"></a>Porting di colori, ombreggiatura e codice Writemask

Quando si portano il codice di colore, ombreggiatura e writemask in OpenGL, tenere presente quanto segue:

-   Sebbene sia possibile impostare gli indici mappa colori con la funzione OpenGL [glIndex](glindex-functions.md) , OpenGL non dispone di una funzione per il caricamento degli indici mappa colori.
-   I valori dei colori vengono normalizzati in base al tipo di dati. Per informazioni sui valori dei colori, vedere [glColor](glcolor-functions.md).
-   Non esiste un equivalente semplice per **CPack**.
-   Potrebbe essere necessario tradurre il codice che include le funzioni **c** o **color** in [**glClearColor**](glclearcolor.md) o [**glClearIndex**](glclearindex.md) anziché **glColor** o **glIndex**.
-   Il writemask RGBA viene applicato a ogni componente, ma non a ogni bit.
-   IRIS GL fornisce costanti di colore definite: nero, blu, rosso, verde, MAGENTA, ciano, giallo e bianco. OpenGL non fornisce queste costanti.

Questo argomento include informazioni sui seguenti elementi.

-   [Chiamate di colore di porting](porting-color-calls.md)
-   [Porting di modelli di ombreggiatura](porting-shading-models.md)

 

 




