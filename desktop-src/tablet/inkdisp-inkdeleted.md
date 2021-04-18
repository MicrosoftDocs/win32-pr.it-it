---
description: Si verifica quando un tratto viene eliminato dall'oggetto InkDisp.
ms.assetid: 59ada470-6620-411d-889e-882f41ccea3e
title: Evento InkDisp. InkDeleted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9022b34b128f92530761a0093b2e7c1823dd88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306052"
---
# <a name="inkdispinkdeleted-event"></a><span data-ttu-id="ed016-103">Evento InkDisp. InkDeleted</span><span class="sxs-lookup"><span data-stu-id="ed016-103">InkDisp.InkDeleted event</span></span>

<span data-ttu-id="ed016-104">Si verifica quando un tratto viene eliminato dall'oggetto [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="ed016-104">Occurs when a stroke is deleted from the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed016-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed016-105">Syntax</span></span>


```C++
void InkDeleted(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="ed016-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed016-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed016-107">*StrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed016-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed016-108">Specifica la matrice di interi delle informazioni sull'ID del tratto per tutti i tratti che sono stati eliminati quando si verifica questo evento.</span><span class="sxs-lookup"><span data-stu-id="ed016-108">Specifies the integer array of stroke ID information for all of the strokes that have been deleted when this event occurs.</span></span>

<span data-ttu-id="ed016-109">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="ed016-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed016-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed016-110">Return value</span></span>

<span data-ttu-id="ed016-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ed016-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed016-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed016-112">Remarks</span></span>

<span data-ttu-id="ed016-113">Se si utilizza l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) (dove [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) è uguale a [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) e [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) è uguale a [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) e si passa la gomma a un tratto, si ottiene la sequenza di eventi seguente:</span><span class="sxs-lookup"><span data-stu-id="ed016-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   <span data-ttu-id="ed016-114">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="ed016-114">**InkDeleted**</span></span>
-   [<span data-ttu-id="ed016-115">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="ed016-115">**InkAdded**</span></span>](inkdisp-inkadded.md)
-   <span data-ttu-id="ed016-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="ed016-116">**InkDeleted**</span></span>

<span data-ttu-id="ed016-117">Si verificano gli eventi [**InkAdded**](inkdisp-inkadded.md) e **InkDeleted** aggiuntivi perché il codice sottostante aggiunge un tratto invisibile interno per tenere traccia della gomma.</span><span class="sxs-lookup"><span data-stu-id="ed016-117">The additional [**InkAdded**](inkdisp-inkadded.md) and **InkDeleted** events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="ed016-118">Questo metodo di evento è definito nell' \_ interfaccia IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="ed016-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="ed016-119">L' \_ interfaccia IInkEvents implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IEInkDeleted.</span><span class="sxs-lookup"><span data-stu-id="ed016-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkDeleted.</span></span>

<span data-ttu-id="ed016-120">L'evento **InkDeleted** viene generato anche in modalità selezione o cancellazione, non solo quando si inserisce input penna.</span><span class="sxs-lookup"><span data-stu-id="ed016-120">The **InkDeleted** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="ed016-121">A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e tenere presente la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="ed016-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="ed016-122">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ed016-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed016-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed016-123">Requirements</span></span>



| <span data-ttu-id="ed016-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed016-124">Requirement</span></span> | <span data-ttu-id="ed016-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ed016-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed016-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed016-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ed016-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ed016-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ed016-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed016-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ed016-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ed016-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ed016-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed016-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed016-131"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ed016-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ed016-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="ed016-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed016-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed016-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ed016-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed016-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed016-135">**Classe InkDisp**</span><span class="sxs-lookup"><span data-stu-id="ed016-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="ed016-136">[**Classe InkOverlay della proprietà EditingMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="ed016-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="ed016-137">[**Classe InkOverlay della proprietà EraserMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="ed016-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="ed016-138">**Evento InkAdded**</span><span class="sxs-lookup"><span data-stu-id="ed016-138">**InkAdded Event**</span></span>](inkdisp-inkadded.md)
</dt> <dt>

[<span data-ttu-id="ed016-139">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="ed016-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="ed016-140">Riferimento al controllo InkPicture</span><span class="sxs-lookup"><span data-stu-id="ed016-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ed016-141">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="ed016-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

