---
title: Scelta di una sequenza di protocollo
description: Le procedure consigliate per la scelta di una sequenza di protocollo prevedono l'uso di ncacn \_ ip \_ tcp e ncalrpc, non ncacn \_ np, ncacn \_ spx e ncadg \_ \ .
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732e00d46f1b471870447e228935a794db8d5dc5aa6486e3296b9936cd1be7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932224"
---
# <a name="choosing-a-protocol-sequence"></a>Scelta di una sequenza di protocollo

**Procedura consigliata:** Usare [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) quando si effettua una chiamata remota. Usare [**ncalrpc per**](/windows/desktop/Midl/ncalrpc) le chiamate locali. Non usare [**ncacn \_ np,**](/windows/desktop/Midl/ncacn-np) [**ncacn \_ spx**](/windows/desktop/Midl/ncacn-spx)o una delle sequenze di protocollo **ncadg, \_ \*** ma sono meno efficienti e hanno funzionalità inferiori.

 

 