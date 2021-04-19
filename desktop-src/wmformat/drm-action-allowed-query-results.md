---
title: Enumerazione DRM_ACTION_ALLOWED_QUERY_RESULTS (wmdrmsdk. h)
description: Il \_ tipo di \_ enumerazione dei risultati delle query consentiti per l'azione DRM \_ \_ viene usato dall'interfaccia QueryActionAllowed di IWMDRMLicenseQuery per specificare il motivo per cui non è consentita un'azione.
ms.assetid: dc784cdf-6efe-415b-ba72-eb8fc50bef10
keywords:
- Formato Windows Media enumerazione DRM_ACTION_ALLOWED_QUERY_RESULTS
- Enumerazione formato Windows Media
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
ms.openlocfilehash: 0d1e328acb915bd32547f3455e8556e4caba2360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332291"
---
# <a name="drm_action_allowed_query_results-enumeration"></a>\_ \_ \_ Enumerazione dei risultati della query consentita azione DRM \_

Il tipo di enumerazione dei **\_ \_ \_ \_ risultati delle query consentiti per l'azione DRM** viene usato dall'interfaccia [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) per specificare il motivo per cui non è consentita un'azione.

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

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**\_ \_ query consentita azione DRM \_ \_ non \_ abilitata**
</dt> <dd>

Specifica che l'azione query non è consentita. Per le azioni non consentite, il valore restituito è questo valore combinato utilizzando un operatore OR bit per bit con uno o più degli altri valori di questa enumerazione.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**\_query di azione DRM \_ consentita \_ \_ non \_ abilitata \_ senza \_ licenza**
</dt> <dd>

Specifica che non esiste una licenza per il contenuto richiesto.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**\_query di azione DRM \_ consentita \_ \_ non \_ abilitata \_ \_**
</dt> <dd>

Specifica che esiste una licenza per il contenuto, ma che il diritto sottoposto a query non è consentito.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_non è \_ stata \_ \_ \_ ABILITAta la query azione \_ DRM consentita**
</dt> <dd>

Specifica che il diritto sottoposto a query è limitato da un conteggio e che non viene più utilizzato.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ \_ scaduta**
</dt> <dd>

Specifica che il diritto sottoposto a query è limitato a una data di scadenza precedente alla data corrente.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**\_query di azione DRM \_ consentita \_ \_ non \_ abilitata \_ non \_ avviata**
</dt> <dd>

Specifica che il diritto sottoposto a query è limitato a una data di inizio successiva alla data corrente.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ abilitata \_ appsec \_ troppo \_ bassa**
</dt> <dd>

Specifica che esiste una licenza per il contenuto e che la licenza consente il diritto di query, ma che il livello di sicurezza dell'applicazione chiamante non è sufficientemente elevato.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**\_richiesta di azione DRM \_ \_ \_ non \_ abilitata per la \_ \_ indiv req**
</dt> <dd>

Specifica che esiste una licenza per il contenuto e che la licenza consente il diritto sottoposto a query, ma che il sottosistema DRM deve essere individualizzato.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ abilitata \_ Copia \_ OPL \_ troppo \_ bassa**
</dt> <dd>

Specifica che il livello di protezione dell'output del client è troppo basso.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**\_azione DRM \_ consentita di \_ query \_ non \_ abilitata \_ Copia \_ OPL \_ esclusa**
</dt> <dd>

Specifica che il livello di protezione dell'output del client si trova nell'elenco di esclusione.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ abilitata \_ senza \_ \_ supporto Clock**
</dt> <dd>

Specifica che la licenza richiede il supporto del clock protetto e che il client non lo fornisce.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ abilitata \_ senza \_ supporto di misurazione \_**
</dt> <dd>

Specifica che l'azione sottoposta a query è consentita da una licenza, ma tale misurazione è obbligatoria e il client non supporta la misurazione.

</dd> <dt>

<span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**azione DRM la \_ \_ query consentita \_ non è \_ \_ abilitata \_ profondità della catena \_ \_ troppo \_ elevata**
</dt> <dd>

Specifica che i diritti per l'azione sottoposta a query non possono essere determinati perché il contenuto è coperto da una licenza concatenata e la licenza foglia è mancante.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori di questo tipo di enumerazione indicano che un'azione non è consentita. Un valore pari a zero indica che l'azione è consentita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





