---
title: Proprietà UID IPropertyFilter (WdsSharedIDL. h)
description: UID per la proprietà in base a cui filtrare.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà UID
- Funzionalità dell'ambiente Windows legacy della proprietà UID, interfaccia IPropertyFilter
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilter, proprietà UID
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529f3f9142345705b9e14cabd2a46200d62fe2ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340902"
---
# <a name="ipropertyfilteruid-property"></a><span data-ttu-id="f5f07-106">Proprietà IPropertyFilter:: UID</span><span class="sxs-lookup"><span data-stu-id="f5f07-106">IPropertyFilter::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="f5f07-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f5f07-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="f5f07-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f07-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="f5f07-109">UID per la proprietà in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="f5f07-109">UID for the property to filter by.</span></span>

<span data-ttu-id="f5f07-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f5f07-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f07-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5f07-111">Syntax</span></span>


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="f5f07-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f5f07-112">Property value</span></span>

<span data-ttu-id="f5f07-113">Imposta la proprietà UID.</span><span class="sxs-lookup"><span data-stu-id="f5f07-113">Sets the UID property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f07-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5f07-114">Requirements</span></span>



| <span data-ttu-id="f5f07-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5f07-115">Requirement</span></span> | <span data-ttu-id="f5f07-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f5f07-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f07-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5f07-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f07-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5f07-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f5f07-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5f07-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f07-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="f5f07-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f5f07-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f5f07-121">Redistributable</span></span><br/>          | <span data-ttu-id="f5f07-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="f5f07-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="f5f07-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5f07-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5f07-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5f07-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





