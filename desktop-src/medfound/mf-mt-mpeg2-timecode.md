---
description: Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica che i pacchetti di trasporto contengono un codice a 4 byte.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: Attributo MF_MT_MPEG2_TIMECODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232387"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>\_ \_ Attributo timecode MF mt MPEG2 \_

Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica che i pacchetti di trasporto contengono un codice a 4 byte.

## <a name="data-type"></a>Tipo di dati

**UINT32**



| Valore                                                                                                | Significato                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nessun codice ora aggiunto.<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | All'inizio di ogni pacchetto di trasporto viene aggiunto un codice a 4 byte. Questo codice temporale è necessario per alcuni standard della televisione digitale.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




