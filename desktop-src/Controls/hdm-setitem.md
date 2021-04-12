---
title: Messaggio HDM_SETITEM (COMmctrl. h)
description: Imposta gli attributi dell'elemento specificato in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro elemento intestazione.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- Controlli di Windows Message HDM_SETITEM
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478268"
---
# <a name="hdm_setitem-message"></a><span data-ttu-id="8ca1a-105">HDM- \_ messaggio di elemento</span><span class="sxs-lookup"><span data-stu-id="8ca1a-105">HDM\_SETITEM message</span></span>

<span data-ttu-id="8ca1a-106">Imposta gli attributi dell'elemento specificato in un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="8ca1a-106">Sets the attributes of the specified item in a header control.</span></span> <span data-ttu-id="8ca1a-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ elemento intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) .</span><span class="sxs-lookup"><span data-stu-id="8ca1a-107">You can send this message explicitly or use the [**Header\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ca1a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ca1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca1a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ca1a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ca1a-110">Indice corrente dell'elemento i cui attributi devono essere modificati.</span><span class="sxs-lookup"><span data-stu-id="8ca1a-110">The current index of the item whose attributes are to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="8ca1a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ca1a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ca1a-112">Puntatore a una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) che contiene informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="8ca1a-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains item information.</span></span> <span data-ttu-id="8ca1a-113">Quando viene inviato questo messaggio, è necessario impostare il membro **mask** della struttura per indicare gli attributi da impostare.</span><span class="sxs-lookup"><span data-stu-id="8ca1a-113">When this message is sent, the **mask** member of the structure must be set to indicate which attributes are being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca1a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ca1a-114">Return value</span></span>

<span data-ttu-id="8ca1a-115">Restituisce un valore diverso da zero in caso di esito positivo o zero.</span><span class="sxs-lookup"><span data-stu-id="8ca1a-115">Returns nonzero upon success, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca1a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ca1a-116">Remarks</span></span>

<span data-ttu-id="8ca1a-117">La struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) che supporta questo messaggio supporta le informazioni sull'ordine degli elementi e sull'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="8ca1a-117">The [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that supports this message supports item order and image list information.</span></span> <span data-ttu-id="8ca1a-118">Usando questi membri, è possibile controllare l'ordine in cui vengono visualizzati gli elementi e specificare le immagini da visualizzare con gli elementi.</span><span class="sxs-lookup"><span data-stu-id="8ca1a-118">By using these members, you can control the order in which items are displayed and specify images to appear with items.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca1a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ca1a-119">Requirements</span></span>



| <span data-ttu-id="8ca1a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca1a-120">Requirement</span></span> | <span data-ttu-id="8ca1a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8ca1a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca1a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ca1a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca1a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ca1a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ca1a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ca1a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca1a-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ca1a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ca1a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ca1a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca1a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca1a-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8ca1a-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8ca1a-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8ca1a-129">**HDM \_ SETITEMW** (Unicode) e **HDM \_ setitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8ca1a-129">**HDM\_SETITEMW** (Unicode) and **HDM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





