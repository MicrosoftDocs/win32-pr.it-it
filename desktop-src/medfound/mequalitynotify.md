---
description: Fornisce commenti e suggerimenti al responsabile qualità sulla qualità della riproduzione.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Evento MEQualityNotify (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528272"
---
# <a name="mequalitynotify-event"></a>Evento MEQualityNotify

Fornisce commenti e suggerimenti al responsabile qualità sulla qualità della riproduzione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                         |
|-------------------|-------------------------------------|
| \_I8 VT<br/> | Vedere la sezione Osservazioni.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene generato da alcuni componenti della pipeline. La sessione multimediale trasmette l'evento al gestore qualità chiamando il metodo [**IMFQualityManager:: NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) .

Il tipo esteso dell'evento indica il significato dei dati dell'evento.



| Tipo esteso                            | Dati dell'evento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ latenza di elaborazione \_ notifica MF qualità | Latenza di elaborazione approssimativa introdotta dal componente, in unità da 100 nanosecondi.<br/> La latenza di elaborazione è la quantità di latenza introdotta da un componente nella pipeline mediante l'elaborazione di un esempio. In alcuni casi, non è possibile derivare la latenza semplicemente esaminando le chiamate a [**IMFQualityManager:: NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) e [**IMFQualityManager:: NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput). Ad esempio, potrebbe non essere presente una corrispondenza uno-a-uno tra gli esempi di input e di output. In questo caso, il componente potrebbe inviare un evento MEQualityNotify con la latenza di elaborazione. Se la latenza di elaborazione cambia, il componente può inviare un nuovo evento in qualsiasi momento durante il flusso.<br/> |
| \_ritardo di \_ esempio di notifica MF Quality \_ \_         | Tempo di ritardo per l'esempio, in unità di 100 nanosecondi. Se il valore è positivo, l'esempio è in ritardo. Se il valore è negativo, il campione è stato anticipato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Per ottenere il tipo esteso, chiamare [**IMFMediaEvent:: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).

I componenti della pipeline non sono necessari per l'invio di questo evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




