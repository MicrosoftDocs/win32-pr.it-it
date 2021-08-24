---
description: I record spline rappresentano le curve quadratica (ovvero b-spline quadratica) usate da TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Record spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbaf3730f327501bd55b2e35b9410f03fd0559cbb5e36d87a3052901d26e5f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613651"
---
# <a name="spline-records"></a>Record spline

I record spline rappresentano le curve quadratica (ovvero b-spline quadratica) usate da TrueType. Un record spline inizia con l'ultimo punto del record precedente (o per il primo record nel contorno, con il punto iniziale). Per il primo record spline, il punto iniziale e l'ultimo punto del record sono sulla struttura del glifo. Per tutti gli altri record spline, solo l'ultimo punto si trova sulla struttura del glifo. Tutti gli altri punti nei record spline sono al di fuori della struttura del glifo e devono essere sottoposti a rendering come punti di controllo di b-spline.

L'ultimo record di spline o polilinea in un contorno termina sempre con il punto iniziale del contorno. Questa disposizione garantisce che ogni contorno sia chiuso.

Poiché le b-spline richiedono tre punti (un punto di distanza dal contorno del glifo tra due punti della struttura), è necessario eseguire alcuni calcoli quando un record spline contiene più di un punto fuori curva.

Ad esempio, se un record spline contiene tre punti (A, B e C) e non è il primo record, i punti A e B sono fuori dalla struttura del glifo. Per interpretare il punto A, usare la posizione corrente (sempre sul contorno del glifo) e il punto sul contorno del glifo tra i punti A e B. Per trovare il punto medio (M) tra A e B, è possibile eseguire il calcolo seguente.

M = A + (B A)/2

Il punto intermedio tra i punti di off-outline consecutivi in un record spline è un punto sul contorno del glifo, in base alla definizione del formato spline usato nei tipi di carattere TrueType.

Se la posizione corrente è designata da P, le due spline quadratica definite da questo record spline sono (P, A, M) e (M, B, C).

 

 



