---
title: Messaggio TTM_ADDTOOL (COMmctrl. h)
description: Registra uno strumento con un controllo ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- Controlli di Windows Message TTM_ADDTOOL
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301658"
---
# <a name="ttm_addtool-message"></a><span data-ttu-id="0f112-104">\_Messaggio TTM ADDTOOL</span><span class="sxs-lookup"><span data-stu-id="0f112-104">TTM\_ADDTOOL message</span></span>

<span data-ttu-id="0f112-105">Registra uno strumento con un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="0f112-105">Registers a tool with a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f112-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f112-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f112-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f112-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f112-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0f112-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0f112-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f112-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f112-110">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) contenente le informazioni necessarie al controllo ToolTip per visualizzare il testo per lo strumento.</span><span class="sxs-lookup"><span data-stu-id="0f112-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure containing information that the tooltip control needs to display text for the tool.</span></span> <span data-ttu-id="0f112-111">Prima di inviare questo messaggio, è necessario compilare il membro **cbSize** della struttura.</span><span class="sxs-lookup"><span data-stu-id="0f112-111">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f112-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f112-112">Return value</span></span>

<span data-ttu-id="0f112-113">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0f112-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f112-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f112-114">Requirements</span></span>



| <span data-ttu-id="0f112-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f112-115">Requirement</span></span> | <span data-ttu-id="0f112-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0f112-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f112-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f112-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f112-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f112-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f112-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f112-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f112-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f112-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f112-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f112-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f112-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f112-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0f112-123">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0f112-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0f112-124">**TTM \_ ADDTOOLW** (Unicode) e **TTM \_ ADDTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0f112-124">**TTM\_ADDTOOLW** (Unicode) and **TTM\_ADDTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="0f112-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f112-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f112-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0f112-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0f112-127">**\_DELTOOL TTM**</span><span class="sxs-lookup"><span data-stu-id="0f112-127">**TTM\_DELTOOL**</span></span>](ttm-deltool.md)
</dt> <dt>

<span data-ttu-id="0f112-128">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0f112-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0f112-129">Informazioni sui controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="0f112-129">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





