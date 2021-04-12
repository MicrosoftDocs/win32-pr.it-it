---
title: Gestione degli identificatori di oggetto
description: L'API WinSNMP fornisce diverse funzioni di utilità WinSNMP che semplificano la manipolazione degli identificatori di oggetto per le applicazioni WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471643"
---
# <a name="managing-object-identifiers"></a>Gestione degli identificatori di oggetto

L'API WinSNMP fornisce diverse [funzioni di utilità WinSNMP](winsnmp-functions.md) che semplificano la manipolazione degli identificatori di oggetto per le applicazioni WinSNMP.

La funzione [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) converte la rappresentazione binaria interna di un identificatore di oggetto nel formato della stringa numerica punteggiata. Quando si chiama [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), specificare un buffer di stringa di lunghezza MAXOBJIDSTRSIZE (1408 byte) per assicurarsi che il buffer di output sia sufficientemente grande da mantenere la stringa convertita. Per convertire un identificatore di oggetto dal formato della stringa numerica punteggiata alla relativa rappresentazione binaria interna, chiamare la funzione [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .

Per copiare un identificatore di oggetto SNMP, chiamare la funzione [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) . Questa funzione alloca qualsiasi memoria necessaria per il nuovo identificatore di oggetto.

Un'applicazione WinSNMP deve chiamare la funzione [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per liberare le risorse allocate per il membro **ptr** della struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) specificata dalle funzioni [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) e [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .

La funzione [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) Confronta due identificatori di oggetto SNMP. L'applicazione WinSNMP può specificare il numero di sottoidentificatori da confrontare. Chiamare **SnmpOidCompare** per determinare se due identificatori di oggetto hanno prefissi comuni.

Per ulteriori informazioni sulla gestione della memoria allocata per gli identificatori di oggetto, vedere [allocazione di oggetti memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




