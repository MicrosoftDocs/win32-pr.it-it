---
title: Enumerazione DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)
description: Il \_ tipo di \_ enumerazione di categoria stato licenze DRM \_ definisce le categorie per le stringhe di licenza DRM visualizzate all'utente.
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- Formato Windows Media enumerazione DRM_LICENSE_STATE_CATEGORY
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40763ec7f610073784e3bd1516d4c955abcd65b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477944"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>Enumerazione DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)

Il tipo di enumerazione di **\_ \_ \_ Categoria stato licenze DRM** definisce le categorie per le stringhe di [*licenza*](wmformat-glossary.md) DRM visualizzate all'utente.

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
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**stato della licenza di WM \_ DRM \_ \_ \_ noright**
</dt> <dd>

Indica che la stringa ha il formato "riproduzione non consentita".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_ \_ \_ UNLIM stato licenza WM \_ DRM**
</dt> <dd>

Indica che la stringa ha il formato "playback Unlimited".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_ \_ \_ conteggio stato licenze WM \_ DRM**
</dt> <dd>

Indica che la stringa ha il formato "riproduzione valida 5 volte".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ stato della licenza WM DRM \_ \_ da**
</dt> <dd>

Indica che la stringa prende il formato "riproduzione valida da 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**\_stato della licenza WM DRM \_ \_ \_ fino a**
</dt> <dd>

Indica che il formato della stringa sarà "riproduzione valida fino a 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ stato della licenza WM DRM \_ \_ da \_ fino a**
</dt> <dd>

Indica che la stringa deve avere il formato "riproduzione valida da 5/12 a 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da**
</dt> <dd>

Indica che la stringa deve avere il formato "riproduzione valida 5 volte da 5/12 a 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_ \_ conteggio stato licenze WM DRM \_ \_ \_ fino a**
</dt> <dd>

Indica che il formato della stringa sarà "riproduzione valida 5 volte fino a 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ conteggio stato licenze WM DRM \_ \_ \_ da \_ fino a**
</dt> <dd>

Indica che la stringa deve avere il formato "riproduzione valida 5 volte da 5/12 a 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_ \_ scadenza dello stato della licenza WM DRM \_ \_ \_ dopo \_ FIRSTUSE**
</dt> <dd>

Indica che la stringa ha il formato "riproduzione valida per 24 ore dal primo utilizzo".

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione indica la categoria per ogni possibile stringa di output da visualizzare. Si tratta di un membro della struttura dei [**\_ dati di \_ stato \_ delle licenze DRM**](drm-license-state-data.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





