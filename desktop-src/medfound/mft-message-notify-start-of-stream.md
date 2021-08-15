---
description: Notifica a una trasformazione Media Foundation (MFT) che il primo esempio sta per essere elaborato.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ed40d9d3514dfa6223d4e20f2eb411caec497e16f2e97c456f16e14442c407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973030"
---
# <a name="mft_message_notify_start_of_stream"></a>MFT \_ MESSAGE \_ NOTIFY \_ START \_ OF \_ STREAM

Notifica a una trasformazione Media Foundation (MFT) che il primo esempio sta per essere elaborato.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Per i MFT sincroni, è facoltativo inviare questo messaggio.

Per i messaggi MFT asincroni, il client deve inviare questo messaggio.

### <a name="implementation"></a>Implementazione

Non è necessario un MFT sincrono per rispondere al messaggio.

Un MFT asincrono deve implementare questo messaggio, come descritto in [MFT asincroni.](asynchronous-mfts.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO DI \_ MESSAGGIO \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




