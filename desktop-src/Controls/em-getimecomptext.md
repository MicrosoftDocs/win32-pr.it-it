---
title: Messaggio di EM_GETIMECOMPTEXT (RichEdit. h)
description: Recupera il testo della composizione IME (Input Method Editor).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- Controlli di Windows Message EM_GETIMECOMPTEXT
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964577"
---
# <a name="em_getimecomptext-message"></a><span data-ttu-id="651bb-104">\_Messaggio GETIMECOMPTEXT em</span><span class="sxs-lookup"><span data-stu-id="651bb-104">EM\_GETIMECOMPTEXT message</span></span>

<span data-ttu-id="651bb-105">Recupera il testo della composizione IME (Input Method Editor).</span><span class="sxs-lookup"><span data-stu-id="651bb-105">Retrieves the Input Method Editor (IME) composition text.</span></span>

## <a name="parameters"></a><span data-ttu-id="651bb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="651bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="651bb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="651bb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="651bb-108">Struttura [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) .</span><span class="sxs-lookup"><span data-stu-id="651bb-108">The [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) structure.</span></span>

</dd> <dt>

<span data-ttu-id="651bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="651bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="651bb-110">Buffer che riceve il testo di composizione.</span><span class="sxs-lookup"><span data-stu-id="651bb-110">The buffer that receives the composition text.</span></span> <span data-ttu-id="651bb-111">La dimensione di questo buffer è contenuta nel membro **CB** della struttura *wParam* .</span><span class="sxs-lookup"><span data-stu-id="651bb-111">The size of this buffer is contained in the **cb** member of the *wParam* structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="651bb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="651bb-112">Return value</span></span>

<span data-ttu-id="651bb-113">Se ha esito positivo, il valore restituito è il numero di caratteri Unicode copiati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="651bb-113">If successful, the return value is the number of Unicode characters copied to the buffer.</span></span> <span data-ttu-id="651bb-114">In caso contrario, è zero.</span><span class="sxs-lookup"><span data-stu-id="651bb-114">Otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="651bb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="651bb-115">Remarks</span></span>

<span data-ttu-id="651bb-116">Questo messaggio accetta solo stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="651bb-116">This message only takes Unicode strings.</span></span>

<span data-ttu-id="651bb-117">**Avviso di sicurezza:** Assicurarsi di disporre di un buffer sufficiente per le dimensioni dell'input.</span><span class="sxs-lookup"><span data-stu-id="651bb-117">**Security Warning:** Be sure to have a buffer sufficient for the size of the input.</span></span> <span data-ttu-id="651bb-118">In caso contrario, potrebbero verificarsi problemi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="651bb-118">Failure to do so could cause problems for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="651bb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="651bb-119">Requirements</span></span>



| <span data-ttu-id="651bb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="651bb-120">Requirement</span></span> | <span data-ttu-id="651bb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="651bb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="651bb-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="651bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="651bb-123">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="651bb-123">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="651bb-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="651bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="651bb-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="651bb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="651bb-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="651bb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="651bb-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="651bb-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="651bb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="651bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="651bb-129">**IMECOMPTEXT**</span><span class="sxs-lookup"><span data-stu-id="651bb-129">**IMECOMPTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





