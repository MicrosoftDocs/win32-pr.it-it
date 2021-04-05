---
description: Notifica a un Media Foundation Transform (MFT) che il primo campione sta per essere elaborato.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049665"
---
# <a name="mft_message_notify_start_of_stream"></a>\_ \_ avvio notifica messaggio \_ MFT \_ del \_ flusso

Notifica a un Media Foundation Transform (MFT) che il primo campione sta per essere elaborato.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Per MFTs sincrono, è facoltativo inviare questo messaggio.

Per MFTs asincrono, il client deve inviare questo messaggio.

### <a name="implementation"></a>Implementazione

Non è necessario un MFT sincrono per rispondere al messaggio.

Un MFT asincrono deve implementare questo messaggio, come descritto in [MFTS asincrono](asynchronous-mfts.md).

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

 

 




