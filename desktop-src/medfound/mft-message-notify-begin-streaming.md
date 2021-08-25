---
description: Notifica a una trasformazione Media Foundation (MFT) che sta per iniziare il flusso.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 491f84ee2dee752cccc251187c43bd497723a64ae6601954051f2aebab34ef85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848066"
---
# <a name="mft_message_notify_begin_streaming"></a>MFT \_ MESSAGE \_ NOTIFY \_ BEGIN \_ STREAMING

Notifica a una trasformazione Media Foundation (MFT) che sta per iniziare il flusso.

## <a name="message-parameter"></a>Parametro del messaggio

No.

## <a name="remarks"></a>Osservazioni

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Il client non deve inviare questo messaggio. Se il client invia questo messaggio, deve eseguire questa operazione dopo aver impostato tutti i tipi di supporti in MFT e prima di [**chiamare ProcessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) MFT può rispondere allocando buffer o altre risorse. Se il client non invia questo messaggio, MFT alloca le risorse alla prima chiamata a **ProcessInput.** Pertanto, l'invio di questo messaggio può ridurre la latenza iniziale all'inizio del flusso.

### <a name="implementation"></a>Implementazione

Non è necessario un MFT per rispondere a questo messaggio.

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

 

 




