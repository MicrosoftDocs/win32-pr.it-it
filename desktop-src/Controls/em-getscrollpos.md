---
title: Messaggio di EM_GETSCROLLPOS (RichEdit. h)
description: Ottiene la posizione di scorrimento corrente del controllo di modifica.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- Controlli di Windows Message EM_GETSCROLLPOS
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476486"
---
# <a name="em_getscrollpos-message"></a><span data-ttu-id="75c9e-104">\_Messaggio GETSCROLLPOS em</span><span class="sxs-lookup"><span data-stu-id="75c9e-104">EM\_GETSCROLLPOS message</span></span>

<span data-ttu-id="75c9e-105">Ottiene la posizione di scorrimento corrente del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="75c9e-105">Obtains the current scroll position of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="75c9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75c9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c9e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75c9e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75c9e-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="75c9e-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="75c9e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75c9e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75c9e-110">Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="75c9e-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="75c9e-111">Dopo la chiamata di **em \_ GETSCROLLPOS**, questo parametro contiene un punto nello spazio del testo virtuale del documento, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="75c9e-111">After calling **EM\_GETSCROLLPOS**, this parameters contains a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="75c9e-112">Questo punto sarà il punto attualmente disponibile nell'angolo superiore sinistro della finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="75c9e-112">This point will be the point that is currently located in the upper-left corner of the edit control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c9e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75c9e-113">Return value</span></span>

<span data-ttu-id="75c9e-114">Questo messaggio restituisce sempre 1.</span><span class="sxs-lookup"><span data-stu-id="75c9e-114">This message always returns 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="75c9e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="75c9e-115">Remarks</span></span>

<span data-ttu-id="75c9e-116">I valori restituiti nella struttura [**Point**](/previous-versions//dd162805(v=vs.85)) sono valori a 16 bit, anche nei campi wide a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="75c9e-116">The values returned in the [**POINT**](/previous-versions//dd162805(v=vs.85)) structure are 16-bit values (even in the 32-bit wide fields).</span></span>

## <a name="requirements"></a><span data-ttu-id="75c9e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75c9e-117">Requirements</span></span>



| <span data-ttu-id="75c9e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c9e-118">Requirement</span></span> | <span data-ttu-id="75c9e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="75c9e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75c9e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75c9e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75c9e-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75c9e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75c9e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75c9e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75c9e-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75c9e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75c9e-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="75c9e-124">Redistributable</span></span><br/>          | <span data-ttu-id="75c9e-125">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="75c9e-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="75c9e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75c9e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="75c9e-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="75c9e-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75c9e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75c9e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c9e-129">**\_SETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="75c9e-129">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

