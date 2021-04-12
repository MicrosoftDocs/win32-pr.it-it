---
title: Messaggio LVM_GETFOOTERITEMRECT (COMmctrl. h)
description: Ottiene le coordinate di un piè di pagina per un elemento specificato in un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFooterItemRect di ListView.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- Controlli di Windows Message LVM_GETFOOTERITEMRECT
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225196"
---
# <a name="lvm_getfooteritemrect-message"></a><span data-ttu-id="46a2d-105">\_Messaggio GETFOOTERITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="46a2d-105">LVM\_GETFOOTERITEMRECT message</span></span>

<span data-ttu-id="46a2d-106">Ottiene le coordinate di un piè di pagina per un elemento specificato in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="46a2d-106">Gets the coordinates of a footer for a specified item in a list-view control.</span></span> <span data-ttu-id="46a2d-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFooterItemRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .</span><span class="sxs-lookup"><span data-stu-id="46a2d-107">Send this message explicitly or by using the [**ListView\_GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="46a2d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46a2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46a2d-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46a2d-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46a2d-110">Indice dell'elemento nel controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="46a2d-110">The index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="46a2d-111">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="46a2d-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46a2d-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per ricevere le coordinate.</span><span class="sxs-lookup"><span data-stu-id="46a2d-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="46a2d-113">L'applicazione chiamante è responsabile dell'allocazione di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="46a2d-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="46a2d-114">Le coordinate ricevute sono espresse come coordinate client.</span><span class="sxs-lookup"><span data-stu-id="46a2d-114">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46a2d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46a2d-115">Return value</span></span>

<span data-ttu-id="46a2d-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="46a2d-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="46a2d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46a2d-117">Requirements</span></span>



| <span data-ttu-id="46a2d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="46a2d-118">Requirement</span></span> | <span data-ttu-id="46a2d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="46a2d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46a2d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46a2d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="46a2d-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46a2d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46a2d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46a2d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="46a2d-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46a2d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46a2d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46a2d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="46a2d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46a2d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

