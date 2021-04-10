---
title: Messaggio HDM_SETHOTDIVIDER (COMmctrl. h)
description: Modifica il colore di un divisore tra gli elementi di intestazione per indicare la destinazione di un'operazione di trascinamento e rilascio esterna. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHotDivider dell'intestazione.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- Controlli di Windows Message HDM_SETHOTDIVIDER
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119658"
---
# <a name="hdm_sethotdivider-message"></a><span data-ttu-id="f566f-105">\_Messaggio HDM SETHOTDIVIDER</span><span class="sxs-lookup"><span data-stu-id="f566f-105">HDM\_SETHOTDIVIDER message</span></span>

<span data-ttu-id="f566f-106">Modifica il colore di un divisore tra gli elementi di intestazione per indicare la destinazione di un'operazione di trascinamento e rilascio esterna.</span><span class="sxs-lookup"><span data-stu-id="f566f-106">Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation.</span></span> <span data-ttu-id="f566f-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHotDivider dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) .</span><span class="sxs-lookup"><span data-stu-id="f566f-107">You can send this message explicitly or use the [**Header\_SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f566f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f566f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f566f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f566f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f566f-110">Tipo di valore rappresentato da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f566f-110">The type of value represented by *lParam*.</span></span> <span data-ttu-id="f566f-111">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f566f-111">This value can be one of the following:</span></span>



| <span data-ttu-id="f566f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f566f-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="f566f-113">Significato</span><span class="sxs-lookup"><span data-stu-id="f566f-113">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="f566f-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f566f-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="f566f-115">Indica che *lParam* include le coordinate client del puntatore.</span><span class="sxs-lookup"><span data-stu-id="f566f-115">Indicates that *lParam* holds the client coordinates of the pointer.</span></span><br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="f566f-116"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f566f-116"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="f566f-117">Indica che *lParam* utilizza un valore di indice del divisore.</span><span class="sxs-lookup"><span data-stu-id="f566f-117">Indicates that *lParam* holds a divider index value.</span></span><br/>                 |



 

</dd> <dt>

<span data-ttu-id="f566f-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f566f-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f566f-119">Un valore contenuto in *lParam* viene interpretato in base al valore di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="f566f-119">A value held in *lParam* is interpreted depending on the value of *wParam*.</span></span>

<span data-ttu-id="f566f-120">Se *wParam* è **true**, *lParam* rappresenta le coordinate x e y del puntatore.</span><span class="sxs-lookup"><span data-stu-id="f566f-120">If *wParam* is **TRUE**, *lParam* represents the x- and y-coordinates of the pointer.</span></span> <span data-ttu-id="f566f-121">La coordinata x si trova nella parola bassa e la coordinata y si trova nella parola alta.</span><span class="sxs-lookup"><span data-stu-id="f566f-121">The x-coordinate is in the low word, and the y-coordinate is in the high word.</span></span> <span data-ttu-id="f566f-122">Quando il controllo intestazione riceve il messaggio, evidenzia il separatore appropriato in base alle coordinate *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f566f-122">When the header control receives the message, it highlights the appropriate divider based on the *lParam* coordinates.</span></span>

<span data-ttu-id="f566f-123">Se *wParam* è **false**, *lParam* rappresenta l'indice Integer del divisore da evidenziare.</span><span class="sxs-lookup"><span data-stu-id="f566f-123">If *wParam* is **FALSE**, *lParam* represents the integer index of the divider to be highlighted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f566f-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f566f-124">Return value</span></span>

<span data-ttu-id="f566f-125">Restituisce un valore uguale all'indice del divisore evidenziato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="f566f-125">Returns a value equal to the index of the divider that the control highlighted.</span></span>

## <a name="remarks"></a><span data-ttu-id="f566f-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="f566f-126">Remarks</span></span>

<span data-ttu-id="f566f-127">Questo messaggio crea un effetto che un controllo intestazione produce automaticamente quando dispone dello stile [**\_ DragDrop di HDS**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f566f-127">This message creates an effect that a header control automatically produces when it has the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="f566f-128">Il messaggio **HDM \_ SETHOTDIVIDER** deve essere usato quando il proprietario del controllo gestisce manualmente le operazioni di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="f566f-128">The **HDM\_SETHOTDIVIDER** message is intended to be used when the owner of the control handles drag-and-drop operations manually.</span></span>

## <a name="requirements"></a><span data-ttu-id="f566f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f566f-129">Requirements</span></span>



| <span data-ttu-id="f566f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f566f-130">Requirement</span></span> | <span data-ttu-id="f566f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f566f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f566f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f566f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f566f-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f566f-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f566f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f566f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f566f-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f566f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f566f-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f566f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f566f-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f566f-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





