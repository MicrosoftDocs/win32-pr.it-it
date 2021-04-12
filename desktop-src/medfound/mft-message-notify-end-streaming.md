---
description: Richiede una trasformazione Media Foundation (MFT) a tale flusso sta per terminare.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527913"
---
# <a name="mft_message_notify_end_streaming"></a>\_ \_ \_ flusso finale notifiche messaggio \_ MFT

Richiede una trasformazione Media Foundation (MFT) a tale flusso sta per terminare.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Il client non deve inviare questo messaggio, anche se il client ha inviato in precedenza il messaggio relativo all' **\_ inizio del \_ \_ \_ flusso di notifica del messaggio MFT** .

### <a name="implementation"></a>Implementazione

Il MFT può rispondere a questo messaggio rilasciando i buffer e altre risorse. MFT non Scarica i dati di input o Reimposta i tipi di supporto in risposta a questo messaggio. Non è necessario un MFT per rispondere a questo messaggio.

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

 

 




