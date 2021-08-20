---
description: Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica che i pacchetti di trasporto contengono un flusso di trasporto di 4 byte time code.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: MF_MT_MPEG2_TIMECODE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7a4ce6868f783ed33c50acd5a8648297648481a58c74198b0dcadd1bd237bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741767"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>Attributo MF \_ MT \_ MPEG2 \_ TIMECODE

Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica che i pacchetti di trasporto contengono un flusso di trasporto di 4 byte time code.

## <a name="data-type"></a>Tipo di dati

**UINT32**



| Valore                                                                                                | Significato                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessuna time code aggiunta.<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Viene aggiunto un time code di 4 byte all'inizio di ogni pacchetto di trasporto. Questo time code è richiesto da alcuni standard della tv digitale.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




