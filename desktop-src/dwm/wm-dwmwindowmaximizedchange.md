---
title: Messaggio WM_DWMWINDOWMAXIMIZEDCHANGE (winuser. h)
description: Inviato quando una finestra composta da Gestione finestre desktop (DWM) viene ingrandita.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- Messaggio WM_DWMWINDOWMAXIMIZEDCHANGE Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400661"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a><span data-ttu-id="c1764-104">\_Messaggio DWMWINDOWMAXIMIZEDCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="c1764-104">WM\_DWMWINDOWMAXIMIZEDCHANGE message</span></span>

<span data-ttu-id="c1764-105">Inviato quando una finestra composta da Gestione finestre desktop (DWM) viene ingrandita.</span><span class="sxs-lookup"><span data-stu-id="c1764-105">Sent when a Desktop Window Manager (DWM) composed window is maximized.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1764-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1764-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1764-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1764-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1764-108">Impostare su true per specificare che la finestra è stata ingrandita.</span><span class="sxs-lookup"><span data-stu-id="c1764-108">Set to true to specify that the window has been maximized.</span></span>

</dd> <dt>

<span data-ttu-id="c1764-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1764-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1764-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c1764-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1764-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1764-111">Return value</span></span>

<span data-ttu-id="c1764-112">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="c1764-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1764-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1764-113">Remarks</span></span>

<span data-ttu-id="c1764-114">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c1764-114">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1764-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1764-115">Requirements</span></span>



| <span data-ttu-id="c1764-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1764-116">Requirement</span></span> | <span data-ttu-id="c1764-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c1764-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1764-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1764-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c1764-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1764-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c1764-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1764-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c1764-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1764-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c1764-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1764-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1764-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1764-123"><dt>Winuser.h</dt></span></span> </dl> |



 

