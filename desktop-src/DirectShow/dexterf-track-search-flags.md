---
description: L' \_ enumerazione DEXTERF Track \_ Search \_ flags specifica le condizioni di limite in una ricerca di un oggetto nella sequenza temporale.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Enumerazione DEXTERF_TRACK_SEARCH_FLAGS (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330660"
---
# <a name="dexterf_track_search_flags-enumeration"></a>\_ \_ Enumerazione flag di ricerca DEXTERF Track \_

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `DEXTERF_TRACK_SEARCH_FLAGS` enumerazione specifica le condizioni di limite in una ricerca di un oggetto nella sequenza temporale.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**\_delimitatore DEXTERF**
</dt> <dd>

Cerca un oggetto che si estende sul tempo specificato.

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ esattamente \_ alle**
</dt> <dd>

Cercare un oggetto che si avvii esattamente all'ora specificata.

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF \_ inoltri**
</dt> <dd>

Cercare un oggetto che inizia all'ora specificata o successiva.

</dd> </dl>

## <a name="remarks"></a>Commenti

Queste condizioni di limite sono riepilogate nella tabella seguente.



| Valore di enumerazione    | Condizione limite                        |
|----------------------|-------------------------------------------|
| \_delimitatore DEXTERF    | Start <= TimeStop > Time<br/> |
| DEXTERF \_ esattamente \_ alle | Inizio = = ora                             |
| DEXTERF \_ inoltri    | Inizio >= ora                          |



 

-   Start: ora di inizio dell'oggetto recuperato.
-   Stop: ora di arresto dell'oggetto recuperato.
-   Ora: tempo di ricerca specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




