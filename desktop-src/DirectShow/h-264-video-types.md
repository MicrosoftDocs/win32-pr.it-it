---
description: Tipi di video H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipi di video H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965456"
---
# <a name="h264-video-types"></a><span data-ttu-id="f9e45-103">Tipi di video H. 264</span><span class="sxs-lookup"><span data-stu-id="f9e45-103">H.264 Video Types</span></span>

<span data-ttu-id="f9e45-104">I sottotipi di supporto seguenti sono definiti per il video H. 264.</span><span class="sxs-lookup"><span data-stu-id="f9e45-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="f9e45-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="f9e45-105">Subtype</span></span>                | <span data-ttu-id="f9e45-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="f9e45-106">FOURCC</span></span> | <span data-ttu-id="f9e45-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9e45-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="f9e45-108">**\_AVC1 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="f9e45-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="f9e45-109">'AVC1'</span><span class="sxs-lookup"><span data-stu-id="f9e45-109">'AVC1'</span></span> | <span data-ttu-id="f9e45-110">Bitstream H. 264 senza codici iniziali.</span><span class="sxs-lookup"><span data-stu-id="f9e45-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="f9e45-111">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="f9e45-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="f9e45-112">H264</span><span class="sxs-lookup"><span data-stu-id="f9e45-112">'H264'</span></span> | <span data-ttu-id="f9e45-113">Bitstream H. 264 con codici iniziali.</span><span class="sxs-lookup"><span data-stu-id="f9e45-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="f9e45-114">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="f9e45-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="f9e45-115">H264</span><span class="sxs-lookup"><span data-stu-id="f9e45-115">'h264'</span></span> | <span data-ttu-id="f9e45-116">Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diverso.</span><span class="sxs-lookup"><span data-stu-id="f9e45-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="f9e45-117">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="f9e45-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="f9e45-118">X264</span><span class="sxs-lookup"><span data-stu-id="f9e45-118">'X264'</span></span> | <span data-ttu-id="f9e45-119">Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diverso.</span><span class="sxs-lookup"><span data-stu-id="f9e45-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="f9e45-120">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="f9e45-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="f9e45-121">x264</span><span class="sxs-lookup"><span data-stu-id="f9e45-121">'x264'</span></span> | <span data-ttu-id="f9e45-122">Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diverso.</span><span class="sxs-lookup"><span data-stu-id="f9e45-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="f9e45-123">Questi GUID del sottotipo sono dichiarati in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="f9e45-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="f9e45-124">La differenza principale tra questi tipi di supporti è la presenza di codici iniziali nel bitstream.</span><span class="sxs-lookup"><span data-stu-id="f9e45-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="f9e45-125">Se il sottotipo è **MEDIASUBTYPE \_ AVC1**, il Bitstream non contiene i codici iniziali.</span><span class="sxs-lookup"><span data-stu-id="f9e45-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="f9e45-126">Bitstream H. 264 con codici iniziali</span><span class="sxs-lookup"><span data-stu-id="f9e45-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="f9e45-127">I Bitstream H. 264 trasmessi in aria o contenuti in flussi di programmi o di trasporto MPEG-2 o registrati in HD-DVD sono formattati come descritto nell'allegato B di ITU-T REC. H. 264.</span><span class="sxs-lookup"><span data-stu-id="f9e45-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="f9e45-128">In base a questa specifica, il Bitstream è costituito da una sequenza di NALUs (Network Abstraction Layer Unit), ognuno dei quali è preceduto da un codice di inizio uguale a 0x000001 o 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="f9e45-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="f9e45-129">Quando i codici iniziali sono presenti in Bitstream, viene usato il seguente tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="f9e45-129">When start codes are present in the bitstream, the following media type is used:</span></span>



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e45-130">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="f9e45-130">Major type</span></span>  | <span data-ttu-id="f9e45-131">**Video di MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="f9e45-131">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="f9e45-132">Sottotipi</span><span class="sxs-lookup"><span data-stu-id="f9e45-132">Subtypes</span></span>    | <span data-ttu-id="f9e45-133">**MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ x264** o **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="f9e45-133">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="f9e45-134">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="f9e45-134">Format type</span></span> | <span data-ttu-id="f9e45-135">**Formato \_ VideoInfo**, **Format \_ VideoInfo2**, **Format \_ mpeg2video** o **GUID \_ null**</span><span class="sxs-lookup"><span data-stu-id="f9e45-135">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="f9e45-136">Se il tipo di formato **è \_ null GUID**, non è presente alcuna struttura di formato.</span><span class="sxs-lookup"><span data-stu-id="f9e45-136">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="f9e45-137">Quando il Bitstream contiene i codici iniziali, i tipi di formato elencati di seguito sono sufficienti, perché il decodificatore non richiede informazioni aggiuntive per analizzare il flusso.</span><span class="sxs-lookup"><span data-stu-id="f9e45-137">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="f9e45-138">Il Bitstream contiene già tutte le informazioni necessarie per il decodificatore e i codici iniziali consentono al decodificatore di individuare l'inizio di ogni NALU.</span><span class="sxs-lookup"><span data-stu-id="f9e45-138">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="f9e45-139">I sottotipi seguenti sono equivalenti:</span><span class="sxs-lookup"><span data-stu-id="f9e45-139">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="f9e45-140">Bitstream H. 264 senza codici iniziali</span><span class="sxs-lookup"><span data-stu-id="f9e45-140">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="f9e45-141">Il formato contenitore MP4 archivia i dati H. 264 senza codici iniziali.</span><span class="sxs-lookup"><span data-stu-id="f9e45-141">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="f9e45-142">Al contrario, ogni NALU è preceduto da un campo Length, che restituisce la lunghezza di NALU in byte.</span><span class="sxs-lookup"><span data-stu-id="f9e45-142">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="f9e45-143">Le dimensioni del campo Length possono variare, ma sono in genere pari a 1, 2 o 4 byte.</span><span class="sxs-lookup"><span data-stu-id="f9e45-143">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="f9e45-144">Quando i codici di avvio non sono presenti nel bitstream, viene usato il seguente tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="f9e45-144">When start codes are not present in the bitstream, the following media type is used.</span></span>



|             |                        |
|-------------|------------------------|
| <span data-ttu-id="f9e45-145">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="f9e45-145">Major type</span></span>  | <span data-ttu-id="f9e45-146">**Video di MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="f9e45-146">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="f9e45-147">Subtype</span><span class="sxs-lookup"><span data-stu-id="f9e45-147">Subtype</span></span>     | <span data-ttu-id="f9e45-148">**\_AVC1 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="f9e45-148">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="f9e45-149">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="f9e45-149">Format type</span></span> | <span data-ttu-id="f9e45-150">**FORMATO \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="f9e45-150">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="f9e45-151">Il blocco di formato è una struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="f9e45-151">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="f9e45-152">Questa struttura deve essere compilata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f9e45-152">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="f9e45-153">**HDR**: struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) che descrive il Bitstream.</span><span class="sxs-lookup"><span data-stu-id="f9e45-153">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="f9e45-154">Non è presente alcuna tabella dei colori dopo la parte [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) della struttura e **biClrUsed** deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f9e45-154">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="f9e45-155">**dwStartTimeCode**: non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f9e45-155">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="f9e45-156">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="f9e45-156">Set to zero.</span></span>
-   <span data-ttu-id="f9e45-157">**cbSequenceHeader**: lunghezza della matrice **dwSequenceHeader** in byte.</span><span class="sxs-lookup"><span data-stu-id="f9e45-157">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="f9e45-158">**dwProfile**: specifica il profilo H. 264.</span><span class="sxs-lookup"><span data-stu-id="f9e45-158">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="f9e45-159">**dwLevel**: specifica il livello H. 264.</span><span class="sxs-lookup"><span data-stu-id="f9e45-159">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="f9e45-160">**dwFlags**: numero di byte utilizzati per il campo Length visualizzato prima di ogni **Nalu**.</span><span class="sxs-lookup"><span data-stu-id="f9e45-160">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="f9e45-161">Il campo lunghezza indica le dimensioni dei seguenti NALU in byte.</span><span class="sxs-lookup"><span data-stu-id="f9e45-161">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="f9e45-162">Ad esempio, se **dwFlags** è 4, ogni Nalu è preceduto da un campo di lunghezza di 4 byte.</span><span class="sxs-lookup"><span data-stu-id="f9e45-162">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="f9e45-163">I valori validi sono 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="f9e45-163">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="f9e45-164">**dwSequenceHeader**: matrice di byte che può contenere set di parametri di sequenza (SPS) e set di parametri immagine (PPS) NALUs.</span><span class="sxs-lookup"><span data-stu-id="f9e45-164">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="f9e45-165">Il contenitore MP4 potrebbe contenere set di parametri di sequenza (SPS) o set di parametri immagine (PPS) come unità NAL speciali nelle intestazioni di file o in un flusso separato (distinto dal flusso video).</span><span class="sxs-lookup"><span data-stu-id="f9e45-165">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="f9e45-166">Quando viene stabilito il formato, il tipo di supporto può specificare unità SPS e PPS NAL nella matrice **dwSequenceHeader** .</span><span class="sxs-lookup"><span data-stu-id="f9e45-166">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="f9e45-167">Se **cbSequenceHeader** è maggiore di zero, **dwSequenceHeader** è l'inizio di una matrice di byte che contiene i NALUs SPS e PPS, delimitati da campi di lunghezza 2 byte, tutti nell'ordine dei byte di rete (big-endian).</span><span class="sxs-lookup"><span data-stu-id="f9e45-167">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="f9e45-168">È possibile avere sia SPS che PPS, solo uno di questi tipi o nessuno.</span><span class="sxs-lookup"><span data-stu-id="f9e45-168">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="f9e45-169">Il tipo effettivo di ogni NALU può essere determinato esaminando il campo **del \_ \_ tipo di unità NAL** del Nalu stesso.</span><span class="sxs-lookup"><span data-stu-id="f9e45-169">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="f9e45-170">Quando si usa questo tipo di supporto, ogni esempio di supporto viene avviato all'inizio di una NALU e le unità NAL non si estendono sugli esempi.</span><span class="sxs-lookup"><span data-stu-id="f9e45-170">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="f9e45-171">In questo modo, il decodificatore è in grado di ripristinare i dati o gli esempi eliminati.</span><span class="sxs-lookup"><span data-stu-id="f9e45-171">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



