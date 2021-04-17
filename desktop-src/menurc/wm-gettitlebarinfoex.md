---
title: Messaggio WM_GETTITLEBARINFOEX (winuser. h)
description: Inviato per richiedere informazioni estese sulla barra del titolo. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- Menu del messaggio WM_GETTITLEBARINFOEX e altre risorse
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400364"
---
# <a name="wm_gettitlebarinfoex-message"></a><span data-ttu-id="7774e-105">\_Messaggio GETTITLEBARINFOEX WM</span><span class="sxs-lookup"><span data-stu-id="7774e-105">WM\_GETTITLEBARINFOEX message</span></span>

<span data-ttu-id="7774e-106">Inviato per richiedere informazioni estese sulla barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="7774e-106">Sent to request extended title bar information.</span></span> <span data-ttu-id="7774e-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7774e-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a><span data-ttu-id="7774e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7774e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7774e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7774e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7774e-110">Questo parametro non viene utilizzato e deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="7774e-110">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="7774e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7774e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7774e-112">Puntatore a una struttura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="7774e-112">A pointer to a [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span> <span data-ttu-id="7774e-113">Il mittente del messaggio è responsabile dell'allocazione della memoria per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="7774e-113">The message sender is responsible for allocating memory for this structure.</span></span> <span data-ttu-id="7774e-114">Impostare il membro **cbSize** della struttura su `sizeof(TITLEBARINFOEX)` prima di passare questa struttura con il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7774e-114">Set the **cbSize** member of this structure to `sizeof(TITLEBARINFOEX)` before passing this structure with the message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7774e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7774e-115">Remarks</span></span>

<span data-ttu-id="7774e-116">Nell'esempio seguente viene illustrato come il ricevitore del messaggio esegue il cast di un valore **lParam** per recuperare la struttura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="7774e-116">The following example shows how the message receiver casts an **LPARAM** value to retrieve the [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span>

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a><span data-ttu-id="7774e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7774e-117">Requirements</span></span>



| <span data-ttu-id="7774e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7774e-118">Requirement</span></span> | <span data-ttu-id="7774e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7774e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7774e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7774e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7774e-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7774e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7774e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7774e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7774e-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7774e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7774e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7774e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7774e-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7774e-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7774e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7774e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7774e-127">Panoramica sui menu</span><span class="sxs-lookup"><span data-stu-id="7774e-127">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

