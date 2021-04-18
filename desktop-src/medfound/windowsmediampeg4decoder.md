---
description: Il decodificatore Windows Media MPEG4 v1/v2 decodifica i flussi video MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Decodificatore Windows Media MPEG4 v1/v2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320513"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a><span data-ttu-id="3a24f-103">Decoder Windows Media MPEG4 v1/v2</span><span class="sxs-lookup"><span data-stu-id="3a24f-103">Windows Media MPEG4 V1/V2 Decoder</span></span>

<span data-ttu-id="3a24f-104">Il decodificatore Windows Media MPEG4 v1/v2 decodifica i flussi video MPEG4 v1/v2.</span><span class="sxs-lookup"><span data-stu-id="3a24f-104">The Windows Media MPEG4 V1/V2 decoder decodes MPEG4 V1/V2 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="3a24f-105">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="3a24f-105">Class Identifier</span></span>

<span data-ttu-id="3a24f-106">L'identificatore di classe (CLSID) per il decodificatore Windows Media MPEG4 v1/v2 è rappresentato dalla costante **CLSID \_ CMpeg4DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="3a24f-106">The class identifier (CLSID) for the Windows Media MPEG4 V1/V2 decoder is represented by the constant **CLSID\_CMpeg4DecMediaObject**.</span></span> <span data-ttu-id="3a24f-107">È possibile creare un'istanza del decodificatore MPEG4 v1/v2 chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="3a24f-107">You can create an instance of the MPEG4 V1/V2 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="3a24f-108">Formati</span><span class="sxs-lookup"><span data-stu-id="3a24f-108">Formats</span></span>

<span data-ttu-id="3a24f-109">Il decodificatore Windows Media MPEG4 v1/v2 supporta i tipi di supporti di input seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a24f-109">The Windows Media MPEG4 V1/V2 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="3a24f-110">\_MPG4 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-110">MEDIASUBTYPE\_MPG4</span></span>
-   <span data-ttu-id="3a24f-111">\_MPG4 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-111">MEDIASUBTYPE\_mpg4</span></span>
-   <span data-ttu-id="3a24f-112">\_MP42 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-112">MEDIASUBTYPE\_MP42</span></span>
-   <span data-ttu-id="3a24f-113">\_MP42 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-113">MEDIASUBTYPE\_mp42</span></span>

<span data-ttu-id="3a24f-114">Il decodificatore Windows Media MPEG4 v1/v2 supporta i sottotipi di supporti di output seguenti quando funge da oggetto DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="3a24f-114">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="3a24f-115">\_YUY2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-115">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="3a24f-116">\_UYVY MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-116">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="3a24f-117">\_Rgb32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-117">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="3a24f-118">\_RGB24 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-118">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="3a24f-119">\_RGB565 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-119">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="3a24f-120">\_RGB8 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-120">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="3a24f-121">\_RGB555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="3a24f-121">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="3a24f-122">Il decodificatore Windows Media MPEG4 v1/v2 supporta i sottotipi di supporti di output seguenti quando funge da trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="3a24f-122">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="3a24f-123">\_YUY2 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="3a24f-123">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="3a24f-124">\_UYVY MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="3a24f-124">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="3a24f-125">\_Rgb32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="3a24f-125">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="3a24f-126">\_RGB24 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="3a24f-126">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="3a24f-127">\_RGB565 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="3a24f-127">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="3a24f-128">\_RGB8 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="3a24f-128">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="3a24f-129">\_RGB555 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="3a24f-129">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="3a24f-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a24f-130">Remarks</span></span>

<span data-ttu-id="3a24f-131">L'oggetto decodificatore Windows Media MPEG4 v1/v2 espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="3a24f-131">The Windows Media MPEG4 V1/V2 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="3a24f-132">L'oggetto ha lo stesso identificatore di classe (CLSID), indipendentemente dal fatto che funga da DMO o da MFT.</span><span class="sxs-lookup"><span data-stu-id="3a24f-132">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="3a24f-133">Un decodificatore MPEG4 v1/v2 si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3a24f-133">An MPEG4 V1/V2 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="3a24f-134">Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore MPEG4 v1/v2 si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="3a24f-134">The following table shows the conditions under which an MPEG4 V1/V2 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="3a24f-135">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3a24f-135">Operating system</span></span>            | <span data-ttu-id="3a24f-136">Comportamento del decodificatore</span><span class="sxs-lookup"><span data-stu-id="3a24f-136">Decoder behavior</span></span>                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a24f-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3a24f-137">Windows XP</span></span>                  | <span data-ttu-id="3a24f-138">Un decodificatore MPEG4 v1/v2 si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="3a24f-138">An MPEG4 V1/V2 decoder always behaves as a DMO.</span></span>                                                                                                                                 |
| <span data-ttu-id="3a24f-139">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a24f-139">Windows Vista and Windows 7</span></span> | <span data-ttu-id="3a24f-140">Per impostazione predefinita, un decodificatore MPEG4 v1/v2 si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="3a24f-140">By default, an MPEG4 V1/V2 decoder behaves as a DMO.</span></span> <span data-ttu-id="3a24f-141">Se si ottiene un'interfaccia [GUID del sottotipo video](video-subtype-guids.md) in un decodificatore MPEG4 v1/v2, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="3a24f-141">If you obtain an [Video Subtype GUIDs](video-subtype-guids.md) interface on an MPEG4 V1/V2 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="3a24f-142">Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un decodificatore funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="3a24f-142">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="3a24f-143">I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un decodificatore funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="3a24f-143">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="3a24f-144">Per informazioni sui GUID che rappresentano sottotipi video, vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3a24f-144">For information about the GUIDs that represent video subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a24f-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a24f-145">Requirements</span></span>



| <span data-ttu-id="3a24f-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a24f-146">Requirement</span></span> | <span data-ttu-id="3a24f-147">Valore</span><span class="sxs-lookup"><span data-stu-id="3a24f-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a24f-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a24f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3a24f-149">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3a24f-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3a24f-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a24f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3a24f-151">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a24f-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3a24f-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a24f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a24f-153"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a24f-153"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="3a24f-154">DLL</span><span class="sxs-lookup"><span data-stu-id="3a24f-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a24f-155"><dt>MPG4DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a24f-155"><dt>MPG4DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a24f-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a24f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a24f-157">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="3a24f-157">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
