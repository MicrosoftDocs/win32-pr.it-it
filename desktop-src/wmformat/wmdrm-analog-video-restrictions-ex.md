---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX struttura (Wmdrmsdk.h)
description: La struttura WMDRM ANALOG VIDEO RESTRICTIONS EX contiene informazioni estese su una restrizione per la riproduzione \_ di contenuto come video \_ \_ \_ analogico.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX struttura windows Media Format
- struttura windows Media Format
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
ms.openlocfilehash: 0e9cbacff2d330c869c35eb7a3d1ca46ae6c80a030495ffec42eabc3726436c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006541"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>Struttura EX DELLE \_ \_ RESTRIZIONI VIDEO \_ ANALOGICHE WMDRM \_

La **struttura WMDRM \_ ANALOG VIDEO \_ \_ RESTRICTIONS \_ EX** contiene informazioni estese su una restrizione per la riproduzione di contenuto come video analogico.

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

Dimensioni dei dati di restrizione in byte.

</dd> <dt>

**pbRestrictionData**
</dt> <dd>

Dati di restrizione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> <dt>

[**RESTRIZIONI VIDEO \_ \_ ANALOGICO WMDRM \_**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





