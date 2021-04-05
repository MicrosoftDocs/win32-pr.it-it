---
description: A causa del footprint delle DLL collegate in modo statico, è consigliabile evitare di usare Microsoft Foundation Classes (MFC) per scrivere un esperto.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Utilizzo di Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097c4baea2ec109933d52eed420042528e9eea76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757613"
---
# <a name="using-microsoft-foundation-classes"></a>Utilizzo di Microsoft Foundation Classes

A causa del footprint delle DLL collegate in modo statico, è consigliabile evitare di usare Microsoft Foundation Classes (MFC) per scrivere un esperto. Tuttavia, se si usa MFC, assicurarsi di accedere a qualsiasi risorsa DLL MFC includendo il codice seguente immediatamente dopo la voce:

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



