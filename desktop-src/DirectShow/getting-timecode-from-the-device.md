---
description: Recupero del codice temporale dal dispositivo
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Recupero del codice temporale dal dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303764"
---
# <a name="getting-timecode-from-the-device"></a><span data-ttu-id="5f81d-103">Recupero del codice temporale dal dispositivo</span><span class="sxs-lookup"><span data-stu-id="5f81d-103">Getting Timecode from the Device</span></span>

<span data-ttu-id="5f81d-104">Mentre un nastro DV viene riprodotto o è in modalità di sospensione dei record, è possibile recuperare il timecode SMPTE o il numero di traccia assoluto.</span><span class="sxs-lookup"><span data-stu-id="5f81d-104">While a DV tape is playing or is in record-pause mode, you can retrieve the SMPTE timecode or the absolute track number.</span></span> <span data-ttu-id="5f81d-105">A tale scopo, chiamare il metodo [**IAMTimecodeReader:: gettimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) .</span><span class="sxs-lookup"><span data-stu-id="5f81d-105">To do this, call the [**IAMTimecodeReader::GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) method.</span></span> <span data-ttu-id="5f81d-106">Questo metodo accetta un puntatore a una struttura di [**\_ esempio del timecode**](/windows/win32/api/strmif/ns-strmif-timecode_sample) , che descrive il timecode.</span><span class="sxs-lookup"><span data-stu-id="5f81d-106">This method takes a pointer to a [**TIMECODE\_SAMPLE**](/windows/win32/api/strmif/ns-strmif-timecode_sample) structure, which describes the timecode.</span></span> <span data-ttu-id="5f81d-107">Prima di chiamare il metodo, inizializzare il membro **dwFlags** della struttura.</span><span class="sxs-lookup"><span data-stu-id="5f81d-107">Before calling the method, initialize the **dwFlags** member of the structure.</span></span> <span data-ttu-id="5f81d-108">Usare il valore \_ DEVCAP \_ timecode \_ Read per recuperare il timecode oppure il valore ed \_ DEVCAP \_ ATN \_ Read per recuperare il numero di traccia assoluto.</span><span class="sxs-lookup"><span data-stu-id="5f81d-108">Use the value ED\_DEVCAP\_TIMECODE\_READ to retrieve the timecode or the value ED\_DEVCAP\_ATN\_READ to retrieve the absolute track number.</span></span>

<span data-ttu-id="5f81d-109">Il membro **timecode** della struttura **di \_ esempio timecode** è una struttura del timecode.</span><span class="sxs-lookup"><span data-stu-id="5f81d-109">The **timecode** member of the **TIMECODE\_SAMPLE** structure is a TIMECODE structure.</span></span> <span data-ttu-id="5f81d-110">Quando il metodo restituisce un risultato, il membro **dwFrames** della struttura del timecode contiene il timecode o il numero di traccia.</span><span class="sxs-lookup"><span data-stu-id="5f81d-110">When the method returns, the **dwFrames** member of the TIMECODE structure contains the timecode or track number.</span></span> <span data-ttu-id="5f81d-111">Per il timecode, le ore, i minuti, i secondi e i frame vengono compressi in un valore DWORD come valori decimali codificati binari (BCD), con il formato *hhmmssff*.</span><span class="sxs-lookup"><span data-stu-id="5f81d-111">For timecode, the hours, minutes, seconds, and frames are packed into a DWORD as binary coded decimal (BCD) values, with the format *hhmmssff*.</span></span> <span data-ttu-id="5f81d-112">Utilizzare le maschere di maschera per estrarre i singoli valori.</span><span class="sxs-lookup"><span data-stu-id="5f81d-112">Use bitmasks to extract the individual values.</span></span>

<span data-ttu-id="5f81d-113">Nell'esempio seguente vengono recuperati il codice temporale e il numero di traccia.</span><span class="sxs-lookup"><span data-stu-id="5f81d-113">The following example retrieves the timecode and track number.</span></span>


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="5f81d-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f81d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f81d-115">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="5f81d-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
