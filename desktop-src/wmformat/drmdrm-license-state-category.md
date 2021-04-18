---
title: Enumerazione DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)
description: Il \_ \_ tipo di enumerazione dello stato della licenza DRM \_ specifica il tipo di restrizione della licenza descritta dalla \_ \_ struttura dei dati dello stato delle licenze DRM \_ .
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- Formato Windows Media enumerazione DRM_LICENSE_STATE_CATEGORY
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e928a95a71d9636f88bc3c79ac36168072527040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330882"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>Enumerazione DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)

Il tipo di enumerazione **\_ \_ dello stato \_** della licenza DRM specifica il tipo di restrizione della licenza descritta dalla struttura [**\_ \_ \_ dei dati dello stato delle licenze DRM**](drmdrm-license-state-data.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef enum DRM_LICENSE_STATE_CATEGORY { 
  WM_DRM_LICENSE_STATE_NORIGHT                    = 0,
  WM_DRM_LICENSE_STATE_UNLIM,
  WM_DRM_LICENSE_STATE_COUNT,
  WM_DRM_LICENSE_STATE_FROM,
  WM_DRM_LICENSE_STATE_UNTIL,
  WM_DRM_LICENSE_STATE_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM,
  WM_DRM_LICENSE_STATE_COUNT_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE
} DRM_LICENSE_STATE_CATEGORY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**stato della licenza di WM \_ DRM \_ \_ \_ noright**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** non è consentita.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_ \_ \_ UNLIM stato licenza WM \_ DRM**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ dati di \_ stato \_ della licenza DRM** è consentita senza restrizioni.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_ \_ \_ conteggio stato licenze WM \_ DRM**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita, ma solo un numero di volte.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ stato della licenza WM DRM \_ \_ da**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita dopo una data impostata.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**\_stato della licenza WM DRM \_ \_ \_ fino a**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita fino a una data impostata.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ stato della licenza WM DRM \_ \_ da \_ fino a**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita tra due date impostate.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita, ma solo per un numero di volte successivo a una data impostata.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_ \_ conteggio stato licenze WM DRM \_ \_ \_ fino a**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita, ma solo un numero di volte fino a una data impostata.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ conteggio stato licenze WM DRM \_ \_ \_ da \_ fino a**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita, ma solo un numero impostato di volte tra due date impostate.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_ \_ scadenza dello stato della licenza WM DRM \_ \_ \_ dopo \_ FIRSTUSE**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita per un periodo di tempo impostato a partire dal primo utilizzo dell'azione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





