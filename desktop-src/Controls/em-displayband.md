---
title: Messaggio di EM_DISPLAYBAND (RichEdit. h)
description: Visualizza una parte del contenuto di un controllo Rich Edit, come in precedenza formattato per un dispositivo usando il \_ messaggio FormatRange em.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- Controlli di Windows Message EM_DISPLAYBAND
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964479"
---
# <a name="em_displayband-message"></a><span data-ttu-id="d35b8-104">\_Messaggio DISPLAYBAND em</span><span class="sxs-lookup"><span data-stu-id="d35b8-104">EM\_DISPLAYBAND message</span></span>

<span data-ttu-id="d35b8-105">Visualizza una parte del contenuto di un controllo Rich Edit, come in precedenza formattato per un dispositivo usando il messaggio [**\_ FormatRange em**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="d35b8-105">Displays a portion of the contents of a rich edit control, as previously formatted for a device using the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="d35b8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d35b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d35b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d35b8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d35b8-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d35b8-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d35b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d35b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d35b8-110">Struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica l'area di visualizzazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d35b8-110">A [**RECT**](/previous-versions//dd162897(v=vs.85)) structure specifying the display area of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d35b8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d35b8-111">Return value</span></span>

<span data-ttu-id="d35b8-112">Se l'operazione ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="d35b8-112">If the operation succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="d35b8-113">Se l'operazione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d35b8-113">If the operation fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d35b8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d35b8-114">Remarks</span></span>

<span data-ttu-id="d35b8-115">Gli oggetti Text e Component Object Model (COM) vengono ritagliati dal rettangolo.</span><span class="sxs-lookup"><span data-stu-id="d35b8-115">Text and Component Object Model (COM) objects are clipped by the rectangle.</span></span> <span data-ttu-id="d35b8-116">Non è necessario che l'applicazione imposti l'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d35b8-116">The application does not need to set the clipping region.</span></span>

<span data-ttu-id="d35b8-117">La banda è il processo mediante il quale viene generata una singola pagina di output utilizzando uno o più rettangoli o bande separate.</span><span class="sxs-lookup"><span data-stu-id="d35b8-117">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="d35b8-118">Quando tutte le bande vengono posizionate nella pagina, viene generato un risultato di un'immagine completa.</span><span class="sxs-lookup"><span data-stu-id="d35b8-118">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="d35b8-119">Questo approccio viene spesso usato dalle stampanti raster che non dispongono di memoria sufficiente o della possibilità di creare un'immagine di una pagina intera in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="d35b8-119">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span> <span data-ttu-id="d35b8-120">I dispositivi di banda includono la maggior parte delle stampanti a matrice punto, oltre ad alcune stampanti laser.</span><span class="sxs-lookup"><span data-stu-id="d35b8-120">Banding devices include most dot matrix printers as well as some laser printers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d35b8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d35b8-121">Requirements</span></span>



| <span data-ttu-id="d35b8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35b8-122">Requirement</span></span> | <span data-ttu-id="d35b8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d35b8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d35b8-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d35b8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d35b8-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d35b8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d35b8-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d35b8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d35b8-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d35b8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d35b8-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d35b8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d35b8-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d35b8-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d35b8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d35b8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d35b8-131">Stampa di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="d35b8-131">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

