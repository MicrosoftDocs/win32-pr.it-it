---
title: Struttura WMDRM_ANALOG_VIDEO_RESTRICTIONS (wmdrmsdk. h)
description: La \_ struttura di restrizioni video analoghe di WMDRM \_ \_ include informazioni su una restrizione per la riproduzione di contenuto come video analogico.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- Formato di Windows Media per la struttura WMDRM_ANALOG_VIDEO_RESTRICTIONS
- struttura Windows Media Format
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
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326608"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>\_Struttura di \_ restrizioni video ANALOGIche WMDRM \_

La struttura di **\_ \_ \_ restrizioni video analoghe di WMDRM** include informazioni su una restrizione per la riproduzione di contenuto come video analogico.

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

Identificatore di restrizione.

</dd> <dt>

**dwRestrictionData**
</dt> <dd>

Dati di restrizione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene ricevuta quando si chiama [**IWMDRMLicense:: GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> <dt>

[**\_ \_ restrizioni video ANALOGIche WMDRM \_ \_**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





