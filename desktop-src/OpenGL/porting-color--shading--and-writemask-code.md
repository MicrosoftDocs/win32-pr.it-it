---
title: Porting color, shading e writemask Code
description: Porting color, shading e writemask Code
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Porting IRIS GL, colore
- porting da IRIS GL, colore
- porting a OpenGL da IRIS GL, colore
- Porting OpenGL da IRIS GL, colore
- Porting IRIS GL, ombreggiatura
- porting da IRIS GL, ombreggiatura
- porting in OpenGL da IRIS GL, ombreggiatura
- Porting OpenGL da IRIS GL, ombreggiatura
- Porting IRIS GL, maschera di scrittura
- porting da IRIS GL, writemask
- porting in OpenGL da IRIS GL, writemask
- Porting OpenGL da IRIS GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d3fcb9cf47b45b4b1174cb20e3259dbb883c2fd0414d255a418c52b50fa28e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485781"
---
# <a name="porting-color-shading-and-writemask-code"></a>Porting color, shading e writemask Code

Quando si esegue la porting di codice a colori, ombreggiatura e writemask in OpenGL, tenere presente quanto segue:

-   Anche se è possibile impostare gli indici della mappa colori con la funzione OpenGL [glIndex,](glindex-functions.md) OpenGL non dispone di una funzione per il caricamento degli indici della mappa colori.
-   I valori dei colori vengono normalizzati al tipo di dati. Per informazioni sui valori dei colori, vedere [glColor](glcolor-functions.md).
-   Non esiste un equivalente semplice per **cpack**.
-   Potrebbe essere necessario convertire il codice che include le funzioni **c** o **color** in [**glClearColor**](glclearcolor.md) o [**glClearIndex**](glclearindex.md) anziché **glColor** **o glIndex**.
-   La maschera di scrittura RGBA si applica a ogni componente, ma non a ogni bit.
-   IRIS GL fornisce costanti di colore definite: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW e WHITE. OpenGL non fornisce queste costanti.

Questo argomento include informazioni sugli argomenti seguenti.

-   [Porting di chiamate a colori](porting-color-calls.md)
-   [Porting di modelli di ombreggiatura](porting-shading-models.md)

 

 




