---
title: Messaggio di EM_GETTOUCHOPTIONS (RichEdit. h)
description: Recupera le opzioni di tocco associate a un controllo Rich Edit.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- Controlli di Windows Message EM_GETTOUCHOPTIONS
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048603"
---
# <a name="em_gettouchoptions-message"></a><span data-ttu-id="b489f-104">\_Messaggio GETTOUCHOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="b489f-104">EM\_GETTOUCHOPTIONS message</span></span>

<span data-ttu-id="b489f-105">Recupera le opzioni di tocco associate a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b489f-105">Retrieves the touch options that are associated with a rich edit control.</span></span>


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a><span data-ttu-id="b489f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b489f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b489f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b489f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b489f-108">Opzioni di tocco da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b489f-108">The touch options to retrieve.</span></span> <span data-ttu-id="b489f-109">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b489f-109">It can be one of the following values.</span></span>



| <span data-ttu-id="b489f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b489f-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="b489f-111">Significato</span><span class="sxs-lookup"><span data-stu-id="b489f-111">Meaning</span></span>                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="b489f-112"><dt>**\_SHOWHANDLES RTO**</dt></span><span class="sxs-lookup"><span data-stu-id="b489f-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="b489f-113">Recupera un valore che indica se le pinze tocco sono visibili.</span><span class="sxs-lookup"><span data-stu-id="b489f-113">Retrieves whether the touch grippers are visible.</span></span><br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="b489f-114"><dt>**\_DISABLEHANDLES RTO**</dt></span><span class="sxs-lookup"><span data-stu-id="b489f-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="b489f-115">Il recupero del flag non è implementato.</span><span class="sxs-lookup"><span data-stu-id="b489f-115">Retrieving this flag is not implemented.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="b489f-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b489f-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b489f-117">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b489f-117">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b489f-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b489f-118">Return value</span></span>

<span data-ttu-id="b489f-119">Restituisce il valore dell'opzione specificata dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="b489f-119">Returns the value of the option specified by the *wParam* parameter.</span></span> <span data-ttu-id="b489f-120">È diverso da zero se *wParam* è **RTO \_ SHOWHANDLES** e le pinze tocco sono visibili; zero, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b489f-120">It is nonzero if *wParam* is **RTO\_SHOWHANDLES** and the touch grippers are visible; zero, otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b489f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b489f-121">Requirements</span></span>



| <span data-ttu-id="b489f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b489f-122">Requirement</span></span> | <span data-ttu-id="b489f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b489f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b489f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b489f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b489f-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b489f-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b489f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b489f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b489f-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b489f-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b489f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b489f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b489f-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b489f-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b489f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b489f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b489f-131">**\_SETTOUCHOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="b489f-131">**EM\_SETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





