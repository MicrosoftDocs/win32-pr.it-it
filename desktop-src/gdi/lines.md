---
description: 'Una linea è un set di pixel evidenziati in una visualizzazione raster (o un set di punti in una pagina stampata) identificato da due punti: un punto iniziale e un punto finale.'
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: Linee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cd678f782567e98d32ab7f8786d5b87aab1918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226687"
---
# <a name="lines"></a>Linee

Una linea è un set di pixel evidenziati in una visualizzazione raster (o un set di punti in una pagina stampata) identificato da due punti: un punto iniziale e un punto finale. Il pixel che si trova nel punto iniziale viene sempre incluso nella riga e il pixel che si trova al punto finale è sempre escluso. (Questo tipo di linea viene talvolta denominato inclusivo-esclusivo).

Quando un'applicazione chiama una delle funzioni di disegno di riga, GDI (Graphics Device Interface) o in alcuni casi un driver di dispositivo, determina i pixel da evidenziare. GDI è una libreria di collegamento dinamico (DLL) che elabora chiamate di funzioni grafiche da un'applicazione e le passa a un driver di dispositivo. Un driver di dispositivo è una DLL che riceve input da GDI, converte l'input nei comandi del dispositivo e li passa al dispositivo appropriato. GDI usa un analizzatore differenziale digitale (DDA) per determinare il set di pixel che definiscono una linea. Una DDA determina il set di pixel esaminando ogni punto sulla riga e identificando tali pixel sulla superficie di visualizzazione (o sui punti in una pagina stampata) che corrispondono ai punti. Nella figura seguente sono illustrate una riga, il punto iniziale, il punto finale e i pixel evidenziati utilizzando un semplice DDA.

![illustrazione che mostra una griglia di pixel, punti di inizio e fine, una linea e ombreggiatura sui pixel che si trovano lungo la linea](images/cslcv-01.png)

Il DDA più semplice e più comune è Bresenham, o incrementale. Una versione modificata di questo algoritmo Disegna righe in Windows. Il DDA incrementale è indicato per la relativa semplicità, ma è indicato anche per la relativa inaccuratezza. Poiché viene arrotondato al valore integer più vicino, a volte non è in grado di rappresentare la riga originale richiesta dall'applicazione. Il DDA utilizzato da GDI non viene arrotondato all'intero più vicino. Di conseguenza, questo nuovo DDA genera un output a volte molto più vicino alla riga originale richiesta dall'applicazione.

> [!Note]  
> Se un'applicazione richiede un output di riga che non può essere raggiunto con la nuova DDA, può tracciare le proprie righe chiamando la funzione [**LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) e fornendo un DDA privato ([**LineDDAProc**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)). Tuttavia, la funzione **LineDDA** disegna linee molto più lente rispetto alle funzioni di disegno di riga. Non usare questa funzione all'interno di un'applicazione se la velocità è un problema principale.

 

Un'applicazione può utilizzare il nuovo DDA per creare linee singole e più segmenti di linea connessi. Un'applicazione può creare una singola riga chiamando la funzione [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) . Questa funzione disegna una linea dalla posizione corrente fino a, ma non include, un punto finale specificato. Un'applicazione può creare una serie di segmenti di linea collegati chiamando la funzione [**polilinea**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) , fornendo una matrice di punti che specificano il punto finale di ogni segmento di linea. Un'applicazione può creare più serie indipendenti di segmenti di linea collegati chiamando la funzione [**polilinea**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) , fornendo i punti finali richiesti.

Nella figura seguente viene illustrato l'output della riga creato chiamando le funzioni [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) [**, polilinea e**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) [**polilinea**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) .

![illustrazione che mostra una linea retta, una casella a forma di "l" e due forme visualizzate tridimensionali](images/cslcv-02.png)

 

 



