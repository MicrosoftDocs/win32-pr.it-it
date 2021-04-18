---
description: Inviato da una trasformazione di Media Foundation asincrona (MFT) quando sono disponibili nuovi dati di output dalla MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Evento METransformHaveOutput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307989"
---
# <a name="metransformhaveoutput-event"></a>Evento METransformHaveOutput

Inviato da una trasformazione di Media Foundation asincrona (MFT) quando sono disponibili nuovi dati di output dalla MFT.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione               |
|----------------------|---------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> |



## <a name="attributes"></a>Attributi

Per questo evento non sono definiti attributi.

## <a name="remarks"></a>Commenti

Il MFTs asincrono invia questo evento tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . MFTs sincroni non inviano mai questo evento.

Quando il client di MFT riceve questo evento, deve chiamare [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) per ottenere l'output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[MFTs asincrono](asynchronous-mfts.md)
</dt> </dl>

 

 




