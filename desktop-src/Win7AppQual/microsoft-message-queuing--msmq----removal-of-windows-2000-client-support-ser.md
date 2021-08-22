---
description: 'Microsoft Message Queuing (MSMQ): rimozione del servizio di supporto client Windows 2000'
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: 'Microsoft Message Queuing (MSMQ): rimozione del servizio di supporto client Windows 2000'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bdcba684faa0a25994f66cc9cd205ba22b5ed949d8dcdd3e67497484f2784ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053049"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ): rimozione del servizio di supporto client Windows 2000

## <a name="affected-platforms"></a>Piattaforme interessate

**Server** - Windows Server 2008 R2  



## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Alta  
**Frequenza** - Bassa  

## <a name="description"></a>Descrizione

Il Windows servizio di supporto client di Windows 2000 è un componente facoltativo del server di Accodamento messaggi che è possibile installare in un computer controller di dominio Windows 2003 o Windows 2008. Questo servizio consente Windows 2000 client di operare in modalità integrata di dominio con qualsiasi server di Accodamento messaggi installato nei computer Windows 2003/2008. I client MSMQ che Windows xp verso l'alto non necessitano di questo servizio.

### <a name="manifestation-of-impact"></a>Manifestazione di impatto

Questa modifica influisce Windows 2000 durante l'interoperabilità in un dominio Windows 7 in cui tutti i controller di dominio Windows Server 2008 R2. Se un cliente esegue l'aggiornamento al dominio Windows 7, le applicazioni MSMQ esistenti in qualsiasi computer Windows 2000 nel dominio non potranno operare in modalità integrata di dominio a meno che questi client non esercitino l'aggiornamento a una versione Windows superiore.

### <a name="mitigation"></a>Strategia di riduzione del rischio

Gli utenti che hanno Windows computer client 2000 in un dominio Windows 7 possono configurare un controller di dominio Windows 2003/2008 nel dominio e installare il servizio di supporto client MSMQ Windows 2000 in questo controller di dominio.

### <a name="leveraging-feature-capabilities"></a>Sfruttare le funzionalità delle funzionalità

Gli utenti che hanno Windows 2000 computer client che eseguono MSMQ devono eseguire l'aggiornamento a una versione Windows superiore per sfruttare l'implementazione basata su Active Directory del server MSMQ.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

Gli utenti che hanno Windows 2000 computer client che eseguono MSMQ in un dominio Windows 7 con uno o più controller di dominio di livello inferiore devono verificare che le applicazioni funzionino in questo dominio misto.

 

 



