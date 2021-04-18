---
title: Proprietà hint IResultProperty (WdsSharedIDL. h)
description: Valore speciale usato per facilitare il recupero dei dati.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Proprietà hint caratteristiche ambiente Windows legacy
- Proprietà hint caratteristiche ambiente Windows legacy, interfaccia IResultProperty
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty, proprietà hint
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301415"
---
# <a name="iresultpropertyhint-property"></a><span data-ttu-id="760fa-106">Proprietà IResultProperty:: hint</span><span class="sxs-lookup"><span data-stu-id="760fa-106">IResultProperty::Hint property</span></span>

> [!NOTE]
> <span data-ttu-id="760fa-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="760fa-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="760fa-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="760fa-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="760fa-109">Valore speciale usato per facilitare il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="760fa-109">Special value used to aid data retrieval.</span></span>

<span data-ttu-id="760fa-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="760fa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="760fa-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="760fa-111">Syntax</span></span>


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a><span data-ttu-id="760fa-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="760fa-112">Property value</span></span>

<span data-ttu-id="760fa-113">Restituisce un puntatore all'hint.</span><span class="sxs-lookup"><span data-stu-id="760fa-113">returns a pointer to the hint.</span></span>

## <a name="requirements"></a><span data-ttu-id="760fa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="760fa-114">Requirements</span></span>



| <span data-ttu-id="760fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="760fa-115">Requirement</span></span> | <span data-ttu-id="760fa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="760fa-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="760fa-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="760fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="760fa-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="760fa-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="760fa-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="760fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="760fa-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="760fa-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="760fa-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="760fa-121">Redistributable</span></span><br/>          | <span data-ttu-id="760fa-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="760fa-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="760fa-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="760fa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="760fa-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="760fa-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





