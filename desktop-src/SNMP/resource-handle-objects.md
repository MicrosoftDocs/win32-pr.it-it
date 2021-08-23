---
title: Oggetti handle di risorsa
description: La struttura di un oggetto risorsa è limitata all'implementazione Microsoft WinSNMP. Un'applicazione WinSNMP può accedere a un oggetto risorsa con un handle.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b05702f0ad43e5b4b80a9b1a3cada471212dec3bc377bddcc95fe9a109ec78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009119"
---
# <a name="resource-handle-objects"></a>Oggetti handle di risorsa

La struttura di un oggetto risorsa è limitata all'implementazione Microsoft WinSNMP. Un'applicazione WinSNMP può accedere a un oggetto risorsa con un handle.

L'implementazione può allocare uno dei tipi seguenti di handle di risorse per un'applicazione WinSNMP.

| Tipo di handle        | Descrizione                       |
|--------------------|-----------------------------------|
| **SESSIONE \_ HSNMP** | Handle per una sessione WinSNMP       |
| **ENTITÀ \_ HSNMP**  | Handle per un'entità SNMP          |
| **CONTESTO \_ HSNMP** | Handle per un contesto WinSNMP       |
| **HSNMP \_ PDU**     | Handle a un'unità dati del protocollo    |
| **HSNMP \_ VBL**     | Handle a un elenco di associazioni di variabili |



 

Un'applicazione WinSNMP può richiedere che l'implementazione crei o elimini gli handle di risorsa, ma l'implementazione esegue l'operazione. Per altre informazioni sulla liberatura di singole risorse, vedere le funzioni [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)e [**SnmpFreeContext.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)

 

 




