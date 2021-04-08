---
description: Generato da un flusso multimediale quando cambia il tipo di supporto del flusso.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Evento MEStreamFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880246"
---
# <a name="mestreamformatchanged-event"></a>Evento MEStreamFormatChanged

Generato da un flusso multimediale quando cambia il tipo di supporto del flusso.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) del nuovo tipo di supporto.<br/> <br/> |



## <a name="remarks"></a>Commenti

Utilizzare questo evento per segnalare le modifiche al formato nel flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




