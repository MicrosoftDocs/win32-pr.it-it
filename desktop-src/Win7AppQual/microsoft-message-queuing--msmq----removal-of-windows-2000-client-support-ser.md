---
description: Microsoft Message Queuing (MSMQ) - Rimozione del servizio di supporto client Windows 2000
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ) - Rimozione del servizio di supporto client Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be68d40271153567bdaf6b04d73218aaf3d3977
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088149"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ) - Rimozione del servizio di supporto client Windows 2000

## <a name="affected-platforms"></a>Piattaforme interessate

**Server** - Windows Server 2008 R2  



## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Alta  
**Frequenza** - Bassa  

## <a name="description"></a>Descrizione

Il servizio di supporto client Windows 2000 è un componente facoltativo del server di Accodamento messaggi che è possibile installare in un computer controller di dominio Windows 2003 o Windows 2008. Questo servizio consente ai client Windows 2000 di operare in modalità integrata di dominio con qualsiasi server di Accodamento messaggi installato nei computer Windows 2003/2008. I client MSMQ che operano in Windows XP verso l'alto non necessitano di questo servizio.

### <a name="manifestation-of-impact"></a>Manifestazione di impatto

Questa modifica influisce su Windows 2000 durante l'interoperabilità in un dominio di Windows 7 in cui tutti i controller di dominio sono Windows Server 2008 R2. Se un cliente esegue l'aggiornamento al dominio Windows 7, le applicazioni MSMQ esistenti in qualsiasi computer Windows 2000 nel dominio non potranno operare in modalità integrata di dominio a meno che questi client non esercitino l'aggiornamento a una versione di Windows superiore.

### <a name="mitigation"></a>Mitigazione

Gli utenti che dispongono di computer client Windows 2000 in un dominio Windows 7 possono configurare un controller di dominio Windows 2003/2008 nel dominio e installare il servizio di supporto client MSMQ Windows 2000 in questo controller di dominio.

### <a name="leveraging-feature-capabilities"></a>Sfruttare le funzionalità delle funzionalità

Gli utenti che dispongono di computer client Windows 2000 che eseguono MSMQ devono eseguire l'aggiornamento a una versione di Windows superiore per sfruttare l'implementazione basata su Active Directory del server MSMQ.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

Gli utenti che dispongono di computer client Windows 2000 che eseguono MSMQ in un dominio Windows 7 con uno o più controller di dominio di livello inferiore devono verificare che le applicazioni funzionino in questo dominio misto.

 

 



