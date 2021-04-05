---
title: Messaggio TB_SETPARENT (COMmctrl. h)
description: Imposta la finestra a cui il controllo Toolbar invia messaggi di notifica.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- Controlli di Windows Message TB_SETPARENT
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874422"
---
# <a name="tb_setparent-message"></a><span data-ttu-id="feefb-104">TB \_ messaggio padre</span><span class="sxs-lookup"><span data-stu-id="feefb-104">TB\_SETPARENT message</span></span>

<span data-ttu-id="feefb-105">Imposta la finestra a cui il controllo Toolbar invia messaggi di notifica.</span><span class="sxs-lookup"><span data-stu-id="feefb-105">Sets the window to which the toolbar control sends notification messages.</span></span>

## <a name="parameters"></a><span data-ttu-id="feefb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="feefb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feefb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="feefb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="feefb-108">Handle per la finestra per la ricezione di messaggi di notifica.</span><span class="sxs-lookup"><span data-stu-id="feefb-108">Handle to the window to receive notification messages.</span></span>

</dd> <dt>

<span data-ttu-id="feefb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="feefb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="feefb-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="feefb-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feefb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="feefb-111">Return value</span></span>

<span data-ttu-id="feefb-112">Il valore restituito è un handle per la finestra di notifica precedente oppure **null** se non è presente una finestra di notifica precedente.</span><span class="sxs-lookup"><span data-stu-id="feefb-112">The return value is a handle to the previous notification window, or **NULL** if there is no previous notification window.</span></span>

## <a name="remarks"></a><span data-ttu-id="feefb-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="feefb-113">Remarks</span></span>

<span data-ttu-id="feefb-114">Il **messaggio \_ padre TB** non modifica la finestra padre specificata al momento della creazione del controllo.</span><span class="sxs-lookup"><span data-stu-id="feefb-114">The **TB\_SETPARENT** message does not change the parent window that was specified when the control was created.</span></span> <span data-ttu-id="feefb-115">Chiamando la funzione [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) per un controllo Toolbar, viene restituita la finestra padre effettiva, non la finestra specificata in **TB \_ padre**.</span><span class="sxs-lookup"><span data-stu-id="feefb-115">Calling the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function for a toolbar control will return the actual parent window, not the window specified in **TB\_SETPARENT**.</span></span> <span data-ttu-id="feefb-116">Per modificare la finestra padre del controllo, chiamare la funzione [**padre**](/windows/desktop/api/winuser/nf-winuser-setparent) .</span><span class="sxs-lookup"><span data-stu-id="feefb-116">To change the control's parent window, call the [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="feefb-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="feefb-117">Requirements</span></span>



| <span data-ttu-id="feefb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="feefb-118">Requirement</span></span> | <span data-ttu-id="feefb-119">Valore</span><span class="sxs-lookup"><span data-stu-id="feefb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="feefb-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="feefb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="feefb-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="feefb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="feefb-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="feefb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="feefb-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="feefb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="feefb-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="feefb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="feefb-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="feefb-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

