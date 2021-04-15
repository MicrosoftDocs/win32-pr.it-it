---
title: Messaggio TTM_NEWTOOLRECT (COMmctrl. h)
description: Imposta un nuovo rettangolo di delimitazione per uno strumento.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- Controlli di Windows Message TTM_NEWTOOLRECT
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476780"
---
# <a name="ttm_newtoolrect-message"></a><span data-ttu-id="b4c70-104">\_Messaggio TTM NEWTOOLRECT</span><span class="sxs-lookup"><span data-stu-id="b4c70-104">TTM\_NEWTOOLRECT message</span></span>

<span data-ttu-id="b4c70-105">Imposta un nuovo rettangolo di delimitazione per uno strumento.</span><span class="sxs-lookup"><span data-stu-id="b4c70-105">Sets a new bounding rectangle for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4c70-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4c70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4c70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4c70-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b4c70-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b4c70-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b4c70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4c70-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4c70-110">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b4c70-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="b4c70-111">I membri **HWND** e **UID** identificano uno strumento e il membro **Rect** specifica il nuovo rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="b4c70-111">The **hwnd** and **uId** members identify a tool, and the **rect** member specifies the new bounding rectangle.</span></span> <span data-ttu-id="b4c70-112">Prima di inviare questo messaggio, è necessario compilare il membro **cbSize** della struttura.</span><span class="sxs-lookup"><span data-stu-id="b4c70-112">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4c70-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4c70-113">Return value</span></span>

<span data-ttu-id="b4c70-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b4c70-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c70-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4c70-115">Requirements</span></span>



| <span data-ttu-id="b4c70-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4c70-116">Requirement</span></span> | <span data-ttu-id="b4c70-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b4c70-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c70-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4c70-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4c70-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4c70-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4c70-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4c70-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4c70-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4c70-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4c70-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4c70-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4c70-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4c70-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b4c70-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b4c70-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b4c70-125">**TTM \_ NEWTOOLRECTW** (Unicode) e **TTM \_ NEWTOOLRECTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b4c70-125">**TTM\_NEWTOOLRECTW** (Unicode) and **TTM\_NEWTOOLRECTA** (ANSI)</span></span><br/>           |



 

 





