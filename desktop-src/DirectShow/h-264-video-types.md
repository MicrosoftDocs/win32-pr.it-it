---
description: Tipi di video H.264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipi di video H.264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692a751e197e2e7bbb088b30dd2a3f5f199d56de
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909019"
---
# <a name="h264-video-types"></a><span data-ttu-id="3d33f-103">Tipi di video H.264</span><span class="sxs-lookup"><span data-stu-id="3d33f-103">H.264 Video Types</span></span>

<span data-ttu-id="3d33f-104">I sottotipi multimediali seguenti sono definiti per il video H.264.</span><span class="sxs-lookup"><span data-stu-id="3d33f-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="3d33f-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="3d33f-105">Subtype</span></span>                | <span data-ttu-id="3d33f-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="3d33f-106">FOURCC</span></span> | <span data-ttu-id="3d33f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d33f-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="3d33f-108">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="3d33f-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="3d33f-109">'AVC1'</span><span class="sxs-lookup"><span data-stu-id="3d33f-109">'AVC1'</span></span> | <span data-ttu-id="3d33f-110">Flusso di bit H.264 senza codici di avvio.</span><span class="sxs-lookup"><span data-stu-id="3d33f-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="3d33f-111">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="3d33f-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="3d33f-112">'H264'</span><span class="sxs-lookup"><span data-stu-id="3d33f-112">'H264'</span></span> | <span data-ttu-id="3d33f-113">Flusso di bit H.264 con codici di avvio.</span><span class="sxs-lookup"><span data-stu-id="3d33f-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="3d33f-114">**MEDIASUBTYPE \_ h264**</span><span class="sxs-lookup"><span data-stu-id="3d33f-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="3d33f-115">'h264'</span><span class="sxs-lookup"><span data-stu-id="3d33f-115">'h264'</span></span> | <span data-ttu-id="3d33f-116">Equivalente a **MEDIASUBTYPE \_ H264,** con un fourcc diverso.</span><span class="sxs-lookup"><span data-stu-id="3d33f-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="3d33f-117">**MEDIASUBTYPE \_ X264**</span><span class="sxs-lookup"><span data-stu-id="3d33f-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="3d33f-118">'X264'</span><span class="sxs-lookup"><span data-stu-id="3d33f-118">'X264'</span></span> | <span data-ttu-id="3d33f-119">Equivalente a **MEDIASUBTYPE \_ H264,** con un fourcc diverso.</span><span class="sxs-lookup"><span data-stu-id="3d33f-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="3d33f-120">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="3d33f-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="3d33f-121">'x264'</span><span class="sxs-lookup"><span data-stu-id="3d33f-121">'x264'</span></span> | <span data-ttu-id="3d33f-122">Equivalente a **MEDIASUBTYPE \_ H264,** con un fourcc diverso.</span><span class="sxs-lookup"><span data-stu-id="3d33f-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="3d33f-123">Questi GUID del sottotipo sono dichiarati in wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="3d33f-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="3d33f-124">La differenza principale tra questi tipi di supporti è la presenza di codici di avvio nel flusso di bit.</span><span class="sxs-lookup"><span data-stu-id="3d33f-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="3d33f-125">Se il sottotipo **è MEDIASUBTYPE \_ AVC1,** il flusso di bit non contiene codici di avvio.</span><span class="sxs-lookup"><span data-stu-id="3d33f-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="3d33f-126">H.264 Bitstream con codici di avvio</span><span class="sxs-lookup"><span data-stu-id="3d33f-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="3d33f-127">I flussi di bit H.264 trasmessi in aria o contenuti in flussi di trasporto o programma MPEG-2 o registrati su HD-DVD sono formattati come descritto nell'allegato B di ITU-T Rec. H.264.</span><span class="sxs-lookup"><span data-stu-id="3d33f-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="3d33f-128">In base a questa specifica, il flusso di bit è costituito da una sequenza di unità del livello di astrazione di rete (NALU), ognuna delle quali è preceduta da un codice iniziale uguale a 0x000001 o 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="3d33f-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="3d33f-129">Quando nel flusso di bit sono presenti codici di avvio, viene usato il tipo di supporto seguente:</span><span class="sxs-lookup"><span data-stu-id="3d33f-129">When start codes are present in the bitstream, the following media type is used:</span></span>



| <span data-ttu-id="3d33f-130">Label</span><span class="sxs-lookup"><span data-stu-id="3d33f-130">Label</span></span> | <span data-ttu-id="3d33f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3d33f-131">Value</span></span> |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d33f-132">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="3d33f-132">Major type</span></span>  | <span data-ttu-id="3d33f-133">**MEDIATYPE \_ Video**</span><span class="sxs-lookup"><span data-stu-id="3d33f-133">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="3d33f-134">Sottotipi</span><span class="sxs-lookup"><span data-stu-id="3d33f-134">Subtypes</span></span>    | <span data-ttu-id="3d33f-135">**MEDIASUBTYPE \_ H264,** **MEDIASUBTYPE \_ h264,** **MEDIASUBTYPE \_ X264** o **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="3d33f-135">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="3d33f-136">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="3d33f-136">Format type</span></span> | <span data-ttu-id="3d33f-137">**FORMAT \_ VideoInfo**, **FORMAT \_ VideoInfo2**, **FORMAT \_ MPEG2Video** o **GUID \_ NULL**</span><span class="sxs-lookup"><span data-stu-id="3d33f-137">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="3d33f-138">Se il tipo di formato è **GUID \_ NULL,** non è presente alcuna struttura di formato.</span><span class="sxs-lookup"><span data-stu-id="3d33f-138">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="3d33f-139">Quando il flusso di bit contiene codici di inizio, uno dei tipi di formato elencati qui è sufficiente, perché il decodificatore non richiede informazioni aggiuntive per analizzare il flusso.</span><span class="sxs-lookup"><span data-stu-id="3d33f-139">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="3d33f-140">Il flusso di bit contiene già tutte le informazioni necessarie per il decodificatore e i codici di avvio consentono al decodificatore di individuare l'inizio di ogni NALU.</span><span class="sxs-lookup"><span data-stu-id="3d33f-140">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="3d33f-141">I sottotipi seguenti sono equivalenti:</span><span class="sxs-lookup"><span data-stu-id="3d33f-141">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="3d33f-142">H.264 Bitstream senza codici di avvio</span><span class="sxs-lookup"><span data-stu-id="3d33f-142">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="3d33f-143">Il formato del contenitore MP4 archivia i dati H.264 senza codici di avvio.</span><span class="sxs-lookup"><span data-stu-id="3d33f-143">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="3d33f-144">Al contrario, ogni NALU è preceduto da un campo di lunghezza, che fornisce la lunghezza del NALU in byte.</span><span class="sxs-lookup"><span data-stu-id="3d33f-144">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="3d33f-145">Le dimensioni del campo length possono variare, ma in genere sono 1, 2 o 4 byte.</span><span class="sxs-lookup"><span data-stu-id="3d33f-145">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="3d33f-146">Quando i codici di avvio non sono presenti nel flusso di bit, viene utilizzato il tipo di supporto seguente.</span><span class="sxs-lookup"><span data-stu-id="3d33f-146">When start codes are not present in the bitstream, the following media type is used.</span></span>



| <span data-ttu-id="3d33f-147">Label</span><span class="sxs-lookup"><span data-stu-id="3d33f-147">Label</span></span> | <span data-ttu-id="3d33f-148">Valore</span><span class="sxs-lookup"><span data-stu-id="3d33f-148">Value</span></span> |
|-------------|------------------------|
| <span data-ttu-id="3d33f-149">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="3d33f-149">Major type</span></span>  | <span data-ttu-id="3d33f-150">**MEDIATYPE \_ Video**</span><span class="sxs-lookup"><span data-stu-id="3d33f-150">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="3d33f-151">Subtype</span><span class="sxs-lookup"><span data-stu-id="3d33f-151">Subtype</span></span>     | <span data-ttu-id="3d33f-152">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="3d33f-152">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="3d33f-153">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="3d33f-153">Format type</span></span> | <span data-ttu-id="3d33f-154">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="3d33f-154">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="3d33f-155">Il blocco di formato è una [**struttura MPEG2VIDEOINFO.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)</span><span class="sxs-lookup"><span data-stu-id="3d33f-155">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="3d33f-156">Questa struttura deve essere compilata nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="3d33f-156">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="3d33f-157">**hdr:** struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) che descrive il flusso di bit.</span><span class="sxs-lookup"><span data-stu-id="3d33f-157">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="3d33f-158">Non è presente alcuna tabella dei colori dopo [**la parte BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) della struttura e **biClrUsed** deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3d33f-158">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="3d33f-159">**dwStartTimeCode:** non usato.</span><span class="sxs-lookup"><span data-stu-id="3d33f-159">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="3d33f-160">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="3d33f-160">Set to zero.</span></span>
-   <span data-ttu-id="3d33f-161">**cbSequenceHeader:** lunghezza in byte della matrice **dwSequenceHeader.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-161">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="3d33f-162">**dwProfile**: specifica il profilo H.264.</span><span class="sxs-lookup"><span data-stu-id="3d33f-162">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="3d33f-163">**dwLevel**: specifica il livello H.264.</span><span class="sxs-lookup"><span data-stu-id="3d33f-163">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="3d33f-164">**dwFlags:** numero di byte usati per il campo di lunghezza visualizzato prima di **ogni NALU.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-164">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="3d33f-165">Il campo length (Lunghezza) indica le dimensioni in byte dell'oggetto NALU seguente.</span><span class="sxs-lookup"><span data-stu-id="3d33f-165">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="3d33f-166">Ad esempio, se **dwFlags** è 4, ogni NALU è preceduta da un campo di lunghezza di 4 byte.</span><span class="sxs-lookup"><span data-stu-id="3d33f-166">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="3d33f-167">I valori validi sono 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="3d33f-167">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="3d33f-168">**dwSequenceHeader:** matrice di byte che può contenere set di parametri di sequenza (SPS) e set di parametri immagine (PPS).</span><span class="sxs-lookup"><span data-stu-id="3d33f-168">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="3d33f-169">Il contenitore MP4 può contenere set di parametri di sequenza (SPS) o set di parametri immagine (PPS) come unità NAL speciali nelle intestazioni dei file o in un flusso separato (distinto dal flusso video).</span><span class="sxs-lookup"><span data-stu-id="3d33f-169">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="3d33f-170">Quando viene stabilito il formato, il tipo di supporto può specificare unità NAL SPS e PPS nella matrice **dwSequenceHeader.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-170">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="3d33f-171">Se **cbSequenceHeader** è maggiore di zero, **dwSequenceHeader** è l'inizio di una matrice di byte contenente LEN SPS e PPS, delimitate da campi di lunghezza di 2 byte, tutti in ordine di byte di rete (big-endian).</span><span class="sxs-lookup"><span data-stu-id="3d33f-171">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="3d33f-172">È possibile avere sia SPS che PPS, solo uno di questi tipi o nessuno.</span><span class="sxs-lookup"><span data-stu-id="3d33f-172">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="3d33f-173">Il tipo effettivo di ogni NALU può essere determinato esaminando il campo del tipo di **\_ unità \_ nal** dell'unità NALU stessa.</span><span class="sxs-lookup"><span data-stu-id="3d33f-173">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="3d33f-174">Quando si usa questo tipo di supporto, ogni campione di supporti inizia all'inizio di un NALU e le unità NAL non si estendono sui campioni.</span><span class="sxs-lookup"><span data-stu-id="3d33f-174">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="3d33f-175">In questo modo il decodificatore può eseguire il ripristino dal danneggiamento dei dati o da campioni eliminati.</span><span class="sxs-lookup"><span data-stu-id="3d33f-175">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



