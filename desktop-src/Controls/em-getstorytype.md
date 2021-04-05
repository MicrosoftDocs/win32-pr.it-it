---
title: Messaggio di EM_GETSTORYTYPE (RichEdit. h)
description: Ottiene il tipo di storia.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- Controlli di Windows Message EM_GETSTORYTYPE
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873713"
---
# <a name="em_getstorytype-message"></a><span data-ttu-id="1f47c-104">\_Messaggio GETSTORYTYPE em</span><span class="sxs-lookup"><span data-stu-id="1f47c-104">EM\_GETSTORYTYPE message</span></span>

<span data-ttu-id="1f47c-105">Ottiene il tipo di storia.</span><span class="sxs-lookup"><span data-stu-id="1f47c-105">Gets the story type.</span></span>


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a><span data-ttu-id="1f47c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f47c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f47c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f47c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f47c-108">Indice della storia.</span><span class="sxs-lookup"><span data-stu-id="1f47c-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="1f47c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f47c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f47c-110">Riservati deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="1f47c-110">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f47c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f47c-111">Return value</span></span>

<span data-ttu-id="1f47c-112">Restituisce il tipo di storia, che può essere un valore personalizzato definito dal client o uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f47c-112">Returns the story type, which can be a client-defined custom value, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1f47c-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="1f47c-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="1f47c-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1f47c-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f47c-128">Requirements</span></span>



| <span data-ttu-id="1f47c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f47c-129">Requirement</span></span> | <span data-ttu-id="1f47c-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1f47c-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f47c-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f47c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1f47c-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1f47c-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1f47c-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f47c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1f47c-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1f47c-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f47c-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f47c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f47c-136"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f47c-136"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f47c-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f47c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f47c-138">**\_SETSTORYTYPE em**</span><span class="sxs-lookup"><span data-stu-id="1f47c-138">**EM\_SETSTORYTYPE**</span></span>](em-setstorytype.md)
</dt> <dt>

[<span data-ttu-id="1f47c-139">**ITextStoryRanges:: Item**</span><span class="sxs-lookup"><span data-stu-id="1f47c-139">**ITextStoryRanges::Item**</span></span>](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





