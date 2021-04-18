---
title: Messaggio TTM_RELAYEVENT (COMmctrl. h)
description: Passa un messaggio del mouse a un controllo ToolTip per l'elaborazione.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- Controlli di Windows Message TTM_RELAYEVENT
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353251"
---
# <a name="ttm_relayevent-message"></a><span data-ttu-id="157b4-104">\_Messaggio TTM RELAYEVENT</span><span class="sxs-lookup"><span data-stu-id="157b4-104">TTM\_RELAYEVENT message</span></span>

<span data-ttu-id="157b4-105">Passa un messaggio del mouse a un controllo ToolTip per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="157b4-105">Passes a mouse message to a tooltip control for processing.</span></span>

## <a name="parameters"></a><span data-ttu-id="157b4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="157b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="157b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="157b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="157b4-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="157b4-108">Must be zero.</span></span> <span data-ttu-id="157b4-109">**Windows 7 e versioni successive:** Se la posizione della descrizione comando viene sfalsata rispetto alla posizione del cursore (in modo che non venga ostacolata da un dito o da un dispositivo di puntamento), questo parametro può contenere informazioni aggiuntive tratte dal messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="157b4-109">**Windows 7 and later:** If the position of the tooltip is offset from the cursor position (in order not be obstructed by a finger or pointing device), this parameter can contain extra information taken from the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="157b4-110">Recuperare queste informazioni aggiuntive con [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span><span class="sxs-lookup"><span data-stu-id="157b4-110">Retrieve this extra information with [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span></span>

</dd> <dt>

<span data-ttu-id="157b4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="157b4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="157b4-112">Puntatore a una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) che contiene il messaggio da inoltrare.</span><span class="sxs-lookup"><span data-stu-id="157b4-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to relay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="157b4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="157b4-113">Return value</span></span>

<span data-ttu-id="157b4-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="157b4-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="157b4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="157b4-115">Remarks</span></span>

<span data-ttu-id="157b4-116">Un controllo ToolTip elabora solo i messaggi seguenti passati dal messaggio **TTM \_ RELAYEVENT** :</span><span class="sxs-lookup"><span data-stu-id="157b4-116">A tooltip control processes only the following messages passed to it by the **TTM\_RELAYEVENT** message:</span></span>

-   <span data-ttu-id="157b4-117">\_LBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="157b4-117">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="157b4-118">\_LBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="157b4-118">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="157b4-119">\_MBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="157b4-119">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="157b4-120">\_MBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="157b4-120">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="157b4-121">MOUSEMOVE di WM \_</span><span class="sxs-lookup"><span data-stu-id="157b4-121">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="157b4-122">\_NCMOUSEMOVE WM</span><span class="sxs-lookup"><span data-stu-id="157b4-122">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="157b4-123">\_RBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="157b4-123">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="157b4-124">\_RBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="157b4-124">WM\_RBUTTONUP</span></span>

<span data-ttu-id="157b4-125">Tutti gli altri messaggi vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="157b4-125">All other messages are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="157b4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="157b4-126">Requirements</span></span>



| <span data-ttu-id="157b4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="157b4-127">Requirement</span></span> | <span data-ttu-id="157b4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="157b4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="157b4-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="157b4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="157b4-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="157b4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="157b4-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="157b4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="157b4-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="157b4-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="157b4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="157b4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="157b4-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="157b4-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

