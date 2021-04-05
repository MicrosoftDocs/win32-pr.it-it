---
description: Formati YUV a 8 bit consigliati per il rendering video
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formati YUV a 8 bit consigliati per il rendering video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753890"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a><span data-ttu-id="2a257-103">Formati YUV a 8 bit consigliati per il rendering video</span><span class="sxs-lookup"><span data-stu-id="2a257-103">Recommended 8-Bit YUV Formats for Video Rendering</span></span>

<span data-ttu-id="2a257-104">Gary Sullivan e Stephen Estrop</span><span class="sxs-lookup"><span data-stu-id="2a257-104">Gary Sullivan and Stephen Estrop</span></span>

<span data-ttu-id="2a257-105">Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="2a257-105">Microsoft Corporation</span></span>

<span data-ttu-id="2a257-106">Aprile 2002, aggiornato il 2008 novembre</span><span class="sxs-lookup"><span data-stu-id="2a257-106">April 2002, updated November 2008</span></span>

<span data-ttu-id="2a257-107">Questo argomento descrive i formati di colore YUV a 8 bit consigliati per il rendering video nel sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="2a257-107">This topic describes the 8-bit YUV color formats that are recommended for video rendering in the Windows operating system.</span></span> <span data-ttu-id="2a257-108">Questo articolo presenta le tecniche per la conversione tra formati YUV e RGB e fornisce anche tecniche per il campionamento dei formati YUV.</span><span class="sxs-lookup"><span data-stu-id="2a257-108">This article presents techniques for converting between YUV and RGB formats, and also provides techniques for upsampling YUV formats.</span></span> <span data-ttu-id="2a257-109">Questo articolo è destinato agli utenti che usano la decodifica video YUV o il rendering in Windows.</span><span class="sxs-lookup"><span data-stu-id="2a257-109">This article is intended for anyone working with YUV video decoding or rendering in Windows.</span></span>

## <a name="introduction"></a><span data-ttu-id="2a257-110">Introduzione</span><span class="sxs-lookup"><span data-stu-id="2a257-110">Introduction</span></span>

<span data-ttu-id="2a257-111">Molti formati YUV sono definiti in tutto il settore video.</span><span class="sxs-lookup"><span data-stu-id="2a257-111">Numerous YUV formats are defined throughout the video industry.</span></span> <span data-ttu-id="2a257-112">Questo articolo identifica i formati YUV a 8 bit consigliati per il rendering video in Windows.</span><span class="sxs-lookup"><span data-stu-id="2a257-112">This article identifies the 8-bit YUV formats that are recommended for video rendering in Windows.</span></span> <span data-ttu-id="2a257-113">I fornitori di decodificatori e i fornitori di visualizzazioni sono invitati a supportare i formati descritti in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="2a257-113">Decoder vendors and display vendors are encouraged to support the formats described in this article.</span></span> <span data-ttu-id="2a257-114">Questo articolo non riguarda altri usi di colore YUV, ad esempio la fotografia continua.</span><span class="sxs-lookup"><span data-stu-id="2a257-114">This article does not address other uses of YUV color, such as still photography.</span></span>

<span data-ttu-id="2a257-115">I formati descritti in questo articolo usano tutti la posizione di 8 bit per pixel per codificare il canale Y (detto anche canale luma) e usano 8 bit per campione per codificare ogni esempio di Chroma U o V.</span><span class="sxs-lookup"><span data-stu-id="2a257-115">The formats described in this article all use 8 bits per pixel location to encode the Y channel (also called the luma channel), and use 8 bits per sample to encode each U or V chroma sample.</span></span> <span data-ttu-id="2a257-116">Tuttavia, la maggior parte dei formati YUV usa una media inferiore a 24 bit per pixel, perché contengono un minor numero di campioni di u e V rispetto a Y. Questo articolo non copre i formati YUV con canali Y a 10 bit o superiori.</span><span class="sxs-lookup"><span data-stu-id="2a257-116">However, most YUV formats use fewer than 24 bits per pixel on average, because they contain fewer samples of U and V than of Y. This article does not cover YUV formats with 10-bit or higher Y channels.</span></span>

> [!Note]  
> <span data-ttu-id="2a257-117">Ai fini di questo articolo, il termine U è equivalente a CB e il termine V è equivalente a CR.</span><span class="sxs-lookup"><span data-stu-id="2a257-117">For the purposes of this article, the term U is equivalent to Cb, and the term V is equivalent to Cr.</span></span>

 

<span data-ttu-id="2a257-118">Questo articolo include gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a257-118">This article covers the following topics:</span></span>

-   <span data-ttu-id="2a257-119">[Campionamento YUV](#yuv-sampling).</span><span class="sxs-lookup"><span data-stu-id="2a257-119">[YUV Sampling](#yuv-sampling).</span></span> <span data-ttu-id="2a257-120">Descrive le tecniche di campionamento YUV più comuni.</span><span class="sxs-lookup"><span data-stu-id="2a257-120">Describes the most common YUV sampling techniques.</span></span>
-   <span data-ttu-id="2a257-121">[Definizioni della superficie](#surface-definitions).</span><span class="sxs-lookup"><span data-stu-id="2a257-121">[Surface Definitions](#surface-definitions).</span></span> <span data-ttu-id="2a257-122">Descrive i formati YUV consigliati.</span><span class="sxs-lookup"><span data-stu-id="2a257-122">Describes the recommended YUV formats.</span></span>
-   <span data-ttu-id="2a257-123">[Conversioni dello spazio colore e della frequenza di campionamento Chroma](#color-space-and-chroma-sampling-rate-conversions).</span><span class="sxs-lookup"><span data-stu-id="2a257-123">[Color Space and Chroma Sampling Rate Conversions](#color-space-and-chroma-sampling-rate-conversions).</span></span> <span data-ttu-id="2a257-124">Fornisce alcune linee guida per la conversione tra formati YUV e RGB e per la conversione tra formati YUV diversi.</span><span class="sxs-lookup"><span data-stu-id="2a257-124">Provides some guidelines for converting between YUV and RGB formats and for converting between different YUV formats.</span></span>
-   <span data-ttu-id="2a257-125">[Identificazione dei formati YUV in Media Foundation](#identifying-yuv-formats-in-media-foundation).</span><span class="sxs-lookup"><span data-stu-id="2a257-125">[Identifying YUV Formats in Media Foundation](#identifying-yuv-formats-in-media-foundation).</span></span> <span data-ttu-id="2a257-126">Viene illustrato come descrivere i tipi di formato YUV in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2a257-126">Explains how to describe YUV format types in Media Foundation.</span></span>

## <a name="yuv-sampling"></a><span data-ttu-id="2a257-127">Campionamento YUV</span><span class="sxs-lookup"><span data-stu-id="2a257-127">YUV Sampling</span></span>

<span data-ttu-id="2a257-128">I canali Chroma possono avere una frequenza di campionamento inferiore rispetto al canale luma, senza alcuna perdita significativa di qualità percettiva.</span><span class="sxs-lookup"><span data-stu-id="2a257-128">Chroma channels can have a lower sampling rate than the luma channel, without any dramatic loss of perceptual quality.</span></span> <span data-ttu-id="2a257-129">Una notazione detta notazione "A:B: C" viene usata per descrivere la frequenza con cui si campionano i e V rispetto a Y:</span><span class="sxs-lookup"><span data-stu-id="2a257-129">A notation called the "A:B:C" notation is used to describe how often U and V are sampled relative to Y:</span></span>

-   <span data-ttu-id="2a257-130">4:4:4 indica nessun sottocampionando dei canali Chroma.</span><span class="sxs-lookup"><span data-stu-id="2a257-130">4:4:4 means no downsampling of the chroma channels.</span></span>
-   <span data-ttu-id="2a257-131">4:2:2 indica 2:1 sottocampionando orizzontali, senza sottocampionando verticali.</span><span class="sxs-lookup"><span data-stu-id="2a257-131">4:2:2 means 2:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="2a257-132">Ogni riga di analisi contiene quattro campioni Y per ogni due campioni U o V.</span><span class="sxs-lookup"><span data-stu-id="2a257-132">Every scan line contains four Y samples for every two U or V samples.</span></span>
-   <span data-ttu-id="2a257-133">4:2:0 indica 2:1 sottocampionando orizzontali, con 2:1 sottocampionando verticali.</span><span class="sxs-lookup"><span data-stu-id="2a257-133">4:2:0 means 2:1 horizontal downsampling, with 2:1 vertical downsampling.</span></span>
-   <span data-ttu-id="2a257-134">4:1:1 indica 4:1 sottocampionando orizzontali, senza sottocampionando verticali.</span><span class="sxs-lookup"><span data-stu-id="2a257-134">4:1:1 means 4:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="2a257-135">Ogni riga di analisi contiene quattro esempi Y per ogni esempio di utente e V.</span><span class="sxs-lookup"><span data-stu-id="2a257-135">Every scan line contains four Y samples for each U and V sample.</span></span> <span data-ttu-id="2a257-136">4:1:1 il campionamento è meno comune di altri formati e non viene descritto in dettaglio in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="2a257-136">4:1:1 sampling is less common than other formats, and is not discussed in detail in this article.</span></span>

<span data-ttu-id="2a257-137">I diagrammi seguenti illustrano come viene campionato Chroma per ogni frequenza sottocampionando.</span><span class="sxs-lookup"><span data-stu-id="2a257-137">The following diagrams shows how chroma is sampled for each of the downsampling rates.</span></span> <span data-ttu-id="2a257-138">Gli esempi di Luma sono rappresentati da una croce e gli esempi di Chroma sono rappresentati da un cerchio.</span><span class="sxs-lookup"><span data-stu-id="2a257-138">Luma samples are represented by a cross, and chroma samples are represented by a circle.</span></span>

![Figura 1.](images/yuv-sampling-grids.png)

<span data-ttu-id="2a257-141">Il formato dominante del campionamento 4:2:2 è definito nella raccomandazione ITU-R BT. 601.</span><span class="sxs-lookup"><span data-stu-id="2a257-141">The dominant form of 4:2:2 sampling is defined in ITU-R Recommendation BT.601.</span></span> <span data-ttu-id="2a257-142">Esistono due varianti comuni del campionamento 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="2a257-142">There are two common variants of 4:2:0 sampling.</span></span> <span data-ttu-id="2a257-143">Uno di questi viene usato nel video MPEG-2 e l'altro viene usato in MPEG-1 e nelle raccomandazioni ITU-T H. 261 e H. 263.</span><span class="sxs-lookup"><span data-stu-id="2a257-143">One of these is used in MPEG-2 video, and the other is used in MPEG-1 and in ITU-T Recommendations H.261 and H.263.</span></span>

<span data-ttu-id="2a257-144">Rispetto allo schema MPEG-1, è più semplice eseguire la conversione tra lo schema MPEG-2 e le griglie di campionamento definite per i formati 4:2:2 e 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="2a257-144">Compared with the MPEG-1 scheme, it is simpler to convert between the MPEG-2 scheme and the sampling grids defined for 4:2:2 and 4:4:4 formats.</span></span> <span data-ttu-id="2a257-145">Per questo motivo, lo schema MPEG-2 è preferibile in Windows e deve essere considerato l'interpretazione predefinita dei formati 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="2a257-145">For this reason, the MPEG-2 scheme is preferred in Windows, and should be considered the default interpretation of 4:2:0 formats.</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="2a257-146">Definizioni di superficie</span><span class="sxs-lookup"><span data-stu-id="2a257-146">Surface Definitions</span></span>

<span data-ttu-id="2a257-147">Questa sezione descrive i formati YUV a 8 bit consigliati per il rendering video.</span><span class="sxs-lookup"><span data-stu-id="2a257-147">This section describes the 8-bit YUV formats that are recommended for video rendering.</span></span> <span data-ttu-id="2a257-148">Questi rientrano in diverse categorie:</span><span class="sxs-lookup"><span data-stu-id="2a257-148">These fall into several categories:</span></span>

-   [<span data-ttu-id="2a257-149">4:4:4 formati, 32 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="2a257-149">4:4:4 Formats, 32 Bits per Pixel</span></span>](#444-formats-32-bits-per-pixel)
-   [<span data-ttu-id="2a257-150">4:2:2 formati, 16 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="2a257-150">4:2:2 Formats, 16 Bits per Pixel</span></span>](#422-formats-16-bits-per-pixel)
-   [<span data-ttu-id="2a257-151">4:2:0 formati, 16 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="2a257-151">4:2:0 Formats, 16 Bits per Pixel</span></span>](#420-formats-16-bits-per-pixel)
-   [<span data-ttu-id="2a257-152">4:2:0 formati, 12 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="2a257-152">4:2:0 Formats, 12 Bits per Pixel</span></span>](#420-formats-12-bits-per-pixel)

<span data-ttu-id="2a257-153">Prima di tutto, è necessario tenere presenti i concetti seguenti per comprendere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="2a257-153">First, you should be aware of the following concepts in order to understand what follows:</span></span>

-   <span data-ttu-id="2a257-154">*Origine della superficie*.</span><span class="sxs-lookup"><span data-stu-id="2a257-154">*Surface origin*.</span></span> <span data-ttu-id="2a257-155">Per i formati YUV descritti in questo articolo, l'origine (0, 0) è sempre l'angolo superiore sinistro della superficie.</span><span class="sxs-lookup"><span data-stu-id="2a257-155">For the YUV formats described in this article, the origin (0,0) is always the top left corner of the surface.</span></span>
-   <span data-ttu-id="2a257-156">*Stride*.</span><span class="sxs-lookup"><span data-stu-id="2a257-156">*Stride*.</span></span> <span data-ttu-id="2a257-157">Lo stride di una superficie, talvolta denominato pitch, è la larghezza in byte della superficie.</span><span class="sxs-lookup"><span data-stu-id="2a257-157">The stride of a surface, sometimes called the pitch, is the width of the surface in bytes.</span></span> <span data-ttu-id="2a257-158">Data un'origine della superficie nell'angolo superiore sinistro, lo stride è sempre positivo.</span><span class="sxs-lookup"><span data-stu-id="2a257-158">Given a surface origin at the top left corner, the stride is always positive.</span></span>
-   <span data-ttu-id="2a257-159">*Allineamento*.</span><span class="sxs-lookup"><span data-stu-id="2a257-159">*Alignment*.</span></span> <span data-ttu-id="2a257-160">L'allineamento di una superficie è a discrezione del driver di visualizzazione grafica.</span><span class="sxs-lookup"><span data-stu-id="2a257-160">The alignment of a surface is at the discretion of the graphics display driver.</span></span> <span data-ttu-id="2a257-161">La superficie deve essere sempre allineata DWORD; ovvero le singole righe all'interno della superficie hanno come origine un limite di 32 bit (DWORD).</span><span class="sxs-lookup"><span data-stu-id="2a257-161">The surface must always be DWORD aligned; that is, individual lines within the surface are guaranteed to originate on a 32-bit (DWORD) boundary.</span></span> <span data-ttu-id="2a257-162">Tuttavia, l'allineamento può essere maggiore di 32 bit, a seconda delle esigenze dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2a257-162">The alignment can be larger than 32 bits, however, depending on the needs of the hardware.</span></span>
-   <span data-ttu-id="2a257-163">Formato compresso rispetto al formato Planar.</span><span class="sxs-lookup"><span data-stu-id="2a257-163">Packed format versus planar format.</span></span> <span data-ttu-id="2a257-164">I formati YUV sono divisi in formati *compressi* e *planari* .</span><span class="sxs-lookup"><span data-stu-id="2a257-164">YUV formats are divided into *packed* formats and *planar* formats.</span></span> <span data-ttu-id="2a257-165">In un formato compresso, i componenti Y, U e V vengono archiviati in una sola matrice.</span><span class="sxs-lookup"><span data-stu-id="2a257-165">In a packed format, the Y, U, and V components are stored in a single array.</span></span> <span data-ttu-id="2a257-166">I pixel sono organizzati in gruppi di macropixels, il cui layout dipende dal formato.</span><span class="sxs-lookup"><span data-stu-id="2a257-166">Pixels are organized into groups of macropixels, whose layout depends on the format.</span></span> <span data-ttu-id="2a257-167">In un formato planare, i componenti Y, U e V vengono archiviati come tre piani distinti.</span><span class="sxs-lookup"><span data-stu-id="2a257-167">In a planar format, the Y, U, and V components are stored as three separate planes.</span></span>

<span data-ttu-id="2a257-168">Per ognuno dei formati YUV descritti in questo articolo è stato assegnato un codice FOURCC.</span><span class="sxs-lookup"><span data-stu-id="2a257-168">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="2a257-169">Un codice FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="2a257-169">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

-   <span data-ttu-id="2a257-170">4:4:4 (32 BPP)</span><span class="sxs-lookup"><span data-stu-id="2a257-170">4:4:4 (32 bpp)</span></span>
    -   [<span data-ttu-id="2a257-171">AYUV</span><span class="sxs-lookup"><span data-stu-id="2a257-171">AYUV</span></span>](#ayuv)
-   <span data-ttu-id="2a257-172">4:2:2 (16 BPP)</span><span class="sxs-lookup"><span data-stu-id="2a257-172">4:2:2 (16 bpp)</span></span>
    -   [<span data-ttu-id="2a257-173">YUY2</span><span class="sxs-lookup"><span data-stu-id="2a257-173">YUY2</span></span>](#yuy2)
    -   [<span data-ttu-id="2a257-174">UYVY</span><span class="sxs-lookup"><span data-stu-id="2a257-174">UYVY</span></span>](#uyvy)
-   <span data-ttu-id="2a257-175">4:2:0 (16 BPP)</span><span class="sxs-lookup"><span data-stu-id="2a257-175">4:2:0 (16 bpp)</span></span>
    -   [<span data-ttu-id="2a257-176">IMC1</span><span class="sxs-lookup"><span data-stu-id="2a257-176">IMC1</span></span>](#imc1)
    -   [<span data-ttu-id="2a257-177">IMC3</span><span class="sxs-lookup"><span data-stu-id="2a257-177">IMC3</span></span>](#imc3)
-   <span data-ttu-id="2a257-178">4:2:0 (12 BPP)</span><span class="sxs-lookup"><span data-stu-id="2a257-178">4:2:0 (12 bpp)</span></span>
    -   [<span data-ttu-id="2a257-179">IMC2</span><span class="sxs-lookup"><span data-stu-id="2a257-179">IMC2</span></span>](#imc2)
    -   [<span data-ttu-id="2a257-180">IMC4</span><span class="sxs-lookup"><span data-stu-id="2a257-180">IMC4</span></span>](#imc4)
    -   [<span data-ttu-id="2a257-181">YV12</span><span class="sxs-lookup"><span data-stu-id="2a257-181">YV12</span></span>](#yv12)
    -   [<span data-ttu-id="2a257-182">NV12</span><span class="sxs-lookup"><span data-stu-id="2a257-182">NV12</span></span>](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a><span data-ttu-id="2a257-183">4:4:4 formati, 32 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="2a257-183">4:4:4 Formats, 32 Bits per Pixel</span></span>

### <a name="ayuv"></a><span data-ttu-id="2a257-184">AYUV</span><span class="sxs-lookup"><span data-stu-id="2a257-184">AYUV</span></span>

<span data-ttu-id="2a257-185">È consigliabile usare un unico formato 4:4:4, con il codice FOURCC AYUV.</span><span class="sxs-lookup"><span data-stu-id="2a257-185">A single 4:4:4 format is recommended, with the FOURCC code AYUV.</span></span> <span data-ttu-id="2a257-186">Si tratta di un formato compresso, in cui ogni pixel è codificato come quattro byte consecutivi, disposti nella sequenza illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2a257-186">This is a packed format, where each pixel is encoded as four consecutive bytes, arranged in the sequence shown in the following illustration.</span></span>

![Figura 2.](images/yuvformats01.gif)

<span data-ttu-id="2a257-189">I byte contrassegnati come contengono valori per Alpha.</span><span class="sxs-lookup"><span data-stu-id="2a257-189">The bytes marked A contain values for alpha.</span></span>

## <a name="422-formats-16-bits-per-pixel"></a><span data-ttu-id="2a257-190">4:2:2 formati, 16 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="2a257-190">4:2:2 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="2a257-191">Sono consigliati due formati 4:2:2, con i codici FOURCC seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a257-191">Two 4:2:2 formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="2a257-192">YUY2</span><span class="sxs-lookup"><span data-stu-id="2a257-192">YUY2</span></span>
-   <span data-ttu-id="2a257-193">UYVY</span><span class="sxs-lookup"><span data-stu-id="2a257-193">UYVY</span></span>

<span data-ttu-id="2a257-194">Entrambi sono formati compressi, in cui ogni macropixel è codificato in due pixel come quattro byte consecutivi.</span><span class="sxs-lookup"><span data-stu-id="2a257-194">Both are packed formats, where each macropixel is two pixels encoded as four consecutive bytes.</span></span> <span data-ttu-id="2a257-195">In questo modo si ottiene un sottocampionando orizzontale del Chroma per un fattore di due.</span><span class="sxs-lookup"><span data-stu-id="2a257-195">This results in horizontal downsampling of the chroma by a factor of two.</span></span>

### <a name="yuy2"></a><span data-ttu-id="2a257-196">YUY2</span><span class="sxs-lookup"><span data-stu-id="2a257-196">YUY2</span></span>

<span data-ttu-id="2a257-197">Nel formato YUY2, i dati possono essere considerati come una matrice di valori **char** senza segno, dove il primo byte contiene il primo campione y, il secondo byte contiene il primo campione U (CB), il terzo byte contiene il secondo campione Y e il quarto byte contiene il primo esempio V (CR), come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="2a257-197">In YUY2 format, the data can be treated as an array of unsigned **char** values, where the first byte contains the first Y sample, the second byte contains the first U (Cb) sample, the third byte contains the second Y sample, and the fourth byte contains the first V (Cr) sample, as shown in the following diagram.</span></span>

![Figura 3.](images/yuvformats02.gif)

<span data-ttu-id="2a257-200">Se l'immagine viene trattata come una matrice di valori di **parola** little-endian, la prima **parola** contiene il primo campione Y nei bit meno significativi (LSB) e il primo campione U (CB) nei bit più significativi (MSBs).</span><span class="sxs-lookup"><span data-stu-id="2a257-200">If the image is addressed as an array of little-endian **WORD** values, the first **WORD** contains the first Y sample in the least significant bits (LSBs) and the first U (Cb) sample in the most significant bits (MSBs).</span></span> <span data-ttu-id="2a257-201">La seconda **parola** contiene il secondo campione Y in LSB e il primo esempio V (CR) in MSBs.</span><span class="sxs-lookup"><span data-stu-id="2a257-201">The second **WORD** contains the second Y sample in the LSBs and the first V (Cr) sample in the MSBs.</span></span>

<span data-ttu-id="2a257-202">YUY2 è il formato di 4:2:2 pixel preferito per l'accelerazione video Microsoft DirectX (DirectX VA).</span><span class="sxs-lookup"><span data-stu-id="2a257-202">YUY2 is the preferred 4:2:2 pixel format for Microsoft DirectX Video Acceleration (DirectX VA).</span></span> <span data-ttu-id="2a257-203">Si prevede che sia un requisito a breve termine per gli acceleratori DirectX VA che supportano 4:2:2 video.</span><span class="sxs-lookup"><span data-stu-id="2a257-203">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:2 video.</span></span>

### <a name="uyvy"></a><span data-ttu-id="2a257-204">UYVY</span><span class="sxs-lookup"><span data-stu-id="2a257-204">UYVY</span></span>

<span data-ttu-id="2a257-205">Questo formato è identico a quello del formato YUY2, ad eccezione del fatto che l'ordine dei byte è invertito, ovvero i byte Chroma e Luma sono capovolti (Figura 4).</span><span class="sxs-lookup"><span data-stu-id="2a257-205">This format is the same as the YUY2 format except the byte order is reversed—that is, the chroma and luma bytes are flipped (Figure 4).</span></span> <span data-ttu-id="2a257-206">Se l'immagine viene trattata come una matrice di due valori di **parola** little-endian, la prima **parola** contiene U in LSB e Y0 in MSBs e la seconda **parola** contiene V in LSB e Y1 in MSBs.</span><span class="sxs-lookup"><span data-stu-id="2a257-206">If the image is addressed as an array of two little-endian **WORD** values, the first **WORD** contains U in the LSBs and Y0 in the MSBs, and the second **WORD** contains V in the LSBs and Y1 in the MSBs.</span></span>

![Figura 4.](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a><span data-ttu-id="2a257-209">4:2:0 formati, 16 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="2a257-209">4:2:0 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="2a257-210">Sono consigliati due formati di 4:2:0 16 bit per pixel (BPP), con i codici FOURCC seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a257-210">Two 4:2:0 16-bits per pixel (bpp) formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="2a257-211">IMC1</span><span class="sxs-lookup"><span data-stu-id="2a257-211">IMC1</span></span>
-   <span data-ttu-id="2a257-212">IMC3</span><span class="sxs-lookup"><span data-stu-id="2a257-212">IMC3</span></span>

<span data-ttu-id="2a257-213">Entrambi i formati YUV sono formati planari.</span><span class="sxs-lookup"><span data-stu-id="2a257-213">Both of these YUV formats are planar formats.</span></span> <span data-ttu-id="2a257-214">I canali Chroma sono sottocampionati da un fattore di due nelle dimensioni orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="2a257-214">The chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc1"></a><span data-ttu-id="2a257-215">IMC1</span><span class="sxs-lookup"><span data-stu-id="2a257-215">IMC1</span></span>

<span data-ttu-id="2a257-216">Tutti gli esempi Y vengono visualizzati prima in memoria come matrice di valori **char** senza segno.</span><span class="sxs-lookup"><span data-stu-id="2a257-216">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="2a257-217">Questa operazione è seguita da tutti gli esempi V (CR), quindi da tutti gli esempi U (CB).</span><span class="sxs-lookup"><span data-stu-id="2a257-217">This is followed by all of the V (Cr) samples, and then all of the U (Cb) samples.</span></span> <span data-ttu-id="2a257-218">I piani V e U hanno lo stesso stride del piano Y, con la conseguente presenza di aree di memoria inutilizzate, come illustrato nella figura 5.</span><span class="sxs-lookup"><span data-stu-id="2a257-218">The V and U planes have the same stride as the Y plane, resulting in unused areas of memory, as shown in Figure 5.</span></span> <span data-ttu-id="2a257-219">I piani utente e V devono iniziare sui limiti di memoria che sono un multiplo di 16 righe.</span><span class="sxs-lookup"><span data-stu-id="2a257-219">The U and V planes must start on memory boundaries that are a multiple of 16 lines.</span></span> <span data-ttu-id="2a257-220">Nella figura 5 viene illustrata l'origine di u e V per un fotogramma video 352 x 240.</span><span class="sxs-lookup"><span data-stu-id="2a257-220">Figure 5 shows the origin of U and V for a 352 x 240 video frame.</span></span> <span data-ttu-id="2a257-221">L'indirizzo iniziale dei piani utente e V viene calcolato come segue:</span><span class="sxs-lookup"><span data-stu-id="2a257-221">The starting address of the U and V planes are calculated as follows:</span></span>

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

<span data-ttu-id="2a257-222">dove *py* è un puntatore di byte all'inizio della matrice di memoria, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2a257-222">where *pY* is a byte pointer to the start of the memory array, as shown in the following diagram.</span></span>

![Figura 5.](images/yuvformats04.gif)

### <a name="imc3"></a><span data-ttu-id="2a257-225">IMC3</span><span class="sxs-lookup"><span data-stu-id="2a257-225">IMC3</span></span>

<span data-ttu-id="2a257-226">Questo formato è identico a IMC1, ad eccezione del fatto che i piani utente e V vengono scambiati, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="2a257-226">This format is identical to IMC1, except the U and V planes are swapped, as shown in the following diagram.</span></span>

![Figura 6.](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a><span data-ttu-id="2a257-229">4:2:0 formati, 12 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="2a257-229">4:2:0 Formats, 12 Bits per Pixel</span></span>

<span data-ttu-id="2a257-230">Sono consigliati quattro formati a 4:2:0 12 BPP, con i codici FOURCC seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a257-230">Four 4:2:0 12-bpp formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="2a257-231">IMC2</span><span class="sxs-lookup"><span data-stu-id="2a257-231">IMC2</span></span>
-   <span data-ttu-id="2a257-232">IMC4</span><span class="sxs-lookup"><span data-stu-id="2a257-232">IMC4</span></span>
-   <span data-ttu-id="2a257-233">YV12</span><span class="sxs-lookup"><span data-stu-id="2a257-233">YV12</span></span>
-   <span data-ttu-id="2a257-234">NV12</span><span class="sxs-lookup"><span data-stu-id="2a257-234">NV12</span></span>

<span data-ttu-id="2a257-235">In tutti questi formati, i canali Chroma vengono sottocampionati in base a un fattore di due nelle dimensioni orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="2a257-235">In all of these formats, the chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc2"></a><span data-ttu-id="2a257-236">IMC2</span><span class="sxs-lookup"><span data-stu-id="2a257-236">IMC2</span></span>

<span data-ttu-id="2a257-237">Questo formato è identico a quello di IMC1, ad eccezione della differenza seguente: le linee V (CR) e U (CB) sono Interleaved con limiti a metà stride.</span><span class="sxs-lookup"><span data-stu-id="2a257-237">This format is the same as IMC1 except for the following difference: The V (Cr) and U (Cb) lines are interleaved at half-stride boundaries.</span></span> <span data-ttu-id="2a257-238">In altre parole, ogni riga a stride totale nell'area Chroma inizia con una riga di campioni V, seguita da una riga di campioni U che inizia al limite di metà stride successivo (Figura 7).</span><span class="sxs-lookup"><span data-stu-id="2a257-238">In other words, each full-stride line in the chroma area starts with a line of V samples, followed by a line of U samples that begins at the next half-stride boundary (Figure 7).</span></span> <span data-ttu-id="2a257-239">Questo layout rende più efficiente l'uso dello spazio degli indirizzi rispetto a IMC1.</span><span class="sxs-lookup"><span data-stu-id="2a257-239">This layout makes more efficient use of address space than IMC1.</span></span> <span data-ttu-id="2a257-240">Taglia lo spazio degli indirizzi Chroma a metà e quindi lo spazio degli indirizzi totale del 25%.</span><span class="sxs-lookup"><span data-stu-id="2a257-240">It cuts the chroma address space in half, and thus the total address space by 25 percent.</span></span> <span data-ttu-id="2a257-241">Tra i formati 4:2:0, IMC2 è il secondo formato preferito, dopo NV12.</span><span class="sxs-lookup"><span data-stu-id="2a257-241">Among 4:2:0 formats, IMC2 is the second-most preferred format, after NV12.</span></span> <span data-ttu-id="2a257-242">Questo processo è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2a257-242">The following image illustrates this process.</span></span>

![Figura 7.](images/yuvformats07.gif)

### <a name="imc4"></a><span data-ttu-id="2a257-245">IMC4</span><span class="sxs-lookup"><span data-stu-id="2a257-245">IMC4</span></span>

<span data-ttu-id="2a257-246">Questo formato è identico a IMC2, ad eccezione delle righe U (CB) e V (CR), come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2a257-246">This format is identical to IMC2, except the U (Cb) and V (Cr) lines are swapped, as shown in the following illustration.</span></span>

![Figura 8.](images/yuvformats06.gif)

### <a name="yv12"></a><span data-ttu-id="2a257-249">YV12</span><span class="sxs-lookup"><span data-stu-id="2a257-249">YV12</span></span>

<span data-ttu-id="2a257-250">Tutti gli esempi Y vengono visualizzati prima in memoria come matrice di valori **char** senza segno.</span><span class="sxs-lookup"><span data-stu-id="2a257-250">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="2a257-251">Questa matrice è seguita immediatamente da tutti gli esempi V (CR).</span><span class="sxs-lookup"><span data-stu-id="2a257-251">This array is followed immediately by all of the V (Cr) samples.</span></span> <span data-ttu-id="2a257-252">Lo stride del piano V è metà dello stride del piano Y; e il piano V contiene metà del numero di righe del piano Y.</span><span class="sxs-lookup"><span data-stu-id="2a257-252">The stride of the V plane is half the stride of the Y plane; and the V plane contains half as many lines as the Y plane.</span></span> <span data-ttu-id="2a257-253">Il piano V è immediatamente seguito da tutti gli esempi U (CB), con lo stesso stride e il numero di righe del piano V, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2a257-253">The V plane is followed immediately by all of the U (Cb) samples, with the same stride and number of lines as the V plane, as shown in the following illustration.</span></span>

![Figura 9.](images/yuvformats08.gif)

### <a name="nv12"></a><span data-ttu-id="2a257-256">NV12</span><span class="sxs-lookup"><span data-stu-id="2a257-256">NV12</span></span>

<span data-ttu-id="2a257-257">Tutti gli esempi Y vengono visualizzati prima in memoria come matrice di valori **char** senza segno con un numero pari di righe.</span><span class="sxs-lookup"><span data-stu-id="2a257-257">All of the Y samples appear first in memory as an array of unsigned **char** values with an even number of lines.</span></span> <span data-ttu-id="2a257-258">Il piano Y è immediatamente seguito da una matrice di valori **char** senza segno che contiene campioni U (CB) e V (CR) compressi.</span><span class="sxs-lookup"><span data-stu-id="2a257-258">The Y plane is followed immediately by an array of unsigned **char** values that contains packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="2a257-259">Quando l'array U-V combinato viene considerato come una matrice di valori di **parola** little-endian, LSB contiene i valori U e MSBs contiene i valori V.</span><span class="sxs-lookup"><span data-stu-id="2a257-259">When the combined U-V array is addressed as an array of little-endian **WORD** values, the LSBs contain the U values, and the MSBs contain the V values.</span></span> <span data-ttu-id="2a257-260">NV12 è il formato preferito di 4:2:0 pixel per DirectX VA.</span><span class="sxs-lookup"><span data-stu-id="2a257-260">NV12 is the preferred 4:2:0 pixel format for DirectX VA.</span></span> <span data-ttu-id="2a257-261">Si prevede che sia un requisito a breve termine per gli acceleratori DirectX VA che supportano 4:2:0 video.</span><span class="sxs-lookup"><span data-stu-id="2a257-261">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:0 video.</span></span> <span data-ttu-id="2a257-262">Nella figura seguente vengono illustrati il piano Y e la matrice contenente gli esempi compressi e V.</span><span class="sxs-lookup"><span data-stu-id="2a257-262">The following illustration shows the Y plane and the array that contains packed U and V samples.</span></span>

![Figura 10.](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a><span data-ttu-id="2a257-265">Conversioni dello spazio colore e della frequenza di campionamento Chroma</span><span class="sxs-lookup"><span data-stu-id="2a257-265">Color Space and Chroma Sampling Rate Conversions</span></span>

<span data-ttu-id="2a257-266">Questa sezione fornisce le linee guida per la conversione tra YUV e RGB e per la conversione tra diversi formati YUV.</span><span class="sxs-lookup"><span data-stu-id="2a257-266">This section provides guidelines for converting between YUV and RGB, and for converting between some different YUV formats.</span></span> <span data-ttu-id="2a257-267">In questa sezione sono considerati due schemi di codifica RGB: *computer a 8 bit RGB*, noti anche come sRGB o "full-scale" RGB e *studio video RGB*, oppure "RGB con Head-Room e toe-room".</span><span class="sxs-lookup"><span data-stu-id="2a257-267">We consider two RGB encoding schemes in this section: *8-bit computer RGB*, also known as sRGB or "full-scale" RGB, and *studio video RGB*, or "RGB with head-room and toe-room."</span></span> <span data-ttu-id="2a257-268">Questi vengono definiti come segue:</span><span class="sxs-lookup"><span data-stu-id="2a257-268">These are defined as follows:</span></span>

-   <span data-ttu-id="2a257-269">Il computer RGB utilizza 8 bit per ogni campione di rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="2a257-269">Computer RGB uses 8 bits for each sample of red, green, and blue.</span></span> <span data-ttu-id="2a257-270">Il nero è rappresentato da R = G = B = 0 e il bianco è rappresentato da R = G = B = 255.</span><span class="sxs-lookup"><span data-stu-id="2a257-270">Black is represented by R = G = B = 0, and white is represented by R = G = B = 255.</span></span>
-   <span data-ttu-id="2a257-271">Studio video RGB usa un numero di bit N per ogni campione di rosso, verde e blu, dove N è 8 o più.</span><span class="sxs-lookup"><span data-stu-id="2a257-271">Studio video RGB uses some number of bits N for each sample of red, green, and blue, where N is 8 or more.</span></span> <span data-ttu-id="2a257-272">Il video RGB di studio usa un fattore di scala diverso rispetto al computer RGB e presenta un offset.</span><span class="sxs-lookup"><span data-stu-id="2a257-272">Studio video RGB uses a different scaling factor than computer RGB, and it has an offset.</span></span> <span data-ttu-id="2a257-273">Il nero è rappresentato da R = G = B = 16 \* 2 ^ (n-8) e il bianco è rappresentato da r = g = b = 235 \* 2 ^ (n-8).</span><span class="sxs-lookup"><span data-stu-id="2a257-273">Black is represented by R = G = B = 16\*2^(N-8), and white is represented by R = G = B = 235\*2^(N-8).</span></span> <span data-ttu-id="2a257-274">Tuttavia, i valori effettivi possono non essere compresi in questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="2a257-274">However, actual values may fall outside this range.</span></span>

<span data-ttu-id="2a257-275">Studio video RGB è la definizione RGB preferita per i video in Windows, mentre il computer RGB è la definizione RGB preferita per le applicazioni non video.</span><span class="sxs-lookup"><span data-stu-id="2a257-275">Studio video RGB is the preferred RGB definition for video in Windows, while computer RGB is the preferred RGB definition for non-video applications.</span></span> <span data-ttu-id="2a257-276">In entrambe le forme di RGB, le coordinate di cromaticità sono specificate in ITU-R BT. 709 per la definizione delle primarie di colore RGB.</span><span class="sxs-lookup"><span data-stu-id="2a257-276">In either form of RGB, the chromaticity coordinates are as specified in ITU-R BT.709 for the definition of the RGB color primaries.</span></span> <span data-ttu-id="2a257-277">Le coordinate (x, y) di R, G e B sono (0,64, 0,33), (0,30, 0,60) e (0,15, 0,06), rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="2a257-277">The (x,y) coordinates of R, G, and B are (0.64, 0.33), (0.30, 0.60), and (0.15, 0.06), respectively.</span></span> <span data-ttu-id="2a257-278">Il riferimento bianco è D65 con coordinate (0,3127, 0,3290).</span><span class="sxs-lookup"><span data-stu-id="2a257-278">Reference white is D65 with coordinates (0.3127, 0.3290).</span></span> <span data-ttu-id="2a257-279">La gamma nominale è 1/0.45 (approssimativamente 2,2), con una gamma precisa definita dettagliatamente in ITU-R BT. 709.</span><span class="sxs-lookup"><span data-stu-id="2a257-279">Nominal gamma is 1/0.45 (approximately 2.2), with precise gamma defined in detail in ITU-R BT.709.</span></span>

<span data-ttu-id="2a257-280">**Conversione tra RGB e 4:4:4 YUV**</span><span class="sxs-lookup"><span data-stu-id="2a257-280">**Conversion between RGB and 4:4:4 YUV**</span></span>

<span data-ttu-id="2a257-281">Viene innanzitutto descritta la conversione tra RGB e 4:4:4 YUV.</span><span class="sxs-lookup"><span data-stu-id="2a257-281">We first describe conversion between RGB and 4:4:4 YUV.</span></span> <span data-ttu-id="2a257-282">Per convertire 4:2:0 o 4:2:2 YUV in RGB, è consigliabile convertire i dati YUV in 4:4:4 YUV e quindi eseguire la conversione da 4:4:4 YUV a RGB.</span><span class="sxs-lookup"><span data-stu-id="2a257-282">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="2a257-283">Il formato AYUV, che è un formato 4:4:4, USA 8 bit ciascuno per gli esempi Y, U e V.</span><span class="sxs-lookup"><span data-stu-id="2a257-283">The AYUV format, which is a 4:4:4 format, uses 8 bits each for the Y, U, and V samples.</span></span> <span data-ttu-id="2a257-284">YUV può anche essere definito usando più di 8 bit per esempio per alcune applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2a257-284">YUV can also be defined using more than 8 bits per sample for some applications.</span></span>

<span data-ttu-id="2a257-285">Per i video digitali sono state definite due conversioni YUV dominanti da RGB.</span><span class="sxs-lookup"><span data-stu-id="2a257-285">Two dominant YUV conversions from RGB have been defined for digital video.</span></span> <span data-ttu-id="2a257-286">Entrambi sono basati sulla specifica nota come ITU-R Recommendation BT. 709.</span><span class="sxs-lookup"><span data-stu-id="2a257-286">Both are based on the specification known as ITU-R Recommendation BT.709.</span></span> <span data-ttu-id="2a257-287">La prima conversione è il modulo YUV precedente definito per l'uso di 50 Hz in BT. 709.</span><span class="sxs-lookup"><span data-stu-id="2a257-287">The first conversion is the older YUV form defined for 50-Hz use in BT.709.</span></span> <span data-ttu-id="2a257-288">Corrisponde alla relazione specificata nella raccomandazione ITU-R BT. 601, nota anche con il nome precedente, CCIR 601.</span><span class="sxs-lookup"><span data-stu-id="2a257-288">It is the same as the relation specified in ITU-R Recommendation BT.601, also known by its older name, CCIR 601.</span></span> <span data-ttu-id="2a257-289">Deve essere considerato il formato YUV preferito per la risoluzione TV Standard-Definition (720 x 576) e il video di risoluzione inferiore.</span><span class="sxs-lookup"><span data-stu-id="2a257-289">It should be considered the preferred YUV format for standard-definition TV resolution (720 x 576) and lower-resolution video.</span></span> <span data-ttu-id="2a257-290">È caratterizzato dai valori di due costanti *KR* e *KB*:</span><span class="sxs-lookup"><span data-stu-id="2a257-290">It is characterized by the values of two constants *Kr* and *Kb*:</span></span>

``` syntax
Kr = 0.299
Kb = 0.114
```

<span data-ttu-id="2a257-291">La seconda conversione è il form YUV più recente definito per l'uso 60-Hz in BT. 709 e deve essere considerato il formato preferito per le risoluzioni video precedenti a SDTV.</span><span class="sxs-lookup"><span data-stu-id="2a257-291">The second conversion is the newer YUV form defined for 60-Hz use in BT.709, and should be considered the preferred format for video resolutions above SDTV.</span></span> <span data-ttu-id="2a257-292">È caratterizzato da valori diversi per queste due costanti:</span><span class="sxs-lookup"><span data-stu-id="2a257-292">It is characterized by different values for these two constants:</span></span>

``` syntax
Kr = 0.2126
Kb = 0.0722
```

<span data-ttu-id="2a257-293">La conversione da RGB a YUV viene definita iniziando con quanto segue:</span><span class="sxs-lookup"><span data-stu-id="2a257-293">Conversion from RGB to YUV is defined by starting with the following:</span></span>

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

<span data-ttu-id="2a257-294">I valori YUV vengono quindi ottenuti come segue:</span><span class="sxs-lookup"><span data-stu-id="2a257-294">The YUV values are then obtained as follows:</span></span>

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

<span data-ttu-id="2a257-295">dove</span><span class="sxs-lookup"><span data-stu-id="2a257-295">where</span></span>

-   <span data-ttu-id="2a257-296">M è il numero di bit per campione YUV (M >= 8).</span><span class="sxs-lookup"><span data-stu-id="2a257-296">M is the number of bits per YUV sample (M >= 8).</span></span>
-   <span data-ttu-id="2a257-297">Z è la variabile di livello nero.</span><span class="sxs-lookup"><span data-stu-id="2a257-297">Z is the black-level variable.</span></span> <span data-ttu-id="2a257-298">Per il computer RGB, Z è uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="2a257-298">For computer RGB, Z equals 0.</span></span> <span data-ttu-id="2a257-299">Per il video RGB di studio, Z equivale a 16 \* 2 ^ (n-8), dove N è il numero di bit per esempio RGB (N >= 8).</span><span class="sxs-lookup"><span data-stu-id="2a257-299">For studio video RGB, Z equals 16\*2^(N-8), where N is the number of bits per RGB sample (N >= 8).</span></span>
-   <span data-ttu-id="2a257-300">S è la variabile di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="2a257-300">S is the scaling variable.</span></span> <span data-ttu-id="2a257-301">Per il computer RGB, S è uguale a 255.</span><span class="sxs-lookup"><span data-stu-id="2a257-301">For computer RGB, S equals 255.</span></span> <span data-ttu-id="2a257-302">Per il video RGB di studio, S è uguale a 219 \* 2 ^ (N-8).</span><span class="sxs-lookup"><span data-stu-id="2a257-302">For studio video RGB, S equals 219\*2^(N-8).</span></span>

<span data-ttu-id="2a257-303">La funzione floor (x) restituisce l'intero più grande minore o uguale a x.</span><span class="sxs-lookup"><span data-stu-id="2a257-303">The function floor(x) returns the largest integer less than or equal to x.</span></span> <span data-ttu-id="2a257-304">La funzione clip3 (x, y, z) viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="2a257-304">The function clip3(x, y, z) is defined as follows:</span></span>

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> <span data-ttu-id="2a257-305">clip3 deve essere implementato come funzione anziché come macro del preprocessore; in caso contrario, si verificheranno più valutazioni degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="2a257-305">clip3 should be implemented as a function rather than a preprocessor macro; otherwise multiple evaluations of the arguments will occur.</span></span>

 

<span data-ttu-id="2a257-306">L'esempio Y rappresenta la luminosità e gli esempi di i e V rappresentano rispettivamente le deviazioni dei colori verso il blu e il rosso.</span><span class="sxs-lookup"><span data-stu-id="2a257-306">The Y sample represents brightness, and the U and V samples represent the color deviations toward blue and red, respectively.</span></span> <span data-ttu-id="2a257-307">L'intervallo nominale per Y è 16 \* 2 ^ (m-8) a 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="2a257-307">The nominal range for Y is 16\*2^(M-8) to 235\*2^(M-8).</span></span> <span data-ttu-id="2a257-308">Il nero è rappresentato da 16 \* 2 ^ (m-8) e il bianco viene rappresentato come 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="2a257-308">Black is represented as 16\*2^(M-8), and white is represented as 235\*2^(M-8).</span></span> <span data-ttu-id="2a257-309">L'intervallo nominale per l'utente e V è 16 \* 2 ^ (m-8) a 240 \* 2 ^ (m-8), con il valore 128 \* 2 ^ (m-8) che rappresenta la Croma neutra.</span><span class="sxs-lookup"><span data-stu-id="2a257-309">The nominal range for U and V are 16\*2^(M-8) to 240\*2^(M-8), with the value 128\*2^(M-8) representing neutral chroma.</span></span> <span data-ttu-id="2a257-310">Tuttavia, i valori effettivi possono non essere compresi in questi intervalli.</span><span class="sxs-lookup"><span data-stu-id="2a257-310">However, actual values may fall outside these ranges.</span></span>

<span data-ttu-id="2a257-311">Per i dati di input sotto forma di video RGB di studio, l'operazione di ritaglio è necessaria per memorizzare i valori dell'utente e della V compresi nell'intervallo compreso tra 0 e (2 ^ M)-1.</span><span class="sxs-lookup"><span data-stu-id="2a257-311">For input data in the form of studio video RGB, the clip operation is necessary to keep the U and V values within the range 0 to (2^M)-1.</span></span> <span data-ttu-id="2a257-312">Se l'input è RGB del computer, l'operazione di ritaglio non è obbligatoria, perché la formula di conversione non può produrre valori al di fuori di questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="2a257-312">If the input is computer RGB, the clip operation is not required, because the conversion formula cannot produce values outside of this range.</span></span>

<span data-ttu-id="2a257-313">Si tratta delle formule esatte senza approssimazione.</span><span class="sxs-lookup"><span data-stu-id="2a257-313">These are the exact formulas without approximation.</span></span> <span data-ttu-id="2a257-314">Tutte le operazioni seguenti in questo documento sono derivate da queste formule.</span><span class="sxs-lookup"><span data-stu-id="2a257-314">Everything that follows in this document is derived from these formulas.</span></span> <span data-ttu-id="2a257-315">In questa sezione vengono descritte le conversioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a257-315">This section describes the following conversions:</span></span>

-   [<span data-ttu-id="2a257-316">Conversione di RGB888 in YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="2a257-316">Converting RGB888 to YUV 4:4:4</span></span>](#converting-rgb888-to-yuv-444)
-   [<span data-ttu-id="2a257-317">Conversione da YUV a 8 bit a RGB888</span><span class="sxs-lookup"><span data-stu-id="2a257-317">Converting 8-bit YUV to RGB888</span></span>](#converting-8-bit-yuv-to-rgb888)
-   [<span data-ttu-id="2a257-318">Conversione da 4:2:0 YUV a 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="2a257-318">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>](#converting-420-yuv-to-422-yuv)
-   [<span data-ttu-id="2a257-319">Conversione da 4:2:2 YUV a 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="2a257-319">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>](#converting-422-yuv-to-444-yuv)
-   [<span data-ttu-id="2a257-320">Conversione da 4:2:0 YUV a 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="2a257-320">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a><span data-ttu-id="2a257-321">Conversione di RGB888 in YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="2a257-321">Converting RGB888 to YUV 4:4:4</span></span>

<span data-ttu-id="2a257-322">Nel caso di input RGB del computer e output YUV BT. 601 a 8 bit, si ritiene che le formule fornite nella sezione precedente possano essere ragionevolmente approssimate in base a quanto segue:</span><span class="sxs-lookup"><span data-stu-id="2a257-322">In the case of computer RGB input and 8-bit BT.601 YUV output, we believe that the formulas given in the previous section can be reasonably approximated by the following:</span></span>

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

<span data-ttu-id="2a257-323">Queste formule producono risultati a 8 bit usando coefficienti che non richiedono più di 8 bit di precisione (senza segno).</span><span class="sxs-lookup"><span data-stu-id="2a257-323">These formulas produce 8-bit results using coefficients that require no more than 8 bits of (unsigned) precision.</span></span> <span data-ttu-id="2a257-324">I risultati intermedi richiederanno fino a 16 bit di precisione.</span><span class="sxs-lookup"><span data-stu-id="2a257-324">Intermediate results will require up to 16 bits of precision.</span></span>

## <a name="converting-8-bit-yuv-to-rgb888"></a><span data-ttu-id="2a257-325">Conversione da YUV a 8 bit a RGB888</span><span class="sxs-lookup"><span data-stu-id="2a257-325">Converting 8-bit YUV to RGB888</span></span>

<span data-ttu-id="2a257-326">Dalle formule originali da RGB a YUV, è possibile derivare le relazioni seguenti per BT. 601.</span><span class="sxs-lookup"><span data-stu-id="2a257-326">From the original RGB-to-YUV formulas, one can derive the following relationships for BT.601.</span></span>

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

<span data-ttu-id="2a257-327">Pertanto, Data:</span><span class="sxs-lookup"><span data-stu-id="2a257-327">Therefore, given:</span></span>

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

<span data-ttu-id="2a257-328">le formule per convertire YUV in RGB possono essere derivate come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2a257-328">the formulas to convert YUV to RGB can be derived as follows:</span></span>

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

<span data-ttu-id="2a257-329">dove `clip()` indica il ritaglio a un intervallo compreso tra \[ 0 e 255 \] .</span><span class="sxs-lookup"><span data-stu-id="2a257-329">where `clip()` denotes clipping to a range of \[0..255\].</span></span> <span data-ttu-id="2a257-330">Si ritiene che queste formule possano essere ragionevolmente approssimate in base a quanto segue:</span><span class="sxs-lookup"><span data-stu-id="2a257-330">We believe these formulas can be reasonably approximated by the following:</span></span>

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

<span data-ttu-id="2a257-331">Queste formule usano alcuni coefficienti che richiedono più di 8 bit di precisione per produrre ogni risultato a 8 bit e i risultati intermedi richiedono più di 16 bit di precisione.</span><span class="sxs-lookup"><span data-stu-id="2a257-331">These formulas use some coefficients that require more than 8 bits of precision to produce each 8-bit result, and intermediate results will require more than 16 bits of precision.</span></span>

<span data-ttu-id="2a257-332">Per convertire 4:2:0 o 4:2:2 YUV in RGB, è consigliabile convertire i dati YUV in 4:4:4 YUV e quindi eseguire la conversione da 4:4:4 YUV a RGB.</span><span class="sxs-lookup"><span data-stu-id="2a257-332">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="2a257-333">Le sezioni seguenti illustrano alcuni metodi per la conversione di formati 4:2:0 e 4:2:2 in 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="2a257-333">The sections that follow present some methods for converting 4:2:0 and 4:2:2 formats to 4:4:4.</span></span>

## <a name="converting-420-yuv-to-422-yuv"></a><span data-ttu-id="2a257-334">Conversione da 4:2:0 YUV a 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="2a257-334">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>

<span data-ttu-id="2a257-335">Per la conversione da YUV a 4:2:0 YUV a 4:2:2 YUV è richiesta la conversione verticale per due fattori.</span><span class="sxs-lookup"><span data-stu-id="2a257-335">Converting 4:2:0 YUV to 4:2:2 YUV requires vertical upconversion by a factor of two.</span></span> <span data-ttu-id="2a257-336">In questa sezione viene descritto un metodo di esempio per eseguire la conversione.</span><span class="sxs-lookup"><span data-stu-id="2a257-336">This section describes an example method for performing the upconversion.</span></span> <span data-ttu-id="2a257-337">Il metodo presuppone che le immagini video siano Progressive Scan.</span><span class="sxs-lookup"><span data-stu-id="2a257-337">The method assumes that the video pictures are progressive scan.</span></span>

> [!Note]  
> <span data-ttu-id="2a257-338">Il processo di conversione dell'analisi interlacciata da 4:2:0 a 4:2:2 presenta problemi atipici ed è difficile da implementare.</span><span class="sxs-lookup"><span data-stu-id="2a257-338">The 4:2:0 to 4:2:2 interlaced scan conversion process presents atypical problems and is difficult to implement.</span></span> <span data-ttu-id="2a257-339">Questo articolo non risolve il problema di conversione dell'analisi interlacciata da 4:2:0 a 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="2a257-339">This article does not address the issue of converting interlaced scan from 4:2:0 to 4:2:2.</span></span>

 

<span data-ttu-id="2a257-340">Consentire a ogni riga verticale di input Chroma samples di essere una matrice `Cin[]` compresa tra 0 e N-1.</span><span class="sxs-lookup"><span data-stu-id="2a257-340">Let each vertical line of input chroma samples be an array `Cin[]` that ranges from 0 to N - 1.</span></span> <span data-ttu-id="2a257-341">La linea verticale corrispondente nell'immagine di output sarà una matrice `Cout[]` che varia da 0 a 2n-1.</span><span class="sxs-lookup"><span data-stu-id="2a257-341">The corresponding vertical line on the output image will be an array `Cout[]` that ranges from 0 to 2N - 1.</span></span> <span data-ttu-id="2a257-342">Per convertire ogni linea verticale, eseguire il processo seguente:</span><span class="sxs-lookup"><span data-stu-id="2a257-342">To convert each vertical line, perform the following process:</span></span>

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

<span data-ttu-id="2a257-343">dove clip () indica il ritaglio a un intervallo compreso tra \[ 0 e 255 \] .</span><span class="sxs-lookup"><span data-stu-id="2a257-343">where clip() denotes clipping to a range of \[0..255\].</span></span>

> [!Note]  
> <span data-ttu-id="2a257-344">Le equazioni per la gestione dei bordi possono essere matematicamente semplificate.</span><span class="sxs-lookup"><span data-stu-id="2a257-344">The equations for handling the edges can be mathematically simplified.</span></span> <span data-ttu-id="2a257-345">Vengono mostrati in questo modulo per illustrare l'effetto di bloccaggio ai bordi dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2a257-345">They are shown in this form to illustrate the clamping effect at the edges of the picture.</span></span>

 

<span data-ttu-id="2a257-346">In effetti, questo metodo calcola ogni valore mancante interpolando la curva sui quattro pixel adiacenti, ponderata in base ai valori dei due pixel più vicini (Figura 11).</span><span class="sxs-lookup"><span data-stu-id="2a257-346">In effect, this method calculates each missing value by interpolating the curve over the four adjacent pixels, weighted toward the values of the two nearest pixels (Figure 11).</span></span> <span data-ttu-id="2a257-347">Il metodo di interpolazione specifico usato in questo esempio genera esempi mancanti in posizioni a metà Integer usando un metodo noto denominato interpolazione Catmull-Rom, nota anche come interpolazione della convoluzione cubica.</span><span class="sxs-lookup"><span data-stu-id="2a257-347">The specific interpolation method used in this example generates missing samples at half-integer positions using a well-known method called Catmull-Rom interpolation, also known as cubic convolution interpolation.</span></span>

![Figura 11.](images/yuvformats14.gif)

<span data-ttu-id="2a257-350">Nei termini di elaborazione dei segnali, la conversione verticale dovrebbe includere idealmente una compensazione dello spostamento della fase per tenere conto dell'offset verticale di metà pixel (rispetto alla griglia di campionamento 4:2:2 di output) tra i percorsi delle righe di esempio 4:2:0 e la posizione di ogni altra riga di esempio 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="2a257-350">In signal processing terms, the vertical upconversion should ideally include a phase shift compensation to account for the half-pixel vertical offset (relative to the output 4:2:2 sampling grid) between the locations of the 4:2:0 sample lines and the location of every other 4:2:2 sample line.</span></span> <span data-ttu-id="2a257-351">Tuttavia, l'introduzione di questo offset aumenterebbe la quantità di elaborazione necessaria per generare gli esempi e renderà impossibile ricostruire gli esempi originali 4:2:0 dall'immagine 4:2:2 sottocampionata.</span><span class="sxs-lookup"><span data-stu-id="2a257-351">However, introducing this offset would increase the amount of processing required to generate the samples, and make it impossible to reconstruct the original 4:2:0 samples from the upsampled 4:2:2 image.</span></span> <span data-ttu-id="2a257-352">Potrebbe anche non essere possibile decodificare il video direttamente in superfici di 4:2:2 e quindi usare tali superfici come immagini di riferimento per la decodifica delle immagini successive nel flusso.</span><span class="sxs-lookup"><span data-stu-id="2a257-352">It would also make it impossible to decode video directly into 4:2:2 surfaces and then use those surfaces as reference pictures for decoding subsequent pictures in the stream.</span></span> <span data-ttu-id="2a257-353">Pertanto, il metodo fornito qui non prende in considerazione l'allineamento verticale preciso degli esempi.</span><span class="sxs-lookup"><span data-stu-id="2a257-353">Therefore, the method provided here does not take into account the precise vertical alignment of the samples.</span></span> <span data-ttu-id="2a257-354">Questa operazione non è probabilmente visivamente dannosa per risoluzioni di immagini ragionevolmente elevate.</span><span class="sxs-lookup"><span data-stu-id="2a257-354">Doing so is probably not visually harmful at reasonably high picture resolutions.</span></span>

<span data-ttu-id="2a257-355">Se si inizia con 4:2:0 video che usa la griglia di campionamento definita nel video H. 261, H. 263 o MPEG-1, la fase degli esempi di Chroma di output 4:2:2 verrà spostata anche da un offset orizzontale a metà pixel rispetto alla spaziatura nella griglia di campionamento luma (un offset di quarto pixel rispetto alla spaziatura della griglia di campionamento Chroma 4:2:2).</span><span class="sxs-lookup"><span data-stu-id="2a257-355">If you start with 4:2:0 video that uses the sampling grid defined in H.261, H.263, or MPEG-1 video, the phase of the output 4:2:2 chroma samples will also be shifted by a half-pixel horizontal offset relative to the spacing on the luma sampling grid (a quarter-pixel offset relative to the spacing of the 4:2:2 chroma sampling grid).</span></span> <span data-ttu-id="2a257-356">Tuttavia, il formato MPEG-2 di 4:2:0 video è probabilmente usato più di frequente nei PC e non subisce questo problema.</span><span class="sxs-lookup"><span data-stu-id="2a257-356">However, the MPEG-2 form of 4:2:0 video is probably more commonly used on PCs and does not suffer from this problem.</span></span> <span data-ttu-id="2a257-357">Inoltre, la distinzione non è probabilmente visivamente dannosa per risoluzioni di immagini ragionevolmente elevate.</span><span class="sxs-lookup"><span data-stu-id="2a257-357">Moreover, the distinction is probably not visually harmful at reasonably high picture resolutions.</span></span> <span data-ttu-id="2a257-358">Il tentativo di correggere questo problema creerebbe lo stesso tipo di problemi trattati per l'offset della fase verticale.</span><span class="sxs-lookup"><span data-stu-id="2a257-358">Trying to correct for this problem would create the same sort of problems discussed for the vertical phase offset.</span></span>

## <a name="converting-422-yuv-to-444-yuv"></a><span data-ttu-id="2a257-359">Conversione da 4:2:2 YUV a 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="2a257-359">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="2a257-360">Per la conversione da YUV a 4:2:2 YUV a 4:4:4 YUV è necessaria una conversione orizzontale per due fattori.</span><span class="sxs-lookup"><span data-stu-id="2a257-360">Converting 4:2:2 YUV to 4:4:4 YUV requires horizontal upconversion by a factor of two.</span></span> <span data-ttu-id="2a257-361">Il metodo descritto in precedenza per la conversione verticale può essere applicato anche alla conversione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="2a257-361">The method described previously for vertical upconversion can also be applied to horizontal upconversion.</span></span> <span data-ttu-id="2a257-362">Per il video MPEG-2 e ITU-R BT. 601, questo metodo produrrà esempi con l'allineamento della fase corretto.</span><span class="sxs-lookup"><span data-stu-id="2a257-362">For MPEG-2 and ITU-R BT.601 video, this method will produce samples with the correct phase alignment.</span></span>

## <a name="converting-420-yuv-to-444-yuv"></a><span data-ttu-id="2a257-363">Conversione da 4:2:0 YUV a 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="2a257-363">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="2a257-364">Per convertire 4:2:0 YUV a 4:4:4 YUV, è possibile seguire semplicemente i due metodi descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="2a257-364">To convert 4:2:0 YUV to 4:4:4 YUV, you can simply follow the two methods described previously.</span></span> <span data-ttu-id="2a257-365">Convertire l'immagine 4:2:0 in 4:2:2 e quindi convertire l'immagine 4:2:2 in 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="2a257-365">Convert the 4:2:0 image to 4:2:2, and then convert the 4:2:2 image to 4:4:4.</span></span> <span data-ttu-id="2a257-366">È anche possibile cambiare l'ordine dei due processi di conversione, perché l'ordine di operazione non è rilevante per la qualità visiva del risultato.</span><span class="sxs-lookup"><span data-stu-id="2a257-366">You can also switch the order of the two upconversion processes, as the order of operation does not really matter to the visual quality of the result.</span></span>

## <a name="other-yuv-formats"></a><span data-ttu-id="2a257-367">Altri formati YUV</span><span class="sxs-lookup"><span data-stu-id="2a257-367">Other YUV Formats</span></span>

<span data-ttu-id="2a257-368">Altri formati YUV meno comuni includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a257-368">Some other, less common YUV formats include the following:</span></span>

-   <span data-ttu-id="2a257-369">AI44 è un formato YUV pallettizzati con 8 bit per campione.</span><span class="sxs-lookup"><span data-stu-id="2a257-369">AI44 is a palettized YUV format with 8 bits per sample.</span></span> <span data-ttu-id="2a257-370">Ogni esempio contiene un indice nei 4 bit più significativi (MSBs) e un valore alfa nei 4 bit meno significativi (LSB).</span><span class="sxs-lookup"><span data-stu-id="2a257-370">Each sample contains an index in the 4 most significant bits (MSBs) and an alpha value in the 4 least significant bits (LSBs).</span></span> <span data-ttu-id="2a257-371">L'indice fa riferimento a una matrice di voci della tavolozza YUV, che devono essere definite nel tipo di supporto per il formato.</span><span class="sxs-lookup"><span data-stu-id="2a257-371">The index refers to an array of YUV palette entries, which must be defined in the media type for the format.</span></span> <span data-ttu-id="2a257-372">Questo formato viene utilizzato principalmente per le immagini di sottoimmagine.</span><span class="sxs-lookup"><span data-stu-id="2a257-372">This format is primarily used for subpicture images.</span></span>
-   <span data-ttu-id="2a257-373">NV11 è un formato Planar 4:1:1 con 12 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="2a257-373">NV11 is a 4:1:1 planar format with 12 bits per pixel.</span></span> <span data-ttu-id="2a257-374">Gli esempi Y vengono visualizzati per primi in memoria.</span><span class="sxs-lookup"><span data-stu-id="2a257-374">The Y samples appear first in memory.</span></span> <span data-ttu-id="2a257-375">Il piano Y è seguito da una matrice di campioni U (CB) e V (CR) compressi.</span><span class="sxs-lookup"><span data-stu-id="2a257-375">The Y plane is followed by an array of packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="2a257-376">Quando l'array U-V combinato viene considerato come una matrice di valori di **parola** little-endian, gli esempi u sono contenuti nel LSB di ogni **parola** e gli esempi V sono contenuti in MSBs.</span><span class="sxs-lookup"><span data-stu-id="2a257-376">When the combined U-V array is addressed as an array of little-endian **WORD** values, the U samples are contained in the LSBs of each **WORD**, and the V samples are contained in the MSBs.</span></span> <span data-ttu-id="2a257-377">Questo layout di memoria è simile a NV12, anche se il campionamento Chroma è diverso.</span><span class="sxs-lookup"><span data-stu-id="2a257-377">(This memory layout is similar to NV12 although the chroma sampling is different.)</span></span>
-   <span data-ttu-id="2a257-378">Y41P è un formato compresso 4:1:1, con l'utente e la V campionati ogni quarto pixel orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="2a257-378">Y41P is a 4:1:1 packed format, with U and V sampled every fourth pixel horizontally.</span></span> <span data-ttu-id="2a257-379">Ogni macropixel contiene 8 pixel in tre byte, con il seguente layout di byte: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span><span class="sxs-lookup"><span data-stu-id="2a257-379">Each macropixel contains 8 pixels in three bytes, with the following byte layout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span></span>
-   <span data-ttu-id="2a257-380">Y41T è identico a Y41P, ad eccezione del bit meno significativo di ogni esempio Y che specifica il tasto Chroma (0 = transparent, 1 = opaque).</span><span class="sxs-lookup"><span data-stu-id="2a257-380">Y41T is identical to Y41P, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="2a257-381">Y42T è identico a UYVY, ad eccezione del bit meno significativo di ogni esempio Y che specifica il tasto Chroma (0 = transparent, 1 = opaque).</span><span class="sxs-lookup"><span data-stu-id="2a257-381">Y42T is identical to UYVY, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="2a257-382">YVYU è equivalente a YUYV, ad eccezione del fatto che gli esempi di i e V sono stati scambiati.</span><span class="sxs-lookup"><span data-stu-id="2a257-382">YVYU is equivalent to YUYV except the U and V samples are swapped.</span></span>

## <a name="identifying-yuv-formats-in-media-foundation"></a><span data-ttu-id="2a257-383">Identificazione dei formati YUV in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a257-383">Identifying YUV Formats in Media Foundation</span></span>

<span data-ttu-id="2a257-384">Per ognuno dei formati YUV descritti in questo articolo è stato assegnato un codice FOURCC.</span><span class="sxs-lookup"><span data-stu-id="2a257-384">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="2a257-385">Un codice FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="2a257-385">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

<span data-ttu-id="2a257-386">Sono disponibili diverse macro C/C++ che semplificano la dichiarazione di valori FOURCC nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="2a257-386">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="2a257-387">La macro **MAKEFOURCC** , ad esempio, è dichiarata in mmsystem. h e la macro **FCC** è dichiarata in Aviriff. h.</span><span class="sxs-lookup"><span data-stu-id="2a257-387">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="2a257-388">Utilizzarli come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2a257-388">Use them as follows:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

<span data-ttu-id="2a257-389">È anche possibile dichiarare direttamente un codice FOURCC come valore letterale stringa semplicemente invertendo l'ordine dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="2a257-389">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="2a257-390">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2a257-390">For example:</span></span>

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

<span data-ttu-id="2a257-391">Invertire l'ordine è necessario perché il sistema operativo Windows usa un'architettura little-endian.</span><span class="sxs-lookup"><span data-stu-id="2a257-391">Reversing the order is necessary because the Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="2a257-392">' Y ' = 0x59,' U ' = 0x55 è 2' = 0x32, quindi ' 2YUY ' è 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="2a257-392">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

<span data-ttu-id="2a257-393">In Media Foundation i formati sono identificati da un GUID di tipo principale e da un GUID del sottotipo.</span><span class="sxs-lookup"><span data-stu-id="2a257-393">In Media Foundation, formats are identified by a major type GUID and a subtype GUID.</span></span> <span data-ttu-id="2a257-394">Il tipo principale per i formati video del computer è sempre \_ video MFMediaType.</span><span class="sxs-lookup"><span data-stu-id="2a257-394">The major type for computer video formats is always MFMediaType\_Video .</span></span> <span data-ttu-id="2a257-395">Il sottotipo può essere costruito eseguendo il mapping del codice FOURCC a un GUID, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2a257-395">The subtype can be constructed by mapping the FOURCC code to a GUID, as follows:</span></span>

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="2a257-396">dove `XXXXXXXX` è il codice FourCC.</span><span class="sxs-lookup"><span data-stu-id="2a257-396">where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="2a257-397">Pertanto, il GUID del sottotipo per YUY2 è:</span><span class="sxs-lookup"><span data-stu-id="2a257-397">Thus, the subtype GUID for YUY2 is:</span></span>

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="2a257-398">Le costanti per i GUID di formato YUV più comuni sono definite nel file di intestazione mfapi. h.</span><span class="sxs-lookup"><span data-stu-id="2a257-398">Constants for the most common YUV format GUIDs are defined in the header file mfapi.h.</span></span> <span data-ttu-id="2a257-399">Per un elenco di queste costanti, vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="2a257-399">For a list of these constants, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a257-400">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a257-400">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a257-401">Video su YUV</span><span class="sxs-lookup"><span data-stu-id="2a257-401">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="2a257-402">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="2a257-402">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



