---
title: Oggetti handle di risorsa
description: La struttura di un oggetto risorsa è limitata all'implementazione di Microsoft WinSNMP. Un'applicazione WinSNMP può accedere a un oggetto risorsa con un handle.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713060"
---
# <a name="resource-handle-objects"></a>Oggetti handle di risorsa

La struttura di un oggetto risorsa è limitata all'implementazione di Microsoft WinSNMP. Un'applicazione WinSNMP può accedere a un oggetto risorsa con un handle.

L'implementazione può allocare uno dei seguenti tipi di handle di risorse per un'applicazione WinSNMP.

| Tipo di handle        | Descrizione                       |
|--------------------|-----------------------------------|
| **\_sessione HSNMP** | Handle per una sessione WinSNMP       |
| **\_entità HSNMP**  | Handle per un'entità SNMP          |
| **\_contesto HSNMP** | Handle per un contesto WinSNMP       |
| **\_PDU HSNMP**     | Handle per un'unità dati del protocollo    |
| **\_VBL HSNMP**     | Handle per un elenco di associazioni variabili |



 

Un'applicazione WinSNMP può richiedere che l'implementazione crei o elimini gli handle di risorsa, ma l'implementazione esegue l'operazione. Per ulteriori informazioni su come liberare le singole risorse, vedere le funzioni [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)e [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .

 

 




