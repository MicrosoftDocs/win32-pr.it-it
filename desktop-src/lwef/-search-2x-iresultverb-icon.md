---
title: Proprietà Icon IResultVerb (WdsSharedIDL. h)
description: Questa proprietà restituisce un puntatore per gestire l'icona facoltativa associata al verbo.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Proprietà icona caratteristiche ambiente Windows legacy
- Proprietà icona caratteristiche ambiente Windows legacy, interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, proprietà Icon
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477668"
---
# <a name="iresultverbicon-property"></a><span data-ttu-id="3782a-106">Proprietà IResultVerb:: icon</span><span class="sxs-lookup"><span data-stu-id="3782a-106">IResultVerb::Icon property</span></span>

> [!NOTE]
> <span data-ttu-id="3782a-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3782a-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="3782a-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="3782a-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="3782a-109">Questa proprietà restituisce un puntatore per gestire l'icona facoltativa associata al verbo.</span><span class="sxs-lookup"><span data-stu-id="3782a-109">This property returns a pointer to handle of the optional icon associated with the verb.</span></span>

<span data-ttu-id="3782a-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3782a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3782a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3782a-111">Syntax</span></span>


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a><span data-ttu-id="3782a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3782a-112">Property value</span></span>

<span data-ttu-id="3782a-113">Hicon è un puntatore all'handle dell'icona facoltativa assocuated con il verbo.</span><span class="sxs-lookup"><span data-stu-id="3782a-113">hicon is a pointer to the handle of the optional icon assocuated with the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="3782a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3782a-114">Requirements</span></span>



| <span data-ttu-id="3782a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3782a-115">Requirement</span></span> | <span data-ttu-id="3782a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3782a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3782a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3782a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3782a-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3782a-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3782a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3782a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3782a-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="3782a-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3782a-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3782a-121">Redistributable</span></span><br/>          | <span data-ttu-id="3782a-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="3782a-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="3782a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3782a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3782a-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3782a-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





