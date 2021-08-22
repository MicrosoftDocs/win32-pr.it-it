---
title: DRM_ACTION_ALLOWED_QUERY_RESULTS di controllo (Wmdrmsdk.h)
description: Il tipo di enumerazione DRM ACTION ALLOWED QUERY RESULTS viene usato dall'interfaccia \_ \_ \_ IWMDRMLicenseQuery QueryActionAllowed per specificare il motivo per cui un'azione \_ non è consentita.
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- DRM_ACTION_ALLOWED_QUERY_RESULTS enumeration windows Media Format
- enumeration windows Media Format
topic_type:
- apiref
api_name:
- DRM_ACTION_ALLOWED_QUERY_RESULTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d66973838bb6d9cf745ae30b885acccf7b4b311834bbe827d96ccbeea501bd17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547811"
---
# <a name="drm_action_allowed_query_results-enumeration"></a>Enumerazione DRM \_ ACTION \_ ALLOWED QUERY \_ \_ RESULTS

Il **tipo di enumerazione DRM ACTION ALLOWED QUERY \_ \_ \_ \_ RESULTS** viene usato dall'interfaccia [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) per specificare il motivo per cui un'azione non è consentita.

## <a name="syntax"></a>Sintassi


```C++
typedef enum DRM_ACTION_ALLOWED_QUERY_RESULTS { 
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED                       = 0x00000001,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE            = 0x00000002,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT              = 0x00000004,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED             = 0x00000008,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED               = 0x00000010,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED           = 0x00000020,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW        = 0x00000040,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV             = 0x00000080,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW      = 0x00000100,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED     = 0x00000200,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT      = 0x00000400,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT   = 0x00000800,
  DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH  = 0x00001000
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**QUERY CONSENTITA AZIONE DRM \_ \_ NON \_ \_ \_ ABILITATA**
</dt> <dd>

Specifica che l'azione query non è consentita. Per le azioni non consentite, il valore restituito è questo valore combinato usando un'operazione OR bit per bit con uno o più degli altri valori di questa enumerazione.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA NESSUNA \_ \_ LICENZA**
</dt> <dd>

Specifica che non esiste una licenza per il contenuto richiesto.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA NESSUN \_ \_ DIRITTO**
</dt> <dd>

Specifica che esiste una licenza per il contenuto, ma che il diritto sottoposto a query non è consentito.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**QUERY CONSENTITA AZIONE DRM \_ \_ NON \_ \_ \_ ABILITATA \_ ESAURITA**
</dt> <dd>

Specifica che il diritto sottoposto a query è limitato da un conteggio e che non rimangono più utilizzi.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA \_ SCADUTA**
</dt> <dd>

Specifica che il diritto sottoposto a query è limitato a una data di scadenza precedente alla data corrente.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA NON \_ \_ AVVIATA**
</dt> <dd>

Specifica che il diritto sottoposto a query è limitato a una data di inizio successiva alla data corrente.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA \_ APPSEC TROPPO \_ \_ BASSA**
</dt> <dd>

Specifica che esiste una licenza per il contenuto e che la licenza consente il diritto sottoposto a query, ma che il livello di sicurezza dell'applicazione chiamante non è sufficientemente elevato.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA \_ REQ \_ INDIV**
</dt> <dd>

Specifica che esiste una licenza per il contenuto e che la licenza consente il diritto sottoposto a query, ma che il sottosistema DRM deve essere individualizzato.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA COPIA \_ \_ OPL TROPPO \_ \_ BASSA**
</dt> <dd>

Specifica che il livello di protezione dell'output del client è troppo basso.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA COPIA \_ \_ OPL \_ ESCLUSA**
</dt> <dd>

Specifica che il livello di protezione dell'output del client si trova nell'elenco di esclusione.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA NESSUN SUPPORTO \_ \_ \_ OROLOGIO**
</dt> <dd>

Specifica che la licenza richiede il supporto dell'orologio sicuro e che il client non lo fornisce.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA NESSUN SUPPORTO DI \_ \_ \_ MISURAZIONE**
</dt> <dd>

Specifica che l'azione su cui viene eseguita una query è consentita da una licenza, ma tale misurazione è obbligatoria e il client non supporta la misurazione.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**AZIONE DRM \_ \_ CONSENTITA \_ QUERY NON \_ \_ ABILITATA PROFONDITÀ CATENA TROPPO \_ \_ \_ \_ ALTA**
</dt> <dd>

Specifica che non è possibile determinare i diritti per l'azione su cui viene eseguita la query perché il contenuto è coperto da una licenza concatenata e la licenza foglia è mancante.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori di questo tipo di enumerazione indicano che un'azione non è consentita. Il valore zero indica che l'azione è consentita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





