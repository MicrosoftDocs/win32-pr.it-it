---
title: Messaggio di EM_GETIMEOPTIONS (RichEdit. h)
description: Recupera le opzioni IME (Input Method Editor) correnti.
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- Controlli di Windows Message EM_GETIMEOPTIONS
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120531"
---
# <a name="em_getimeoptions-message"></a><span data-ttu-id="cd071-104">\_Messaggio GETIMEOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="cd071-104">EM\_GETIMEOPTIONS message</span></span>

<span data-ttu-id="cd071-105">Recupera le opzioni IME (Input Method Editor) correnti.</span><span class="sxs-lookup"><span data-stu-id="cd071-105">Retrieves the current Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="cd071-106">Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="cd071-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="cd071-107">Non è supportata nelle versioni successive di Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cd071-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="cd071-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd071-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd071-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd071-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd071-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cd071-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd071-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd071-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd071-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cd071-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd071-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd071-113">Return value</span></span>

<span data-ttu-id="cd071-114">Questo messaggio restituisce uno o più valori del flag di opzione IME descritti nel messaggio [**\_ SETIMEOPTIONS em**](em-setimeoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="cd071-114">This message returns one or more of the IME option flag values described in the [**EM\_SETIMEOPTIONS**](em-setimeoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd071-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd071-115">Requirements</span></span>



| <span data-ttu-id="cd071-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd071-116">Requirement</span></span> | <span data-ttu-id="cd071-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cd071-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd071-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd071-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd071-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd071-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd071-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd071-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd071-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd071-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd071-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd071-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd071-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd071-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd071-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd071-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd071-125">**\_SETIMEOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="cd071-125">**EM\_SETIMEOPTIONS**</span></span>](em-setimeoptions.md)
</dt> </dl>

 

 





