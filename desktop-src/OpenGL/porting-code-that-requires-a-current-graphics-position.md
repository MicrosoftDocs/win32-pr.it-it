---
title: Codice di porta che richiede una posizione grafica corrente
description: OpenGL non mantiene una posizione grafica corrente. Le funzioni GL IRIS che dipendono dalla posizione grafica corrente, ad esempio spostamento, disegno e rmv, non hanno equivalenti in OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Porting IRIS GL, posizione grafica corrente
- porting da IRIS GL, posizione grafica corrente
- porting a OpenGL da IRIS GL, posizione grafica corrente
- Porting OpenGL da IRIS GL, posizione grafica corrente
- posizione grafica corrente
- posizioni raster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2354264ed5ad022c0657c95a31007ad33df2882d3c9ab2c44cfafeea99b53d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485791"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a>Codice di porta che richiede una posizione grafica corrente

OpenGL non mantiene una posizione grafica corrente. Le funzioni GL IRIS che dipendono dalla posizione grafica corrente, ad esempio **move**, **draw** e **rmv**, non hanno equivalenti in OpenGL.

Le versioni precedenti di IRIS GL includevano comandi di disegno che si basavano sulla posizione grafica corrente, anche se il loro uso è stato sconsigliato. Sarà necessario riscrivere il codice se si è basata sulla posizione grafica corrente in qualsiasi modo o se è stata usata una delle routine seguenti:

-   **disegnare** e **spostare**
-   **pmv,** **pdr** e **pclos**
-   **rdr,** **rmv,** **rpdr** e **rpmv**
-   **getgpos**

OpenGL ha un concetto di posizione raster che corrisponde alla posizione del carattere corrente di IRIS GL. Per altre informazioni sul posizionamento raster, vedere [Porting Pixel Operations](porting-pixel-operations.md).

Questo argomento include informazioni sugli argomenti seguenti.

-   [Comandi di cancellazione dello schermo e del buffer](porting-screen-and-buffer-clearing-commands.md)
-   [Funzioni di trasformazione e matrice di porting](porting-matrix-and-transformation-functions.md)
-   [Porting del codice in modalità MSINGLE](porting-msingle-mode-code.md)
-   [Funzioni di porting che ottengono matrici e trasformazioni](porting-functions-that-get-matrices-and-transformations.md)
-   [Porting viewports, Screenmasks e Scrboxes](porting-viewports--screenmasks--and-scrboxes.md)
-   [Porting dei piani di ritaglio](porting-clipping-planes.md)

 

 




