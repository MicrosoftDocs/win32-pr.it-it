---
description: .
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ)-rimozione del servizio di supporto client di Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54688ee4ad24eb691c95e4d70ce0acb881e212eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058058"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ)-rimozione del servizio di supporto client di Windows 2000

## <a name="affected-platforms"></a>Piattaforme interessate

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -alta  
**Frequenza** -bassa  

## <a name="description"></a>Descrizione

Il servizio di supporto client di Windows 2000 è un componente facoltativo del server di Accodamento messaggi che è possibile installare in un computer con controller di dominio Windows 2003 o Windows 2008. Questo servizio consente ai client Windows 2000 di operare in una modalità integrata del dominio con qualsiasi server di Accodamento messaggi installato nei computer Windows 2003/2008. I client MSMQ che operano su Windows XP verso l'alto non necessitano di questo servizio.

### <a name="manifestation-of-impact"></a>Manifesto di effetto

Questa modifica ha effetto su Windows 2000 quando si interopera in un dominio di Windows 7 in cui tutti i controller di dominio sono Windows Server 2008 R2. Se un cliente si aggiorna al dominio di Windows 7, le applicazioni MSMQ esistenti in qualsiasi computer Windows 2000 nel dominio non saranno in grado di funzionare in una modalità integrata a livello di dominio, a meno che questi client non eseguano l'aggiornamento a una versione di Windows più recente.

### <a name="mitigation"></a>Strategia di riduzione del rischio

Gli utenti che dispongono di computer client Windows 2000 in un dominio Windows 7 possono configurare un controller di dominio Windows 2003/2008 nel dominio e installare il servizio di supporto client Windows 2000 MSMQ in questo controller di dominio.

### <a name="leveraging-feature-capabilities"></a>Sfruttando le funzionalità

Gli utenti con computer client Windows 2000 che eseguono MSMQ dovranno eseguire l'aggiornamento a una versione di Windows superiore per sfruttare i vantaggi dell'implementazione basata su Active Directory del server MSMQ.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilità, prestazioni, affidabilità e test di usabilità

Gli utenti con computer client Windows 2000 che eseguono MSMQ in un dominio Windows 7 con uno o più controller di dominio di livello inferiore devono verificare che le applicazioni siano funzionali in questo dominio misto.

 

 



