---
title: Struttura WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX (wmdrmsdk. h)
description: La \_ \_ struttura ex restrizioni video WMDRM analoghe \_ \_ include informazioni estese su una restrizione per la riproduzione di contenuto come video analogico.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- Formato di Windows Media per la struttura WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326609"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>WMDRM \_ la \_ \_ struttura ex restrizione del video analogico \_

La **struttura \_ \_ \_ \_ ex restrizioni video WMDRM analoghe** include informazioni estese su una restrizione per la riproduzione di contenuto come video analogico.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

Numero di versione.

</dd> <dt>

**guidRestrictionID**
</dt> <dd>

ID restrizione.

</dd> <dt>

**cbRestrictionData**
</dt> <dd>

Dimensioni in byte dei dati di restrizione.

</dd> <dt>

**pbRestrictionData**
</dt> <dd>

Dati di restrizione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> <dt>

[**\_restrizioni video analogiche WMDRM \_ \_**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





