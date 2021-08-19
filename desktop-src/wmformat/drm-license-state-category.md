---
title: DRM_LICENSE_STATE_CATEGORY enumerazione (Drmexternals.h)
description: Il tipo di enumerazione DRM LICENSE STATE CATEGORY definisce le categorie per le stringhe di \_ \_ licenza \_ DRM visualizzate all'utente.
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- DRM_LICENSE_STATE_CATEGORY enumerazione Windows Media Format
- enumeration windows Media Format
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
ms.openlocfilehash: 2bbfd6c566d6c58314416c787110ea77da25416ed73d80ec87fd2d66602d820b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931001"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>DRM_LICENSE_STATE_CATEGORY enumerazione (Drmexternals.h)

Il **tipo di enumerazione DRM LICENSE STATE \_ \_ \_ CATEGORY** definisce le categorie per le stringhe di [*licenza*](wmformat-glossary.md) DRM visualizzate all'utente.

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

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**STATO \_ LICENZA WM DRM \_ \_ \_ NORIGHT**
</dt> <dd>

Indica che la stringa avrà il formato "Riproduzione non consentita".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**STATO DELLA LICENZA DI WM \_ DRM \_ \_ \_ UNLIM**
</dt> <dd>

Indica che la stringa avrà il formato "Playback unlimited".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**CONTEGGIO \_ STATO LICENZA WM DRM \_ \_ \_**
</dt> <dd>

Indica che la stringa avrà il formato "Playback valid 5 times" (Riproduzione valida 5 volte).

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**STATO DELLA LICENZA DI WM \_ DRM \_ \_ \_ DA**
</dt> <dd>

Indica che la stringa avrà il formato "Playback valid from 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**STATO DELLA LICENZA DI WM \_ DRM \_ FINO \_ \_ A**
</dt> <dd>

Indica che la stringa avrà il formato "Playback valid until 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**STATO DELLA LICENZA DI WM \_ DRM \_ DA FINO \_ \_ \_ A**
</dt> <dd>

Indica che la stringa avrà il formato "Playback valid from 5/12 to 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**CONTEGGIO STATO LICENZA WM \_ DRM \_ \_ \_ \_ DA**
</dt> <dd>

Indica che la stringa avrà il formato "Playback valid 5 times from 5/12 to 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ COUNT \_ UNTIL**
</dt> <dd>

Indica che la stringa avrà il formato "Playback valid 5 times until 7/12/00".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**CONTEGGIO \_ STATO LICENZA WM DRM \_ DA FINO \_ \_ \_ \_ A**
</dt> <dd>

Indica che la stringa avrà il formato "Playback valid 5 times from 5/12 to 9/12".

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**SCADENZA DELLO STATO DELLA LICENZA DI WM \_ DRM \_ DOPO \_ \_ \_ \_ FIRSTUSE**
</dt> <dd>

Indica che la stringa avrà il formato "Playback valid for 24 hours from first use".

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione indica la categoria per ogni possibile stringa di output da visualizzare. È un membro della struttura [**DRM \_ LICENSE \_ STATE \_**](drm-license-state-data.md) DATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





