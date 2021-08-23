---
title: Specifica dei callback
description: È possibile specificare fino a cinque funzioni di callback per una rappresentazione a più elementi.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilità OpenGL (GLU), specifica di funzioni di callback
- GLU (utilità OpenGL), specifica di funzioni di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e57a5f961a980f20451f594fa59885eda99d1e2de94a55fbfd2abd4b8301b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553781"
---
# <a name="specifying-callbacks"></a>Specifica dei callback

È possibile specificare fino a cinque funzioni di callback per una rappresentazione a più elementi. Le funzioni che non vengono specificate non vengono chiamate durante la rappresentazione a interlinea e non si ottengono informazioni che potrebbero essere state restituite. Specificare le funzioni di callback [*con gluTessCallback*](glutess.md).

La **funzione gluTessCallback** associa la funzione di callback *fn* all'oggetto *tessobj dell'oggetto a tessellazione.* Il tipo di callback è determinato dal tipo di parametro *,* che può essere **GLU \_ BEGIN**, **GLU EDGE \_ \_ FLAG**, **GLU \_ VERTEX**, **GLU \_ END** o **GLU \_ ERROR**. Le cinque possibili funzioni di callback hanno i prototipi seguenti.



| Funzione di callback   | Prototipo                                    |
|---------------------|----------------------------------------------|
| **GLU \_ BEGIN**      | **void** **begin**(**tipo GLenum**_);_       |
| **GLU \_ EDGE \_ FLAG** | **void** **edgeFlag**(_flag_ **GLboolean**); |
| **GLU \_ VERTEX**     | **void** **vertex**(**void \* ***data* );     |
| **GLU \_ END**        | **void** **end**( *void* );                  |
| **ERRORE \_ GLU**      | **void** **error**(**GLenum**_errno_ );      |



 

Per modificare una funzione di callback, [*chiamare gluTessCallback*](glutess.md) con la nuova funzione. Per eliminare una funzione di callback senza sostituirla con una nuova, passare **gluTessCallback** a un puntatore Null per la funzione appropriata.

Con il passare del tempo, le funzioni di callback vengono chiamate in modo simile a come si usano le funzioni OpenGL [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md)e [**glEnd**](glend.md).

La funzione di callback **GLU \_ BEGIN** viene richiamata con uno dei tre parametri possibili:

-   VENTOLA \_ TRIANGOLO GL \_
-   GL \_ TRIANGLE \_ STRIP
-   TRIANGOLI GL \_

Dopo aver chiamato la funzione di callback **GLU \_ BEGIN** e prima di chiamare la funzione di callback associata a **GLU \_ END,** viene richiamata una combinazione dei callback **GLU EDGE \_ \_ FLAG** e **GLU \_ VERTEX.** I vertici e i flag di bordo associati vengono interpretati esattamente come in OpenGL tra **glBegin**(GL \_ TRIANGLE \_ FAN), **glBegin**(GL TRIANGLE STRIP) o \_ \_ **glBegin**(GL \_ TRIANGLES) e il **glEnd** corrispondente.

Poiché i flag di bordo non hanno senso in una ventola triangolare o in una striscia di triangoli, se è presente una funzione di callback associata a **GLU \_ EDGE \_ FLAG**, il callback **GLU \_ BEGIN** viene chiamato solo con **GL \_ TRIANGLES**. La funzione di callback **GLU \_ EDGE \_ FLAG** funziona in modo analogo alla funzione OpenGL [glEdgeFlag.](gledgeflag-functions.md)

Se si verifica un errore durante lo schema a più elementi, viene richiamata la funzione di callback dell'errore. Alla funzione di callback degli errori viene passato un numero di errore GLU. È possibile ottenere una stringa di caratteri che descrive l'errore con la [**funzione gluErrorString.**](gluerrorstring.md)

 

 




