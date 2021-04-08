---
title: Stringhe di tipo C
description: Un'applicazione WinSNMP può usare stringhe di tipo C con terminazione NULL per convertire oggetti di entità e identificatori di oggetto (OID) in e dalle relative rappresentazioni di stringa.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855214"
---
# <a name="c-style-strings"></a>Stringhe di tipo C

Un'applicazione WinSNMP può usare stringhe di tipo C con terminazione **null** per convertire oggetti di entità e identificatori di oggetto (OID) in e dalle relative rappresentazioni di stringa.

Le funzioni WinSNMP che modificano le stringhe di tipo C includono [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr). Poiché [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) restituiscono un puntatore a una variabile stringa di tipo C, l'applicazione WinSNMP deve passare un valore appropriato nel parametro *size* quando effettua chiamate a queste funzioni. Per ulteriori informazioni, vedere le pagine di riferimento per queste funzioni.

> [!Note]  
> Il parametro *context* delle funzioni [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) e [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) deve essere una struttura di stringhe di ottetti, ovvero una struttura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) . Il parametro *context* non può essere una stringa di tipo C. La stringa contenuta in una struttura **smiOCTETS** non richiede un byte di terminazione **null**.

 

 

 




