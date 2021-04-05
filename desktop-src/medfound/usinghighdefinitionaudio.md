---
description: Uso di High-Definition audio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Uso di High-Definition audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755239"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a><span data-ttu-id="b3f9b-103">Uso di High-Definition audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="b3f9b-103">Using High-Definition Audio (Microsoft Media Foundation)</span></span>

<span data-ttu-id="b3f9b-104">L'audio ad alta definizione, nel contesto dei codec di Windows Media Audio, è qualsiasi tipo di audio con più di due canali o più di 16 bit per campione.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-104">High-definition audio, in the context of the Windows Media Audio codecs, is any audio type with more than two channels or more than 16 bits per sample.</span></span> <span data-ttu-id="b3f9b-105">L'audio ad alta definizione è supportato dalle categorie Professional e lossless del [codificatore Windows Media Audio](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="b3f9b-105">High-definition audio is supported by the Professional and Lossless categories of the [Windows Media Audio Encoder](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="b3f9b-106">I tipi audio ad alta definizione non compressi vengono definiti usando la struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3f9b-106">Uncompressed high-definition audio types are defined using the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> <span data-ttu-id="b3f9b-107">**WAVEFORMATEXTENSIBLE** è un'estensione strutturata della struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3f9b-107">**WAVEFORMATEXTENSIBLE** is a structured extension of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="b3f9b-108">Quando si usa DMOs, il membro **formatType** della struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) che descrive un tipo audio ad alta definizione deve essere impostato su WMCFORMAT \_ WAVEFORMATEX, così come per l'audio normale. non esiste alcun identificatore di formato speciale per **WAVEFORMATEXTENSIBLE**.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-108">When you are using DMOs, the **formattype** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure that describes a high-definition audio type must be set to WMCFORMAT\_WaveFormatEx, just as it is for normal audio; there is no special format identifier for **WAVEFORMATEXTENSIBLE**.</span></span> <span data-ttu-id="b3f9b-109">Se un formato USA **WAVEFORMATEXTENSIBLE** , è necessario impostare il membro **cbSize** della struttura **WAVEFORMATEX** su 22.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-109">If a format uses **WAVEFORMATEXTENSIBLE** , you must set the **cbSize** member of the **WAVEFORMATEX** structure to 22.</span></span>

<span data-ttu-id="b3f9b-110">Quando si usa Media Foundation, è possibile costruire il tipo di supporto corretto da una struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) usando la funzione [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span><span class="sxs-lookup"><span data-stu-id="b3f9b-110">When using Media Foundation, you can construct the correct media type from a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure by using the function [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span></span>

<span data-ttu-id="b3f9b-111">I tipi di output multicanale supportati dal codec Windows Media Audio 10 Professional non usano [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), ma segnalano il numero corretto di canali e BITS per campione nella struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3f9b-111">The multi-channel output types supported by the Windows Media Audio 10 Professional codec do not use [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), but report the correct number of channels and bits per sample in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="b3f9b-112">Come per tutti i tipi audio che descrivono il contenuto compresso di Windows Media Audio, sono presenti informazioni aggiuntive aggiunte alla struttura **WAVEFORMATEX** usata dal decodificatore per la decompressione.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-112">As with all audio types describing compressed Windows Media Audio content, there is additional information appended to the **WAVEFORMATEX** structure that is used by the decoder for decompression.</span></span>

## <a name="decoding-high-definition-audio"></a><span data-ttu-id="b3f9b-113">Decodifica audio High-Definition</span><span class="sxs-lookup"><span data-stu-id="b3f9b-113">Decoding High-Definition Audio</span></span>

<span data-ttu-id="b3f9b-114">Per decodificare l'audio ad alta definizione, è necessario impostare la proprietà [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-114">To decode high-definition audio, you must set the [MFPKEY\_WMADEC\_HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) property to VARIANT\_TRUE.</span></span> <span data-ttu-id="b3f9b-115">Se questa proprietà non è impostata, il decodificatore fornirà contenuto stereo con un massimo di 16 bit per campione, indipendentemente dal formato compresso.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-115">If this property is not set, the decoder will deliver stereo content with a maximum of 16 bits per sample, regardless of the compressed format.</span></span>

> [!Note]  
> <span data-ttu-id="b3f9b-116">L'audio ad alta definizione è supportato solo per Windows XP, Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-116">High-definition audio is supported only for Windows XP, Windows Vista and later.</span></span> <span data-ttu-id="b3f9b-117">Nelle versioni precedenti di Windows, il contenuto Windows Media Audio codificato con definizione alta viene visualizzato come audio a due canali con un massimo di 16 bit per campione.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-117">On earlier versions of Windows, Windows Media Audio content encoded with high definition is rendered as two-channel audio with a maximum of 16 bits per sample.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b3f9b-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b3f9b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3f9b-119">Utilizzo di audio</span><span class="sxs-lookup"><span data-stu-id="b3f9b-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 
