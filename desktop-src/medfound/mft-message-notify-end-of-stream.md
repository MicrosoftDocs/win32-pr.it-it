---
description: Notifica a un Media Foundation trasformazione (MFT) che un flusso di input è terminato.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310215"
---
# <a name="mft_message_notify_end_of_stream"></a>\_ \_ \_ fine \_ del flusso di notifica del messaggio MFT \_

Notifica a un Media Foundation trasformazione (MFT) che un flusso di input è terminato.

## <a name="message-parameter"></a>Parametro del messaggio

Il parametro *ulParam* contiene l'identificatore del flusso di input, specificato come valore **DWORD** . Nelle applicazioni a 64 bit, inserire questo valore nei 32 bit inferiori del **\_ ptr ULONG**.

## <a name="remarks"></a>Commenti

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Il client non è necessario per l'invio di questo messaggio.

Al termine di un flusso, il client può chiamare nuovamente [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per inviare i nuovi dati per il flusso. In tal caso, il client deve impostare l'attributo discontinuity (attributo [**\_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) ) sul primo campione di input dopo la fine del flusso. Il client deve sempre impostare questo attributo sul primo nuovo campione dopo la fine di un flusso, indipendentemente dal fatto che il client abbia inviato il messaggio MFT per la **\_ \_ notifica \_ \_ della fine del \_ flusso** . Per ulteriori informazioni sulla gestione delle discontinuità, vedere [Basic MFT Processing Model](basic-mft-processing-model.md).

Dopo l'invio di questo messaggio per ogni flusso di input, il client in genere invia un comando di **\_ svuotamento del \_ comando \_ del messaggio MFT** e quindi raccoglie l'output rimanente. Tuttavia, non è necessario che il client scarichi il MFT. Se il client non svuota il computer MFT, in genere il MFT eliminerà tutti i dati non elaborati alla chiamata successiva a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), quando rileverà la discontinuità del flusso. In alternativa, il client potrebbe scaricare il MFT prima di chiamare **ProcessInput**.

Questo messaggio non rimuove il flusso di input o Reimposta il tipo di supporto.

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

 

 




