---
description: Richiede una Media Foundation (MFT) a tale flusso sta per terminare.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae36412a35dd142efab89f17827b1c9cb6475494ff88f8af800bd8fee65d456f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871965"
---
# <a name="mft_message_notify_end_streaming"></a>MFT \_ MESSAGE \_ NOTIFY \_ END \_ STREAMING

Richiede una Media Foundation (MFT) a tale flusso sta per terminare.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Il client non deve inviare questo messaggio, anche se il client ha inviato in precedenza il messaggio **MFT \_ MESSAGE NOTIFY \_ BEGIN \_ \_ STREAMING.**

### <a name="implementation"></a>Implementazione

MFT può rispondere a questo messaggio rilasciando buffer e altre risorse. MFT non scarica i dati di input né reimposta i tipi di supporti in risposta a questo messaggio. Non è necessario un MFT per rispondere a questo messaggio.

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

 

 




