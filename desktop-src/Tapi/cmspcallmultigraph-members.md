---
description: Membri di CMSPCallMultiGraph
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Membri di CMSPCallMultiGraph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7e8842e0520d9325746cf663be8225199d4761ea8b93186bd681c4d3a4d0bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118868944"
---
# <a name="cmspcallmultigraph-members"></a>Membri di CMSPCallMultiGraph

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

I blocchi di attesa archiviano le informazioni sull'attesa registrata nel pool di thread. Include gli handle di attesa restituiti [**dalla chiamata RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) e un puntatore alla struttura del contesto. Ogni blocco nella matrice è per un grafo in uno degli oggetti flusso. L'offset di un blocco in questa matrice corrisponde all'offset del flusso proprietario del grafico.

 

 
