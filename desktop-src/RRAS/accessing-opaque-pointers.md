---
title: Accesso a puntatori opachi
description: I client sono in grado di accedere alle informazioni archiviate nelle destinazioni usando puntatori opachi.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515877"
---
# <a name="accessing-opaque-pointers"></a>Accesso a puntatori opachi

I client sono in grado di accedere alle informazioni archiviate nelle destinazioni usando puntatori opachi. Per usare lo spazio di archiviazione, il client deve prima chiamare [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) per ottenere il puntatore. Ogni volta che è necessaria una modifica alle informazioni, il client deve prima bloccare la destinazione chiamando [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) con il parametro *LockDest* impostato su **true**. Una volta bloccata la destinazione, il client può apportare le modifiche necessarie. È possibile sbloccare la destinazione usando un'altra chiamata a **RtmLockDestination** con il parametro *LockDest* impostato su **false**.

La funzione [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) consente inoltre a un client di utilizzare un blocco di lettura o un blocco di scrittura, utilizzando il parametro *Exclusive* . Un client deve utilizzare il blocco di scrittura solo quando sta apportando modifiche alle informazioni conservate utilizzando il puntatore opaco. I client possono utilizzare il blocco Read per visualizzare le informazioni del puntatore opaco archiviate in una destinazione.

Per il codice di esempio che illustra come usare queste funzioni, vedere [accedere al puntatore opaco in una destinazione](access-the-opaque-pointer-in-a-destination.md).

 

 




