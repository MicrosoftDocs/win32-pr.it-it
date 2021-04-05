---
title: Proprietà DisplayName IResultVerb (WdsSharedIDL. h)
description: Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy, interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, proprietà DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048217"
---
# <a name="iresultverbdisplayname-property"></a><span data-ttu-id="385fa-106">IResultVerb::D proprietà di riproduzione</span><span class="sxs-lookup"><span data-stu-id="385fa-106">IResultVerb::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="385fa-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="385fa-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="385fa-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="385fa-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="385fa-109">Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.</span><span class="sxs-lookup"><span data-stu-id="385fa-109">This property returns a pointer to the localized display name for the verb.</span></span>

<span data-ttu-id="385fa-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="385fa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="385fa-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="385fa-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a><span data-ttu-id="385fa-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="385fa-112">Property value</span></span>

<span data-ttu-id="385fa-113">Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.</span><span class="sxs-lookup"><span data-stu-id="385fa-113">This property returns a pointer to the localized display name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="385fa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="385fa-114">Requirements</span></span>



| <span data-ttu-id="385fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="385fa-115">Requirement</span></span> | <span data-ttu-id="385fa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="385fa-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="385fa-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="385fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="385fa-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="385fa-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="385fa-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="385fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="385fa-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="385fa-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="385fa-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="385fa-121">Redistributable</span></span><br/>          | <span data-ttu-id="385fa-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="385fa-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="385fa-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="385fa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="385fa-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="385fa-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





