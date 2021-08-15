---
description: Generato da un'origine multimediale che fornisce topologie tramite l'interfaccia IMFMediaSourceTopologyProvider, ad esempio l'origine sequencer. L'origine genera l'evento quando ha una nuova presentazione. La sessione multimediale inoltra questo evento all'applicazione.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Evento MENewPresentation (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2adec5b3dbb8544e537bdcc8f5c724130175b3167f9c51dc005112fdbd9a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228881"
---
# <a name="menewpresentation-event"></a>EVENTO MENewPresentation

Generato da un'origine multimediale che fornisce topologie tramite [**l'interfaccia IMFMediaSourceTopologyProvider,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) ad esempio l'origine sequencer. L'origine genera l'evento quando ha una nuova presentazione. La sessione multimediale inoltra questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntatore [**all'interfaccia IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descrittore di presentazione per la nuova presentazione.<br/> <br/> |



## <a name="remarks"></a>Commenti

L'applicazione può ottenere la topologia che corrisponde al descrittore di presentazione chiamando [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) nell'origine multimediale. L'applicazione può quindi accodare la nuova topologia nella sessione multimediale chiamando [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> <dt>

[Origine Sequencer](sequencer-source.md)
</dt> </dl>

 

 




