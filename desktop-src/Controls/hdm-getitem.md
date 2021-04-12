---
title: Messaggio HDM_GETITEM (COMmctrl. h)
description: Ottiene informazioni su un elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetItem dell'intestazione.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- Controlli di Windows Message HDM_GETITEM
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119835"
---
# <a name="hdm_getitem-message"></a><span data-ttu-id="7c4d8-105">HDM \_ messaggio GETitem</span><span class="sxs-lookup"><span data-stu-id="7c4d8-105">HDM\_GETITEM message</span></span>

<span data-ttu-id="7c4d8-106">Ottiene informazioni su un elemento in un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-106">Gets information about an item in a header control.</span></span> <span data-ttu-id="7c4d8-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetItem dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) .</span><span class="sxs-lookup"><span data-stu-id="7c4d8-107">You can send this message explicitly or use the [**Header\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c4d8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c4d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c4d8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c4d8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d8-110">Indice dell'elemento per il quale devono essere recuperate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-110">The index of the item for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c4d8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d8-112">Puntatore a una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="7c4d8-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="7c4d8-113">Quando il messaggio viene inviato, il membro **mask** indica il tipo di informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-113">When the message is sent, the **mask** member indicates the type of information being requested.</span></span> <span data-ttu-id="7c4d8-114">Quando il messaggio viene restituito, gli altri membri ricevono le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-114">When the message returns, the other members receive the requested information.</span></span> <span data-ttu-id="7c4d8-115">Se il membro **mask** specifica zero, il messaggio restituisce **true** , ma non copia alcuna informazione nella struttura.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-115">If the **mask** member specifies zero, the message returns **TRUE** but copies no information to the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c4d8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c4d8-116">Return value</span></span>

<span data-ttu-id="7c4d8-117">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c4d8-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c4d8-118">Remarks</span></span>

<span data-ttu-id="7c4d8-119">Se il \_ flag di testo HDI è impostato nel membro **mask** della struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , il controllo può modificare il membro **pszText** della struttura in modo che punti al nuovo testo anziché riempire il buffer con il testo richiesto.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-119">If the HDI\_TEXT flag is set in the **mask** member of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="7c4d8-120">Le applicazioni non devono presupporre che il testo venga sempre inserito nel buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="7c4d8-120">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4d8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c4d8-121">Requirements</span></span>



| <span data-ttu-id="7c4d8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c4d8-122">Requirement</span></span> | <span data-ttu-id="7c4d8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7c4d8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4d8-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c4d8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7c4d8-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c4d8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c4d8-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c4d8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7c4d8-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c4d8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c4d8-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c4d8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c4d8-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c4d8-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7c4d8-130">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7c4d8-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7c4d8-131">**HDM \_ GETITEMW** (Unicode) e **HDM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7c4d8-131">**HDM\_GETITEMW** (Unicode) and **HDM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





