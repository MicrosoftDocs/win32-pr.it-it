---
description: In alcune situazioni le chiavi devono essere esportate dall'ambiente sicuro del provider del servizio di crittografia (CSP) nello spazio dati di un'applicazione. Le chiavi esportate vengono archiviate in strutture BLOB di chiavi crittografate.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Chiavi di crittografia Archiviazione e Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3028efb449b59deb24a7097369d8894d0876907f3555c836e95e14d8c4bf5cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768758"
---
# <a name="cryptographic-key-storage-and-exchange"></a>Chiavi di crittografia Archiviazione e Exchange

In alcune situazioni le chiavi devono essere esportate dall'ambiente sicuro del [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) nello spazio dati di un'applicazione. Le chiavi esportate vengono archiviate in strutture [*BLOB di chiavi*](../secgloss/k-gly.md) crittografate.

Esistono due situazioni specifiche in cui è necessario esportare le chiavi:

-   Per salvare una [*chiave di sessione*](../secgloss/s-gly.md) per un uso successivo da parte di un'applicazione, se, ad esempio, un'applicazione ha appena crittografato un file di database da decrittografare in un secondo momento. L'applicazione è responsabile dell'archiviazione della chiave di crittografia. Ciò è necessario perché i CSP non mantengono [*le chiavi simmetriche*](../secgloss/s-gly.md) da una sessione all'altra.
-   Per inviare una chiave a un altro utente. Questo sarebbe più semplice se i rispettivi CSP fossero in grado di comunicare direttamente, ma non possono. Poiché i CSP non possono comunicare, la chiave deve essere esportata da un CSP, trasmessa all'applicazione di destinazione e quindi importata nel CSP di destinazione. Questo processo può diventare più complicato se il percorso di comunicazione non è attendibile.

In entrambi i casi, un'applicazione deve archiviare una chiave di sessione all'esterno del provider di servizi di configurazione per un periodo di tempo. Per altre informazioni, vedere [Procedura per l'archiviazione di una chiave di sessione.](procedure-for-storing-a-session-key.md)

 

 
