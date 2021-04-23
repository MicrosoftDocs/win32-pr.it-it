---
description: Quando il filtro DVD Navigator passa alla modalità schermo intero, informa il decodificatore audio tramite la proprietà \_ AM PROPERTY \_ DVDKARAOKE \_ ENABLE.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Set di proprietà DVD Dvd Dvdmedia.h
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909069"
---
# <a name="dvd-karaoke-property-set"></a>DVD Karaoke Property Set

Quando il [filtro DVD Navigator](dvd-navigator-filter.md) passa alla modalità schermo intero, informa il decodificatore audio tramite la proprietà AM PROPERTY **\_ \_ DVDKARAOKE \_ ENABLE.** Il decodificatore deve quindi disattivare i canali audio da 2 a 5 fino a quando non riceve dallo strumento di navigazione DVD una proprietà **\_ AM PROPERTY \_ DVDKARAOKE \_ DATA** con un puntatore a una struttura di dati [**\_ DVDKaraokeData am**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) che indica come devono essere misti i canali ausiliari.



| Label | Valore |
|-------------------|-----------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ DvdKaraoke |



 



| ID proprietà                      | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE | Valore BOOLEAN. Lo strumento di navigazione dvd invia al decodificatore un \_ DVD AM PROPERTYKARAOKE ENABLE con valore TRUE per abilitare il downmixing o FALSE per \_ \_ disabilitarlo.                                                                                                                                      |
| PROPRIETÀ \_ AM \_ DVDKARAOKE \_ DATA   | Lo strumento di navigazione dvd invia al decodificatore una proprietà AM PROPERTY DVDKARAOKE DATA con un puntatore a una struttura \_ \_ AM \_ [**\_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) per modificare la configurazione downmix, ad esempio per attivare o disattivare determinati canali di canali e indirizzarli al canale di output destro o sinistro. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




