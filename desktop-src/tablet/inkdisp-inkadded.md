---
description: Si verifica quando viene aggiunto un tratto all'oggetto InkDisp.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Evento InkDisp. InkAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049459"
---
# <a name="inkdispinkadded-event"></a><span data-ttu-id="e78b8-103">Evento InkDisp. InkAdded</span><span class="sxs-lookup"><span data-stu-id="e78b8-103">InkDisp.InkAdded event</span></span>

<span data-ttu-id="e78b8-104">Si verifica quando viene aggiunto un tratto all'oggetto [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e78b8-104">Occurs when a stroke is added to the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78b8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e78b8-105">Syntax</span></span>


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="e78b8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e78b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e78b8-107">*StrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e78b8-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78b8-108">Matrice di interi delle informazioni sull'ID del tratto per tutti i tratti aggiunti quando si verifica questo evento.</span><span class="sxs-lookup"><span data-stu-id="e78b8-108">The integer array of stroke ID information for all of the strokes that have been added when this event occurs.</span></span>

<span data-ttu-id="e78b8-109">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="e78b8-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e78b8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e78b8-110">Return value</span></span>

<span data-ttu-id="e78b8-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e78b8-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e78b8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e78b8-112">Remarks</span></span>

<span data-ttu-id="e78b8-113">Se si utilizza l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) (dove [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) è uguale a [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) e [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) è uguale a [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) e si passa la gomma a un tratto, si ottiene la sequenza di eventi seguente:</span><span class="sxs-lookup"><span data-stu-id="e78b8-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   [<span data-ttu-id="e78b8-114">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="e78b8-114">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)
-   <span data-ttu-id="e78b8-115">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="e78b8-115">**InkAdded**</span></span>
-   [<span data-ttu-id="e78b8-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="e78b8-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)

<span data-ttu-id="e78b8-117">Si verificano gli eventi **InkAdded** e [**InkDeleted**](inkdisp-inkdeleted.md) aggiuntivi perché il codice sottostante aggiunge un tratto invisibile interno per tenere traccia della gomma.</span><span class="sxs-lookup"><span data-stu-id="e78b8-117">The additional **InkAdded** and [**InkDeleted**](inkdisp-inkdeleted.md) events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="e78b8-118">Questo metodo di evento è definito nell' \_ interfaccia IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="e78b8-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="e78b8-119">L' \_ interfaccia IInkEvents implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IEInkAdded.</span><span class="sxs-lookup"><span data-stu-id="e78b8-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkAdded.</span></span>

<span data-ttu-id="e78b8-120">L'evento **InkAdded** viene generato anche in modalità selezione o cancellazione, non solo quando si inserisce input penna.</span><span class="sxs-lookup"><span data-stu-id="e78b8-120">The **InkAdded** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="e78b8-121">A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e tenere presente la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="e78b8-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="e78b8-122">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e78b8-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="e78b8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e78b8-123">Requirements</span></span>



| <span data-ttu-id="e78b8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e78b8-124">Requirement</span></span> | <span data-ttu-id="e78b8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e78b8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78b8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e78b8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e78b8-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e78b8-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e78b8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e78b8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e78b8-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e78b8-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e78b8-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e78b8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e78b8-131"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e78b8-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e78b8-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="e78b8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e78b8-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e78b8-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e78b8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e78b8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78b8-135">**Classe InkDisp**</span><span class="sxs-lookup"><span data-stu-id="e78b8-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="e78b8-136">[**Classe InkOverlay della proprietà EditingMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="e78b8-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="e78b8-137">[**Classe InkOverlay della proprietà EraserMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="e78b8-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="e78b8-138">**Evento InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="e78b8-138">**InkDeleted Event**</span></span>](inkdisp-inkdeleted.md)
</dt> <dt>

[<span data-ttu-id="e78b8-139">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="e78b8-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="e78b8-140">Riferimento al controllo InkPicture</span><span class="sxs-lookup"><span data-stu-id="e78b8-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e78b8-141">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="e78b8-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

