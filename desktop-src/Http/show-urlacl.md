---
title: show urlacl
description: Elenca gli elenchi DACL per l'URL riservato specificato o per tutti gli URL riservati.
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- Mostra HTTP urlacl
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86f7856e70a1be327297bb3fd4b892b3bf39789
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "103956025"
---
# <a name="show-urlacl"></a><span data-ttu-id="9e6ff-104">show urlacl</span><span class="sxs-lookup"><span data-stu-id="9e6ff-104">show urlacl</span></span>

<span data-ttu-id="9e6ff-105">Elenca gli elenchi DACL per l'URL riservato specificato o per tutti gli URL riservati.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-105">Lists DACLs for the specified reserved URL or all reserved URLs.</span></span>

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a><span data-ttu-id="9e6ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e6ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e6ff-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* stringa*</span><span class="sxs-lookup"><span data-stu-id="9e6ff-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="9e6ff-108">Specifica l'URL completo.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-108">Specifies the fully qualified URL.</span></span> <span data-ttu-id="9e6ff-109">Se non specificato, implica tutti gli URL.</span><span class="sxs-lookup"><span data-stu-id="9e6ff-109">If unspecified, implies all URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9e6ff-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="9e6ff-110">Examples</span></span>

<span data-ttu-id="9e6ff-111">**Mostra URL urlacl =https://+:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="9e6ff-111">**show urlacl url=https://+:80/MyUrl**</span></span>

<span data-ttu-id="9e6ff-112">**Mostra URL urlacl =https://www.contoso.com:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="9e6ff-112">**show urlacl url=https://www.contoso.com:80/MyUrl**</span></span>

 

 




