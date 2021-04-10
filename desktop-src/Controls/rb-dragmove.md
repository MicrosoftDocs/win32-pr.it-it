---
title: Messaggio RB_DRAGMOVE (COMmctrl. h)
description: Aggiorna la posizione del trascinamento nel controllo Rebar dopo un \_ messaggio RB BEGINDRAG precedente.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- Controlli di Windows Message RB_DRAGMOVE
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964555"
---
# <a name="rb_dragmove-message"></a><span data-ttu-id="f4621-104">\_Messaggio DRAGMOVE RB</span><span class="sxs-lookup"><span data-stu-id="f4621-104">RB\_DRAGMOVE message</span></span>

<span data-ttu-id="f4621-105">Aggiorna la posizione del trascinamento nel controllo Rebar dopo un messaggio [**RB \_ BEGINDRAG**](rb-begindrag.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="f4621-105">Updates the drag position in the rebar control after a previous [**RB\_BEGINDRAG**](rb-begindrag.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4621-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4621-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4621-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4621-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4621-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f4621-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f4621-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4621-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4621-110">Valore **DWORD** che contiene le nuove coordinate del mouse.</span><span class="sxs-lookup"><span data-stu-id="f4621-110">**DWORD** value that contains the new mouse coordinates.</span></span> <span data-ttu-id="f4621-111">La coordinata orizzontale è contenuta in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la coordinata verticale è contenuta in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f4621-111">The horizontal coordinate is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical coordinate is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="f4621-112">Se si passa (DWORD)-1, il controllo Rebar utilizzerà la posizione del mouse nell'ultima volta in cui il thread del controllo ha chiamato [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span><span class="sxs-lookup"><span data-stu-id="f4621-112">If you pass (DWORD)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4621-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4621-113">Return value</span></span>

<span data-ttu-id="f4621-114">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f4621-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4621-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4621-115">Requirements</span></span>



| <span data-ttu-id="f4621-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4621-116">Requirement</span></span> | <span data-ttu-id="f4621-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f4621-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4621-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4621-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f4621-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4621-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4621-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4621-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f4621-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4621-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4621-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4621-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4621-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4621-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4621-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4621-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4621-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f4621-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f4621-126">**RB \_ ENDDRAG**</span><span class="sxs-lookup"><span data-stu-id="f4621-126">**RB\_ENDDRAG**</span></span>](rb-enddrag.md)
</dt> </dl>

 

