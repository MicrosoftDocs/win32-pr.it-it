---
description: I record spline rappresentano le curve quadratiche (ovvero le spline b quadratiche) utilizzate da TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Record spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755839"
---
# <a name="spline-records"></a>Record spline

I record spline rappresentano le curve quadratiche (ovvero le spline b quadratiche) utilizzate da TrueType. Un record spline inizia con l'ultimo punto del record precedente (o per il primo record nel contorno con il punto iniziale). Per il primo record spline, il punto iniziale e l'ultimo punto del record si trovano sulla struttura del glifo. Per tutti gli altri record spline, solo l'ultimo punto si trova nella struttura del glifo. Tutti gli altri punti nei record della spline si trovano fuori dal contorno del glifo ed è necessario eseguirne il rendering come punti di controllo di b-spline.

L'ultimo record spline o polilinea in un contorno termina sempre con il punto iniziale del contorno. Questa disposizione garantisce la chiusura di ogni contorno.

Poiché le spline b richiedono tre punti (un punto fuori dal contorno del glifo tra due punti che si trovano sulla struttura), è necessario eseguire alcuni calcoli quando un record spline contiene più di un punto fuori curva.

Se, ad esempio, un record spline contiene tre punti (A, B e C) e non è il primo record, i punti A e B sono fuori dal contorno del glifo. Per interpretare il punto A, usare la posizione corrente (che è sempre sul contorno del glifo) e il punto sulla struttura del glifo tra i punti A e B. Per trovare il punto medio (M) tra A e B, è possibile eseguire il calcolo seguente.

M = A + (B A)/2

Il punto medio tra i punti fuori struttura consecutivi in un record spline è un punto del contorno del glifo, in base alla definizione del formato spline usato nei tipi di carattere TrueType.

Se la posizione corrente è designata da P, le due spline quadratiche definite da questo record spline sono (P, A, M) e (M, B, C).

 

 



