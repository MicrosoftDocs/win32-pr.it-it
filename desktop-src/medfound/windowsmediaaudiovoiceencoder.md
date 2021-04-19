---
description: Il codificatore Windows Media Audio Voice è ottimizzato per la codifica della voce umana a rapporti di compressione elevati. Si tratta del codificatore preferito per i flussi costituiti principalmente da parole vocali.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Codificatore Voice Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332241"
---
# <a name="windows-media-audio-voice-encoder"></a><span data-ttu-id="4025c-104">Codificatore Voice Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="4025c-104">Windows Media Audio Voice Encoder</span></span>

<span data-ttu-id="4025c-105">Il codificatore Windows Media Audio Voice è ottimizzato per la codifica della voce umana a rapporti di compressione elevati.</span><span class="sxs-lookup"><span data-stu-id="4025c-105">The Windows Media Audio Voice encoder is optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="4025c-106">Si tratta del codificatore preferito per i flussi costituiti principalmente da parole vocali.</span><span class="sxs-lookup"><span data-stu-id="4025c-106">This is the preferred encoder for streams consisting mostly of spoken words.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="4025c-107">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="4025c-107">Class Identifier</span></span>

<span data-ttu-id="4025c-108">L'identificatore di classe (CLSID) per il codificatore Voice Windows Media Audio è rappresentato dalla costante **CLSID \_ CWMSPEncMediaObject2**.</span><span class="sxs-lookup"><span data-stu-id="4025c-108">The class identifier (CLSID) for the Windows Media Audio Voice encoder is represented by the constant **CLSID\_CWMSPEncMediaObject2**.</span></span> <span data-ttu-id="4025c-109">È possibile creare un'istanza del codificatore vocale chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="4025c-109">You can create an instance of the voice encoder by calling **CoCreateInstance**.</span></span>

## <a name="output-formats"></a><span data-ttu-id="4025c-110">Formati di output</span><span class="sxs-lookup"><span data-stu-id="4025c-110">Output Formats</span></span>

<span data-ttu-id="4025c-111">Windows Media Audio contenuto con codifica Voice viene identificato dal tag di formato 0x00A.</span><span class="sxs-lookup"><span data-stu-id="4025c-111">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="4025c-112">Proprietà del codificatore</span><span class="sxs-lookup"><span data-stu-id="4025c-112">Encoder Properties</span></span>

<span data-ttu-id="4025c-113">Il codificatore Windows Media Audio Voice supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="4025c-113">The Windows Media Audio Voice encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4025c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4025c-114">Property</span></span></th>
<th><span data-ttu-id="4025c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4025c-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4025c-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span><span class="sxs-lookup"><span data-stu-id="4025c-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span></span></td>
<td><span data-ttu-id="4025c-117">Specifica la finestra del buffer, in millisecondi, utilizzata per il codec voce.</span><span class="sxs-lookup"><span data-stu-id="4025c-117">Specifies the buffer window, in milliseconds, used for the voice codec.</span></span><br/> <dl> <span data-ttu-id="4025c-118">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4025c-118">Windows XP and later.</span></span><br />
<span data-ttu-id="4025c-119">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="4025c-119">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4025c-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span><span class="sxs-lookup"><span data-stu-id="4025c-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span></span></td>
<td><span data-ttu-id="4025c-121">Specifica la latenza del codificatore in unità di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="4025c-121">Specifies encoder latency in packet units.</span></span><br/> <dl> <span data-ttu-id="4025c-122">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4025c-122">Windows XP and later.</span></span><br />
<span data-ttu-id="4025c-123">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="4025c-123">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4025c-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span><span class="sxs-lookup"><span data-stu-id="4025c-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span></span></td>
<td><span data-ttu-id="4025c-125">Specifica le parti di contenuto da codificare come musica dal codec vocale.</span><span class="sxs-lookup"><span data-stu-id="4025c-125">Specifies the portions of content to be encoded as music by the voice codec.</span></span><br/> <dl> <span data-ttu-id="4025c-126">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4025c-126">Windows XP and later.</span></span><br />
<span data-ttu-id="4025c-127">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4025c-127">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4025c-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span><span class="sxs-lookup"><span data-stu-id="4025c-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span></span></td>
<td><span data-ttu-id="4025c-129">Specifica la modalità del codec vocale.</span><span class="sxs-lookup"><span data-stu-id="4025c-129">Specifies the mode of the voice codec.</span></span><br/> <dl> <span data-ttu-id="4025c-130">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4025c-130">Windows XP and later.</span></span><br />
<span data-ttu-id="4025c-131">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4025c-131">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="4025c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4025c-132">Requirements</span></span>



| <span data-ttu-id="4025c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4025c-133">Requirement</span></span> | <span data-ttu-id="4025c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="4025c-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4025c-135">Client</span><span class="sxs-lookup"><span data-stu-id="4025c-135">Client</span></span><br/> | <span data-ttu-id="4025c-136">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="4025c-136">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="4025c-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4025c-137">Header</span></span><br/> | <dl> <span data-ttu-id="4025c-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4025c-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="4025c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4025c-139">DLL</span></span><br/>    | <dl> <span data-ttu-id="4025c-140"><dt>Wmspdmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4025c-140"><dt>Wmspdmoe.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4025c-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4025c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4025c-142">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="4025c-142">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="4025c-143">Uso del codec Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="4025c-143">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




