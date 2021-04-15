---
title: Messaggio LVM_SCROLL (COMmctrl. h)
description: Scorre il contenuto di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro di scorrimento ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- Controlli di Windows Message LVM_SCROLL
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477560"
---
# <a name="lvm_scroll-message"></a><span data-ttu-id="46c09-105">\_Messaggio di scorrimento LVM</span><span class="sxs-lookup"><span data-stu-id="46c09-105">LVM\_SCROLL message</span></span>

<span data-ttu-id="46c09-106">Scorre il contenuto di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="46c09-106">Scrolls the content of a list-view control.</span></span> <span data-ttu-id="46c09-107">È possibile inviare questo messaggio in modo esplicito o usando la macro di [**\_ scorrimento ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) .</span><span class="sxs-lookup"><span data-stu-id="46c09-107">You can send this message explicitly or by using the [**ListView\_Scroll**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="46c09-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46c09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c09-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46c09-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46c09-110">Valore di tipo **int** che specifica la quantità di scorrimento orizzontale, in pixel, rispetto alla posizione corrente del contenuto della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="46c09-110">Value of type **int** that specifies the amount of horizontal scrolling, in pixels, relative to the current position of the list view content.</span></span> <span data-ttu-id="46c09-111">Se il controllo visualizzazione elenco è in visualizzazione elenco, questo valore viene arrotondato per eccesso al numero di pixel più vicino che formano una colonna intera.</span><span class="sxs-lookup"><span data-stu-id="46c09-111">If the list-view control is in list view, this value is rounded up to the nearest number of pixels that form a whole column.</span></span>

</dd> <dt>

<span data-ttu-id="46c09-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46c09-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46c09-113">Valore di tipo **int** che specifica la quantità di scorrimento verticale, in pixel, rispetto alla posizione corrente del contenuto della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="46c09-113">Value of type **int** that specifies the amount of vertical scrolling, in pixels, relative to the current position of the list view content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c09-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46c09-114">Return value</span></span>

<span data-ttu-id="46c09-115">Restituisce **true** se l'operazione ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="46c09-115">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="46c09-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="46c09-116">Remarks</span></span>

<span data-ttu-id="46c09-117">Quando il controllo elenco-visualizzazione è in visualizzazione report, è possibile scorrere il controllo verticalmente solo in incrementi di riga interi.</span><span class="sxs-lookup"><span data-stu-id="46c09-117">When the list-view control is in report view, the control can only be scrolled vertically in whole line increments.</span></span> <span data-ttu-id="46c09-118">Pertanto, il parametro *lParam* verrà arrotondato al numero di pixel più vicino che formano un incremento di riga intero.</span><span class="sxs-lookup"><span data-stu-id="46c09-118">Therefore, the *lParam* parameter will be rounded to the nearest number of pixels that form a whole line increment.</span></span> <span data-ttu-id="46c09-119">Se, ad esempio, l'altezza di una linea è 16 pixel e 8 viene passato per *lParam*, l'elenco verrà spostato di 16 pixel (1 riga).</span><span class="sxs-lookup"><span data-stu-id="46c09-119">For example, if the height of a line is 16 pixels and 8 is passed for *lParam*, the list will be scrolled by 16 pixels (1 line).</span></span> <span data-ttu-id="46c09-120">Se viene passato 7 per *lParam*, l'elenco verrà spostato di 0 pixel (0 righe).</span><span class="sxs-lookup"><span data-stu-id="46c09-120">If 7 is passed for *lParam*, the list will be scrolled 0 pixels (0 lines).</span></span>

## <a name="requirements"></a><span data-ttu-id="46c09-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46c09-121">Requirements</span></span>



| <span data-ttu-id="46c09-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="46c09-122">Requirement</span></span> | <span data-ttu-id="46c09-123">Valore</span><span class="sxs-lookup"><span data-stu-id="46c09-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46c09-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46c09-124">Minimum supported client</span></span><br/> | <span data-ttu-id="46c09-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46c09-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46c09-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46c09-126">Minimum supported server</span></span><br/> | <span data-ttu-id="46c09-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46c09-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46c09-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46c09-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="46c09-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46c09-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





