---
description: L'interfaccia IAMTimelineTrans fornisce metodi per la modifica delle transizioni in servizi di modifica DirectShow (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Interfaccia IAMTimelineTrans (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332973"
---
# <a name="iamtimelinetrans-interface"></a><span data-ttu-id="574fe-103">Interfaccia IAMTimelineTrans</span><span class="sxs-lookup"><span data-stu-id="574fe-103">IAMTimelineTrans interface</span></span>

> [!Note]  
> <span data-ttu-id="574fe-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="574fe-104">\[Deprecated.</span></span> <span data-ttu-id="574fe-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="574fe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="574fe-106">L' `IAMTimelineTrans` interfaccia fornisce metodi per la modifica delle transizioni nei [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="574fe-106">The `IAMTimelineTrans` interface provides methods for manipulating transitions in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="574fe-107">Una transizione è una progressione tra un livello video e la composita sottoposta a rendering di tutti i livelli video con una priorità più bassa.</span><span class="sxs-lookup"><span data-stu-id="574fe-107">A transition is a progression between one video layer and the rendered composite of all video layers with a lower priority.</span></span> <span data-ttu-id="574fe-108">È possibile aggiungere una transizione a qualsiasi oggetto sequenza temporale che espone l'interfaccia [**IAMTimelineTransable**](iamtimelinetransable.md) .</span><span class="sxs-lookup"><span data-stu-id="574fe-108">A transition can be added to any timeline object that exposes the [**IAMTimelineTransable**](iamtimelinetransable.md) interface.</span></span> <span data-ttu-id="574fe-109">Per impostare le proprietà di una transizione, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="574fe-109">To set properties on a transition, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="574fe-110">L'oggetto di transizione DES è effettivamente un wrapper per un oggetto Transform di DirectX.</span><span class="sxs-lookup"><span data-stu-id="574fe-110">The DES transition object is actually a wrapper for a DirectX Transform object.</span></span> <span data-ttu-id="574fe-111">Qualsiasi oggetto di trasformazione DirectX a 2 input può essere usato per implementare l'effetto visivo per la transizione.</span><span class="sxs-lookup"><span data-stu-id="574fe-111">Any 2-input DirectX Transform object can be used to implement the visual effect for the transition.</span></span> <span data-ttu-id="574fe-112">Microsoft non supporta più lo sviluppo di oggetti di trasformazione DirectX di terze parti.</span><span class="sxs-lookup"><span data-stu-id="574fe-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="574fe-113">Per specificare l'oggetto di trasformazione DirectX per una transizione, chiamare il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="574fe-113">To specify the DirectX Transform object for a transition, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="574fe-114">Per creare un oggetto di transizione, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con la sequenza temporale del valore \_ principale \_ Transition del tipo \_ .</span><span class="sxs-lookup"><span data-stu-id="574fe-114">To create a transition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRANSITION.</span></span> <span data-ttu-id="574fe-115">È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l' `IAMTimelineTrans` interfaccia.</span><span class="sxs-lookup"><span data-stu-id="574fe-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineTrans` interface.</span></span>

## <a name="members"></a><span data-ttu-id="574fe-116">Membri</span><span class="sxs-lookup"><span data-stu-id="574fe-116">Members</span></span>

<span data-ttu-id="574fe-117">L'interfaccia **IAMTimelineTrans** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="574fe-117">The **IAMTimelineTrans** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="574fe-118">**IAMTimelineTrans** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="574fe-118">**IAMTimelineTrans** also has these types of members:</span></span>

-   [<span data-ttu-id="574fe-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="574fe-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="574fe-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="574fe-120">Methods</span></span>

<span data-ttu-id="574fe-121">L'interfaccia **IAMTimelineTrans** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="574fe-121">The **IAMTimelineTrans** interface has these methods.</span></span>



| <span data-ttu-id="574fe-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="574fe-122">Method</span></span>                                                  | <span data-ttu-id="574fe-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="574fe-123">Description</span></span>                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="574fe-124">**GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="574fe-124">**GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)     | <span data-ttu-id="574fe-125">Recupera il punto di taglio.</span><span class="sxs-lookup"><span data-stu-id="574fe-125">Retrieves the cut point.</span></span><br/>                                                    |
| [<span data-ttu-id="574fe-126">**GetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="574fe-126">**GetCutPoint2**</span></span>](iamtimelinetrans-getcutpoint2.md)   | <span data-ttu-id="574fe-127">Recupera il punto di taglio come valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="574fe-127">Retrieves the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>             |
| [<span data-ttu-id="574fe-128">**GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="574fe-128">**GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)     | <span data-ttu-id="574fe-129">Determina se viene eseguito il rendering della transizione come taglia.</span><span class="sxs-lookup"><span data-stu-id="574fe-129">Determines whether the transition is rendered as a cut.</span></span><br/>                     |
| [<span data-ttu-id="574fe-130">**GetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="574fe-130">**GetSwapInputs**</span></span>](iamtimelinetrans-getswapinputs.md) | <span data-ttu-id="574fe-131">Recupera un valore che indica se gli input di transizione vengono scambiati.</span><span class="sxs-lookup"><span data-stu-id="574fe-131">Retrieves a value that indicates whether the transition inputs are swapped.</span></span><br/> |
| [<span data-ttu-id="574fe-132">**SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="574fe-132">**SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)     | <span data-ttu-id="574fe-133">Imposta il punto di taglio.</span><span class="sxs-lookup"><span data-stu-id="574fe-133">Sets the cut point.</span></span><br/>                                                         |
| [<span data-ttu-id="574fe-134">**SetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="574fe-134">**SetCutPoint2**</span></span>](iamtimelinetrans-setcutpoint2.md)   | <span data-ttu-id="574fe-135">Imposta il punto di taglio come valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="574fe-135">Sets the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>                  |
| [<span data-ttu-id="574fe-136">**SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="574fe-136">**SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)     | <span data-ttu-id="574fe-137">Specifica se viene eseguito il rendering della transizione come taglia.</span><span class="sxs-lookup"><span data-stu-id="574fe-137">Specifies whether the transition is rendered as a cut.</span></span><br/>                      |
| [<span data-ttu-id="574fe-138">**SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="574fe-138">**SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md) | <span data-ttu-id="574fe-139">Specifica se gli input di transizione vengono scambiati.</span><span class="sxs-lookup"><span data-stu-id="574fe-139">Specifies whether the transition inputs are swapped.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="574fe-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="574fe-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="574fe-141">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="574fe-141">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="574fe-142">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="574fe-142">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="574fe-143">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="574fe-143">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="574fe-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="574fe-144">Requirements</span></span>



| <span data-ttu-id="574fe-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="574fe-145">Requirement</span></span> | <span data-ttu-id="574fe-146">Valore</span><span class="sxs-lookup"><span data-stu-id="574fe-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="574fe-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="574fe-147">Header</span></span><br/>  | <dl> <span data-ttu-id="574fe-148"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="574fe-148"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="574fe-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="574fe-149">Library</span></span><br/> | <dl> <span data-ttu-id="574fe-150"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="574fe-150"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="574fe-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="574fe-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="574fe-152">Utilizzo degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="574fe-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
