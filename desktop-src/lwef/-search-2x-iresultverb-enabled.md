---
title: Proprietà Enabled di IResultVerb (WdsSharedIDL. h)
description: Questa proprietà restituisce TRUE se il verbo è abilitato.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- Funzionalità della proprietà Enabled ambiente Windows legacy
- Funzionalità abilitate proprietà ambiente Windows legacy, interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, proprietà Enabled
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8570e7bbb06843467080dd0dd748391234f259d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964492"
---
# <a name="iresultverbenabled-property"></a><span data-ttu-id="73154-106">Proprietà IResultVerb:: Enabled</span><span class="sxs-lookup"><span data-stu-id="73154-106">IResultVerb::Enabled property</span></span>

> [!NOTE]
> <span data-ttu-id="73154-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="73154-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="73154-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="73154-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="73154-109">Questa proprietà restituisce TRUE se il verbo è abilitato.</span><span class="sxs-lookup"><span data-stu-id="73154-109">This property returns TRUE if the verb is enabled.</span></span>

<span data-ttu-id="73154-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="73154-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73154-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73154-111">Syntax</span></span>


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a><span data-ttu-id="73154-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="73154-112">Property value</span></span>

<span data-ttu-id="73154-113">Questa proprietà restituisce true se il verbo è abilitato o false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="73154-113">This property returns True if the verb is enabled or False if not.</span></span>

## <a name="requirements"></a><span data-ttu-id="73154-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73154-114">Requirements</span></span>



| <span data-ttu-id="73154-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="73154-115">Requirement</span></span> | <span data-ttu-id="73154-116">Valore</span><span class="sxs-lookup"><span data-stu-id="73154-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="73154-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73154-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73154-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="73154-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="73154-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73154-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73154-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="73154-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="73154-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="73154-121">Redistributable</span></span><br/>          | <span data-ttu-id="73154-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="73154-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="73154-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73154-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="73154-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="73154-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





