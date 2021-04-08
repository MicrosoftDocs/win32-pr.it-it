---
description: Interfacce del dispositivo esterno per videocamere DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfacce del dispositivo esterno per videocamere DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52b6d0fe00ff91ff87e9c810bbe7ecc319e9bfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103877109"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="cc0ec-103">Interfacce del dispositivo esterno per videocamere DV</span><span class="sxs-lookup"><span data-stu-id="cc0ec-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="cc0ec-104">Il filtro di [acquisizione video WDM](wdm-video-capture-filter.md) espone tre interfacce per il controllo di una videocamera.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="cc0ec-105">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="cc0ec-105">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="cc0ec-106">Interfaccia di base per il controllo del dispositivo esterno.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-106">The base interface for external device control.</span></span> |
| [<span data-ttu-id="cc0ec-107">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="cc0ec-107">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="cc0ec-108">Controlla le funzioni VCR.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-108">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="cc0ec-109">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="cc0ec-109">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="cc0ec-110">Legge il timecode dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-110">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="cc0ec-111">Per usare queste interfacce con il driver della videocamera MSDV, includere il file di intestazione XPrtDefs. h nel progetto.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-111">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="cc0ec-112">Dopo aver selezionato un dispositivo di acquisizione e creato un'istanza del filtro di acquisizione, eseguire una query sul filtro per tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="cc0ec-112">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="cc0ec-113">Nell'esempio seguente viene dichiarata una struttura personalizzata che include i puntatori di interfaccia, oltre a valori booleani che specificano la disponibilità di ogni interfaccia:</span><span class="sxs-lookup"><span data-stu-id="cc0ec-113">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a><span data-ttu-id="cc0ec-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc0ec-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc0ec-115">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="cc0ec-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



