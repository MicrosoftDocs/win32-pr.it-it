---
description: A causa del footprint delle DLL collegate in modo statico, è consigliabile evitare di usare Microsoft Foundation Classes (MFC) per scrivere un esperto.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Uso di Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec1b01260d3fd7d1e7058c9fff8aa3cc32390b3f2f6cc715c91563a871fbf20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362930"
---
# <a name="using-microsoft-foundation-classes"></a>Uso di Microsoft Foundation Classes

A causa del footprint delle DLL collegate in modo statico, è consigliabile evitare di usare Microsoft Foundation Classes (MFC) per scrivere un esperto. Tuttavia, se si usa MFC, assicurarsi di accedere a qualsiasi risorsa DLL MFC includendo il codice seguente immediatamente dopo l'immissione:

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



