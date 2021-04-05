---
description: Formato segnale
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato segnale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876641"
---
# <a name="signal-format"></a><span data-ttu-id="79049-103">Formato segnale</span><span class="sxs-lookup"><span data-stu-id="79049-103">Signal Format</span></span>

<span data-ttu-id="79049-104">Il formato del segnale di una videocamera DV può essere NTSC o PAL, standard o Long-Play.</span><span class="sxs-lookup"><span data-stu-id="79049-104">A DV camcorder's signal format can be NTSC or PAL, standard or long-play.</span></span>

<span data-ttu-id="79049-105">**Driver MSDV**</span><span class="sxs-lookup"><span data-stu-id="79049-105">**MSDV Driver**</span></span>

<span data-ttu-id="79049-106">Per ottenere il formato del segnale di input dal driver MSDV, chiamare il metodo [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) e passare il flag del segnale di input di ed \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="79049-106">To get the input signal format from the MSDV driver, call the [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) method and pass in the ED\_TRANSBASIC\_INPUT\_SIGNAL flag.</span></span> <span data-ttu-id="79049-107">Il metodo restituisce una costante definita, che indica il formato.</span><span class="sxs-lookup"><span data-stu-id="79049-107">The method returns a defined constant, indicating the format.</span></span>

<span data-ttu-id="79049-108">Il codice seguente controlla il formato del segnale e usa questo valore per calcolare il tempo medio per frame.</span><span class="sxs-lookup"><span data-stu-id="79049-108">The following code checks the signal format, and uses this value to calculates the average time per frame.</span></span> <span data-ttu-id="79049-109">La modalità variabile riceve la costante del formato del segnale.</span><span class="sxs-lookup"><span data-stu-id="79049-109">The variable Mode receives the signal-format constant.</span></span>


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



<span data-ttu-id="79049-110">Per ottenere il formato del segnale di output, chiamare lo stesso metodo con il flag del segnale di output di ED \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="79049-110">To get the output signal format, call the same method with the ED\_TRANSBASIC\_OUTPUT\_SIGNAL flag.</span></span>

<span data-ttu-id="79049-111">**Driver UVC**</span><span class="sxs-lookup"><span data-stu-id="79049-111">**UVC Driver**</span></span>

<span data-ttu-id="79049-112">Per ottenere il formato del segnale di input o output dal driver UVC, chiamare [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) sul pin ed esaminare il blocco del formato video.</span><span class="sxs-lookup"><span data-stu-id="79049-112">To get the input or output signal format from the UVC driver, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) on the pin and examine the video format block.</span></span> <span data-ttu-id="79049-113">Per i dispositivi UVC, il codice illustrato nell'esempio precedente restituisce in genere ED \_ \_Segnale transbasic \_ sconosciuto, quindi non è affidabile.</span><span class="sxs-lookup"><span data-stu-id="79049-113">(For UVC devices, the code shown in the previous example usually returns ED\_TRANSBASIC\_SIGNAL\_UNKNOWN, so it is not reliable.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="79049-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79049-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79049-115">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="79049-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



