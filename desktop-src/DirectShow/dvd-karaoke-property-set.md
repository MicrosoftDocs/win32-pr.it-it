---
description: Quando il filtro DVD Navigator passa alla modalità tutto schermo, informa il decodificatore audio tramite la proprietà \_ AM PROPERTY \_ DVDKARAOKE \_ ENABLE.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Set di proprietà DVD Persa (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3f7674b240934ae7440858b7317fd1abaf9b7833e36f80d7edc6cc185bc932
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016019"
---
# <a name="dvd-karaoke-property-set"></a>Set di proprietà DVD Per dvd

Quando il [filtro DVD Navigator](dvd-navigator-filter.md) passa alla modalità tutto schermo, informa il decodificatore audio tramite la proprietà AM PROPERTY **\_ \_ DVDKARAOKE \_ ENABLE.** Il decodificatore deve quindi disattivare i canali audio da 2 a 5 finché non riceve dallo strumento di navigazione DVD una proprietà **\_ AM PROPERTY \_ DVDKARAOKE \_ DATA** con un puntatore a una struttura di dati [**AM \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) che indica come devono essere misti i canali ausiliari.



| Etichetta | Valore |
|-------------------|-----------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ DvdKaraoke |



 



| ID proprietà                      | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROPRIETÀ \_ \_ AM DVDKARAOKE \_ ENABLE | Valore BOOLEAN. Lo strumento di navigazione DVD invia al decodificatore una PROPRIETÀ AM DVDKARAOKE ENABLE con valore TRUE per abilitare \_ \_ \_ l'downmixing per il karaoke o **FALSE** per  disabilitarlo.                                                                                                                                    |
| PROPRIETÀ \_ \_ AM DVDKARAOKE \_ DATA   | Lo strumento di navigazione DVD invia al decodificatore una proprietà AM PROPERTY DVDKARAOKE DATA con un puntatore a una struttura \_ \_ AM \_ [**\_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) per modificare la configurazione downmix, ad esempio per attivare o disattivare determinati canali di tutto il sistema e indirizzarli al canale di output destro o sinistro. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




