---
title: Messaggio di EM_SETSCROLLPOS (RichEdit. h)
description: Scorre il contenuto di un controllo Rich Edit fino al punto specificato.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- Controlli di Windows Message EM_SETSCROLLPOS
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478557"
---
# <a name="em_setscrollpos-message"></a><span data-ttu-id="43682-104">\_Messaggio SETSCROLLPOS em</span><span class="sxs-lookup"><span data-stu-id="43682-104">EM\_SETSCROLLPOS message</span></span>

<span data-ttu-id="43682-105">Scorre il contenuto di un controllo Rich Edit fino al punto specificato.</span><span class="sxs-lookup"><span data-stu-id="43682-105">Scrolls the contents of a rich edit control to the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="43682-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43682-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43682-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43682-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43682-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="43682-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="43682-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43682-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43682-110">Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che specifica un punto nello spazio di testo virtuale del documento, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="43682-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure which specifies a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="43682-111">Il documento verrà spostato fino a quando questo punto si trova nell'angolo superiore sinistro della finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="43682-111">The document will be scrolled until this point is located in the upper-left corner of the edit control window.</span></span> <span data-ttu-id="43682-112">Se si desidera modificare la visualizzazione in modo che l'angolo superiore sinistro della visualizzazione sia costituito da due righe e da un carattere nel bordo sinistro.</span><span class="sxs-lookup"><span data-stu-id="43682-112">If you want to change the view such that the upper left corner of the view is two lines down and one character in from the left edge.</span></span> <span data-ttu-id="43682-113">Si passerà un punto di (7, 22).</span><span class="sxs-lookup"><span data-stu-id="43682-113">You would pass a point of (7, 22).</span></span>

<span data-ttu-id="43682-114">Il controllo Rich Edit controlla le coordinate x e y e le regola se necessario, in modo che venga visualizzata una riga completa nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="43682-114">The rich edit control checks the x and y coordinates and adjusts them if necessary, so that a complete line is displayed at the top.</span></span> <span data-ttu-id="43682-115">Garantisce inoltre che il testo non venga mai completamente spostato al di fuori del rettangolo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="43682-115">It also ensures that the text is never completely scrolled off the view rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43682-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43682-116">Return value</span></span>

<span data-ttu-id="43682-117">Questo messaggio restituisce sempre 1.</span><span class="sxs-lookup"><span data-stu-id="43682-117">This message always returns 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="43682-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43682-118">Requirements</span></span>



| <span data-ttu-id="43682-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="43682-119">Requirement</span></span> | <span data-ttu-id="43682-120">Valore</span><span class="sxs-lookup"><span data-stu-id="43682-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43682-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43682-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43682-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43682-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43682-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43682-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43682-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43682-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43682-125">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="43682-125">Redistributable</span></span><br/>          | <span data-ttu-id="43682-126">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="43682-126">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="43682-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43682-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="43682-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="43682-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43682-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43682-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43682-130">**\_GETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="43682-130">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> </dl>

 

