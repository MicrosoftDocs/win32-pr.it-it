---
description: "Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito"
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: "Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2b73e347f5d5a768780afc5d2153909c6f5a9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088099"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** - Windows XP, Windows Vista, Windows 7  
**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

In Windows 7, MSMQ usa SHA-2 come impostazione predefinita per la firma di un messaggio in uscita. Inoltre, tutti i messaggi in ingresso devono essere firmati con SHA-2. È possibile abilitare il supporto per un algoritmo di crittografia inferiore tramite una chiave del Registro di sistema accessibile dall'amministratore.

## <a name="manifestation-of-impact"></a>Manifestazione di impatto

-   MSMQ in Windows 2003 o versioni seguenti non accetterà messaggi firmati provenienti da MSMQ in Windows 7
-   MSMQ in Windows 7 non accetterà messaggi firmati provenienti da Windows 2008 o versioni seguenti

## <a name="mitigation"></a>Mitigazione

Gli utenti devono prendere in considerazione l'aggiornamento a Windows 7 per sfruttare l'algoritmo di firma più avanzato. Per abilitare lo scambio di messaggi firmati senza interruzioni tra Windows 7 e qualsiasi sistema operativo di livello inferiore, l'amministratore deve aggiungere le eccezioni appropriate nei computer MSMQ.

 

 



