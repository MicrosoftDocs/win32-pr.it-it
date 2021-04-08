---
title: Messaggio di EM_SETHYPHENATEINFO (RichEdit. h)
description: Imposta il modo in cui un controllo Rich Edit esegue la sillabazione.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- Controlli di Windows Message EM_SETHYPHENATEINFO
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874357"
---
# <a name="em_sethyphenateinfo-message"></a><span data-ttu-id="de7fb-104">\_Messaggio SETHYPHENATEINFO em</span><span class="sxs-lookup"><span data-stu-id="de7fb-104">EM\_SETHYPHENATEINFO message</span></span>

<span data-ttu-id="de7fb-105">Imposta il modo in cui un controllo Rich Edit esegue la sillabazione.</span><span class="sxs-lookup"><span data-stu-id="de7fb-105">Sets the way a rich edit control does hyphenation.</span></span>

## <a name="parameters"></a><span data-ttu-id="de7fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de7fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de7fb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de7fb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de7fb-108">Puntatore a una struttura [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .</span><span class="sxs-lookup"><span data-stu-id="de7fb-108">Pointer to a [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="de7fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de7fb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de7fb-110">Non utilizzato, deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="de7fb-110">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de7fb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="de7fb-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="de7fb-112">Per abilitare la sillabazione, il client deve chiamare [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), specificando \_ ADVANCEDTYPOGRAPHY.</span><span class="sxs-lookup"><span data-stu-id="de7fb-112">To enable hyphenation, the client must call [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), specifying TO\_ADVANCEDTYPOGRAPHY.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de7fb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de7fb-113">Requirements</span></span>



| <span data-ttu-id="de7fb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de7fb-114">Requirement</span></span> | <span data-ttu-id="de7fb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="de7fb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de7fb-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de7fb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de7fb-117">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-117">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de7fb-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de7fb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de7fb-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de7fb-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de7fb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de7fb-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de7fb-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de7fb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de7fb-123">**\_GETHYPHENATEINFO em**</span><span class="sxs-lookup"><span data-stu-id="de7fb-123">**EM\_GETHYPHENATEINFO**</span></span>](em-gethyphenateinfo.md)
</dt> </dl>

 

 





