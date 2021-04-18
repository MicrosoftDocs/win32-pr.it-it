---
description: Con l'aumento dei dispositivi di archiviazione multimediale che richiedono formati audio compressi, le applicazioni devono identificare, descrivere e usare un'ampia gamma di nuovi contenuti audio codificati per la trasmissione di contenuto da PC a dispositivi come il ricevitore HDMI o DisplayPort.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Rappresentazione di formati per trasmissioni IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0700329aafe7e7bc0e09b532c1ac29b9957ca905
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304958"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a><span data-ttu-id="95067-103">Rappresentazione di formati per trasmissioni IEC 61937</span><span class="sxs-lookup"><span data-stu-id="95067-103">Representing Formats for IEC 61937 Transmissions</span></span>

<span data-ttu-id="95067-104">Con l'aumento dei dispositivi di archiviazione multimediale che richiedono formati audio compressi, le applicazioni devono identificare, descrivere e usare un'ampia gamma di nuovi contenuti audio codificati per la trasmissione di contenuto da PC a dispositivi come il ricevitore HDMI o DisplayPort.</span><span class="sxs-lookup"><span data-stu-id="95067-104">With the increase in media storage devices that require compressed audio formats, applications must identify, describe, and use a variety of new encoded audio content for transmitting content from PCs to devices such as HDMI or DisplayPort receiver.</span></span>

<span data-ttu-id="95067-105">Per rappresentare un flusso audio codificato da trasmettere tramite un'interfaccia compatibile con IEC 61937, un'applicazione deve fornire:</span><span class="sxs-lookup"><span data-stu-id="95067-105">To represent an encoded audio stream to be transmitted over an IEC 61937-compatible interface, an application must provide:</span></span>

-   <span data-ttu-id="95067-106">Caratteristiche di un flusso audio codificato da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="95067-106">The characteristics of an encoded audio stream to be transmitted.</span></span>

-   <span data-ttu-id="95067-107">Caratteristiche di un flusso audio decodificato nel dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="95067-107">The characteristics of a decoded audio stream on the target device.</span></span>

<span data-ttu-id="95067-108">In Windows Vista e nei sistemi operativi Windows precedenti, un'applicazione può dedurre il livello di qualità di un formato audio dal numero di canali, le dimensioni del campione e la velocità dati di un flusso audio che usa il formato.</span><span class="sxs-lookup"><span data-stu-id="95067-108">In Windows Vista and earlier Windows operating systems, an application can infer the quality level of an audio format from the number of channels, the sample size, and the data rate of an audio stream that uses the format.</span></span> <span data-ttu-id="95067-109">Per un formato PCM, queste informazioni sono disponibili dai membri **nChannels**, **nSamplesPerSec** e **nAvgBytesPerSec** della struttura **WAVEFORMATEX** che specifica il formato.</span><span class="sxs-lookup"><span data-stu-id="95067-109">For a PCM format, this information is available from the **nChannels**, **nSamplesPerSec**, and **nAvgBytesPerSec** members of the **WAVEFORMATEX** structure that specifies the format.</span></span> <span data-ttu-id="95067-110">Per un formato non PCM, questi tre membri sono stati requisiti per archiviare le informazioni sui dati compressi nel flusso audio.</span><span class="sxs-lookup"><span data-stu-id="95067-110">For a non-PCM format, these three members have been commandeered to store information about the compressed data in the audio stream.</span></span> <span data-ttu-id="95067-111">Quindi, la struttura **WAVEFORMATEX** non dispone di informazioni sul numero effettivo di canali, le dimensioni del campione e la velocità dati del flusso audio non PCM dopo che il flusso è stato decompresso e riprodotto.</span><span class="sxs-lookup"><span data-stu-id="95067-111">Thus, the **WAVEFORMATEX** structure lacks information about the effective number of channels, sample size, and data rate of the non-PCM audio stream after the stream is decompressed and played.</span></span> <span data-ttu-id="95067-112">In base alle informazioni contenute in questa struttura, un utente o un'applicazione potrebbe avere difficoltà a dedurre il livello di qualità del flusso non PCM.</span><span class="sxs-lookup"><span data-stu-id="95067-112">Based on the information in this structure, a user or an application might have difficulty inferring the quality level of the non-PCM stream.</span></span>

<span data-ttu-id="95067-113">Il **WAVEFORMATEX** è stato esteso alla struttura **WAVEFORMATEXTENSIBLE** per fornire le caratteristiche di flusso aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="95067-113">The **WAVEFORMATEX** was extended to the **WAVEFORMATEXTENSIBLE** structure to provide the extra stream characteristics.</span></span> <span data-ttu-id="95067-114">Questa struttura non è tuttavia adatta per la descrizione del flusso per trasmissioni IEC 61937, poiché è stata progettata per rappresentare un singolo set di caratteristiche e utilizzato per dati PCM non compressi e multicanale.</span><span class="sxs-lookup"><span data-stu-id="95067-114">However, this structure is also not adequate in describing the stream for IEC 61937 transmissions because it was intended to represent a single set of characteristics and used for uncompressed, multi-channel PCM data.</span></span>

<span data-ttu-id="95067-115">In Windows 7, il sistema operativo risolve questo problema fornendo supporto per una nuova struttura, **WAVEFORMATEXTENSIBLE \_ IEC61937** , che estende la struttura **WAVEFORMATEXTENSIBLE** per archiviare due set di caratteristiche di flusso audio: il formato audio codificato prima della trasmissione e le caratteristiche del flusso audio dopo che è stato decodificato.</span><span class="sxs-lookup"><span data-stu-id="95067-115">In Windows 7, the operating system addresses this problem by providing support for a new structure, **WAVEFORMATEXTENSIBLE\_IEC61937** which extends **WAVEFORMATEXTENSIBLE** structure to store two sets of audio stream characteristics: the encoded audio format before transmission and characteristics of the audio stream after it has been decoded.</span></span> <span data-ttu-id="95067-116">La nuova struttura specifica in modo esplicito il numero effettivo di canali, le dimensioni del campione e la velocità dati di un formato non PCM.</span><span class="sxs-lookup"><span data-stu-id="95067-116">The new structure explicitly specifies the effective number of channels, sample size, and data rate of a non-PCM format.</span></span> <span data-ttu-id="95067-117">Con queste informazioni, un'applicazione può dedurre il livello di qualità del flusso non PCM dopo che è stato decompresso e riprodotto.</span><span class="sxs-lookup"><span data-stu-id="95067-117">With this information, an application can infer the quality level of the non-PCM stream after it is decompressed and played.</span></span>

<span data-ttu-id="95067-118">La struttura **WAVEFORMATEXTENSIBLE \_ IEC61937** è dichiarata nell'intestazione KsMedia. h inclusa in Windows 7 SDK.</span><span class="sxs-lookup"><span data-stu-id="95067-118">The **WAVEFORMATEXTENSIBLE\_IEC61937** structure is declared in the KsMedia.h header included with the Windows 7 SDK.</span></span> <span data-ttu-id="95067-119">Il membro **FormatExt** è la struttura **WAVEFORMATEXTENSIBLE** che archivia le caratteristiche del flusso da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="95067-119">The **FormatExt** member is the **WAVEFORMATEXTENSIBLE** structure that stores the characteristics of the stream to be transmitted.</span></span> <span data-ttu-id="95067-120">Il **formato** membro della struttura **WAVEFORMATEXTENSIBLE** è la struttura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="95067-120">The **Format** member of the **WAVEFORMATEXTENSIBLE** structure is the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="95067-121">Il contenuto di **WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE** indica a un'applicazione se la struttura può essere interpretata come una struttura **WAVEFORMATEXTENSIBLE \_ IEC61937** .</span><span class="sxs-lookup"><span data-stu-id="95067-121">The contents of this **WAVEFORMATEX** and **WAVEFORMATEXTENSIBLE** indicate to an application whether the structure can be interpreted as a **WAVEFORMATEXTENSIBLE\_IEC61937** structure.</span></span> <span data-ttu-id="95067-122">Per una **struttura \_ IEC61937 di WAVEFORMATEXTENSIBLE** :</span><span class="sxs-lookup"><span data-stu-id="95067-122">For a **WAVEFORMATEXTENSIBLE\_IEC61937** structure:</span></span>

-   <span data-ttu-id="95067-123">Il membro **wFormatTag** di **WAVEFORMATEX** deve contenere il \_ formato Wave \_ estendibile ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).</span><span class="sxs-lookup"><span data-stu-id="95067-123">The **wFormatTag** member of **WAVEFORMATEX** must contain WAVE\_FORMAT\_EXTENSIBLE (`FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE`).</span></span>

-   <span data-ttu-id="95067-124">Il membro del **sottoformato** della struttura **WAVEFORMATEXTENSIBLE** specifica il GUID del formato codificato da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="95067-124">The **SubFormat** member of the **WAVEFORMATEXTENSIBLE** structure specifies the GUID of the encoded format to be transmitted.</span></span> <span data-ttu-id="95067-125">Ad esempio, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indica il formato Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="95067-125">For example, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indicates the Dolby Digital Plus format.</span></span> <span data-ttu-id="95067-126">Per i GUID supportati, vedere GUID di sottoformato.</span><span class="sxs-lookup"><span data-stu-id="95067-126">For the supported GUIDs, see SubFormat GUIDs.</span></span>

-   <span data-ttu-id="95067-127">Le dimensioni indicate dal membro **cbSize** di WAVEFORMATEX sono 34 byte.</span><span class="sxs-lookup"><span data-stu-id="95067-127">The size indicated by **cbSize** member of the WAVEFORMATEX is 34 bytes.</span></span> <span data-ttu-id="95067-128">(`FormatExt.Format.cbSize = 34`).</span><span class="sxs-lookup"><span data-stu-id="95067-128">(`FormatExt.Format.cbSize = 34`).</span></span> <span data-ttu-id="95067-129">Le dimensioni totali di **WAVEFORMATEXTENSIBLE \_ IEC61937** sono pari a 52 byte.</span><span class="sxs-lookup"><span data-stu-id="95067-129">The total size of **WAVEFORMATEXTENSIBLE\_IEC61937** is 52 bytes.</span></span>

<span data-ttu-id="95067-130">I membri **dwEncodedSamplesPerSec**, **dwEncodedChannelCount** e **dwAverageBytesPerSec** di **WAVEFORMATEXTENSIBLE \_ IEC61937** descrivono la frequenza di campionamento, il numero di canali e la velocità in bit, in byte, del flusso audio dopo che è stato decodificato.</span><span class="sxs-lookup"><span data-stu-id="95067-130">The **dwEncodedSamplesPerSec**, **dwEncodedChannelCount**, and **dwAverageBytesPerSec** members of **WAVEFORMATEXTENSIBLE\_IEC61937** describe the sampling rate, number of channels, and bit rate in bytes of the stream of the audio stream after it has been decoded.</span></span>

## <a name="subformat-guids"></a><span data-ttu-id="95067-131">GUID di sottoforma</span><span class="sxs-lookup"><span data-stu-id="95067-131">SubFormat GUIDs</span></span>

<span data-ttu-id="95067-132">In Windows 7, l'intestazione KsMedia. h contiene le definizioni dei GUID di sottoformato per i formati audio compressi definiti da CEA-861-D.</span><span class="sxs-lookup"><span data-stu-id="95067-132">In Windows 7, the KsMedia.h header contains definitions for the SubFormat GUIDs for the compressed audio formats defined by CEA-861-D.</span></span> <span data-ttu-id="95067-133">I GUID vengono specificati nel membro subformat di **WAVEFORMATEXTENSIBLE**, specificato nel membro **FormatExt** della struttura **WAVEFORMATEXTENSIBLE \_ IEC61937** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).</span><span class="sxs-lookup"><span data-stu-id="95067-133">The GUIDs are specified in the SubFormat member of the **WAVEFORMATEXTENSIBLE**, specified in the **FormatExt** member of the **WAVEFORMATEXTENSIBLE\_IEC61937** structure (`WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat`).</span></span>

<span data-ttu-id="95067-134">Nella tabella seguente sono elencati i GUID per i formati audio compressi disponibili come formati audio con codifica IEC 61937 standard.</span><span class="sxs-lookup"><span data-stu-id="95067-134">The GUIDs for the compressed audio formats that are available as standard IEC 61937 encoded audio formats are listed in the following table.</span></span> <span data-ttu-id="95067-135">Questi formati sono simili alle rappresentazioni del codice attivo esistente 3 (AC-3) e del formato DTS (Digital Theater Sound) in Windows.</span><span class="sxs-lookup"><span data-stu-id="95067-135">These formats are similar to the existing Active Coding 3 (AC-3) and Digital Theater Sound (DTS) formats representations in Windows.</span></span>



| <span data-ttu-id="95067-136">Tipo CEA 861</span><span class="sxs-lookup"><span data-stu-id="95067-136">CEA 861 Type</span></span> | <span data-ttu-id="95067-137">GUID del sottoformato</span><span class="sxs-lookup"><span data-stu-id="95067-137">SubFormat GUID</span></span>                                                                                                          | <span data-ttu-id="95067-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95067-138">Description</span></span>                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="95067-139">0x00</span><span class="sxs-lookup"><span data-stu-id="95067-139">0x00</span></span>         |                                                                                                                         | <span data-ttu-id="95067-140">Fare riferimento al flusso.</span><span class="sxs-lookup"><span data-stu-id="95067-140">Refer to the stream.</span></span>                         |
| <span data-ttu-id="95067-141">0x01</span><span class="sxs-lookup"><span data-stu-id="95067-141">0x01</span></span>         | <span data-ttu-id="95067-142">00000000-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-142">00000000-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-143">\_sottotipo KSDATAFORMAT \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="95067-143">KSDATAFORMAT\_SUBTYPE\_WAVEFORMATEX</span></span><br/>                          | <span data-ttu-id="95067-144">PCM IEC 60958</span><span class="sxs-lookup"><span data-stu-id="95067-144">IEC 60958 PCM</span></span>                                |
| <span data-ttu-id="95067-145">0x02</span><span class="sxs-lookup"><span data-stu-id="95067-145">0x02</span></span>         | <span data-ttu-id="95067-146">00000092-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-146">00000092-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-147">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital</span><span class="sxs-lookup"><span data-stu-id="95067-147">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL</span></span><br/>              | <span data-ttu-id="95067-148">AC-3</span><span class="sxs-lookup"><span data-stu-id="95067-148">AC-3</span></span>                                         |
| <span data-ttu-id="95067-149">0x03</span><span class="sxs-lookup"><span data-stu-id="95067-149">0x03</span></span>         | <span data-ttu-id="95067-150">00000003-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-150">00000003-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-151">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ MPEG1</span><span class="sxs-lookup"><span data-stu-id="95067-151">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG1</span></span><br/>                       | <span data-ttu-id="95067-152">MPEG-1 (livello 1 & 2)</span><span class="sxs-lookup"><span data-stu-id="95067-152">MPEG-1 (Layer 1 & 2)</span></span>                         |
| <span data-ttu-id="95067-153">0x04</span><span class="sxs-lookup"><span data-stu-id="95067-153">0x04</span></span>         | <span data-ttu-id="95067-154">00000004-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-154">00000004-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-155">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ MPEG3</span><span class="sxs-lookup"><span data-stu-id="95067-155">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG3</span></span><br/>                       | <span data-ttu-id="95067-156">MPEG-3 (livello 3)</span><span class="sxs-lookup"><span data-stu-id="95067-156">MPEG-3 (Layer 3)</span></span>                             |
| <span data-ttu-id="95067-157">0x05</span><span class="sxs-lookup"><span data-stu-id="95067-157">0x05</span></span>         | <span data-ttu-id="95067-158">00000005-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-158">00000005-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-159">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="95067-159">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG2</span></span> <br/>                      | <span data-ttu-id="95067-160">MPEG-2 (multicanale)</span><span class="sxs-lookup"><span data-stu-id="95067-160">MPEG-2(multichannel)</span></span>                         |
| <span data-ttu-id="95067-161">0x06</span><span class="sxs-lookup"><span data-stu-id="95067-161">0x06</span></span>         | <span data-ttu-id="95067-162">00000006-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-162">00000006-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-163">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ AAC</span><span class="sxs-lookup"><span data-stu-id="95067-163">KSDATAFORMAT\_SUBTYPE\_IEC61937\_AAC</span></span><br/>                         | <span data-ttu-id="95067-164">Codifica audio avanzata (MPEG-2/4 AAC in ADTS)</span><span class="sxs-lookup"><span data-stu-id="95067-164">Advanced Audio Coding (MPEG-2/4 AAC in ADTS)</span></span> |
| <span data-ttu-id="95067-165">0x07</span><span class="sxs-lookup"><span data-stu-id="95067-165">0x07</span></span>         | <span data-ttu-id="95067-166">00000008-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-166">00000008-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-167">KSDATAFORMAT \_ sottotipo \_ IEC61937 \_ DTS</span><span class="sxs-lookup"><span data-stu-id="95067-167">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS</span></span><br/>                         | <span data-ttu-id="95067-168">DTS</span><span class="sxs-lookup"><span data-stu-id="95067-168">DTS</span></span>                                          |
| <span data-ttu-id="95067-169">0x0A</span><span class="sxs-lookup"><span data-stu-id="95067-169">0x0a</span></span>         | <span data-ttu-id="95067-170">0000000a-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-170">0000000a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-171">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital \_ Plus</span><span class="sxs-lookup"><span data-stu-id="95067-171">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS</span></span><br/>        | <span data-ttu-id="95067-172">Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="95067-172">Dolby Digital Plus</span></span>                           |
| <span data-ttu-id="95067-173">0x0A</span><span class="sxs-lookup"><span data-stu-id="95067-173">0x0a</span></span>         | <span data-ttu-id="95067-174">0000010a-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-174">0000010a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-175">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital \_ Plus \_ ATMOS</span><span class="sxs-lookup"><span data-stu-id="95067-175">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS\_ATMOS</span></span><br/> | <span data-ttu-id="95067-176">Dolby Atmos codificato con Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="95067-176">Dolby Atmos encoded with Dolby Digital Plus</span></span>  |
| <span data-ttu-id="95067-177">0x0F</span><span class="sxs-lookup"><span data-stu-id="95067-177">0x0f</span></span>         |                                                                                                                         | <span data-ttu-id="95067-178">Riservato non usato</span><span class="sxs-lookup"><span data-stu-id="95067-178">Unused Reserved</span></span>                              |



 

<span data-ttu-id="95067-179">Nella tabella seguente sono elencati i GUID per i formati audio compressi trasmessi nei pacchetti di esempio audio ad alta velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="95067-179">The GUIDs for the compressed audio formats that are transmitted in high bit-rate audio sample packets are listed in the following table.</span></span>



| <span data-ttu-id="95067-180">Tipo CEA 861</span><span class="sxs-lookup"><span data-stu-id="95067-180">CEA 861 Type</span></span> | <span data-ttu-id="95067-181">GUID del sottoformato</span><span class="sxs-lookup"><span data-stu-id="95067-181">SubFormat GUID</span></span>                                                                                           | <span data-ttu-id="95067-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95067-182">Description</span></span>                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95067-183">0x0B</span><span class="sxs-lookup"><span data-stu-id="95067-183">0x0b</span></span>         | <span data-ttu-id="95067-184">0000000b-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-184">0000000b-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-185">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ DTS \_ HD</span><span class="sxs-lookup"><span data-stu-id="95067-185">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS\_HD</span></span><br/>      | <span data-ttu-id="95067-186">DTS-HD (24 bit, 96Khz)</span><span class="sxs-lookup"><span data-stu-id="95067-186">DTS-HD (24-bit, 96Khz)</span></span>                                                                                                          |
| <span data-ttu-id="95067-187">0x0c</span><span class="sxs-lookup"><span data-stu-id="95067-187">0x0c</span></span>         | <span data-ttu-id="95067-188">0000000c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-188">0000000c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-189">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ MLP</span><span class="sxs-lookup"><span data-stu-id="95067-189">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MLP</span></span><br/>   | <span data-ttu-id="95067-190">Dolby MAT 1,0:</span><span class="sxs-lookup"><span data-stu-id="95067-190">Dolby MAT 1.0:</span></span><br/> <span data-ttu-id="95067-191">Dolby TrueHD (MLP-Meridian Lossless Packing) – 192KHz a 24 bit/fino a 18 Mbps, 8 canali</span><span class="sxs-lookup"><span data-stu-id="95067-191">Dolby TrueHD (MLP – Meridian Lossless Packing) – 24-bit 192KHz/up to 18 Mbps, 8 channels)</span></span> <br/> |
| <span data-ttu-id="95067-192">0x0c</span><span class="sxs-lookup"><span data-stu-id="95067-192">0x0c</span></span>         | <span data-ttu-id="95067-193">0000010c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-193">0000010c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-194">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ MAT20</span><span class="sxs-lookup"><span data-stu-id="95067-194">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT20</span></span><br/> | <span data-ttu-id="95067-195">Dolby MAT 2,0:</span><span class="sxs-lookup"><span data-stu-id="95067-195">Dolby MAT 2.0:</span></span> <br/> <span data-ttu-id="95067-196">Dolby TrueHD – 192KHz a 24 bit/fino a 18 Mbps, 8 canali o LPCM fino a 24 Mbps.</span><span class="sxs-lookup"><span data-stu-id="95067-196">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="95067-197">0x0c</span><span class="sxs-lookup"><span data-stu-id="95067-197">0x0c</span></span>         | <span data-ttu-id="95067-198">0000030c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-198">0000030c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-199">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ MAT21</span><span class="sxs-lookup"><span data-stu-id="95067-199">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT21</span></span><br/> | <span data-ttu-id="95067-200">Dolby MAT 2,1:</span><span class="sxs-lookup"><span data-stu-id="95067-200">Dolby MAT 2.1:</span></span> <br/> <span data-ttu-id="95067-201">Dolby TrueHD – 192KHz a 24 bit/fino a 18 Mbps, 8 canali o LPCM fino a 24 Mbps.</span><span class="sxs-lookup"><span data-stu-id="95067-201">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="95067-202">0x0E</span><span class="sxs-lookup"><span data-stu-id="95067-202">0x0e</span></span>         | <span data-ttu-id="95067-203">00000164-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-203">00000164-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-204">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ WMA \_ Pro</span><span class="sxs-lookup"><span data-stu-id="95067-204">KSDATAFORMAT\_SUBTYPE\_IEC61937\_WMA\_PRO</span></span><br/>     | <span data-ttu-id="95067-205">Windows Media Audio (WMA) Pro</span><span class="sxs-lookup"><span data-stu-id="95067-205">Windows Media Audio (WMA) Pro</span></span>                                                                                                   |



 

<span data-ttu-id="95067-206">Il driver di classe audio HD fornito da Microsoft supporta i formati PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT (MLP).</span><span class="sxs-lookup"><span data-stu-id="95067-206">Microsoft-provided HD Audio class driver supports PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT(MLP) formats.</span></span> <span data-ttu-id="95067-207">Nella tabella seguente sono elencati i GUID per i formati audio compressi che non sono supportati dal driver della classe audio HD e possono essere implementati da soluzioni di terze parti.</span><span class="sxs-lookup"><span data-stu-id="95067-207">The GUIDs for the compressed audio formats that are not supported by the HD audio class driver and can be implemented by third-party solutions are listed in the following table.</span></span>



| <span data-ttu-id="95067-208">Tipo CEA 861</span><span class="sxs-lookup"><span data-stu-id="95067-208">CEA 861 Type</span></span> | <span data-ttu-id="95067-209">GUID del sottoformato</span><span class="sxs-lookup"><span data-stu-id="95067-209">SubFormat GUID</span></span>                                                                                              | <span data-ttu-id="95067-210">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95067-210">Description</span></span>                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="95067-211">0x08</span><span class="sxs-lookup"><span data-stu-id="95067-211">0x08</span></span>         | <span data-ttu-id="95067-212">00000008-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-212">00000008-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-213">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ ATRAC</span><span class="sxs-lookup"><span data-stu-id="95067-213">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ATRAC</span></span><br/>           | <span data-ttu-id="95067-214">Codifica acustica Adaptive Transform (ATRAC)</span><span class="sxs-lookup"><span data-stu-id="95067-214">Adaptive Transform Acoustic Coding (ATRAC)</span></span>                                     |
| <span data-ttu-id="95067-215">0x09</span><span class="sxs-lookup"><span data-stu-id="95067-215">0x09</span></span>         | <span data-ttu-id="95067-216">00000009-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-216">00000009-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-217">KSDATAFORMAT \_ sottotipo \_ IEC61937 \_ One \_ bit \_ audio</span><span class="sxs-lookup"><span data-stu-id="95067-217">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ONE\_BIT\_AUDIO</span></span><br/> | <span data-ttu-id="95067-218">Audio One-Bit</span><span class="sxs-lookup"><span data-stu-id="95067-218">One-Bit Audio</span></span>                                                                  |
| <span data-ttu-id="95067-219">0x0D</span><span class="sxs-lookup"><span data-stu-id="95067-219">0x0d</span></span>         | <span data-ttu-id="95067-220">0000000d-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="95067-220">0000000d-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="95067-221">\_Sottotipo KSDATAFORMAT \_ IEC61937 \_ DST</span><span class="sxs-lookup"><span data-stu-id="95067-221">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DST</span></span><br/>             | <span data-ttu-id="95067-222">Direct Stream Transport (DST): la DSD compressa Lossless (Direct Stream Digital).</span><span class="sxs-lookup"><span data-stu-id="95067-222">Direct Stream Transport (DST)—lossless compressed DSD (Direct Stream Digital).</span></span> |



 

## <a name="dolby-digital-plus-format"></a><span data-ttu-id="95067-223">Formato Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="95067-223">Dolby Digital Plus Format</span></span>

<span data-ttu-id="95067-224">Quando il contenuto Dolby Digital Plus viene trasmesso tramite IEC 60958, la frequenza di campionamento del collegamento deve essere quattro volte la frequenza di campionamento del contenuto.</span><span class="sxs-lookup"><span data-stu-id="95067-224">When Dolby Digital Plus content is transmitted over IEC 60958, the link-sampling rate must be four times the sampling rate of the content.</span></span> <span data-ttu-id="95067-225">Dolby Digital Plus supporta la frequenza di campionamento del contenuto di 32 KHz, 44,1 KHz e 48 KHz.</span><span class="sxs-lookup"><span data-stu-id="95067-225">Dolby Digital Plus supports content sample rates of 32 KHz, 44.1 KHz, and 48 KHz.</span></span> <span data-ttu-id="95067-226">Le interfacce come HDMI non supportano 128 KHz (32 KHz x 4), pertanto è possibile supportare solo le frequenze di campionamento del contenuto 44,1 e 48 KHz.</span><span class="sxs-lookup"><span data-stu-id="95067-226">Interfaces such as HDMI do not support 128 KHz (32 KHz x 4), so only 44.1 and 48 KHz content sample rates can be supported.</span></span>

<span data-ttu-id="95067-227">Nell'esempio seguente vengono illustrati i valori impostati da un'applicazione nella \_ struttura IEC61937 di WAVEFORMATEXTENSIBLE per rappresentare il formato Dolby Digital Plus a una frequenza di campionamento del contenuto di 48 kHz.</span><span class="sxs-lookup"><span data-stu-id="95067-227">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby Digital Plus format at a content sample rate of 48 KHz are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a><span data-ttu-id="95067-228">Dolby TrueHD (MAT)</span><span class="sxs-lookup"><span data-stu-id="95067-228">Dolby TrueHD (MAT)</span></span>

<span data-ttu-id="95067-229">Il contenuto Dolby TrueHD viene trasmesso tramite IEC 60958 a 176,4 kHz/8 canali (che richiedono una frequenza di fotogrammi IEC 60958 pari a 705,6 kHz) per le frequenze di esempio del contenuto di 44,1, 88,2 e 176,4 kHz e 192 kHz/8 canali (che richiedono una frequenza dei fotogrammi IEC 60958 di 768 kHz) per le frequenze di esempio del contenuto di 48, 96 e 192 kHz.</span><span class="sxs-lookup"><span data-stu-id="95067-229">Dolby TrueHD content is transmitted over IEC 60958 at 176.4 kHz / 8 channels (requiring an IEC 60958 frame rate of 705.6 kHz) for content sample rates of 44.1, 88.2 and 176.4 kHz, and 192 kHz / 8 channels (requiring an IEC 60958 frame rate of 768 kHz) for content sample rates of 48, 96 and 192 kHz.</span></span>

<span data-ttu-id="95067-230">Gli esempi seguenti illustrano i valori impostati da un'applicazione nella \_ struttura IEC61937 di WAVEFORMATEXTENSIBLE per rappresentare Dolby TrueHD a una frequenza di campionamento del contenuto di 96 kHz.</span><span class="sxs-lookup"><span data-stu-id="95067-230">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby TrueHD at a content sample rate of 96 KHz are shown in the following examples.</span></span>

<span data-ttu-id="95067-231">Dolby MAT 1,0</span><span class="sxs-lookup"><span data-stu-id="95067-231">Dolby MAT 1.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="95067-232">Dolby MAT 2,0</span><span class="sxs-lookup"><span data-stu-id="95067-232">Dolby MAT 2.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="95067-233">Dolby MAT 2,1</span><span class="sxs-lookup"><span data-stu-id="95067-233">Dolby MAT 2.1</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> <span data-ttu-id="95067-234">Il supporto per una versione di Dolby MAT non implica il supporto per Dolby MAT con un numero di versione inferiore.</span><span class="sxs-lookup"><span data-stu-id="95067-234">Support for one version of Dolby MAT does not imply support for Dolby MAT with a lower version number.</span></span> <span data-ttu-id="95067-235">Poiché Dolby MAT 2,1 è compatibile con le versioni precedenti di Dolby MAT, un driver di classe che indica il supporto per Dolby MAT 2,1 indicherà in genere anche il supporto per Dolby MAT 2,0 e Dolby MAT 1,0, usando una \_ struttura WAVEFORMATEXTENSIBLE IEC61937 separata per ogni versione.</span><span class="sxs-lookup"><span data-stu-id="95067-235">Since Dolby MAT 2.1 is backwards compatible with previous versions of Dolby MAT, a class driver that indicates support for Dolby MAT 2.1 will typically also indicate support for Dolby MAT 2.0 and Dolby MAT 1.0, using a separate WAVEFORMATEXTENSIBLE\_IEC61937 structure for each version.</span></span>

 

## <a name="wma-pro"></a><span data-ttu-id="95067-236">WMA Pro</span><span class="sxs-lookup"><span data-stu-id="95067-236">WMA Pro</span></span>

<span data-ttu-id="95067-237">Il contenuto audio WMA Pro può essere codificato in uno dei quattro profili elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="95067-237">WMA Pro audio content can be encoded in one of the four profiles listed in the following table.</span></span>



| <span data-ttu-id="95067-238">Profilo</span><span class="sxs-lookup"><span data-stu-id="95067-238">Profile</span></span> | <span data-ttu-id="95067-239">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="95067-239">Property - Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="95067-240">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95067-240">Description</span></span>                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95067-241">M0</span><span class="sxs-lookup"><span data-stu-id="95067-241">M0</span></span>      | <span data-ttu-id="95067-242">Velocità in bit massima-192000 BPS</span><span class="sxs-lookup"><span data-stu-id="95067-242">Maximum bit rate – 192000 bps</span></span> <br/> <span data-ttu-id="95067-243">Frequenza di campionamento massima-48 KHz</span><span class="sxs-lookup"><span data-stu-id="95067-243">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="95067-244">Numero massimo di canali-2</span><span class="sxs-lookup"><span data-stu-id="95067-244">Maximum channel count – 2</span></span> <br/> <span data-ttu-id="95067-245">Dimensioni massime buffer-600 \* bit 1024</span><span class="sxs-lookup"><span data-stu-id="95067-245">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="95067-246">Numero massimo di campioni per fotogramma-2048</span><span class="sxs-lookup"><span data-stu-id="95067-246">Maximum samples per frame – 2048</span></span> <br/> <span data-ttu-id="95067-247">Numero massimo di bit per fotogramma-655536</span><span class="sxs-lookup"><span data-stu-id="95067-247">Maximum bits per frame - 655536</span></span><br/>   | <span data-ttu-id="95067-248">Consigliato per la musica e lo streaming in modalità radio.</span><span class="sxs-lookup"><span data-stu-id="95067-248">Recommended for over-the-air music and streaming.</span></span><br/> <span data-ttu-id="95067-249">La velocità in bit massima in un frame audio è 1536000 bps.</span><span class="sxs-lookup"><span data-stu-id="95067-249">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/>          |
| <span data-ttu-id="95067-250">M1</span><span class="sxs-lookup"><span data-stu-id="95067-250">M1</span></span>      | <span data-ttu-id="95067-251">Velocità in bit massima-385000 BPS</span><span class="sxs-lookup"><span data-stu-id="95067-251">Maximum bit rate – 385000 bps</span></span> <br/> <span data-ttu-id="95067-252">Frequenza di campionamento massima-48 KHz</span><span class="sxs-lookup"><span data-stu-id="95067-252">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="95067-253">Numero massimo di canali-6</span><span class="sxs-lookup"><span data-stu-id="95067-253">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="95067-254">Dimensioni massime buffer-600 \* bit 1024</span><span class="sxs-lookup"><span data-stu-id="95067-254">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="95067-255">Numero massimo di campioni per fotogramma-4096</span><span class="sxs-lookup"><span data-stu-id="95067-255">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="95067-256">Numero massimo di bit per fotogramma-131072</span><span class="sxs-lookup"><span data-stu-id="95067-256">Maximum bits per frame - 131072</span></span><br/>   | <span data-ttu-id="95067-257">Consigliato per i filmati con definizione standard del suono surround.</span><span class="sxs-lookup"><span data-stu-id="95067-257">Recommended for surround-sound standard definition movies.</span></span><br/> <span data-ttu-id="95067-258">La velocità in bit massima in un frame audio è 1536000 bps.</span><span class="sxs-lookup"><span data-stu-id="95067-258">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/> |
| <span data-ttu-id="95067-259">M2</span><span class="sxs-lookup"><span data-stu-id="95067-259">M2</span></span>      | <span data-ttu-id="95067-260">Velocità in bit massima-769000 BPS</span><span class="sxs-lookup"><span data-stu-id="95067-260">Maximum bit rate – 769000 bps</span></span> <br/> <span data-ttu-id="95067-261">Frequenza di campionamento massima-96 KHz</span><span class="sxs-lookup"><span data-stu-id="95067-261">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="95067-262">Numero massimo di canali-6</span><span class="sxs-lookup"><span data-stu-id="95067-262">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="95067-263">Dimensioni massime buffer-1200 \* bit 1024</span><span class="sxs-lookup"><span data-stu-id="95067-263">Maximum buffer size – 1200\*1024 bits</span></span> <br/> <span data-ttu-id="95067-264">Numero massimo di campioni per fotogramma-4096</span><span class="sxs-lookup"><span data-stu-id="95067-264">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="95067-265">Numero massimo di bit per fotogramma-131072</span><span class="sxs-lookup"><span data-stu-id="95067-265">Maximum bits per frame - 131072</span></span><br/>  | <span data-ttu-id="95067-266">Consigliato per i filmati ad alta definizione audio surround.</span><span class="sxs-lookup"><span data-stu-id="95067-266">Recommended for surround-sound high definition movies.</span></span><br/> <span data-ttu-id="95067-267">La frequenza massima in un frame audio è 3072000 bps.</span><span class="sxs-lookup"><span data-stu-id="95067-267">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>         |
| <span data-ttu-id="95067-268">M3</span><span class="sxs-lookup"><span data-stu-id="95067-268">M3</span></span>      | <span data-ttu-id="95067-269">Velocità in bit massima-3 milioni BPS</span><span class="sxs-lookup"><span data-stu-id="95067-269">Maximum bit rate – 3000000 bps</span></span> <br/> <span data-ttu-id="95067-270">Frequenza di campionamento massima-96 KHz</span><span class="sxs-lookup"><span data-stu-id="95067-270">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="95067-271">Numero massimo di canali-8</span><span class="sxs-lookup"><span data-stu-id="95067-271">Maximum channel count – 8</span></span> <br/> <span data-ttu-id="95067-272">Dimensioni massime buffer-2400 \* bit 1024</span><span class="sxs-lookup"><span data-stu-id="95067-272">Maximum buffer size – 2400\*1024 bits</span></span> <br/> <span data-ttu-id="95067-273">Numero massimo di campioni per fotogramma-4096</span><span class="sxs-lookup"><span data-stu-id="95067-273">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="95067-274">Numero massimo di bit per fotogramma-131072</span><span class="sxs-lookup"><span data-stu-id="95067-274">Maximum bits per frame - 131072</span></span><br/> | <span data-ttu-id="95067-275">Consigliato per Digital Theater.</span><span class="sxs-lookup"><span data-stu-id="95067-275">Recommended for digital theater.</span></span><br/> <span data-ttu-id="95067-276">La frequenza massima in un frame audio è 3072000 bps.</span><span class="sxs-lookup"><span data-stu-id="95067-276">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>                               |



 

<span data-ttu-id="95067-277">I profili M0 e M1 rientrano in un flusso IEC 60958 a 48 KHz/16 bit/stereo (1536000 BPS).</span><span class="sxs-lookup"><span data-stu-id="95067-277">The M0 and M1 profiles fit into a 48 KHz/16 bit/Stereo (1536000 bps) IEC 60958 stream.</span></span> <span data-ttu-id="95067-278">I profili m2 e M3 rientrano in un flusso IEC 60958 a 96 KHz/16 bit/stereo (3072000 BPS).</span><span class="sxs-lookup"><span data-stu-id="95067-278">The M2 and M3 profiles fit into a 96 KHz/16 bit/Stereo (3072000 bps) IEC 60958 stream.</span></span>

<span data-ttu-id="95067-279">Nell'esempio seguente vengono illustrati i valori impostati da un'applicazione nella \_ struttura IEC61937 di WAVEFORMATEXTENSIBLE per rappresentare WMA Pro come profilo m2.</span><span class="sxs-lookup"><span data-stu-id="95067-279">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent WMA Pro as an M2 profile are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a><span data-ttu-id="95067-280">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95067-280">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95067-281">Formati di dispositivo</span><span class="sxs-lookup"><span data-stu-id="95067-281">Device Formats</span></span>](device-formats.md)
</dt> </dl>

 

 




