---
description: Inviato dalla pipeline al codificatore MFT in modo seriale con esempi multimediali tramite IMFTransform::P rocessEvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Evento MEEncodingParameters (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2230640adf1f92111569a39558f2959271a23ea2b5dbe5d0d915b6a2b989d371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723831"
---
# <a name="meencodingparameters-event"></a>EVENTO MEEncodingParameters

Inviato dalla pipeline al codificatore MFT in modo seriale con esempi multimediali tramite [**IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                         | Descrizione                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**Attributi IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | Contiene le nuove impostazioni basate su ICodecAPI che il codificatore deve applicare agli esempi in ingresso successivi.<br/> <br/> |



## <a name="remarks"></a>Commenti

Il payload dell'evento è un archivio attributi (puntatore IMFAttributes) che contiene le nuove impostazioni /// basate su ICodecAPI che il codificatore deve applicare agli esempi in ingresso successivi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




