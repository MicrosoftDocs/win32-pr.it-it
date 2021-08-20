---
description: L'enumerazione TRACK \_ SEARCH FLAGS specifica le condizioni limite per la ricerca di un oggetto nella sequenza \_ \_ temporale.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: DEXTERF_TRACK_SEARCH_FLAGS enumerazione (Qedit.h)
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
ms.openlocfilehash: 55d7c70dffbf57ae4d9788a10dfea02911a998e21ab5ea8e3d9ad7fffcf91624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952940"
---
# <a name="dexterf_track_search_flags-enumeration"></a>Enumerazione FLAGSF \_ TRACK \_ SEARCH \_ FLAGS

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`DEXTERF_TRACK_SEARCH_FLAGS`L'enumerazione specifica le condizioni limite per la ricerca di un oggetto nella sequenza temporale.

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

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DELIMITAZIONE DI \_ BOUNDING DI BOUNDF**
</dt> <dd>

Cercare un oggetto che si estende nell'ora specificata.

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**EVASO \_ \_ ESATTAMENTE ALLE ORE**
</dt> <dd>

Cercare un oggetto che inizia esattamente all'ora specificata.

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**FORWARDS DI \_ EF**
</dt> <dd>

Cercare un oggetto che inizia all'ora specificata o successiva.

</dd> </dl>

## <a name="remarks"></a>Commenti

Queste condizioni limite sono riepilogate nella tabella seguente.



| Valore di enumerazione    | Condizione limite                        |
|----------------------|-------------------------------------------|
| DELIMITAZIONE DI \_ BOUNDING DI BOUNDF    | Start <= TimeStop > Time<br/> |
| EVASO \_ \_ ESATTAMENTE ALLE ORE | Start == Time                             |
| FORWARDS DI \_ EF    | Start >= Time                          |



 

-   Start: ora di inizio dell'oggetto recuperato.
-   Stop: ora di arresto dell'oggetto recuperato.
-   Time: tempo di ricerca specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




