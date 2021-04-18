---
title: Messaggio WM_DWMCOMPOSITIONCHANGED (winuser. h)
description: Informa tutte le finestre di primo livello che Gestione finestre desktop la composizione (DWM) è stata abilitata o disabilitata.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- Messaggio WM_DWMCOMPOSITIONCHANGED Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301718"
---
# <a name="wm_dwmcompositionchanged-message"></a><span data-ttu-id="5b624-104">\_Messaggio DWMCOMPOSITIONCHANGED WM</span><span class="sxs-lookup"><span data-stu-id="5b624-104">WM\_DWMCOMPOSITIONCHANGED message</span></span>

<span data-ttu-id="5b624-105">Informa tutte le finestre di primo livello che Gestione finestre desktop la composizione (DWM) è stata abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5b624-105">Informs all top-level windows that Desktop Window Manager (DWM) composition has been enabled or disabled.</span></span>

> [!Note]  
> <span data-ttu-id="5b624-106">A partire da Windows 8, la composizione di DWM è sempre abilitata, quindi questo messaggio non viene inviato indipendentemente dalle modifiche della modalità video.</span><span class="sxs-lookup"><span data-stu-id="5b624-106">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="5b624-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b624-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b624-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b624-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b624-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5b624-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5b624-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b624-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b624-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5b624-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b624-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b624-112">Return value</span></span>

<span data-ttu-id="5b624-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="5b624-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b624-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b624-114">Remarks</span></span>

<span data-ttu-id="5b624-115">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5b624-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="5b624-116">La funzione [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) può essere utilizzata per determinare lo stato di composizione corrente.</span><span class="sxs-lookup"><span data-stu-id="5b624-116">The [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) function can be used to determine the current composition state.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b624-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b624-117">Requirements</span></span>



| <span data-ttu-id="5b624-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b624-118">Requirement</span></span> | <span data-ttu-id="5b624-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5b624-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b624-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b624-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5b624-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b624-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5b624-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b624-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5b624-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b624-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b624-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b624-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b624-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b624-125"><dt>Winuser.h</dt></span></span> </dl> |



 

