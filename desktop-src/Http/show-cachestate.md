---
title: show cachestate
description: Elenca tutte le risorse e le relative proprietà associate memorizzate nella cache di risposta HTTP o Visualizza una singola risorsa e le proprietà associate.
ms.assetid: 9daa445e-dd2f-4b73-8938-58df931c015b
keywords:
- Mostra HTTP capetto
topic_type:
- apiref
api_name:
- show cachestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088a59eaa92db8ed9e8cbe59075d540507e51535
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104335047"
---
# <a name="show-cachestate"></a><span data-ttu-id="2b1e8-104">show cachestate</span><span class="sxs-lookup"><span data-stu-id="2b1e8-104">show cachestate</span></span>

<span data-ttu-id="2b1e8-105">Elenca tutte le risorse e le relative proprietà associate memorizzate nella cache di risposta HTTP o Visualizza una singola risorsa e le proprietà associate.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-105">Lists all resources and their associated properties that are cached in the HTTP response cache or displays a single resource and its associated properties.</span></span>

``` syntax
show cachestate [[url=]string]
 
```

## <a name="parameters"></a><span data-ttu-id="2b1e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b1e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b1e8-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[URL = \] ***stringa***\]**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[url=\]***string***\]**</span></span>
</dt> <dd>

<span data-ttu-id="2b1e8-108">URL completo.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-108">Fully qualified URL.</span></span> <span data-ttu-id="2b1e8-109">Se non specificato, implica tutti gli URL.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-109">If unspecified, implies all URLs.</span></span> <span data-ttu-id="2b1e8-110">L'URL può anche essere un prefisso per gli URL registrati.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-110">The URL can also be a prefix to registered URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2b1e8-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="2b1e8-111">Examples</span></span>

<span data-ttu-id="2b1e8-112">**Mostra URL capetto =https://www.contoso.com:80/myresource**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-112">**show cachestate url=https://www.contoso.com:80/myresource**</span></span>

 

 




