---
description: Media Stream usa questo evento per inviare metadati specifici del sistema di protezione al decodificatore.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Evento MEContentProtectionMetadata (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d972dc667c7119f01b39bff132b36dfa11c2810960ed638bd41a0cd9336f7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062288"
---
# <a name="mecontentprotectionmetadata-event"></a>EVENTO MEContentProtectionMetadata

Media Stream usa questo evento per inviare metadati specifici del sistema di protezione al decodificatore.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                                              | Descrizione                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [METADATI DEL FLUSSO DI EVENTI MF \_ \_ \_ \_ KEYDATA](mf-event-stream-metadata-keydata.md)<br/>                | Questo è un attributo facoltativo. Dati specifici del sistema di protezione.<br/> <br/>              |
| [ID DI \_ CHIAVE DEL CONTENUTO DEI METADATI DEL FLUSSO DI \_ \_ \_ \_ EVENTI MF](mf-event-stream-metadata-content-keyids.md)<br/> | ID chiave del contenuto a cui è associato l'evento.<br/> <br/>                          |
| [SYSTEMID DEI \_ METADATI DEL FLUSSO DI EVENTI \_ \_ \_ MF](mf-event-stream-metadata-systemid.md)<br/>              | Questo è un attributo facoltativo. ID di sistema a cui sono destinati i dati della chiave.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene usato, ad esempio, per comunicare l'evento di rotazione dei tasti. In questo caso deve essere inviato il prima possibile per concedere al decodificatore il tempo necessario per prepararsi prima che inizino ad arrivare campioni crittografati con il nuovo ID chiave.

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

 

 




