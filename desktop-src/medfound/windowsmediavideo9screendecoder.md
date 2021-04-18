---
description: Il decodificatore di Windows Media Video 9 dello schermo decodifica i flussi codificati dal codificatore dello schermo Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Decodificatore dello schermo Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327979"
---
# <a name="windows-media-video-9-screen-decoder"></a><span data-ttu-id="13abd-103">Decodificatore dello schermo Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="13abd-103">Windows Media Video 9 Screen Decoder</span></span>

<span data-ttu-id="13abd-104">Il decodificatore di Windows Media Video 9 dello schermo decodifica i flussi codificati dal [**codificatore dello schermo Windows Media video 9**](windowsmediavideo9screenencoder.md).</span><span class="sxs-lookup"><span data-stu-id="13abd-104">The Windows Media Video 9 Screen decoder decodes streams that were encoded by the [**Windows Media Video 9 Screen Encoder**](windowsmediavideo9screenencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="13abd-105">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="13abd-105">Class Identifier</span></span>

<span data-ttu-id="13abd-106">L'identificatore di classe (CLSID) per il decodificatore della schermata Windows Media Video 9 è rappresentato dalla costante **CLSID \_ CMSSCDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="13abd-106">The class identifier (CLSID) for the Windows Media Video 9 Screen decoder is represented by the constant **CLSID\_CMSSCDecMediaObject**.</span></span> <span data-ttu-id="13abd-107">È possibile creare un'istanza del decodificatore chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="13abd-107">You can create an instance of the decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="13abd-108">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="13abd-108">Input Types</span></span>

<span data-ttu-id="13abd-109">Il codice di quattro caratteri (FOURCC) per il contenuto codificato Windows Media Video schermata versione 9 è "MSS2".</span><span class="sxs-lookup"><span data-stu-id="13abd-109">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="13abd-110">I tipi di input seguenti sono supportati dal decodificatore dello schermo versione 9.</span><span class="sxs-lookup"><span data-stu-id="13abd-110">The following input types are supported by the Version 9 Screen decoder.</span></span>

-   <span data-ttu-id="13abd-111">\_Mss2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="13abd-111">MEDIASUBTYPE\_MSS2</span></span>

## <a name="output-types"></a><span data-ttu-id="13abd-112">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="13abd-112">Output Types</span></span>

<span data-ttu-id="13abd-113">I tipi di output seguenti sono supportati dal decodificatore dello schermo versione 9 quando viene usato come DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="13abd-113">The following output types are supported by the Version 9 Screen decoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="13abd-114">\_RGB24 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="13abd-114">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="13abd-115">\_Rgb32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="13abd-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="13abd-116">\_ARGB32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="13abd-116">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="13abd-117">\_RGB565 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="13abd-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="13abd-118">\_RGB555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="13abd-118">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="13abd-119">\_RGB8 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="13abd-119">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="13abd-120">I tipi di output seguenti sono supportati dal decodificatore dello schermo versione 9 quando viene usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="13abd-120">The following output types are supported by the Version 9 Screen decoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="13abd-121">\_RGB24 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="13abd-121">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="13abd-122">\_Rgb32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="13abd-122">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="13abd-123">\_ARGB32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="13abd-123">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="13abd-124">\_RGB565 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="13abd-124">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="13abd-125">\_RGB555 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="13abd-125">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="13abd-126">\_RGB8 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="13abd-126">MFVideoFormat\_RGB8</span></span>

## <a name="remarks"></a><span data-ttu-id="13abd-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="13abd-127">Remarks</span></span>

<span data-ttu-id="13abd-128">Un oggetto decodificatore dello schermo espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="13abd-128">A screen decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="13abd-129">Un decodificatore dello schermo si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="13abd-129">A screen decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="13abd-130">Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore dello schermo si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="13abd-130">The following table shows the conditions under which a screen decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="13abd-131">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="13abd-131">Operating system</span></span>            | <span data-ttu-id="13abd-132">Comportamento del decodificatore</span><span class="sxs-lookup"><span data-stu-id="13abd-132">Decoder behavior</span></span>                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13abd-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="13abd-133">Windows XP</span></span>                  | <span data-ttu-id="13abd-134">Un decodificatore Windows Media Screen si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="13abd-134">A Windows Media Screen decoder always behaves as a DMO.</span></span>                                                                                                                 |
| <span data-ttu-id="13abd-135">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="13abd-135">Windows Vista and Windows 7</span></span> | <span data-ttu-id="13abd-136">Per impostazione predefinita, un decodificatore Windows Media Screen si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="13abd-136">By default, a Windows Media Screen decoder behaves as a DMO.</span></span> <span data-ttu-id="13abd-137">Se si ottiene un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) su un decodificatore dello schermo, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="13abd-137">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a screen decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="13abd-138">È possibile utilizzare lo stesso CLSID (CLSID \_ CMSSCDecMediaObject) per creare il decodificatore dello schermo versione 7 e il decodificatore della schermata versione 9.</span><span class="sxs-lookup"><span data-stu-id="13abd-138">You can use the same CLSID (CLSID\_CMSSCDecMediaObject) to create the Version 7 Screen decoder and the Version 9 Screen decoder.</span></span> <span data-ttu-id="13abd-139">Il FOURCC per il contenuto codificato Windows Media Video schermata versione 7 è "MSS1".</span><span class="sxs-lookup"><span data-stu-id="13abd-139">The FOURCC for Windows Media Video Screen Version 7 encoded content is "MSS1".</span></span> <span data-ttu-id="13abd-140">Il decodificatore della schermata versione 7 supporta il \_ tipo di input MSS1 di MEDIASUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="13abd-140">The Version 7 Screen decoder supports the MEDIASUBTYPE\_MSS1 input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="13abd-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13abd-141">Requirements</span></span>



| <span data-ttu-id="13abd-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="13abd-142">Requirement</span></span> | <span data-ttu-id="13abd-143">Valore</span><span class="sxs-lookup"><span data-stu-id="13abd-143">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13abd-144">Client</span><span class="sxs-lookup"><span data-stu-id="13abd-144">Client</span></span><br/> | <span data-ttu-id="13abd-145">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="13abd-145">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="13abd-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13abd-146">Header</span></span><br/> | <dl> <span data-ttu-id="13abd-147"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="13abd-147"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="13abd-148">DLL</span><span class="sxs-lookup"><span data-stu-id="13abd-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="13abd-149"><dt>Wmvsdecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13abd-149"><dt>Wmvsdecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13abd-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13abd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13abd-151">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="13abd-151">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="13abd-152">Implementazione del codec</span><span class="sxs-lookup"><span data-stu-id="13abd-152">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="13abd-153">Uso del codec della schermata Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="13abd-153">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="13abd-154">Codificatore dello schermo Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="13abd-154">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
