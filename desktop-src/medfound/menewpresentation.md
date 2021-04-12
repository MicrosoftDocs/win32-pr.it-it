---
description: Generato da un'origine multimediale che fornisce topologie tramite l'interfaccia IMFMediaSourceTopologyProvider, ad esempio l'origine del sequencer. L'origine genera l'evento quando dispone di una nuova presentazione. La sessione multimediale trasmette questo evento all'applicazione.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Evento MENewPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226662"
---
# <a name="menewpresentation-event"></a>Evento MENewPresentation

Generato da un'origine multimediale che fornisce topologie tramite l'interfaccia [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , ad esempio l'origine del sequencer. L'origine genera l'evento quando dispone di una nuova presentazione. La sessione multimediale trasmette questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descrittore della presentazione per la nuova presentazione.<br/> <br/> |



## <a name="remarks"></a>Commenti

L'applicazione può ottenere la topologia che corrisponde al descrittore di presentazione chiamando [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) sull'origine multimediale. L'applicazione può quindi accodare la nuova topologia nella sessione multimediale chiamando [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 




