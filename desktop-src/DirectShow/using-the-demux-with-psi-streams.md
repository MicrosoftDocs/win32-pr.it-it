---
description: Uso di Demux con flussi PSI
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: Uso di Demux con flussi PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659e4a12bfef25f24a5e6cac38d191f86ab80b4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314394"
---
# <a name="using-the-demux-with-psi-streams"></a><span data-ttu-id="97f5b-103">Uso di Demux con flussi PSI</span><span class="sxs-lookup"><span data-stu-id="97f5b-103">Using the Demux with PSI Streams</span></span>

<span data-ttu-id="97f5b-104">Per ottenere informazioni PSI da un flusso di trasporto MPEG-2 usando il filtro MPEG-2 demux, creare un pin di output in Demux con il seguente tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="97f5b-104">To get PSI information from an MPEG-2 transport stream using the MPEG-2 demux filter, create an output pin on the demux with the following media type:</span></span>

-   <span data-ttu-id="97f5b-105">Tipo principale: KSDATAFORMAT di \_ tipo \_ MPEG2 \_ sezioni</span><span class="sxs-lookup"><span data-stu-id="97f5b-105">Major type: KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>
-   <span data-ttu-id="97f5b-106">Sottotipo: MEDIASUBTYPE \_ None</span><span class="sxs-lookup"><span data-stu-id="97f5b-106">Subtype: MEDIASUBTYPE\_None</span></span>
-   <span data-ttu-id="97f5b-107">Tipo di formato: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="97f5b-107">Format type: GUID\_NULL</span></span>

<span data-ttu-id="97f5b-108">Chiamare quindi il metodo [**IMPEG2PIDMap:: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) del PIN di output con il PID desiderato e il flag media \_ MPEG2 \_ psi.</span><span class="sxs-lookup"><span data-stu-id="97f5b-108">Then call the output pin's [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) method with the desired PID and the flag MEDIA\_MPEG2\_PSI.</span></span>


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux = NULL;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Define the media type.
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
    mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;
    mt.subtype = MEDIASUBTYPE_None;

    // Create a new output pin.
    IPin *pPin;
    hr = pDemux->CreateOutputPin(&mt, L"PSI Pin", &pPin);
    if (SUCCEEDED(hr))
    {
        // Map the PID.
        IMPEG2PIDMap *pPidMap = NULL;
        hr = pPin->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
        if (SUCCEEDED(hr))
        {
            ULONG Pid[] = { 0x00 }; // Map any desired PIDs. 
            ULONG cPid = 1;
            hr = pPidMap->MapPID(cPid, Pid, MEDIA_MPEG2_PSI);
            pPidMap->Release();
        }
        pPin->Release();
    }
    pDemux->Release();
}
```



<span data-ttu-id="97f5b-109">Ogni sezione complete PSI viene fornita in un esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="97f5b-109">Each complete PSI section is delivered in one media sample.</span></span> <span data-ttu-id="97f5b-110">Per recuperare il numero PID associato a una sezione della tabella, chiamare [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="97f5b-110">To retrieve the PID number associated with a table section, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the media sample.</span></span> <span data-ttu-id="97f5b-111">Il PID viene fornito nei 13 bit meno significativi del flag **dwTypeSpecificFlags** nella struttura delle **\_ \_ Proprietà SAMPLE2** .</span><span class="sxs-lookup"><span data-stu-id="97f5b-111">The PID is given in the low 13 bits of the **dwTypeSpecificFlags** flag in the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="97f5b-112">Questa opzione è utile se si esegue il mapping di più PID PSI allo stesso pin di output.</span><span class="sxs-lookup"><span data-stu-id="97f5b-112">This is useful if you map multiple PSI PIDs to the same output pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97f5b-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97f5b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97f5b-114">Uso del Demultiplexer MPEG-2</span><span class="sxs-lookup"><span data-stu-id="97f5b-114">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



