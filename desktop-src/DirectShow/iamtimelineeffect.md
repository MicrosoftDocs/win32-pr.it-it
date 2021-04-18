---
description: L'interfaccia IAMTimelineEffect fornisce i metodi per modificare gli effetti audio e video in DirectShow editing Services (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interfaccia IAMTimelineEffect (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333700"
---
# <a name="iamtimelineeffect-interface"></a><span data-ttu-id="2f363-103">Interfaccia IAMTimelineEffect</span><span class="sxs-lookup"><span data-stu-id="2f363-103">IAMTimelineEffect interface</span></span>

> [!Note]  
> <span data-ttu-id="2f363-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="2f363-104">\[Deprecated.</span></span> <span data-ttu-id="2f363-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2f363-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2f363-106">L' `IAMTimelineEffect` interfaccia fornisce i metodi per modificare gli effetti audio e video in [DirectShow editing Services](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="2f363-106">The `IAMTimelineEffect` interface provides methods for manipulating audio and video effects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="2f363-107">Un effetto può essere aggiunto a qualsiasi oggetto sequenza temporale che espone l'interfaccia [**IAMTimelineEffectable**](iamtimelineeffectable.md) .</span><span class="sxs-lookup"><span data-stu-id="2f363-107">An effect can be added to any timeline object that exposes the [**IAMTimelineEffectable**](iamtimelineeffectable.md) interface.</span></span> <span data-ttu-id="2f363-108">Per impostare le proprietà di un effetto, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="2f363-108">To set properties on an effect, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="2f363-109">L'oggetto effetto DES è effettivamente un wrapper per uno degli altri due oggetti:</span><span class="sxs-lookup"><span data-stu-id="2f363-109">The DES effect object is actually a wrapper for one of two other objects:</span></span>

-   <span data-ttu-id="2f363-110">Per gli effetti audio, qualsiasi filtro effetto audio DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2f363-110">For audio effects, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="2f363-111">Per gli effetti video e l'oggetto trasformazione DirectX con 1 input.</span><span class="sxs-lookup"><span data-stu-id="2f363-111">For video effects, and 1-input DirectX Transform object.</span></span>

<span data-ttu-id="2f363-112">Microsoft non supporta più lo sviluppo di oggetti di trasformazione DirectX di terze parti.</span><span class="sxs-lookup"><span data-stu-id="2f363-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span>

<span data-ttu-id="2f363-113">Per specificare l'oggetto filtro o trasformazione DirectX per un effetto, chiamare il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="2f363-113">To specify the filter or DirectX Transform object for an effect, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="2f363-114">Per creare un oggetto Effect, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con l'effetto di tipo principale della sequenza temporale del valore \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2f363-114">To create an effect object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_EFFECT.</span></span> <span data-ttu-id="2f363-115">È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l' `IAMTimelineEffect` interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2f363-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineEffect` interface.</span></span>

## <a name="members"></a><span data-ttu-id="2f363-116">Membri</span><span class="sxs-lookup"><span data-stu-id="2f363-116">Members</span></span>

<span data-ttu-id="2f363-117">L'interfaccia **IAMTimelineEffect** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2f363-117">The **IAMTimelineEffect** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2f363-118">**IAMTimelineEffect** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2f363-118">**IAMTimelineEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="2f363-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="2f363-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2f363-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="2f363-120">Methods</span></span>

<span data-ttu-id="2f363-121">L'interfaccia **IAMTimelineEffect** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2f363-121">The **IAMTimelineEffect** interface has these methods.</span></span>



| <span data-ttu-id="2f363-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="2f363-122">Method</span></span>                                                           | <span data-ttu-id="2f363-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f363-123">Description</span></span>                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="2f363-124">**EffectGetPriority**</span><span class="sxs-lookup"><span data-stu-id="2f363-124">**EffectGetPriority**</span></span>](iamtimelineeffect-effectgetpriority.md) | <span data-ttu-id="2f363-125">Recupera il livello di priorità dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="2f363-125">Retrieves the effect's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f363-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f363-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2f363-127">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="2f363-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2f363-128">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f363-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2f363-129">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2f363-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2f363-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f363-130">Requirements</span></span>



| <span data-ttu-id="2f363-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f363-131">Requirement</span></span> | <span data-ttu-id="2f363-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2f363-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f363-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f363-133">Header</span></span><br/>  | <dl> <span data-ttu-id="2f363-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f363-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2f363-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f363-135">Library</span></span><br/> | <dl> <span data-ttu-id="2f363-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f363-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f363-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f363-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f363-138">Utilizzo degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="2f363-138">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
