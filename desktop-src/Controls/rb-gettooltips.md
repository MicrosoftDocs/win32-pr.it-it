---
title: Messaggio RB_GETTOOLTIPS (COMmctrl. h)
description: Recupera l'handle per qualsiasi controllo ToolTip associato al controllo Rebar.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- Controlli di Windows Message RB_GETTOOLTIPS
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b500e7009ca5f5cad46dc72d5deebeebca047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120275"
---
# <a name="rb_gettooltips-message"></a><span data-ttu-id="d2695-104">\_Messaggio RB GETtooltips</span><span class="sxs-lookup"><span data-stu-id="d2695-104">RB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="d2695-105">Recupera l'handle per qualsiasi controllo ToolTip associato al controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="d2695-105">Retrieves the handle to any tooltip control associated with the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2695-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2695-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2695-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2695-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d2695-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d2695-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d2695-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2695-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2695-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d2695-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2695-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2695-111">Return value</span></span>

<span data-ttu-id="d2695-112">Restituisce un valore **HWND** che rappresenta l'handle per il controllo ToolTip associato al controllo Rebar oppure zero se al controllo Rebar non è associato alcun controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d2695-112">Returns an **HWND** value that is the handle to the tooltip control associated with the rebar control, or zero if no tooltip control is associated with the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2695-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2695-113">Requirements</span></span>



| <span data-ttu-id="d2695-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2695-114">Requirement</span></span> | <span data-ttu-id="d2695-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d2695-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2695-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2695-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d2695-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2695-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2695-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2695-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d2695-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2695-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2695-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2695-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2695-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2695-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





