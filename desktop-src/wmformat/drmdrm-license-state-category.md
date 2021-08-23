---
title: DRM_LICENSE_STATE_CATEGORY enumerazione (Wmdrmsdk.h)
description: Il tipo di enumerazione DRM LICENSE STATE CATEGORY specifica il tipo di restrizione di licenza descritto \_ \_ da una struttura \_ DRM LICENSE STATE \_ \_ \_ DATA.
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- DRM_LICENSE_STATE_CATEGORY di enumerazione windows Media Format
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
ms.openlocfilehash: 43b8724526142236b70faade68bf7d3ca358eb3f3810cae73f58adde17f25a0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591571"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>DRM_LICENSE_STATE_CATEGORY enumerazione (Wmdrmsdk.h)

Il **tipo di enumerazione DRM LICENSE STATE \_ \_ \_ CATEGORY** specifica il tipo di restrizione di licenza descritto da una struttura [**DRM LICENSE STATE \_ \_ \_ DATA.**](drmdrm-license-state-data.md)

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

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**STATO \_ LICENZA WM DRM \_ \_ \_ NORIGHT**
</dt> <dd>

Specifica che non è consentita l'azione per la quale sono stati ricevuti i dati relativi allo stato **DRM \_ LICENSE. \_ \_**

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**STATO \_ LICENZA WM DRM \_ \_ \_ UNLIM**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti **i dati DRM \_ LICENSE STATE \_ \_ è** consentita senza restrizioni.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**CONTEGGIO STATO LICENZA WM \_ DRM \_ \_ \_**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti **i dati DRM \_ LICENSE STATE \_ \_ è** consentita, ma solo un certo numero di volte.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**STATO DELLA LICENZA DI WM \_ DRM \_ \_ \_ DA**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **dati DRM \_ LICENSE STATE \_ \_ è** consentita dopo una data impostata.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**STATO DELLA LICENZA DI WM \_ DRM \_ FINO \_ \_ A**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti **i dati DRM \_ LICENSE STATE \_ \_ è** consentita fino a una data impostata.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**STATO DELLA LICENZA DI WM \_ DRM \_ DA FINO \_ \_ \_ A**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti **i dati DRM \_ LICENSE STATE \_ \_ è** consentita tra due date impostate.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**CONTEGGIO STATO LICENZA WM \_ DRM \_ \_ \_ \_ DA**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **dati DRM \_ LICENSE STATE \_ \_ è** consentita, ma solo un numero impostato di volte dopo una data impostata.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**CONTEGGIO STATO LICENZA WM \_ DRM \_ FINO \_ \_ \_ A**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **dati DRM \_ LICENSE STATE \_ \_ è** consentita, ma solo un certo numero di volte fino a una data impostata.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**CONTEGGIO STATO LICENZA WM \_ DRM \_ DA FINO \_ \_ \_ \_ A**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **dati DRM \_ LICENSE STATE \_ \_ è** consentita, ma solo un certo numero di volte tra due date impostate.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**SCADENZA \_ DELLO STATO DELLA LICENZA WM DRM DOPO \_ \_ \_ \_ \_ FIRSTUSE**
</dt> <dd>

Specifica che l'azione per cui sono stati ricevuti i **dati DRM \_ LICENSE STATE \_ \_ è** consentita per un periodo di tempo impostato a partire dal primo utilizzo dell'azione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





