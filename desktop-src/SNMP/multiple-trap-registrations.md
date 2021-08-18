---
title: Più registrazioni trap
description: Sono disponibili diverse opzioni quando un'applicazione WinSNMP registra una sessione WinSNMP per trap o notifiche.
ms.assetid: 76a4095f-ab5c-4f7a-9b60-a383a632fd65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2149e4ac1e9880601ae64718cd78991718d54a6228488a03e593376d9a7937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009328"
---
# <a name="multiple-trap-registrations"></a>Più registrazioni trap

Sono disponibili diverse opzioni quando un'applicazione WinSNMP registra una sessione WinSNMP per trap o notifiche. Per questo scopo, un'applicazione può chiamare la [**funzione SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) più volte, definendo in effetti un filtro personalizzato per la ricezione di trap e notifiche. Ad esempio, è possibile registrarsi per un tipo di trap o notifica o per tutte le trap e le notifiche, a seconda del valore del *parametro di* notifica. Inoltre, l'applicazione può specificare valori in altri parametri per la **funzione SnmpRegister** per definire ulteriormente le trap e le notifiche che devono raggiungere un'applicazione. Per altre informazioni, vedere [Gestione di trap e notifiche](managing-traps-and-notifications.md).

Di seguito sono riportate le istanze in cui più chiamate a **SnmpRegister** sono ridondanti. In questi casi **SnmpRegister** restituisce SNMPAPI SUCCESS se la funzione viene completata correttamente, ma la registrazione \_ ridondante non è efficace.

1.  Chiamata alla funzione [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) che richiede il recapito filtrato di trap e notifiche alla sessione, dopo una chiamata precedente a **SnmpRegister** che richiede il recapito di tutte le trap e le notifiche (recapito non filtrato). Questa chiamata è ridondante perché la sessione riceve già tutte le trap e le notifiche, incluso il singolo tipo definito dal filtro.
2.  Chiamata duplicata a **SnmpRegister** o in cui l'elenco di parametri è identico all'elenco di parametri in una chiamata precedente a **SnmpRegister** per la sessione.
3.  Chiamata alla funzione [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) che richiede il recapito filtrato di trap e notifiche in base a un identificatore di oggetto (OID) il cui prefisso è un OID specificato in una chiamata precedente a **SnmpRegister**. Ad esempio, è possibile specificare "1.3.6.1.4.1.311" nel parametro *di* notifica per ricevere notifiche provenienti da qualsiasi entità agente Microsoft SNMP. Se si chiama di nuovo **SnmpRegister** e si specifica "1.3.6.1.4.1.311.1", la seconda chiamata è ridondante perché la sessione riceve già tutte le trap e le notifiche che contengono il prefisso OID "1.3.6.1.4.1.311".

Per annullare la registrazione della sessione, è necessario corrispondere a ogni chiamata di registrazione univoca alla [**funzione SnmpRegister.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) Chiamare **SnmpRegister** per annullare la registrazione della sessione e assicurarsi che i primi cinque parametri di **SnmpRegister** siano identici a quelli nella chiamata di registrazione iniziale. L'unica differenza tra la chiamata iniziale e la chiamata di annullamento della registrazione è che durante la registrazione è necessario specificare il valore SNMPAPI ON nel parametro status e quando si chiama la funzione per annullare la registrazione, è necessario specificare \_ SNMPAPI  \_ OFF. Non è necessario associare chiamate di registrazione ridondanti alla **funzione SnmpRegister.** È necessario corrispondere solo alla prima chiamata di registrazione univoca.

Per modificare i criteri di filtro, potrebbe essere necessario prima annullare la registrazione e disabilitare il recapito di determinate trap o notifiche. L'applicazione può quindi creare un nuovo filtro chiamando [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), passando i valori appropriati.

 

 




