---
title: Accesso ai puntatori opachi
description: I client possono accedere alle informazioni archiviate nelle destinazioni usando puntatori opachi.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b76e99a66b13c696951a0d46684726f79f29df5b0287e9c4923dc4054943e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030621"
---
# <a name="accessing-opaque-pointers"></a>Accesso ai puntatori opachi

I client possono accedere alle informazioni archiviate nelle destinazioni usando puntatori opachi. Per usare l'archiviazione, il client deve prima chiamare [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) per ottenere il puntatore. Ogni volta che è necessaria una modifica alle informazioni, il client deve prima bloccare la destinazione chiamando [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) con il *parametro LockDest* impostato su **TRUE.** Dopo aver bloccato la destinazione, il client può apportare la modifica necessaria. La destinazione può essere sbloccata usando un'altra chiamata a **RtmLockDestination con** il *parametro LockDest* impostato su **FALSE.**

La [**funzione RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) consente inoltre a un client di usare un blocco di lettura o di scrittura, usando il *parametro Exclusive.* Un client deve usare il blocco di scrittura solo quando apporta modifiche alle informazioni mantenute usando il puntatore opaco. I client possono usare il blocco di lettura per visualizzare le informazioni sul puntatore opaco archiviate in una destinazione.

Per il codice di esempio che illustra come usare queste funzioni, vedere [Accedere al puntatore opaco in una destinazione](access-the-opaque-pointer-in-a-destination.md).

 

 




