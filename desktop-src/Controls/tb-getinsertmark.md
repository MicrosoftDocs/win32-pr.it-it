---
title: Messaggio TB_GETINSERTMARK (COMmctrl. h)
description: Recupera il segno di inserimento corrente per la barra degli strumenti.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- Controlli di Windows Message TB_GETINSERTMARK
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047988"
---
# <a name="tb_getinsertmark-message"></a><span data-ttu-id="8f95f-104">TB \_ GETINSERTMARK messaggio</span><span class="sxs-lookup"><span data-stu-id="8f95f-104">TB\_GETINSERTMARK message</span></span>

<span data-ttu-id="8f95f-105">Recupera il segno di inserimento corrente per la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="8f95f-105">Retrieves the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f95f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f95f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f95f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f95f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8f95f-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8f95f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8f95f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f95f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f95f-110">Puntatore a una struttura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) che riceve il segno di inserimento.</span><span class="sxs-lookup"><span data-stu-id="8f95f-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f95f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f95f-111">Return value</span></span>

<span data-ttu-id="8f95f-112">Restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="8f95f-112">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f95f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f95f-113">Requirements</span></span>



| <span data-ttu-id="8f95f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f95f-114">Requirement</span></span> | <span data-ttu-id="8f95f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8f95f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f95f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f95f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8f95f-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f95f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f95f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f95f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8f95f-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8f95f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f95f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f95f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f95f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f95f-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f95f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f95f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f95f-123">**TB \_ SETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="8f95f-123">**TB\_SETINSERTMARK**</span></span>](tb-setinsertmark.md)
</dt> </dl>

 

 





