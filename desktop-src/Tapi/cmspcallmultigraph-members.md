---
description: Membri di CMSPCallMultiGraph
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Membri di CMSPCallMultiGraph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312722"
---
# <a name="cmspcallmultigraph-members"></a>Membri di CMSPCallMultiGraph

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

I blocchi di attesa archiviano le informazioni relative all'attesa registrata nel pool di thread. Include gli handle di attesa restituiti dalla chiamata [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) e un puntatore alla struttura del contesto. Ogni blocco nella matrice è per un grafico in uno degli oggetti flusso. L'offset di un blocco in questa matrice è uguale all'offset del flusso proprietario del grafico.

 

 
