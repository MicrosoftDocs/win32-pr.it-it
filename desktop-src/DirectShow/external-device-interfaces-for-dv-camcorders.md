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
# <a name="external-device-interfaces-for-dv-camcorders"></a>Interfacce di dispositivo esterne per i camcorder DV

Il [filtro Acquisizione video WDM](wdm-video-capture-filter.md) espone tre interfacce per il controllo di un camcorder.



| Label | Valore |
|------------------------------------------------|-------------------------------------------------|
| [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | Interfaccia di base per il controllo del dispositivo esterno. |
| [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | Controlla le funzioni vcr.                     |
| [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | Legge il codice temporale dal dispositivo.                 |



 

> [!Note]  
> Per usare queste interfacce con il driver del camcorder MSDV, includere il file di intestazione XPrtDefs.h nel progetto.

 

Dopo aver selezionato un dispositivo di acquisizione e aver creato un'istanza del filtro di acquisizione, eseguire una query sul filtro per queste interfacce. L'esempio seguente dichiara una struttura personalizzata che contiene i puntatori a interfaccia, insieme ai valori booleani che specificano la disponibilità di ogni interfaccia:


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

[Controllo di un camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



