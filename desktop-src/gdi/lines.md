---
description: 'Una linea è un set di pixel evidenziati su una visualizzazione raster (o un set di punti su una pagina stampata) identificato da due punti: un punto iniziale e un punto finale.'
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: Linee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b81976984cecc3d4d3b27fb3e474e896c6e81f03e6f601db36418b9e3cf197c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062101"
---
# <a name="lines"></a>Linee

Una linea è un set di pixel evidenziati su una visualizzazione raster (o un set di punti su una pagina stampata) identificato da due punti: un punto iniziale e un punto finale. Il pixel che si trova nel punto iniziale è sempre incluso nella linea e il pixel che si trova nel punto finale è sempre escluso. Questo tipo di riga viene talvolta chiamato inclusive-exclusive.

Quando un'applicazione chiama una delle funzioni di disegno linea, L'interfaccia GDI (Graphics Device Interface) o in alcuni casi un driver di dispositivo determina quali pixel devono essere evidenziati. GDI è una libreria a collegamento dinamico (DLL) che elabora chiamate di funzioni grafiche da un'applicazione e le passa a un driver di dispositivo. Un driver di dispositivo è una DLL che riceve input da GDI, converte l'input in comandi del dispositivo e li passa al dispositivo appropriato. GDI usa un analizzatore differenziale digitale (DDA) per determinare il set di pixel che definiscono una linea. Un DDA determina il set di pixel esaminando ogni punto sulla linea e identificando i pixel sulla superficie di visualizzazione (o punti su una pagina stampata) che corrispondono ai punti. La figura seguente mostra una linea, il punto iniziale, il punto finale e i pixel evidenziati usando un DDA semplice.

![figura che mostra una griglia di pixel, punti iniziale e finale, una linea e ombreggiatura sui pixel che si trovano lungo la linea](images/cslcv-01.png)

Il DDA più semplice e più comune è il DDA Di Bresenham, o incrementale. Una versione modificata di questo algoritmo disegna linee Windows. Il DDA incrementale è noto per la semplicità, ma è anche noto per la sua imprecisione. Poiché viene arrotondato al valore intero più vicino, talvolta non riesce a rappresentare la riga originale richiesta dall'applicazione. Il valore DDA usato da GDI non viene arrotondato all'intero più vicino. Di conseguenza, questo nuovo DDA produce un output talvolta molto più simile alla riga originale richiesta dall'applicazione.

> [!Note]  
> Se un'applicazione richiede un output di riga che non può essere ottenuto con il nuovo DDA, può disegnare le proprie linee chiamando la [**funzione LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) e fornendo un DDA privato ([**LineDDAProc**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)). Tuttavia, la **funzione LineDDA** disegna linee molto più lente rispetto alle funzioni di disegno linea. Non usare questa funzione all'interno di un'applicazione se la velocità è un problema principale.

 

Un'applicazione può usare il nuovo DDA per disegnare linee singole e più segmenti di linea connessi. Un'applicazione può disegnare una singola riga chiamando la [**funzione LineTo.**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) Questa funzione disegna una linea dalla posizione corrente fino a un punto finale specificato, ma non incluso. Un'applicazione può disegnare una serie di segmenti di linea connessi chiamando la funzione [**Polyline,**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) fornendo una matrice di punti che specificano il punto finale di ogni segmento di linea. Un'applicazione può disegnare più serie non contigue di segmenti di linea connessi chiamando la funzione [**PolyPolyline,**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) fornendo i punti finali necessari.

La figura seguente illustra l'output di riga creato chiamando le [**funzioni LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)e [**PolyPolyline.**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)

![figura che mostra una linea retta, una casella a forma di "l" e due forme che appaiono tridimensionali](images/cslcv-02.png)

 

 



