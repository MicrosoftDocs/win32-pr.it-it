---
title: Primitive e comandi
description: Primitive e comandi
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitive
- OpenGL, comandi
- primitive OpenGL
- comandi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709460"
---
# <a name="primitives-and-commands"></a>Primitive e comandi

OpenGL disegna punti *primitivi* , segmenti di linea o polygonssubject a diverse modalità selezionabili. È possibile controllare le modalità indipendentemente l'una dall'altra. Ciò significa che l'impostazione di una modalità non influisce sulla possibilità di impostare altre modalità (anche se molte modalità possono interagire per determinare la fine del buffer). Per specificare le primitive, impostare le modalità ed eseguire altre operazioni OpenGL, è possibile eseguire i comandi sotto forma di chiamate di funzione.

Le primitive sono definite da un gruppo di uno o più *vertici*. Un vertice definisce un punto, un endpoint di una linea o un angolo di un poligono in cui si incontrano due bordi. I dati (costituiti da coordinate dei vertici, colori, normali, coordinate di trama e flag perimetrali) sono associati a un vertice e ogni vertice e i dati associati vengono elaborati in modo indipendente, nell'ordine e nello stesso modo. Le uniche eccezioni a questa regola sono i casi in cui il gruppo di vertici deve essere ritagliato in modo che una particolare primitiva entri in un'area specificata. In questo caso, i dati dei vertici possono essere modificati e nuovi vertici creati. Il tipo di ritaglio dipende dalla primitiva rappresentata dal gruppo di vertici.

I comandi vengono sempre elaborati nell'ordine in cui vengono ricevuti, sebbene sia possibile che si verifichi un ritardo indeterminato prima che un comando venga applicato. Ciò significa che ogni primitiva viene disegnata completamente prima che un comando successivo venga applicato. Significa anche che i comandi di query di stato restituiscono dati coerenti con l'esecuzione completa di tutti i comandi OpenGL precedentemente rilasciati.

 

 




