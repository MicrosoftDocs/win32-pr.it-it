---
description: Quando il filtro dello strumento di spostamento DVD passa alla modalità karaoke, informa il decodificatore audio tramite la proprietà AM \_ \_ DVDKARAOKE \_ Enable.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Set di proprietà DVD karaoke (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e9fe53ad35dac0c3c0f54a8e04a6fbe698fc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325726"
---
# <a name="dvd-karaoke-property-set"></a>Set di proprietà di DVD karaoke

Quando il filtro dello [strumento di spostamento DVD](dvd-navigator-filter.md) passa alla modalità karaoke, informa il decodificatore audio tramite la proprietà **am \_ \_ DVDKARAOKE \_ Enable** . Il decodificatore deve quindi disattivare i canali audio da 2 a 5 fino a quando non riceve dal navigatore DVD una proprietà **\_ \_ \_ dei dati DVDKARAOKE della proprietà am** con un puntatore a una struttura di dati [**\_ DvdKaraokeData am**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) che indica il modo in cui devono essere combinati i canali ausiliari.



|                   |                             |
|-------------------|-----------------------------|
| GUID set di proprietà | \_DvdKaraoke KSPROPSETID \_ |



 



| ID proprietà                      | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Proprietà am \_ DVDKARAOKE \_ Enable | Valore BOOLEANo. Il navigatore DVD invia al decodificatore la \_ Proprietà am \_ DVDKARAOKE \_ Enable con il valore **true** per abilitare il karaoke downmixing o **false** per disabilitarlo.                                                                                                                                    |
| \_ \_ dati DVDKARAOKE proprietà \_ am   | Il navigatore DVD invia al decodificatore una \_ \_ proprietà dei dati DVDKARAOKE della proprietà am \_ con un puntatore a una struttura [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) per modificare la configurazione downmix, ovvero per attivare o disattivare determinati canali karaoke e indirizzarli al canale di output a destra o a sinistra. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




