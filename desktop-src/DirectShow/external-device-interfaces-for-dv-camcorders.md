---
description: Interfacce di dispositivo esterne per i camcorder DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfacce di dispositivo esterne per i camcorder DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e7106ec6e9b744da0d1f71958aeb895ec8df1a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909799"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="72160-103">Interfacce di dispositivo esterne per i camcorder DV</span><span class="sxs-lookup"><span data-stu-id="72160-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="72160-104">Il [filtro Acquisizione video WDM](wdm-video-capture-filter.md) espone tre interfacce per il controllo di un camcorder.</span><span class="sxs-lookup"><span data-stu-id="72160-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



| <span data-ttu-id="72160-105">Label</span><span class="sxs-lookup"><span data-stu-id="72160-105">Label</span></span> | <span data-ttu-id="72160-106">Valore</span><span class="sxs-lookup"><span data-stu-id="72160-106">Value</span></span> |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="72160-107">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="72160-107">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="72160-108">Interfaccia di base per il controllo del dispositivo esterno.</span><span class="sxs-lookup"><span data-stu-id="72160-108">The base interface for external device control.</span></span> |
| [<span data-ttu-id="72160-109">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="72160-109">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="72160-110">Controlla le funzioni vcr.</span><span class="sxs-lookup"><span data-stu-id="72160-110">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="72160-111">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="72160-111">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="72160-112">Legge il codice temporale dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72160-112">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="72160-113">Per usare queste interfacce con il driver del camcorder MSDV, includere il file di intestazione XPrtDefs.h nel progetto.</span><span class="sxs-lookup"><span data-stu-id="72160-113">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="72160-114">Dopo aver selezionato un dispositivo di acquisizione e aver creato un'istanza del filtro di acquisizione, eseguire una query sul filtro per queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="72160-114">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="72160-115">L'esempio seguente dichiara una struttura personalizzata che contiene i puntatori a interfaccia, insieme ai valori booleani che specificano la disponibilità di ogni interfaccia:</span><span class="sxs-lookup"><span data-stu-id="72160-115">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="72160-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72160-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72160-117">Controllo di un camcorder DV</span><span class="sxs-lookup"><span data-stu-id="72160-117">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



