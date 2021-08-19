---
description: Contrassegna un punto nel flusso. Questo messaggio si applica solo ai MFT asincroni.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc55a96ae9680b37d83ec776c66848ed04f4a30b62d1d0378035c88823d2c19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872171"
---
# <a name="mft_message_command_marker"></a>INDICATORE DI COMANDO DEL MESSAGGIO MFT \_ \_ \_

Contrassegna un punto nel flusso. Questo messaggio si applica solo ai [MFT asincroni.](asynchronous-mfts.md)

## <a name="message-parameter"></a>Parametro del messaggio

Valore arbitrario. MFT restituisce il valore al client [nell'evento METransformMarker.](metransformmarker.md)

## <a name="remarks"></a>Commenti

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Il MFT risponde a questo messaggio come segue:

1.  MFT genera il maggior numero possibile di esempi di output dai dati di input esistenti, inviando un evento [METransformHaveOutput](metransformhaveoutput.md) per ogni esempio di output.
2.  Dopo la generazione di tutto l'output, MFT invia un [evento METransformMarker.](metransformmarker.md) Questo evento deve essere inviato dopo tutti gli [eventi METransformHaveOutput.](metransformhaveoutput.md)

Il client non è necessario per inviare questo messaggio e deve inviare questo messaggio solo a MFT asincroni. Un MFT sincrono non invierà un [evento METransformMarker](metransformmarker.md) in risposta a questo messaggio.

### <a name="implementation"></a>Implementazione

I messaggi MFT asincroni devono rispondere a questo messaggio come descritto. I messaggi MFT sincroni devono ignorare questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO DI \_ MESSAGGIO \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




