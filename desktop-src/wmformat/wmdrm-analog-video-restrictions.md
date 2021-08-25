---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS struttura (Wmdrmsdk.h)
description: La struttura WMDRM ANALOG VIDEO RESTRICTIONS contiene informazioni su una restrizione per la riproduzione \_ di contenuto come video \_ \_ analogo.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS struttura windows Media Format
- struttura windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8221fe325983387107f4e0c03f5672a6762502d8865e1d5895a9e48e96b99d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928811"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>Struttura DELLE RESTRIZIONI \_ \_ VIDEO \_ ANALOGICO WMDRM

La **struttura WMDRM \_ ANALOG VIDEO \_ \_ RESTRICTIONS** contiene informazioni su una restrizione per la riproduzione di contenuto come video analogo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**guidRestrictionID**
</dt> <dd>

Identificatore della restrizione.

</dd> <dt>

**dwRestrictionData**
</dt> <dd>

Dati di restrizione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene ricevuta quando si chiama [**IWMDRMLicense::GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> <dt>

[**RESTRIZIONI VIDEO \_ \_ ANALOGICO WMDRM \_ \_ AD ESEMPIO**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





