---
title: Messaggio ACM_ISPLAYING (COMmctrl. h)
description: Verifica se è in esecuzione un Audio-Video clip con interfoliazione (AVI). È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro di animazione.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- Controlli di Windows Message ACM_ISPLAYING
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048073"
---
# <a name="acm_isplaying-message"></a><span data-ttu-id="abb68-105">\_Messaggio di riproduzione ACM</span><span class="sxs-lookup"><span data-stu-id="abb68-105">ACM\_ISPLAYING message</span></span>

<span data-ttu-id="abb68-106">Verifica se è in esecuzione un Audio-Video clip con interfoliazione (AVI).</span><span class="sxs-lookup"><span data-stu-id="abb68-106">Checks whether an Audio-Video Interleaved (AVI) clip is playing.</span></span> <span data-ttu-id="abb68-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro di [**animazione \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .</span><span class="sxs-lookup"><span data-stu-id="abb68-107">You can send this message explicitly or use the [**Animate\_IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="abb68-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="abb68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abb68-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abb68-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abb68-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="abb68-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="abb68-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abb68-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abb68-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="abb68-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abb68-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abb68-113">Return value</span></span>

<span data-ttu-id="abb68-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="abb68-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="abb68-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abb68-115">Requirements</span></span>



| <span data-ttu-id="abb68-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="abb68-116">Requirement</span></span> | <span data-ttu-id="abb68-117">Valore</span><span class="sxs-lookup"><span data-stu-id="abb68-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abb68-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abb68-118">Minimum supported client</span></span><br/> | <span data-ttu-id="abb68-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abb68-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="abb68-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abb68-120">Minimum supported server</span></span><br/> | <span data-ttu-id="abb68-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abb68-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abb68-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abb68-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="abb68-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="abb68-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





