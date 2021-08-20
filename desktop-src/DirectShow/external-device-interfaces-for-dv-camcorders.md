---
description: Interfacce di dispositivo esterne per i videocamere DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfacce di dispositivo esterne per i videocamere DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80a89356a18d25f1fb3536cdc8f6e95be4e1947433d1c0437f1d80d47c8008
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651521"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a>Interfacce di dispositivo esterne per i videocamere DV

Il [filtro WdM Video Capture](wdm-video-capture-filter.md) espone tre interfacce per il controllo di un videocamere.



| Etichetta | Valore |
|------------------------------------------------|-------------------------------------------------|
| [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | Interfaccia di base per il controllo dispositivo esterno. |
| [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | Controlla le funzioni vcr.                     |
| [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | Legge il timecode dal dispositivo.                 |



 

> [!Note]  
> Per usare queste interfacce con il driver del camcorder MSDV, includere il file di intestazione XPrtDefs.h nel progetto.

 

Dopo aver selezionato un dispositivo di acquisizione e creato un'istanza del filtro di acquisizione, eseguire una query sul filtro per queste interfacce. L'esempio seguente dichiara una struttura personalizzata che contiene i puntatori a interfaccia, insieme a valori booleani che specificano la disponibilità di ogni interfaccia:


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

[Controllo di un videocamere DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



