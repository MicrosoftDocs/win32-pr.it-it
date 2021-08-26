---
description: Segnala lo stato di avanzamento di un oggetto content enabler. Gli oggetti che espongono l'interfaccia IMFContentEnabler possono generare questo evento per notificare all'applicazione lo stato delle azioni di abilitazione del contenuto.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Evento MEEnablerProgress (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9772a076e1d9de0cff2336b4c6d6b9b068f11e4fc572b44f0f914a8353f651bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013761"
---
# <a name="meenablerprogress-event"></a>Evento MEEnablerProgress

Segnala lo stato di avanzamento di un oggetto content enabler. Gli oggetti che espongono [**l'interfaccia IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) possono generare questo evento per notificare all'applicazione lo stato delle azioni dell'abilitazione del contenuto.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE               | Descrizione                                                               |
|-----------------------|---------------------------------------------------------------------------|
| VT \_ LPWSTR<br/> | Stringa di caratteri wide che descrive lo stato di avanzamento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Per ricevere questo evento, eseguire una query [**sull'interfaccia IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) per [**l'interfaccia IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Chiamare quindi [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), come descritto nell'argomento [Generatori di eventi multimediali](media-event-generators.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Generatori di eventi multimediali](media-event-generators.md)
</dt> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




