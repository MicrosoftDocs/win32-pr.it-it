---
description: Il flusso multimediale usa questo evento per inviare metadati specifici del sistema di protezione al decodificatore.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Evento MEContentProtectionMetadata (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879822"
---
# <a name="mecontentprotectionmetadata-event"></a>Evento MEContentProtectionMetadata

Il flusso multimediale usa questo evento per inviare metadati specifici del sistema di protezione al decodificatore.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                                              | Descrizione                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [\_dati di \_ metadati del flusso di eventi MF \_ \_](mf-event-stream-metadata-keydata.md)<br/>                | Questo è un attributo facoltativo. Dati specifici del sistema di protezione.<br/> <br/>              |
| [\_ \_ \_ \_ KEYIDS contenuto metadati flusso di eventi MF \_](mf-event-stream-metadata-content-keyids.md)<br/> | ID della chiave simmetrica a cui è associato l'evento.<br/> <br/>                          |
| [\_ \_ SYSTEMID metadati del flusso di eventi MF \_ \_](mf-event-stream-metadata-systemid.md)<br/>              | Questo è un attributo facoltativo. ID di sistema per il quale sono previsti i dati della chiave.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene usato, ad esempio, per la comunicazione dell'evento di rotazione delle chiavi. In questo caso deve essere inviato il prima possibile per fornire al decodificatore il tempo necessario per prepararsi prima che i campioni crittografati con il nuovo ID chiave inizino ad arrivare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




