---
description: 'MFT_MESSAGE_COMMAND_FLUSH: richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.'
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092739"
---
# <a name="mft_message_command_flush"></a>MFT \_ MESSAGE \_ COMMAND \_ FLUSH

Richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Dopo l'invio di questo messaggio, il MFT può accettare nuovi esempi di input. I tipi di supporti correnti non vengono invalidati.

### <a name="implementation"></a>Implementazione

Tutti i MFT devono implementare questo messaggio. Quando riceve questo messaggio, il MFT deve rimuovere tutti i campioni di supporti in esso contenuti.

[MFT](asynchronous-mfts.md)asincroni: MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) fino a quando non riceve un messaggio [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM**](mft-message-notify-start-of-stream.md) dal client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO DI \_ MESSAGGIO \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




