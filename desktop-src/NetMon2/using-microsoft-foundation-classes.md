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
# <a name="using-microsoft-foundation-classes"></a><span data-ttu-id="f7f2d-103">Utilizzo di Microsoft Foundation Classes</span><span class="sxs-lookup"><span data-stu-id="f7f2d-103">Using Microsoft Foundation Classes</span></span>

<span data-ttu-id="f7f2d-104">A causa del footprint delle DLL collegate in modo statico, è consigliabile evitare di usare Microsoft Foundation Classes (MFC) per scrivere un esperto.</span><span class="sxs-lookup"><span data-stu-id="f7f2d-104">Because of the footprint of statically linked DLLs, you should avoid using Microsoft Foundation Classes (MFCs) to write an expert.</span></span> <span data-ttu-id="f7f2d-105">Tuttavia, se si usa MFC, assicurarsi di accedere a qualsiasi risorsa DLL MFC includendo il codice seguente immediatamente dopo la voce:</span><span class="sxs-lookup"><span data-stu-id="f7f2d-105">However, if you use the MFC, ensure access to any of the MFC DLL resources by including the following code immediately upon entry:</span></span>

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



