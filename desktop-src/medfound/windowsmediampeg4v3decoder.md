---
description: Il decodificatore Windows Media MPEG-4 v3 decodifica i flussi video MPEG-4 v3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Windows Media MPEG-4 v3 decoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320575"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a><span data-ttu-id="5d398-103">Decodificatore Windows Media MPEG-4 v3</span><span class="sxs-lookup"><span data-stu-id="5d398-103">Windows Media MPEG-4 V3 Decoder</span></span>

<span data-ttu-id="5d398-104">Il decodificatore Windows Media MPEG-4 v3 decodifica i flussi video MPEG-4 v3.</span><span class="sxs-lookup"><span data-stu-id="5d398-104">The Windows Media MPEG-4 V3 decoder decodes MPEG-4 V3 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="5d398-105">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="5d398-105">Class Identifier</span></span>

<span data-ttu-id="5d398-106">L'identificatore di classe (CLSID) per il decodificatore MPEG-4 V3 di Windows è rappresentato dalla costante **CLSID \_ CMpeg43DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="5d398-106">The class identifier (CLSID) for the Windows MPEG-4 V3 decoder is represented by the constant **CLSID\_CMpeg43DecMediaObject**.</span></span> <span data-ttu-id="5d398-107">È possibile creare un'istanza del decodificatore MPEG-4 v3 chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="5d398-107">You can create an instance of the MPEG-4 V3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="5d398-108">Formati</span><span class="sxs-lookup"><span data-stu-id="5d398-108">Formats</span></span>

<span data-ttu-id="5d398-109">Il decodificatore Windows Media MPEG-4 V3 supporta i tipi di supporti di input seguenti.</span><span class="sxs-lookup"><span data-stu-id="5d398-109">The Windows Media MPEG-4 V3 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="5d398-110">\_Mp43 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5d398-110">MEDIASUBTYPE\_MP43</span></span>
-   <span data-ttu-id="5d398-111">\_Mp43 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5d398-111">MEDIASUBTYPE\_mp43</span></span>

<span data-ttu-id="5d398-112">Il decodificatore Windows Media MPEG-4 V3 supporta i sottotipi di supporti di output seguenti quando funge da oggetto DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="5d398-112">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="5d398-113">\_YUY2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5d398-113">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="5d398-114">\_UYVY MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5d398-114">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="5d398-115">\_Rgb32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5d398-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="5d398-116">\_RGB24 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5d398-116">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="5d398-117">\_RGB565 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5d398-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="5d398-118">\_RGB8 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5d398-118">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="5d398-119">\_RGB555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="5d398-119">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="5d398-120">Il decodificatore Windows Media MPEG-4 V3 supporta i sottotipi di supporti di output seguenti quando funge da trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="5d398-120">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="5d398-121">\_YUY2 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="5d398-121">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="5d398-122">\_UYVY MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="5d398-122">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="5d398-123">\_Rgb32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="5d398-123">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="5d398-124">\_RGB24 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="5d398-124">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="5d398-125">\_RGB565 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="5d398-125">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="5d398-126">\_RGB8 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="5d398-126">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="5d398-127">\_RGB555 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="5d398-127">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="5d398-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d398-128">Remarks</span></span>

<span data-ttu-id="5d398-129">L'oggetto decodificatore Windows Media MPEG-4 v3 espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="5d398-129">The Windows Media MPEG-4 V3 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="5d398-130">L'oggetto ha lo stesso identificatore di classe (CLSID), indipendentemente dal fatto che funga da DMO o da MFT.</span><span class="sxs-lookup"><span data-stu-id="5d398-130">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="5d398-131">Il decodificatore MPEG-4 V3 si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5d398-131">The MPEG-4 V3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="5d398-132">Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore MPEG-4 V3 si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="5d398-132">The following table shows the conditions under which an MPEG-4 V3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="5d398-133">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5d398-133">Operating system</span></span>            | <span data-ttu-id="5d398-134">Comportamento del decodificatore</span><span class="sxs-lookup"><span data-stu-id="5d398-134">Decoder behavior</span></span>                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d398-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d398-135">Windows XP</span></span>                  | <span data-ttu-id="5d398-136">Il decodificatore MPEG-4 V3 si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="5d398-136">The MPEG-4 V3 decoder always behaves as a DMO.</span></span>                                                                                                                      |
| <span data-ttu-id="5d398-137">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="5d398-137">Windows Vista and Windows 7</span></span> | <span data-ttu-id="5d398-138">Per impostazione predefinita, il decodificatore MPEG-4 V3 si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="5d398-138">By default, the MPEG-4 V3 decoder behaves as a DMO.</span></span> <span data-ttu-id="5d398-139">Se si ottiene un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sul decodificatore MPEG-4 v3, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="5d398-139">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on the MPEG-4 V3 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="5d398-140">Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un decodificatore funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="5d398-140">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="5d398-141">I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un decodificatore funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="5d398-141">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="5d398-142">Per informazioni sui GUID che rappresentano sottotipi di supporti, vedere GUID del [sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="5d398-142">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d398-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d398-143">Requirements</span></span>



| <span data-ttu-id="5d398-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d398-144">Requirement</span></span> | <span data-ttu-id="5d398-145">Valore</span><span class="sxs-lookup"><span data-stu-id="5d398-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d398-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d398-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5d398-147">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5d398-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5d398-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d398-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5d398-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d398-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d398-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d398-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d398-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d398-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="5d398-152">DLL</span><span class="sxs-lookup"><span data-stu-id="5d398-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d398-153"><dt>MP43DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d398-153"><dt>MP43DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d398-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d398-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d398-155">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="5d398-155">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
