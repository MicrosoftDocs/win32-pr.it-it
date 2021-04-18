---
description: Esistono situazioni in cui le chiavi devono essere esportate dall'ambiente protetto del provider del servizio di crittografia (CSP) nello spazio dati di un'applicazione. Le chiavi esportate vengono archiviate in strutture BLOB di chiavi crittografate.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Archiviazione delle chiavi crittografiche ed Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306460"
---
# <a name="cryptographic-key-storage-and-exchange"></a>Archiviazione delle chiavi crittografiche ed Exchange

Esistono situazioni in cui le chiavi devono essere esportate dall'ambiente protetto del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) nello spazio dati di un'applicazione. Le chiavi esportate vengono archiviate in strutture [*BLOB di chiavi*](../secgloss/k-gly.md) crittografate.

Esistono due situazioni specifiche in cui è necessario esportare le chiavi:

-   Per salvare una [*chiave di sessione*](../secgloss/s-gly.md) per un uso successivo da un'applicazione, se, ad esempio, un'applicazione ha appena crittografato un file di database da decrittografare in un secondo momento. L'applicazione è responsabile dell'archiviazione della chiave di crittografia. Questa operazione è necessaria perché i CSP non conservano le [*chiavi simmetriche*](../secgloss/s-gly.md) dalla sessione alla sessione.
-   Per inviare una chiave a un altro utente. Questo sarebbe più semplice se i rispettivi CSP potessero comunicare direttamente, ma non possono. Poiché i CSP non possono comunicare, la chiave deve essere esportata da un CSP, trasmessa all'applicazione di destinazione e quindi importata nel CSP di destinazione. Questo processo può diventare più complesso se il percorso di comunicazione non è attendibile.

In entrambi i casi, un'applicazione deve archiviare una chiave di sessione all'esterno del CSP per un determinato periodo di tempo. Per ulteriori informazioni, vedere [la procedura per l'archiviazione di una chiave di sessione](procedure-for-storing-a-session-key.md).

 

 
