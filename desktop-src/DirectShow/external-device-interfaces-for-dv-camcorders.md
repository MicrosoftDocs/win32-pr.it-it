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
# <a name="external-device-interfaces-for-dv-camcorders"></a>Interfacce del dispositivo esterno per videocamere DV

Il filtro di [acquisizione video WDM](wdm-video-capture-filter.md) espone tre interfacce per il controllo di una videocamera.



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | Interfaccia di base per il controllo del dispositivo esterno. |
| [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | Controlla le funzioni VCR.                     |
| [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | Legge il timecode dal dispositivo.                 |



 

> [!Note]  
> Per usare queste interfacce con il driver della videocamera MSDV, includere il file di intestazione XPrtDefs. h nel progetto.

 

Dopo aver selezionato un dispositivo di acquisizione e creato un'istanza del filtro di acquisizione, eseguire una query sul filtro per tali interfacce. Nell'esempio seguente viene dichiarata una struttura personalizzata che include i puntatori di interfaccia, oltre a valori booleani che specificano la disponibilità di ogni interfaccia:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



