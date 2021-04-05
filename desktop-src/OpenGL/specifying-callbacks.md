---
title: Specifica di callback
description: È possibile specificare fino a cinque funzioni di callback per uno schema a mosaico.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilità OpenGL (GLU), che specifica le funzioni di callback
- GLU (utilità OpenGL), specifica di funzioni di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516030"
---
# <a name="specifying-callbacks"></a>Specifica di callback

È possibile specificare fino a cinque funzioni di callback per uno schema a mosaico. Tutte le funzioni non specificate non vengono chiamate durante la suddivisione a mosaico e non vengono restituite informazioni che potrebbero essere state restituite. Si specificano le funzioni di callback con [*gluTessCallback*](glutess.md).

La funzione **gluTessCallback** associa la funzione di callback *FN* al *tessobj* dell'oggetto a mosaico. Il tipo del callback è determinato dal *tipo* di parametro, che può essere **Glu \_ Begin**, **Glu \_ Edge \_ flag**, **Glu \_ Vertex**, **Glu \_ end** o **Glu \_ Error**. Le cinque funzioni di callback possibili includono i prototipi seguenti.



| Funzione di callback   | Prototipo                                    |
|---------------------|----------------------------------------------|
| **\_inizio Glu**      | **void** **Begin**(**GLEnum * * * tipo* );       |
| **\_flag di Edge Glu \_** | **void** **EdgeFlag**(**GLboolean * * * flag* ); |
| **\_vertice Glu**     | **void** **Vertex**(**void * \* * * Data* );     |
| **\_estremità Glu**        | **void** **end**( *void* );                  |
| **\_errore Glu**      |  **errore** void (**GLEnum * * * errno* );      |



 

Per modificare una funzione di callback, chiamare [*gluTessCallback*](glutess.md) con la nuova funzione. Per eliminare una funzione di callback senza sostituirla con una nuova, passare **gluTessCallback** un puntatore null per la funzione appropriata.

Quando si procede a mosaico, le funzioni di callback vengono chiamate in modo analogo al modo in cui si usano le funzioni OpenGL [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md)e [**glEnd**](glend.md).

La funzione **Glu \_ Begin** callback viene richiamata con uno dei tre parametri possibili:

-   \_ventola del triangolo GL \_
-   \_striscia del triangolo GL \_
-   triangoli GL \_

Dopo aver chiamato la funzione **Glu \_ Begin** callback e prima di chiamare la funzione di callback associata a **Glu \_ end**, viene richiamata una combinazione del **\_ \_ flag di Edge Glu** e dei callback del **\_ vertice Glu** . I vertici e i flag perimetrali associati vengono interpretati esattamente come sono in OpenGL tra **glBegin**( \_ ventola del triangolo GL \_ ), **glBegin**(striscia del \_ triangolo GL \_ ) o **GlBegin**( \_ triangoli GL **)** e l'oggetto **glEnd** corrispondente.

Poiché i flag perimetrali non hanno senso in una ventola a triangolo o in una striscia di triangolo, se è presente una funzione di callback associata al **\_ \_ flag di Edge di Glu**, il callback di **Glu \_ Begin** viene chiamato solo con **\_ triangoli GL**. La funzione di callback di **Glu \_ Edge \_ flag** funziona in modo analogo alla funzione [glEdgeFlag](gledgeflag-functions.md) di OpenGL.

Se si verifica un errore durante il mosaico, viene richiamata la funzione di callback degli errori. Alla funzione di callback di errore viene passato un numero di errore GLU. È possibile ottenere una stringa di caratteri che descrive l'errore con la funzione [**gluErrorString**](gluerrorstring.md) .

 

 




