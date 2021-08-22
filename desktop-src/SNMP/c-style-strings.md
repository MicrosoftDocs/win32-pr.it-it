---
title: Stringhe di tipo C
description: Un'applicazione WinSNMP può usare stringhe di tipo C con terminazione NULL per convertire oggetti identificatore di entità e oggetto (OID) in e dalle relative rappresentazioni di stringa.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6449514d4c08baae638d950a42f7f553e0037efe6bdc45b8045dbd315c1a2c65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009750"
---
# <a name="c-style-strings"></a>Stringhe di tipo C

Un'applicazione WinSNMP può usare stringhe di tipo C con terminazione **NULL** per convertire oggetti identificatore di entità e oggetto (OID) in e dalle relative rappresentazioni di stringa.

Le funzioni WinSNMP che modificano le stringhe di tipo C includono [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr). Poiché [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) restituiscono un puntatore a una variabile stringa di tipo C, l'applicazione WinSNMP deve passare un valore appropriato nel parametro *size* quando effettua chiamate a queste funzioni. Per altre informazioni, vedere le pagine di riferimento per queste funzioni.

> [!Note]  
> Il *parametro* di contesto [**delle funzioni SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) e [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) deve essere una struttura di stringhe ottetti, ad esempio una [**struttura smiOCTETS.**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) Il *parametro di* contesto non può essere una stringa di tipo C. La stringa contenuta in **una struttura smiOCTETS** non richiede un byte con terminazione **NULL.**

 

 

 




