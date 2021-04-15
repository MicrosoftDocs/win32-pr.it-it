---
title: Più registrazioni trap
description: Quando un'applicazione WinSNMP registra una sessione di WinSNMP per trap o notifiche, sono disponibili diverse opzioni.
ms.assetid: 76a4095f-ab5c-4f7a-9b60-a383a632fd65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81aebf94d60ca26f39bcd53b26cb1f794f43af0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331356"
---
# <a name="multiple-trap-registrations"></a>Più registrazioni trap

Quando un'applicazione WinSNMP registra una sessione di WinSNMP per trap o notifiche, sono disponibili diverse opzioni. Per questo motivo, un'applicazione può chiamare la funzione [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) più volte, definendo in effetti un filtro personalizzato per la ricezione di trap e notifiche. È ad esempio possibile eseguire la registrazione per un tipo di trap o notifica oppure per tutti i trap e le notifiche, a seconda del valore del parametro di *notifica* . Inoltre, l'applicazione può specificare i valori in altri parametri per la funzione **SnmpRegister** per definire ulteriormente i trap e le notifiche che devono raggiungere un'applicazione. Per altre informazioni, vedere [gestione di trap e notifiche](managing-traps-and-notifications.md).

Di seguito sono riportate le istanze in cui più chiamate a **SnmpRegister** sono ridondanti. In queste istanze **SnmpRegister** restituisce snmpapi \_ Success se la funzione viene completata correttamente, ma la registrazione ridondante è inefficace.

1.  Chiamata alla funzione [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) che richiede il recapito filtrato di trap e notifiche alla sessione, dopo una precedente chiamata a **SnmpRegister** che richiede il recapito di tutti i trap e le notifiche (recapito non filtrato). Questa chiamata è ridondante perché la sessione sta già ricevendo tutti i trap e le notifiche, incluso il singolo tipo definito dal filtro.
2.  Una chiamata duplicata a **SnmpRegister** o una chiamata in cui l'elenco di parametri è identico all'elenco di parametri in una precedente chiamata a **SnmpRegister** per la sessione.
3.  Chiamata alla funzione [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) che richiede il recapito filtrato di trap e notifiche in base a un identificatore di oggetto (OID) il cui prefisso è un OID specificato in una precedente chiamata a **SnmpRegister**. Ad esempio, è possibile specificare "1.3.6.1.4.1.311" nel parametro *Notification* per ricevere le notifiche provenienti da qualsiasi entità Microsoft SNMP Agent. Se si chiama di nuovo **SnmpRegister** e si specifica "1.3.6.1.4.1.311.1", la seconda chiamata è ridondante perché la sessione sta già ricevendo tutti i trap e le notifiche che contengono il prefisso OID "1.3.6.1.4.1.311".

Per annullare la registrazione della sessione, è necessario associare ogni chiamata di registrazione univoca alla funzione [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) . Chiamare **SnmpRegister** per annullare la registrazione della sessione e assicurarsi che i primi cinque parametri per **SnmpRegister** siano identici a quelli della chiamata di registrazione iniziale. L'unica differenza tra la chiamata iniziale e la chiamata di annullamento della registrazione è che, durante la registrazione, è necessario specificare il valore SNMPAPI \_ in nel parametro *status* e quando si chiama la funzione per annullare la registrazione, è necessario specificare snmpapi \_ off. Non è necessario trovare una corrispondenza tra le chiamate di registrazione ridondanti e la funzione **SnmpRegister** . È necessario che corrisponda solo alla prima chiamata di registrazione univoca.

Per modificare i criteri di filtro, potrebbe essere necessario per un'applicazione annullare prima la registrazione e disabilitare il recapito di determinati Trap o notifiche. Quindi, l'applicazione può creare un nuovo filtro chiamando [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), passando i valori appropriati.

 

 




