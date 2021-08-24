---
title: Primitive e comandi
description: Primitive e comandi
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitive
- OpenGL,comandi
- primitive OpenGL
- comandi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0729b71e9c25abf22045884910fcec3780d50aff2fe94dbe485f83f640cdeced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888061"
---
# <a name="primitives-and-commands"></a>Primitive e comandi

OpenGL disegna punti *primitivi,* segmenti di linea o poligonisoggetta in diverse modalità selezionabili. È possibile controllare le modalità indipendentemente l'una dall'altra. In altre parole, l'impostazione di una modalità non influisce sull'impostazione di altre modalità(anche se molte modalità possono interagire per determinare cosa alla fine finisce nel framebuffer). Per specificare primitive, impostare le modalità ed eseguire altre operazioni OpenGL, è necessario eseguire comandi sotto forma di chiamate di funzione.

Le primitive sono definite da un gruppo di uno o *più vertici.* Un vertice definisce un punto, un endpoint di una linea o un angolo di un poligono in cui si incontrano due bordi. I dati (costituiti da coordinate dei vertici, colori, normali, coordinate di trama e flag di bordo) sono associati a un vertice e ogni vertice e i relativi dati associati vengono elaborati in modo indipendente, nell'ordine e nello stesso modo. Le uniche eccezioni a questa regola sono i casi in cui il gruppo di vertici deve essere ritagliato in modo che una particolare primitiva si adatti all'interno di un'area specificata. In questo caso, i dati dei vertici possono essere modificati e creati nuovi vertici. Il tipo di ritaglio dipende dalla primitiva che rappresenta il gruppo di vertici.

I comandi vengono sempre elaborati nell'ordine in cui vengono ricevuti, anche se potrebbe verificarsi un ritardo indeterminato prima che un comando venga reso attivo. Ciò significa che ogni primitiva viene disegnata completamente prima che qualsiasi comando successivo venga eseguito. Significa anche che i comandi di query sullo stato restituiscono dati coerenti con l'esecuzione completa di tutti i comandi OpenGL emessi in precedenza.

 

 




