---
description: Segnala lo stato di avanzamento di un oggetto abilitatore del contenuto. Gli oggetti che espongono l'interfaccia IMFContentEnabler possono generare questo evento per notificare all'applicazione lo stato di avanzamento delle azioni di abilitazione del contenuto.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Evento MEEnablerProgress (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226665"
---
# <a name="meenablerprogress-event"></a>Evento MEEnablerProgress

Segnala lo stato di avanzamento di un oggetto abilitatore del contenuto. Gli oggetti che espongono l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) possono generare questo evento per notificare all'applicazione lo stato di avanzamento delle azioni del Content Enabler.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE               | Descrizione                                                               |
|-----------------------|---------------------------------------------------------------------------|
| \_LPWSTR VT<br/> | Stringa di caratteri wide che descrive lo stato di avanzamento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Per ricevere questo evento, eseguire una query sull'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) per l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Chiamare quindi [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), come descritto nell'argomento [generatori di eventi multimediali](media-event-generators.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Generatori di eventi multimediali](media-event-generators.md)
</dt> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




