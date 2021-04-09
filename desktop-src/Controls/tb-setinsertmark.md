---
title: Messaggio TB_SETINSERTMARK (COMmctrl. h)
description: Imposta il segno di inserimento corrente per la barra degli strumenti.
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- Controlli di Windows Message TB_SETINSERTMARK
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f65ba83d13cbb45f54833725a46de61a5f0444c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118974"
---
# <a name="tb_setinsertmark-message"></a><span data-ttu-id="5ed29-104">TB \_ SETINSERTMARK messaggio</span><span class="sxs-lookup"><span data-stu-id="5ed29-104">TB\_SETINSERTMARK message</span></span>

<span data-ttu-id="5ed29-105">Imposta il segno di inserimento corrente per la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="5ed29-105">Sets the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ed29-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ed29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed29-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ed29-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5ed29-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5ed29-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5ed29-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ed29-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ed29-110">Puntatore a una struttura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) che contiene il segno di inserimento.</span><span class="sxs-lookup"><span data-stu-id="5ed29-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that contains the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed29-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ed29-111">Return value</span></span>

<span data-ttu-id="5ed29-112">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5ed29-112">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed29-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ed29-113">Requirements</span></span>



| <span data-ttu-id="5ed29-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed29-114">Requirement</span></span> | <span data-ttu-id="5ed29-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5ed29-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed29-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ed29-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed29-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ed29-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ed29-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ed29-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed29-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5ed29-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ed29-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ed29-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed29-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ed29-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed29-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ed29-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed29-123">**TB \_ GETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="5ed29-123">**TB\_GETINSERTMARK**</span></span>](tb-getinsertmark.md)
</dt> </dl>

 

 





