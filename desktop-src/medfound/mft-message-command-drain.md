---
description: 'MFT_MESSAGE_COMMAND_DRAIN: richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.'
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8faf20ca1169d87370a7dc1b5a128b11c9f17937a514f4aaea37631aee4d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012621"
---
# <a name="mft_message_command_drain"></a>SVUOTAMENTO \_ DEI COMANDI DEI \_ MESSAGGI \_ MFT

Richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Dopo l'invio di questo messaggio, il flusso di input specificato non accetta input fino a quando il MFT non elabora tutti i dati delle chiamate precedenti a [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Il processo di svuotamento varia leggermente tra MFT sincroni e MFT asincroni:

**MFT sincroni**

1.  Dopo l'invio del messaggio, il client chiama [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in un ciclo, finché **ProcessOutput** non restituisce il codice di errore **MF \_ E TRANSFORM NEED MORE \_ \_ \_ \_ INPUT**.
2.  Finché il MFT ha ancora dati da elaborare, le altre chiamate a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) avranno esito negativo. MFT continua a produrre output fino a quando non usa tutti i dati archiviati. MFT elimina tutti i dati che non possono essere elaborati in un campione di output completo. Ad esempio, deve eliminare un fotogramma video parziale.

**MFT asincroni**

1.  MFT continua a inviare [gli eventi METransformHaveOutput](metransformhaveoutput.md) finché non ha più dati da elaborare. Non invia eventi [METransformNeedInput](metransformneedinput.md) durante questo periodo di tempo.
2.  Dopo l'invio dell'ultimo [evento METransformHaveOutput,](metransformhaveoutput.md) MFT invia un [evento METransformDrainComplete.](metransformdraincomplete.md)
3.  Al termine dello svuotamento, MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) fino a quando non riceve un messaggio [**MFT \_ MESSAGE NOTIFY START \_ OF \_ \_ \_ STREAM**](mft-message-notify-start-of-stream.md) dal client.

Dopo che il client ha svuotato il MFT, il client può inviare più dati di input. Il primo esempio dopo l'operazione di svuotamento deve avere l'attributo discontinuità [**(attributo MFSampleExtension \_ Discontinuity).**](mfsampleextension-discontinuity-attribute.md)

> [!Note]  
> Nelle versioni precedenti di questa documentazione è stato dichiarato che il *parametro dell'evento ulParam* è un membro dell'enumerazione [**\_ MFT \_ DRAIN \_ TYPE.**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) Risposta errata. UlParam *contiene* un identificatore di flusso.

 

### <a name="implementation"></a>Implementazione

Un MFT asincrono deve sempre restituire [METransformDrainComplete](metransformdraincomplete.md) dopo che è stato svuotato.

Un MFT sincrono può ignorare questo messaggio e restituire S \_ OK se si verificano le condizioni seguenti:

-   MFT non archivia mai più di un campione di input alla volta.
-   Ogni esempio di input produce un singolo esempio di output.

In caso contrario, un MFT sincrono deve implementare questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO DI \_ MESSAGGIO \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[MFT asincroni](asynchronous-mfts.md)
</dt> </dl>

 

 




