---
title: Gestione degli identificatori di oggetto
description: L'API WinSNMP offre diverse funzioni di utilità WinSNMP che semplificano la manipolazione degli identificatori di oggetto per le applicazioni WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362adbf445901f25307452d67c313ef2a8d0ac5aea038ebfcf61863a72370cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009419"
---
# <a name="managing-object-identifiers"></a>Gestione degli identificatori di oggetto

L'API WinSNMP offre diverse funzioni di utilità [WinSNMP](winsnmp-functions.md) che semplificano la manipolazione degli identificatori di oggetto per le applicazioni WinSNMP.

La [**funzione SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) converte la rappresentazione binaria interna di un identificatore di oggetto nel formato di stringa numerico tratteggiato. Quando si chiama [**SnmpOidToStr,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)specificare un buffer di stringa di lunghezza MAXOBJIDSTRSIZE (1408 byte) per assicurarsi che il buffer di output sia sufficientemente grande da contenere la stringa convertita. Per convertire un identificatore di oggetto dal formato di stringa numerica tratteggiata alla relativa rappresentazione binaria interna, chiamare [**la funzione SnmpStrToOid.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

Per copiare un identificatore di oggetto SNMP, chiamare [**la funzione SnmpOidCopy.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) Questa funzione alloca la memoria necessaria per il nuovo identificatore di oggetto.

Un'applicazione WinSNMP deve chiamare la funzione [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per liberare le risorse allocate per il membro **ptr** della struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) specificata dalle funzioni [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) e [**SnmpOidCopy.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)

La [**funzione SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) confronta due identificatori di oggetto SNMP. L'applicazione WinSNMP può specificare il numero di sottoidentificatori da confrontare. Chiamare **SnmpOidCompare per** determinare se due identificatori di oggetto hanno prefissi comuni.

Per altre informazioni sulla gestione della memoria allocata per gli identificatori di oggetto, vedere Allocazione di oggetti di memoria [WinSNMP.](allocating-winsnmp-memory-objects.md)

 

 




