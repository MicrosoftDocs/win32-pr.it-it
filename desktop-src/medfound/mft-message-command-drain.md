---
description: Richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa533cfddfda53fd8eb0ee512b0535aaf9ad8f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310219"
---
# <a name="mft_message_command_drain"></a>\_ \_ svuotamento comando messaggio \_ MFT

Richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Una volta inviato questo messaggio, il flusso di input specificato non accetta l'input finché la MFT non elabora tutti i dati delle chiamate precedenti a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Il processo di svuotamento varia leggermente tra MFTs sincrono e MFTs asincrono:

**MFTs sincrono**

1.  Quando il client invia questo messaggio, chiama [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in un ciclo, fino a quando **ProcessOutput** restituisce il codice di errore **MF \_ E \_ Transform \_ necessitano di \_ più \_ input**.
2.  Fino a quando la MFT dispone ancora di dati da elaborare, le chiamate a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) avranno esito negativo. Il MFT continua a produrre output fino a quando non usa tutti i dati archiviati. Il MFT Elimina tutti i dati che non possono essere elaborati in un esempio di output completo. (Ad esempio, dovrebbe eliminare un fotogramma video parziale).

**MFTs asincrono**

1.  Il MFT continua a inviare gli eventi [METransformHaveOutput](metransformhaveoutput.md) fino a quando non sono disponibili altri dati da elaborare. Non invia eventi [METransformNeedInput](metransformneedinput.md) durante questo periodo di tempo.
2.  Dopo l'invio dell'ultimo evento [METransformHaveOutput](metransformhaveoutput.md) da parte di MFT, viene inviato un evento [METransformDrainComplete](metransformdraincomplete.md) .
3.  Una volta completato lo svuotamento, il MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) fino a quando non riceve un messaggio [**MFT \_ \_ Notify \_ avvio del messaggio \_ di \_ flusso**](mft-message-notify-start-of-stream.md) dal client.

Dopo che il client ha svuotato il MFT, il client può inviare più dati di input. Il primo campione dopo l'operazione di svuotamento deve avere l'attributo discontinuity (attributo di [**\_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) ).

> [!Note]  
> Nelle versioni precedenti di questa documentazione è stato dichiarato che il parametro dell'evento *ulParam* è un membro dell'enumerazione del [**\_ \_ \_ tipo di svuotamento MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) . Risposta errata. *UlParam* contiene un identificatore di flusso.

 

### <a name="implementation"></a>Implementazione

Una MFT asincrona deve sempre restituire [METransformDrainComplete](metransformdraincomplete.md) dopo lo svuotamento.

Un MFT sincrono può ignorare questo messaggio e restituire S \_ OK se sono soddisfatte le condizioni seguenti:

-   MFT non archivia mai più di un campione di input alla volta.
-   Ogni esempio di input produce un singolo esempio di output.

In caso contrario, un MFT sincrono deve implementare questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tipo di messaggio MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[MFTs asincrono](asynchronous-mfts.md)
</dt> </dl>

 

 




