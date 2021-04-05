---
description: .
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Microsoft Message Queuing (MSMQ)-gestione delle code migliorata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffcc566c4c4ea461fdd9c4634b26ff69f239f03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967710"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>Microsoft Message Queuing (MSMQ)-gestione delle code migliorata

## <a name="platforms"></a>Piattaforme

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

Il servizio MSMQ non impone un limite fisso al numero di code che è possibile creare in un sistema. Tuttavia, le prestazioni del sistema sono interessate quando viene creato un numero elevato di code. In particolare, quando sono presenti più di migliaia di code, il tempo di avvio del servizio MSMQ aumenta in modo esponenziale con un conseguente effetto visibile.

Microsoft ha ottimizzato l'avvio del servizio MSMQ in Windows 7 per ridurre l'overhead di ricerca per il caricamento delle code in memoria. Questa ottimizzazione ha comportato un notevole miglioramento del tempo di avvio del servizio MSMQ anche quando nel sistema vengono create diverse migliaia di code.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

Questo miglioramento delle prestazioni non influisca sulle funzionalità di un'applicazione esistente.

## <a name="leveraging-the-changed-feature"></a>Uso della funzionalità modificata

Gli sviluppatori di applicazioni che utilizzano MSMQ in Windows 7 possono ora progettare le proprie soluzioni senza limitare il numero di code. Si noti che il numero di code continua a influire sulle prestazioni complessive del server MSMQ, ma l'impatto sulle prestazioni è ora in una scala lineare anziché esponenziale.

## <a name="compatibility-performance-reliability-and-usability-tests"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

Se si usa un numero elevato di code, simulare l'ambiente di produzione su un letto di test, monitorare le prestazioni e analizzare il tempo di avvio del servizio e la velocità effettiva dei messaggi con un numero elevato di code e messaggi presenti nel sistema di test.

 

 



