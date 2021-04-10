---
title: Messaggio TB_PRESSBUTTON (COMmctrl. h)
description: Preme o rilascia il pulsante specificato in una barra degli strumenti.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- Controlli di Windows Message TB_PRESSBUTTON
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e86092951b242cee7388fc0d5d1bbdbca835e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120679"
---
# <a name="tb_pressbutton-message"></a><span data-ttu-id="b9d91-104">TB \_ PRESSBUTTON messaggio</span><span class="sxs-lookup"><span data-stu-id="b9d91-104">TB\_PRESSBUTTON message</span></span>

<span data-ttu-id="b9d91-105">Preme o rilascia il pulsante specificato in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="b9d91-105">Presses or releases the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9d91-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9d91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9d91-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9d91-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d91-108">Identificatore di comando del pulsante da premere o rilasciare.</span><span class="sxs-lookup"><span data-stu-id="b9d91-108">Command identifier of the button to press or release.</span></span>

</dd> <dt>

<span data-ttu-id="b9d91-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9d91-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d91-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **bool** che indica se premere o rilasciare il pulsante specificato.</span><span class="sxs-lookup"><span data-stu-id="b9d91-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to press or release the specified button.</span></span> <span data-ttu-id="b9d91-111">Se **true**, viene premuto il pulsante.</span><span class="sxs-lookup"><span data-stu-id="b9d91-111">If **TRUE**, the button is pressed.</span></span> <span data-ttu-id="b9d91-112">Se **false**, il pulsante viene rilasciato.</span><span class="sxs-lookup"><span data-stu-id="b9d91-112">If **FALSE**, the button is released.</span></span>

<span data-ttu-id="b9d91-113">Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b9d91-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9d91-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9d91-114">Return value</span></span>

<span data-ttu-id="b9d91-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b9d91-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9d91-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9d91-116">Requirements</span></span>



| <span data-ttu-id="b9d91-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9d91-117">Requirement</span></span> | <span data-ttu-id="b9d91-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b9d91-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d91-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9d91-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b9d91-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9d91-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b9d91-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9d91-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b9d91-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b9d91-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b9d91-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9d91-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9d91-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9d91-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

