---
description: Richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753951"
---
# <a name="mft_message_command_flush"></a>\_ \_ scaricamento comando messaggio MFT \_

Richiede una trasformazione Media Foundation (MFT) per scaricare tutti i dati archiviati.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Una volta inviato questo messaggio, il MFT può accettare nuovi esempi di input. I tipi di file multimediali correnti non vengono invalidati.

### <a name="implementation"></a>Implementazione

Tutti MFTs devono implementare questo messaggio. Quando riceve questo messaggio, la MFT deve eliminare tutti gli esempi di supporti che contiene.

[MFTS asincrono](asynchronous-mfts.md): il MFT non invia un altro evento [METransformNeedInput](metransformneedinput.md) fino a quando non riceve un messaggio [**MFT \_ \_ Notify \_ avvio del messaggio \_ di \_ flusso**](mft-message-notify-start-of-stream.md) dal client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tipo di messaggio MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




