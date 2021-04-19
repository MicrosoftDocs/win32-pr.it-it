---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: "Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb62f55f07565e76cefb5463a095d11ae789f379
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314964"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** -Windows XP, Windows Vista, Windows 7  
**Server** : windows Server 2003, windows Server 2008, windows Server 2008 R2  










## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

In Windows 7, MSMQ USA SHA-2 come impostazione predefinita per la firma di un messaggio in uscita. Inoltre, tutti i messaggi in arrivo devono essere firmati con SHA-2. È possibile abilitare il supporto per un algoritmo di crittografia inferiore tramite una chiave del registro di sistema accessibile dall'amministratore.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

-   MSMQ in Windows 2003 o versioni precedenti non accetterà i messaggi firmati provenienti da MSMQ in Windows 7
-   MSMQ in Windows 7 non accetterà i messaggi firmati provenienti da Windows 2008 o versioni precedenti

## <a name="mitigation"></a>Strategia di riduzione del rischio

Gli utenti devono prendere in considerazione l'aggiornamento a Windows 7 per sfruttare l'algoritmo di firma più solido. Per consentire lo scambio di messaggi firmato senza problemi tra Windows 7 e qualsiasi sistema operativo di livello inferiore, l'amministratore deve aggiungere le eccezioni appropriate nei computer MSMQ.

 

 



