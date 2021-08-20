---
description: Notifica a una trasformazione Media Foundation (MFT) che un flusso di input è terminato.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951337fb91a26f1498b2aa82d42754fb2954ab649b4a021d37d42047be331ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872161"
---
# <a name="mft_message_notify_end_of_stream"></a>MFT \_ MESSAGE \_ NOTIFY \_ END \_ OF \_ STREAM

Notifica a una trasformazione Media Foundation (MFT) che un flusso di input è terminato.

## <a name="message-parameter"></a>Parametro del messaggio

Il *parametro ulParam* contiene l'identificatore del flusso di input, specificato come **valore DWORD.** Nelle applicazioni a 64 bit inserire questo valore nei 32 bit inferiori del **\_ PTR ULONG.**

## <a name="remarks"></a>Commenti

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Il client non è necessario per inviare questo messaggio.

Al termine di un flusso, il client può chiamare [**di nuovo ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per inviare nuovi dati per tale flusso. In tal caso, il client deve impostare l'attributo discontinuità [**(attributo MFSampleExtension \_ Discontinuity)**](mfsampleextension-discontinuity-attribute.md) nel primo esempio di input al termine del flusso. Il client deve sempre impostare questo attributo nel primo nuovo esempio al termine di un flusso, indipendentemente dal fatto che il client ha inviato il messaggio **MFT \_ MESSAGE NOTIFY END OF \_ \_ \_ \_ STREAM.** Per altre informazioni sulla gestione delle discontinuità, vedere [Modello di elaborazione MFT di base.](basic-mft-processing-model.md)

Dopo aver inviato questo messaggio per ogni flusso di input, il client in genere invia un comando **MFT \_ MESSAGE COMMAND \_ \_ DRAIN** e quindi raccoglie l'output rimanente. Tuttavia, il client non è necessario per svuotare il MFT. Se il client non svuota la MFT, MFT in genere scarterà tutti i dati non elaborati alla successiva chiamata a [**ProcessInput,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)quando rileva la discontinuità del flusso. In alternativa, il client potrebbe scaricare MFT prima di chiamare **ProcessInput**.

Questo messaggio non rimuove il flusso di input né reimposta il tipo di supporto.

### <a name="implementation"></a>Implementazione

Non è necessario un MFT per rispondere a questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO DI \_ MESSAGGIO \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




