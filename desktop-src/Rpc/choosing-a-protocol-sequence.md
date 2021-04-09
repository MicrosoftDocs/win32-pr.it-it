---
title: Scelta di una sequenza di protocollo
description: Le procedure consigliate per la scelta di una sequenza di protocollo coinvolgono l'uso di ncacn \_ IP \_ TCP e ncalrpc, non ncacn \_ NP, ncacn \_ SPX e ncadg \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3dea44868b96361ccaddc6e339f94fde92704f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047277"
---
# <a name="choosing-a-protocol-sequence"></a>Scelta di una sequenza di protocollo

**Procedura consigliata:** Usare [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) quando si effettua una chiamata remota. Usare [**ncalrpc**](/windows/desktop/Midl/ncalrpc) per le chiamate locali. Non usare [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ SPX**](/windows/desktop/Midl/ncacn-spx)o una delle sequenze di protocollo **ncadg \_ \*** ; sono meno efficienti e hanno funzionalità inferiori.

 

 