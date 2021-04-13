---
description: Generato quando un'origine multimediale viene avviata senza cercare.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Evento MESourceStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528261"
---
# <a name="mesourcestarted-event"></a>Evento MESourceStarted

Generato quando un'origine multimediale viene avviata senza cercare.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento. L'ora di inizio è stata dalla posizione corrente.<br/> <br/>                            |
| \_I8 VT<br/>    | Ora di inizio, in unità di 100 nanosecondi, relativa ai timestamp degli esempi.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                                     | Descrizione                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ inizio effettivo origine evento \_ MF**](mf-event-source-actual-start-attribute.md)<br/> | Ora di inizio. L'origine multimediale imposta questo attributo se viene riavviato dalla posizione corrente.<br/> <br/>                     |
| [**\_ \_ \_ inizio Fake origine evento \_ MF**](mf-event-source-fake-start-attribute.md)<br/>     | Specifica se la topologia del segmento corrente è vuota. L'origine di Sequencer imposta questo attributo.<br/> <br/>             |
| [**\_origine evento \_ MF \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)<br/>  | Ora di inizio per un segmento rispetto all'inizio della presentazione. L'origine di Sequencer imposta questo attributo.<br/> <br/> |



## <a name="remarks"></a>Commenti

Un'origine multimediale genera questo evento quando inizia da uno stato interrotto o inizia da uno stato di sospensione nella stessa posizione dell'origine. L'evento viene generato se il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) restituisce S \_ OK.

Se l'origine multimediale inizia dalla posizione corrente e lo stato precedente dell'origine è in esecuzione o in pausa, i dati dell'evento possono essere vuoti (VT \_ vuoto). Se i dati dell'evento sono VT \_ vuoti, l'origine del supporto potrebbe impostare l'attributo [**\_ \_ \_ \_ Start effettivo dell'origine eventi MF**](mf-event-source-actual-start-attribute.md) con l'ora di inizio effettiva.

Se l'origine multimediale viene avviata da una nuova posizione o lo stato precedente dell'origine è stato arrestato, i dati dell'evento devono essere l'ora di inizio (VT \_ I8).

Se il metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causa una ricerca, l'origine multimediale invia l'evento [MESourceSeeked](mesourceseeked.md) anziché MESourceStarted.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




