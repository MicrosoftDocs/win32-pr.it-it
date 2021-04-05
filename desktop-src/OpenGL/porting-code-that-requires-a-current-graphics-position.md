---
title: Codice porta che necessita di una posizione grafica corrente
description: OpenGL non mantiene una posizione grafica corrente. Le funzioni di IRIS GL che dipendono dalla posizione grafica corrente, ad esempio Move, disegnato e RMV, non hanno equivalenti in OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Porting di IRIS GL, posizione grafica corrente
- porting da IRIS GL, posizione grafica corrente
- porting in OpenGL da IRIS GL, posizione grafica corrente
- Porting OpenGL da IRIS GL, posizione grafica corrente
- posizione grafica corrente
- posizioni raster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/27/2019
ms.locfileid: "103719597"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a>Codice porta che necessita di una posizione grafica corrente

OpenGL non mantiene una posizione grafica corrente. Le funzioni di IRIS GL che dipendono dalla posizione grafica corrente, ad esempio **Move**, **disegnato** e **RMV**, non hanno equivalenti in OpenGL.

Le versioni precedenti di IRIS GL includevano i comandi che si basavano sulla posizione grafica corrente, sebbene il loro utilizzo fosse sconsigliato. Sarà necessario riscrivere il codice se si è basata sulla posizione grafica corrente in qualsiasi modo o se è stata usata una delle routine seguenti:

-   **disegni** e **spostamenti**
-   **PMV**, **PDR** e **PCLOS**
-   **RDR**, **RMV**, **rpdr** e **rpmv**
-   **oggetti GetGPO**

OpenGL presenta un concetto di posizione raster che corrisponde alla posizione corrente del carattere di IRIS GL. Per altre informazioni sul posizionamento raster, vedere [porting pixel Operation](porting-pixel-operations.md).

Questo argomento include informazioni sui seguenti elementi.

-   [Porting dei comandi di cancellazione dello schermo e del buffer](porting-screen-and-buffer-clearing-commands.md)
-   [Porting di matrici e funzioni di trasformazione](porting-matrix-and-transformation-functions.md)
-   [Porting del codice in modalità MSINGLE](porting-msingle-mode-code.md)
-   [Funzioni di porting che ottengono matrici e trasformazioni](porting-functions-that-get-matrices-and-transformations.md)
-   [Porting di viewport, Screenmasks e Scrboxes](porting-viewports--screenmasks--and-scrboxes.md)
-   [Porting di piani di ritaglio](porting-clipping-planes.md)

 

 




