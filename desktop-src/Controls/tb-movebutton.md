---
title: Messaggio TB_MOVEBUTTON (COMmctrl. h)
description: Sposta un pulsante da un indice a un altro.
ms.assetid: 030aedc5-2de5-4751-90b2-63794322f503
keywords:
- Controlli di Windows Message TB_MOVEBUTTON
topic_type:
- apiref
api_name:
- TB_MOVEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac4cd303e895998b12e710910432ba2c38b230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120682"
---
# <a name="tb_movebutton-message"></a><span data-ttu-id="e19e6-104">TB \_ MOVEBUTTON messaggio</span><span class="sxs-lookup"><span data-stu-id="e19e6-104">TB\_MOVEBUTTON message</span></span>

<span data-ttu-id="e19e6-105">Sposta un pulsante da un indice a un altro.</span><span class="sxs-lookup"><span data-stu-id="e19e6-105">Moves a button from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="e19e6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e19e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e19e6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e19e6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e19e6-108">Indice in base zero del pulsante da spostare.</span><span class="sxs-lookup"><span data-stu-id="e19e6-108">Zero-based index of the button to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="e19e6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e19e6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e19e6-110">Indice in base zero in cui verrà spostato il pulsante.</span><span class="sxs-lookup"><span data-stu-id="e19e6-110">Zero-based index where the button will be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e19e6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e19e6-111">Return value</span></span>

<span data-ttu-id="e19e6-112">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e19e6-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e19e6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e19e6-113">Requirements</span></span>



| <span data-ttu-id="e19e6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e19e6-114">Requirement</span></span> | <span data-ttu-id="e19e6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e19e6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e19e6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e19e6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e19e6-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e19e6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e19e6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e19e6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e19e6-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e19e6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e19e6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e19e6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e19e6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e19e6-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e19e6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e19e6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e19e6-123">**TB \_ SETANCHORHIGHLIGHT**</span><span class="sxs-lookup"><span data-stu-id="e19e6-123">**TB\_SETANCHORHIGHLIGHT**</span></span>](tb-setanchorhighlight.md)
</dt> </dl>

 

 





