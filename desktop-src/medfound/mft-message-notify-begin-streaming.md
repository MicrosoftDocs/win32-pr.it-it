---
description: Notifica a una Media Foundation trasformazione (MFT) che il flusso sta per iniziare.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226529"
---
# <a name="mft_message_notify_begin_streaming"></a>\_notifica di \_ \_ inizio \_ trasmissione del messaggio MFT

Notifica a una Media Foundation trasformazione (MFT) che il flusso sta per iniziare.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Il client non è necessario per l'invio di questo messaggio. Se il client invia questo messaggio, è necessario eseguire questa operazione dopo avere impostato tutti i tipi di supporto in MFT e prima di chiamare [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). Il MFT può rispondere allocando buffer o altre risorse. Se il client non invia questo messaggio, il MFT alloca le risorse alla prima chiamata a **ProcessInput**. Pertanto, l'invio di questo messaggio può ridurre la latenza iniziale all'avvio del flusso.

### <a name="implementation"></a>Implementazione

Non è necessario un MFT per rispondere a questo messaggio.

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

 

 




