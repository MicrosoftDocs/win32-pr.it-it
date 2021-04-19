---
description: Inviato da un flusso di byte quando le caratteristiche del flusso di byte sono state modificate.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Evento MEByteStreamCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308742"
---
# <a name="mebytestreamcharacteristicschanged-event"></a>Evento MEByteStreamCharacteristicsChanged

Inviato da un flusso di byte quando le caratteristiche del flusso di byte sono state modificate.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE               | Descrizione                           |
|-----------------------|---------------------------------------|
| VT \_ vuoto <br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento indica che sono state modificate una o più delle seguenti caratteristiche:

-   Flag funzionalità ([**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))
-   Flag di fine flusso ([**IMFByteStream:: IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))
-   Lunghezza ([**IMFByteStream:: GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))

Non tutte le implementazioni di [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) supportano questo evento. Per ricevere l'evento, eseguire una query sull'oggetto flusso di byte per l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




