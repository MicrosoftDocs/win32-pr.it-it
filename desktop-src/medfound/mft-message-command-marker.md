---
description: Contrassegna un punto nel flusso. Questo messaggio si applica solo ai MFTs asincroni.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310218"
---
# <a name="mft_message_command_marker"></a>\_ \_ marcatore del comando del messaggio MFT \_

Contrassegna un punto nel flusso. Questo messaggio si applica solo ai [MFTS asincroni](asynchronous-mfts.md).

## <a name="message-parameter"></a>Parametro del messaggio

Valore arbitrario. Il MFT restituisce il valore al client nell'evento [METransformMarker](metransformmarker.md) .

## <a name="remarks"></a>Commenti

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Il MFT risponde ai messaggi seguenti:

1.  Il MFT genera il numero di campioni di output possibili dai dati di input esistenti, inviando un evento [METransformHaveOutput](metransformhaveoutput.md) per ogni esempio di output.
2.  Una volta generato tutto l'output, il MFT Invia un evento [METransformMarker](metransformmarker.md) . Questo evento deve essere inviato dopo tutti gli eventi [METransformHaveOutput](metransformhaveoutput.md) .

Il client non è necessario per inviare questo messaggio e deve inviare questo messaggio solo a MFTs asincrono. Un MFT sincrono non invierà un evento [METransformMarker](metransformmarker.md) in risposta a questo messaggio.

### <a name="implementation"></a>Implementazione

Il MFTs asincrono deve rispondere a questo messaggio come descritto. Il MFTs sincrono deve ignorare questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tipo di messaggio MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




