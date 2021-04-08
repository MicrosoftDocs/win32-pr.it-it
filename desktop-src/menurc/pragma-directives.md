---
title: Direttive pragma
description: RC non supporta le direttive pragma supportate dal compilatore C/C++.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046721"
---
# <a name="pragma-directives"></a><span data-ttu-id="22e53-103">Direttive pragma</span><span class="sxs-lookup"><span data-stu-id="22e53-103">Pragma Directives</span></span>

<span data-ttu-id="22e53-104">RC non supporta le direttive pragma supportate dal compilatore C/C++.</span><span class="sxs-lookup"><span data-stu-id="22e53-104">RC does not support the pragma directives supported by the C/C++ compiler.</span></span> <span data-ttu-id="22e53-105">Tuttavia, RC supporta la direttiva pragma seguente per modificare la tabella codici:</span><span class="sxs-lookup"><span data-stu-id="22e53-105">However, RC does support the following pragma directive for changing the code page:</span></span>

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

<span data-ttu-id="22e53-106">Questo pragma non è supportato in un file di risorse incluso (RC).</span><span class="sxs-lookup"><span data-stu-id="22e53-106">This pragma is not supported in an included resource file (.rc).</span></span> <span data-ttu-id="22e53-107">Se pertanto si dispone di un file RC padre che include i file RC per più lingue, utilizzare questo pragma prima di includere un altro file RC anziché utilizzarlo nel file RC incluso.</span><span class="sxs-lookup"><span data-stu-id="22e53-107">Therefore, if you have a parent .rc file and it includes .rc files for multiple languages, use this pragma before including another .rc file rather than using it in the included .rc file itself.</span></span> <span data-ttu-id="22e53-108">Questo approccio è illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="22e53-108">This is demonstrated in the following example.</span></span>

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

<span data-ttu-id="22e53-109">Per un elenco di valori per CodePageNum, vedere la pagina relativa agli [identificatori](../intl/code-page-identifiers.md)delle tabelle codici.</span><span class="sxs-lookup"><span data-stu-id="22e53-109">For a list of values for CodePageNum, see [Code Page Identifiers](../intl/code-page-identifiers.md).</span></span>

 

 