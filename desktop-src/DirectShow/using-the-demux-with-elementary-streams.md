---
description: Uso di Demux con flussi elementari
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Uso di Demux con flussi elementari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b9004d6c99db96405797016b0d9854c96dae92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346396"
---
# <a name="using-the-demux-with-elementary-streams"></a><span data-ttu-id="003ee-103">Uso di Demux con flussi elementari</span><span class="sxs-lookup"><span data-stu-id="003ee-103">Using the Demux with Elementary Streams</span></span>

<span data-ttu-id="003ee-104">Quando il demux MPEG-2 fornisce payload di PES, invia il flusso di byte ES in batch di esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="003ee-104">When the MPEG-2 demux delivers PES payloads, it sends the ES byte stream in batches of media samples.</span></span> <span data-ttu-id="003ee-105">La dimensione predefinita del campione è 8 KB.</span><span class="sxs-lookup"><span data-stu-id="003ee-105">The default sample size is 8K.</span></span> <span data-ttu-id="003ee-106">Il demux avvia un nuovo esempio di supporto in ogni limite PES, ma può suddividere un singolo payload di PES in diversi esempi.</span><span class="sxs-lookup"><span data-stu-id="003ee-106">The demux starts a new media sample on each PES boundary, but may break a single PES payload into several samples.</span></span> <span data-ttu-id="003ee-107">Se, ad esempio, un payload PES è 20.000, verrà distribuito in due campioni da 8 KB seguiti da un campione 4K.</span><span class="sxs-lookup"><span data-stu-id="003ee-107">For example, if a PES payload is 20K, it will be delivered in two 8K samples followed by one 4K sample.</span></span> <span data-ttu-id="003ee-108">Demux non esamina il contenuto del flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="003ee-108">The demux does not examine the contents of the byte stream.</span></span> <span data-ttu-id="003ee-109">Il decodificatore analizza le intestazioni di sequenza e cerca le modifiche del formato.</span><span class="sxs-lookup"><span data-stu-id="003ee-109">It is up to the decoder to parse the sequence headers and look for format changes.</span></span>

<span data-ttu-id="003ee-110">Quando il pin di output del filtro demux si connette al decodificatore, offre il tipo di supporto che è stato specificato al momento della creazione del PIN.</span><span class="sxs-lookup"><span data-stu-id="003ee-110">When the demux filter's output pin connects to the decoder, it offers the media type that was specified when the pin was created.</span></span> <span data-ttu-id="003ee-111">Poiché demux non esamina il flusso di byte ES, non convalida il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="003ee-111">Because the demux does not examine the ES byte stream, it does not validate the media type.</span></span> <span data-ttu-id="003ee-112">In teoria, un decodificatore MPEG-2 dovrebbe essere in grado di connettersi solo con il tipo e il sottotipo principale, per indicare il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="003ee-112">In theory, an MPEG-2 decoder should be able to connect with just the major type and subtype filled in, to indicate the type of data.</span></span> <span data-ttu-id="003ee-113">Il decodificatore deve quindi esaminare le intestazioni di sequenza che arrivano negli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="003ee-113">The decoder should then examine the sequence headers that arrive in the media samples.</span></span> <span data-ttu-id="003ee-114">Tuttavia, in pratica, molti decodificatori non si connetteranno, a meno che il tipo di supporto non includa un blocco di formato completo.</span><span class="sxs-lookup"><span data-stu-id="003ee-114">However, in practice, many decoders will not connect unless the media type includes a complete format block.</span></span>

<span data-ttu-id="003ee-115">Si supponga, ad esempio, che PID 0x31 contenga il video del profilo principale MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="003ee-115">For example, suppose that PID 0x31 contains MPEG-2 main profile video.</span></span> <span data-ttu-id="003ee-116">Come minimo, è necessario eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="003ee-116">At a minimum, you would need to do the following steps.</span></span>

<span data-ttu-id="003ee-117">Per prima cosa, creare un tipo di supporto per il video MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="003ee-117">First, create a media type for MPEG-2 video.</span></span> <span data-ttu-id="003ee-118">A questo punto, lasciare il blocco di formato:</span><span class="sxs-lookup"><span data-stu-id="003ee-118">Leaving aside the format block for now:</span></span>


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



<span data-ttu-id="003ee-119">Successivamente, creare un pin di output in Demux:</span><span class="sxs-lookup"><span data-stu-id="003ee-119">Next, create an output pin on the demux:</span></span>


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Create a new output pin.
    IPin *pPin0;
    hr = pDemux->CreateOutputPin(&mt, L"Video Pin", &pPin0);
    if (SUCCEEDED(hr))
    {
        ....
    }
}
```



<span data-ttu-id="003ee-120">Eseguire quindi una query sul nuovo PIN per l'interfaccia **IMPEG2PIDMap** e chiamare **MapPID**.</span><span class="sxs-lookup"><span data-stu-id="003ee-120">Then, query the new pin for the **IMPEG2PIDMap** interface and call **MapPID**.</span></span> <span data-ttu-id="003ee-121">Specificare il numero PID 0x30 e il \_ flusso elementare multimediale \_ per i payload PES.</span><span class="sxs-lookup"><span data-stu-id="003ee-121">Specify PID number 0x30, and MEDIA\_ELEMENTARY\_STREAM for PES payloads.</span></span>


```C++
// Query the pin for IMPEG2PIDMap. This implicitly configures the
// demux to carry a transport stream. 
IMPEG2PIDMap *pPidMap;
hr = pPin0->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
if (SUCCEEDED(hr))
{
    // Assign PID 0x31 to pin 0. Set the type to "PES payload."
    ULONG Pid = 0x031;
    hr = pPidMap->MapPID(1, &Pid, MEDIA_ELEMENTARY_STREAM);
    pPidMap->Release();
}
```



<span data-ttu-id="003ee-122">Infine, rilasciare tutte le interfacce al termine dell'operazione:</span><span class="sxs-lookup"><span data-stu-id="003ee-122">Finally, release all interfaces when you are done:</span></span>


```C++
pPin0->Release();
pDemux->Release();
```



<span data-ttu-id="003ee-123">Di seguito è riportato un esempio più completo di impostazione del tipo di supporto, incluso il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="003ee-123">Here is a more complete example of setting the media type, including the format block.</span></span> <span data-ttu-id="003ee-124">In questo esempio si presuppone ancora un video del profilo principale MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="003ee-124">This example still assumes an MPEG-2 main profile video.</span></span> <span data-ttu-id="003ee-125">I dettagli variano a seconda del contenuto del flusso:</span><span class="sxs-lookup"><span data-stu-id="003ee-125">The details will vary depending on stream contents:</span></span>


```C++
// Set up a byte array to hold the first sequence header. 
// This may or may not be required, depending on the decoder.
BYTE SeqHdr[] = { ... };  // Contains the sequence header (not shown).

AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
mt.formattype = FORMAT_MPEG2Video;

// Allocate the format block, including space for the sequence header. 
mt.cbFormat = sizeof(MPEG2VIDEOINFO) + sizeof(SeqHdr);
mt.pbFormat = (BYTE*)CoTaskMemAlloc(mt.cbFormat);
if (mt.pbFormat == NULL)
{
    // Out of memory; return an error code.
}
ZeroMemory(mt.pbFormat, mt.cbFormat);

// Cast the buffer pointer to an MPEG2VIDEOINFO struct.
MPEG2VIDEOINFO *pMVIH = (MPEG2VIDEOINFO*)mt.pbFormat;

RECT rcSrc = {0, 480, 0, 720};        // Source rectangle.
pMVIH->hdr.rcSource = rcSrc;
pMVIH->hdr.dwBitRate = 4000000;       // Bit rate.
pMVIH->hdr.AvgTimePerFrame = 333667;  // 29.97 fps.
pMVIH->hdr.dwPictAspectRatioX = 4;    // 4:3 aspect ratio.
pMVIH->hdr.dwPictAspectRatioY = 3;

// BITMAPINFOHEADER information.
pMVIH->hdr.bmiHeader.biSize = 40;
pMVIH->hdr.bmiHeader.biWidth = 720;
pMVIH->hdr.bmiHeader.biHeight = 480;

pMVIH->dwLevel = AM_MPEG2Profile_Main;  // MPEG-2 profile. 
pMVIH->dwProfile = AM_MPEG2Level_Main;  // MPEG-2 level.

// Copy the sequence header into the format block.
pMVIH->cbSequenceHeader = sizeof(SeqHdr); // Size of sequence header.
memcpy(pMVIH->dwSequenceHeader, SeqHdr, sizeof(SeqHdr));
```



## <a name="related-topics"></a><span data-ttu-id="003ee-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="003ee-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="003ee-127">Uso del Demultiplexer MPEG-2</span><span class="sxs-lookup"><span data-stu-id="003ee-127">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



