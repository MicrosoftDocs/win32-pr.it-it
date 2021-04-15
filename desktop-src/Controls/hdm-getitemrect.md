---
title: Messaggio HDM_GETITEMRECT (COMmctrl. h)
description: Ottiene il rettangolo di delimitazione per un elemento specificato in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetItemRect dell'intestazione.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- Controlli di Windows Message HDM_GETITEMRECT
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477584"
---
# <a name="hdm_getitemrect-message"></a><span data-ttu-id="104a7-105">\_Messaggio HDM GETITEMRECT</span><span class="sxs-lookup"><span data-stu-id="104a7-105">HDM\_GETITEMRECT message</span></span>

<span data-ttu-id="104a7-106">Ottiene il rettangolo di delimitazione per un elemento specificato in un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="104a7-106">Gets the bounding rectangle for a given item in a header control.</span></span> <span data-ttu-id="104a7-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetItemRect dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="104a7-107">You can send this message explicitly or use the [**Header\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="104a7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="104a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="104a7-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="104a7-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104a7-110">Indice in base zero dell'elemento di controllo dell'intestazione per il quale recuperare il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="104a7-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="104a7-111">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="104a7-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="104a7-112">Puntatore a una struttura [**Rect**](/windows/win32/api/windef/ns-windef-rect) che riceve le informazioni sul rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="104a7-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="104a7-113">Il mittente del messaggio è responsabile dell'allocazione della struttura.</span><span class="sxs-lookup"><span data-stu-id="104a7-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="104a7-114">Le coordinate restituite nella struttura RECT sono espresse in relazione all'elemento padre del controllo Header.</span><span class="sxs-lookup"><span data-stu-id="104a7-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="104a7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="104a7-115">Return value</span></span>

<span data-ttu-id="104a7-116">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="104a7-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="104a7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="104a7-117">Requirements</span></span>



| <span data-ttu-id="104a7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="104a7-118">Requirement</span></span> | <span data-ttu-id="104a7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="104a7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="104a7-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="104a7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="104a7-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="104a7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="104a7-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="104a7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="104a7-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="104a7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="104a7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="104a7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="104a7-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="104a7-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





