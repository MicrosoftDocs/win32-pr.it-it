---
description: Il decodificatore Windows Media MP3 decodifica i file audio codificati nei formati seguenti.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Windows Media MP3 decoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332290"
---
# <a name="windows-media-mp3-decoder"></a><span data-ttu-id="5f287-103">Decoder Windows Media MP3</span><span class="sxs-lookup"><span data-stu-id="5f287-103">Windows Media MP3 Decoder</span></span>

<span data-ttu-id="5f287-104">Il decodificatore Windows Media MP3 decodifica i file audio codificati nei formati seguenti.</span><span class="sxs-lookup"><span data-stu-id="5f287-104">The Windows Media MP3 decoder decodes audio files that have been encoded in the following formats.</span></span>

-   <span data-ttu-id="5f287-105">ISO/IEC 11172-3 (MPEG-1 audio) Layer 3</span><span class="sxs-lookup"><span data-stu-id="5f287-105">ISO/IEC 11172-3 (MPEG-1 Audio) Layer 3</span></span>
-   <span data-ttu-id="5f287-106">ISO/IEC 13818-3 (MPEG-2 audio) Layer 3, estensione frequenza di campionamento bassa</span><span class="sxs-lookup"><span data-stu-id="5f287-106">ISO/IEC 13818-3 (MPEG-2 Audio) Layer 3, low sampling frequency extension</span></span>

## <a name="class-identifier"></a><span data-ttu-id="5f287-107">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="5f287-107">Class Identifier</span></span>

<span data-ttu-id="5f287-108">L'identificatore di classe (CLSID) per il decodificatore Windows Media MP3 è rappresentato dalla costante **CLSID \_ CMP3DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="5f287-108">The class identifier (CLSID) for the Windows Media MP3 decoder is represented by the constant **CLSID\_CMP3DecMediaObject**.</span></span> <span data-ttu-id="5f287-109">È possibile creare un'istanza del decodificatore MP3 chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="5f287-109">You can create an instance of the MP3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="5f287-110">Interfacce</span><span class="sxs-lookup"><span data-stu-id="5f287-110">Interfaces</span></span>

<span data-ttu-id="5f287-111">Un oggetto decoder MP3 espone l'interfaccia **IMediaObject** in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia **IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="5f287-111">An MP3 decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="5f287-112">Un decodificatore Windows Media MP3 si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5f287-112">A Windows Media MP3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="5f287-113">Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore Windows Media MP3 si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="5f287-113">The following table shows the conditions under which a Windows Media MP3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="5f287-114">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5f287-114">Operating system</span></span> | <span data-ttu-id="5f287-115">Comportamento del decodificatore</span><span class="sxs-lookup"><span data-stu-id="5f287-115">Decoder behavior</span></span>                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f287-116">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5f287-116">Windows XP</span></span>       | <span data-ttu-id="5f287-117">Un decodificatore Windows Media MP3 si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="5f287-117">A Windows Media MP3 decoder always behaves as a DMO.</span></span>                                                                                                                                           |
| <span data-ttu-id="5f287-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f287-118">Windows Vista</span></span>    | <span data-ttu-id="5f287-119">Per impostazione predefinita, un decodificatore Windows Media MP3 si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="5f287-119">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="5f287-120">Se si ottiene un'interfaccia **IMFTransform** o un'interfaccia **IPropertyStore** su un decodificatore Windows Media MP3, si comporta come una MFT.</span><span class="sxs-lookup"><span data-stu-id="5f287-120">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="5f287-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f287-121">Windows 7</span></span>        | <span data-ttu-id="5f287-122">Per impostazione predefinita, un decodificatore Windows Media MP3 si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="5f287-122">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="5f287-123">Se si ottiene un'interfaccia **IMFTransform** in un decodificatore Windows Media MP3, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="5f287-123">If you obtain an **IMFTransform** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="input-formats"></a><span data-ttu-id="5f287-124">Formati di input</span><span class="sxs-lookup"><span data-stu-id="5f287-124">Input Formats</span></span>

<span data-ttu-id="5f287-125">Nella tabella seguente viene illustrato il tag di formato audio che rappresenta il tipo di input supportato dal decodificatore Windows Media MP3.</span><span class="sxs-lookup"><span data-stu-id="5f287-125">The following table shows the audio format tag that represents the input type supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="5f287-126">Costante tag di formato</span><span class="sxs-lookup"><span data-stu-id="5f287-126">Format tag constant</span></span>      | <span data-ttu-id="5f287-127">Valore del tag di formato</span><span class="sxs-lookup"><span data-stu-id="5f287-127">Format tag value</span></span> | <span data-ttu-id="5f287-128">Formato audio</span><span class="sxs-lookup"><span data-stu-id="5f287-128">Audio format</span></span>     |
|--------------------------|------------------|------------------|
| <span data-ttu-id="5f287-129">\_Formato Wave \_ MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="5f287-129">WAVE\_FORMAT\_MPEGLAYER3</span></span> | <span data-ttu-id="5f287-130">0x55</span><span class="sxs-lookup"><span data-stu-id="5f287-130">0x55</span></span>             | <span data-ttu-id="5f287-131">MPEG Layer 3 ISO</span><span class="sxs-lookup"><span data-stu-id="5f287-131">ISO MPEG Layer 3</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="5f287-132">Formati di output</span><span class="sxs-lookup"><span data-stu-id="5f287-132">Output Formats</span></span>

<span data-ttu-id="5f287-133">La tabella seguente illustra i tag di formato audio che rappresentano i tipi di output supportati dal decodificatore Windows Media MP3.</span><span class="sxs-lookup"><span data-stu-id="5f287-133">The following table shows the audio format tags that represent the output types supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="5f287-134">Costante tag di formato</span><span class="sxs-lookup"><span data-stu-id="5f287-134">Format tag constant</span></span>       | <span data-ttu-id="5f287-135">Valore del tag di formato</span><span class="sxs-lookup"><span data-stu-id="5f287-135">Format tag value</span></span> | <span data-ttu-id="5f287-136">Formato audio</span><span class="sxs-lookup"><span data-stu-id="5f287-136">Audio format</span></span>                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5f287-137">\_PCM in formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="5f287-137">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="5f287-138">0x0001</span><span class="sxs-lookup"><span data-stu-id="5f287-138">0x0001</span></span>           | <span data-ttu-id="5f287-139">Formato PCM (se usato come DMO o MFT)</span><span class="sxs-lookup"><span data-stu-id="5f287-139">PCM format (when used as a DMO or an MFT)</span></span>                                   |
| <span data-ttu-id="5f287-140">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="5f287-140">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="5f287-141">0x0003</span><span class="sxs-lookup"><span data-stu-id="5f287-141">0x0003</span></span>           | <span data-ttu-id="5f287-142">Virgola mobile IEEE (se usato come MFT)</span><span class="sxs-lookup"><span data-stu-id="5f287-142">IEEE floating point (when used as an MFT)</span></span>                                   |
| <span data-ttu-id="5f287-143">\_formato Wave \_ estendibile</span><span class="sxs-lookup"><span data-stu-id="5f287-143">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="5f287-144">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="5f287-144">0xFFFE</span></span>           | <span data-ttu-id="5f287-145">Formato PCM/IEEE nella struttura **WAVEFORMATEXTENSIBLE** (se usato come MFT)</span><span class="sxs-lookup"><span data-stu-id="5f287-145">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure (when used as an MFT)</span></span> |



 

<span data-ttu-id="5f287-146">Il decodificatore Windows Media MP3 supporta ed enumera i tipi di supporti di output seguenti.</span><span class="sxs-lookup"><span data-stu-id="5f287-146">The Windows Media MP3 decoder supports and enumerates the following output media types.</span></span>

-   <span data-ttu-id="5f287-147">Tipo di output con lo stesso frequenza di campionamento e numero di canali del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="5f287-147">An output type that has the same sampling rate and number of channels as the input type.</span></span>
-   <span data-ttu-id="5f287-148">Output mono per input stereo.</span><span class="sxs-lookup"><span data-stu-id="5f287-148">Mono output for stereo input.</span></span>
-   <span data-ttu-id="5f287-149">Tipi di output con profondità di bit di 8 e 16.</span><span class="sxs-lookup"><span data-stu-id="5f287-149">Output types with bit depths of 8 and 16.</span></span>
-   <span data-ttu-id="5f287-150">Output a virgola mobile, se il decodificatore si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="5f287-150">Floating point output, if the decoder is behaving as an MFT.</span></span>

<span data-ttu-id="5f287-151">Il decodificatore Windows Media MP3 supporta, ma non enumera, i seguenti tipi di supporti di output.</span><span class="sxs-lookup"><span data-stu-id="5f287-151">The Windows Media MP3 decoder supports, but does not enumerate, the following output media types.</span></span>

-   <span data-ttu-id="5f287-152">Tipo di output con metà della frequenza di campionamento del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="5f287-152">An output type that has half the sampling rate of the input type.</span></span>
-   <span data-ttu-id="5f287-153">Tipo di output con un quarto della frequenza di campionamento del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="5f287-153">An output type that has one fourth the sampling rate of the input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f287-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f287-154">Requirements</span></span>



| <span data-ttu-id="5f287-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f287-155">Requirement</span></span> | <span data-ttu-id="5f287-156">Valore</span><span class="sxs-lookup"><span data-stu-id="5f287-156">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f287-157">Client</span><span class="sxs-lookup"><span data-stu-id="5f287-157">Client</span></span><br/> | <span data-ttu-id="5f287-158">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f287-158">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="5f287-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f287-159">Header</span></span><br/> | <dl> <span data-ttu-id="5f287-160"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f287-160"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="5f287-161">DLL</span><span class="sxs-lookup"><span data-stu-id="5f287-161">DLL</span></span><br/>    | <dl> <span data-ttu-id="5f287-162"><dt>Mp3dmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f287-162"><dt>Mp3dmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5f287-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f287-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f287-164">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="5f287-164">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="5f287-165">Implementazione del codec</span><span class="sxs-lookup"><span data-stu-id="5f287-165">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




