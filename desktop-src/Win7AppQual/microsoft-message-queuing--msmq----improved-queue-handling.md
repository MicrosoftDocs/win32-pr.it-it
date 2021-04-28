---
description: Microsoft Message Queuing (MSMQ) - Gestione delle code migliorata
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Microsoft Message Queuing (MSMQ) - Gestione delle code migliorata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7b7b00cfce68a183d7925f7cfab5ff7ab54b9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088159"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>Microsoft Message Queuing (MSMQ) - Gestione delle code migliorata

## <a name="platforms"></a>Piattaforme

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

Il servizio MSMQ non limita il numero di code che è possibile creare in un sistema. Tuttavia, le prestazioni del sistema sono influenzate quando viene creato un numero elevato di code. In particolare, quando sono presenti più di poche migliaia di code, il tempo di avvio del servizio MSMQ aumenta in modo esponenziale, con un impatto visibile.

Microsoft ha ottimizzato l'avvio del servizio MSMQ in Windows 7 per ridurre l'overhead di ricerca per il caricamento delle code in memoria. Questa ottimizzazione ha portato a un miglioramento significativo del tempo di avvio del servizio MSMQ anche quando nel sistema vengono create diverse migliaia di code.

## <a name="manifestation-of-impact"></a>Impatto significativo

Questo miglioramento delle prestazioni non influisce sulle funzionalità delle applicazioni esistenti.

## <a name="leveraging-the-changed-feature"></a>Uso della funzionalità modificata

Gli sviluppatori di applicazioni che usano MSMQ in Windows 7 possono ora architettare le proprie soluzioni senza limitare il numero di code. Si noti che il numero di code influisce ancora sulle prestazioni complessive del server MSMQ, ma l'impatto sulle prestazioni è ora su una scala lineare anziché esponenziale.

## <a name="compatibility-performance-reliability-and-usability-tests"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

Se si usa un numero elevato di code, simulare l'ambiente di produzione in un ambiente di test, monitorare le prestazioni e analizzare il tempo di avvio del servizio e la velocità effettiva dei messaggi con un numero elevato di code e messaggi presenti nel sistema di test.

 

 



