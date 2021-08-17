---
description: Fornisce commenti e suggerimenti al gestore qualità sulla qualità della riproduzione.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Evento MEQualityNotify (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd019db55a0791ec5464cf67c7ee4d3e4a86f918efc2b4e87f4ddde2f3574ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061876"
---
# <a name="mequalitynotify-event"></a>EVENTO MEQualityNotify

Fornisce commenti e suggerimenti al gestore qualità sulla qualità della riproduzione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                         |
|-------------------|-------------------------------------|
| VT \_ I8<br/> | Vedere la sezione Osservazioni.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene generato da alcuni componenti della pipeline. La sessione multimediale inoltra l'evento al gestore qualità chiamando il [**metodo IMFQualityManager::NotifyQualityEvent.**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent)

Il tipo esteso dell'evento indica il significato dei dati dell'evento.



| Tipo esteso                            | Dati dell'evento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LATENZA ELABORAZIONE NOTIFICA QUALITÀ MF \_ \_ \_ \_ | Latenza di elaborazione approssimativa introdotta dal componente, in unità di 100 nanosecondi.<br/> La latenza di elaborazione è la quantità di latenza che un componente introduce nella pipeline elaborando un campione. In alcuni casi, la latenza non può essere derivata semplicemente esaminando le chiamate a [**IMFQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) e [**IMFQualityManager::NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput). Ad esempio, potrebbe non esserci una corrispondenza uno-a-uno tra gli esempi di input e gli esempi di output. In questo caso, il componente potrebbe inviare un evento MEQualityNotify con la latenza di elaborazione. Se la latenza di elaborazione cambia, il componente può inviare un nuovo evento in qualsiasi momento durante il flusso.<br/> |
| MF \_ QUALITY \_ NOTIFY \_ SAMPLE \_ LAG         | Tempo di ritardo per il campione, in unità di 100 nanosecondi. Se il valore è positivo, il campione è in ritardo. Se il valore è negativo, il campione è stato in anticipo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Per ottenere il tipo esteso, chiamare [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).

I componenti della pipeline non sono necessari per inviare questo evento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




