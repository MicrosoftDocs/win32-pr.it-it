---
description: "Generato da un'origine multimediale per richiedere una nuova velocità di riproduzione. L'applicazione deve chiamare IMFRateControl:: serate con la frequenza richiesta. Un'origine multimediale potrebbe generare questo evento se non può continuare la riproduzione alla frequenza corrente."
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Evento MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226655"
---
# <a name="mesourceratechangerequested-event"></a>Evento MESourceRateChangeRequested

Generato da un'origine multimediale per richiedere una nuova velocità di riproduzione. L'applicazione deve chiamare [**IMFRateControl:: serate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) con la frequenza richiesta. Un'origine multimediale potrebbe generare questo evento se non può continuare la riproduzione alla frequenza corrente.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                                             |
|-------------------|---------------------------------------------------------|
| \_R4 VT<br/> | La nuova frequenza di riproduzione richiesta.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                    | Descrizione                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**MF \_ evento \_ do \_ assottigliamento**](mf-event-do-thinning-attribute.md)<br/> | Specifica se l'origine multimediale richiede anche l'assottigliamento.<br/> <br/> |



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

 

 




