---
title: Metodi CreateWicBitmapRenderTarget di ID2D1Factory
description: Crea una destinazione di rendering che esegue il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Metodo CreateWicBitmapRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325791"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a><span data-ttu-id="6edc2-104">Metodi ID2D1Factory:: CreateWicBitmapRenderTarget</span><span class="sxs-lookup"><span data-stu-id="6edc2-104">ID2D1Factory::CreateWicBitmapRenderTarget methods</span></span>

<span data-ttu-id="6edc2-105">Crea una destinazione di rendering che esegue il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="6edc2-105">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6edc2-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="6edc2-106">Overload list</span></span>



| <span data-ttu-id="6edc2-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="6edc2-107">Method</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="6edc2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6edc2-108">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6edc2-109">[**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ \_ proprietà della destinazione \_ di rendering \* , ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="6edc2-109">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES\*,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span></span> | <span data-ttu-id="6edc2-110">Crea una destinazione di rendering che esegue il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="6edc2-110">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |
| <span data-ttu-id="6edc2-111">[**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ proprietà della destinazione di rendering \_ \_&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="6edc2-111">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES&,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span></span>  | <span data-ttu-id="6edc2-112">Crea una destinazione di rendering che esegue il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="6edc2-112">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6edc2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6edc2-113">Remarks</span></span>

<span data-ttu-id="6edc2-114">L'applicazione deve creare le destinazioni di rendering una volta e mantenerle per la durata dell'applicazione o fino a quando non viene ricevuto l'errore di [**\_ \_ destinazione D2DERR ricreate**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6edc2-114">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="6edc2-115">Quando si riceve questo errore, è necessario ricreare la destinazione di rendering (e tutte le risorse create).</span><span class="sxs-lookup"><span data-stu-id="6edc2-115">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

<span data-ttu-id="6edc2-116">**Nota**   Questo metodo non è supportato in Windows Phone e avrà esito negativo quando viene chiamato su un dispositivo con codice di errore 0x8899000b (nessun dispositivo di rendering hardware disponibile per questa operazione).</span><span class="sxs-lookup"><span data-stu-id="6edc2-116">**Note**   This method isn't supported on Windows Phone and will fail when called on a device with error code 0x8899000b ( There is no hardware rendering device available for this operation ).</span></span> <span data-ttu-id="6edc2-117">Poiché l'emulatore Windows Phone supporta il rendering WARP, questo metodo avrà esito negativo quando viene chiamato sull'emulatore con un codice di errore diverso, 0x88982f80 (WinCoDec \_ Err \_ unsupportedpixelformat).</span><span class="sxs-lookup"><span data-stu-id="6edc2-117">Because the Windows Phone Emulator supports WARP rendering, this method will fail when called on the emulator with a different error code, 0x88982f80 (wincodec\_err\_unsupportedpixelformat).</span></span>

## <a name="requirements"></a><span data-ttu-id="6edc2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6edc2-118">Requirements</span></span>



| <span data-ttu-id="6edc2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6edc2-119">Requirement</span></span> | <span data-ttu-id="6edc2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6edc2-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6edc2-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="6edc2-121">Library</span></span><br/> | <dl> <span data-ttu-id="6edc2-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6edc2-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="6edc2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6edc2-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="6edc2-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6edc2-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6edc2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6edc2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edc2-126">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="6edc2-126">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

