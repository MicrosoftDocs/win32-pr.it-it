---
description: "Generato dall'origine del sequencer quando il metodo IMFSequencerSource:: UpdateTopology viene completato in modo asincrono."
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Evento MESequencerSourceTopologyUpdated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309619"
---
# <a name="mesequencersourcetopologyupdated-event"></a>Evento MESequencerSourceTopologyUpdated

Generato dall'origine del sequencer quando il metodo [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) viene completato in modo asincrono.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE            | Descrizione                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_UI4 VT<br/> | Identificatore dell'elemento sequencer della topologia da aggiornare. L'applicazione specifica questo valore nel parametro *dwID* del metodo [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) .<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento segnala che l'origine del sequencer ha aggiornato la topologia, ma non significa che la topologia è pronta per la riproduzione. L'applicazione deve attendere l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 




