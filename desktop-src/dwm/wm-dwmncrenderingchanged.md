---
title: Messaggio WM_DWMNCRENDERINGCHANGED (winuser. h)
description: Inviato quando i criteri di rendering dell'area non client vengono modificati.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- Messaggio WM_DWMNCRENDERINGCHANGED Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964302"
---
# <a name="wm_dwmncrenderingchanged-message"></a><span data-ttu-id="e7c23-104">\_Messaggio DWMNCRENDERINGCHANGED WM</span><span class="sxs-lookup"><span data-stu-id="e7c23-104">WM\_DWMNCRENDERINGCHANGED message</span></span>

<span data-ttu-id="e7c23-105">Inviato quando i criteri di rendering dell'area non client vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="e7c23-105">Sent when the non-client area rendering policy has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7c23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7c23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7c23-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7c23-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7c23-108">Specifica se il rendering di DWM è abilitato per l'area non client della finestra.</span><span class="sxs-lookup"><span data-stu-id="e7c23-108">Specifies whether DWM rendering is enabled for the non-client area of the window.</span></span> <span data-ttu-id="e7c23-109">**True** se abilitata; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e7c23-109">**TRUE** if enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e7c23-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7c23-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7c23-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e7c23-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7c23-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7c23-112">Return value</span></span>

<span data-ttu-id="e7c23-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="e7c23-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7c23-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7c23-114">Remarks</span></span>

<span data-ttu-id="e7c23-115">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e7c23-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="e7c23-116">Le funzioni [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) vengono usate per ottenere o impostare i criteri di rendering non client.</span><span class="sxs-lookup"><span data-stu-id="e7c23-116">The [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions are used to get or set the non-client rendering policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c23-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7c23-117">Requirements</span></span>



| <span data-ttu-id="e7c23-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7c23-118">Requirement</span></span> | <span data-ttu-id="e7c23-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e7c23-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c23-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7c23-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c23-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7c23-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e7c23-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7c23-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c23-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7c23-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e7c23-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7c23-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7c23-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7c23-125"><dt>Winuser.h</dt></span></span> </dl> |



 

