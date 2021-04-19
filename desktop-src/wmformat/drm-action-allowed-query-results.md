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
# <a name="drm_action_allowed_query_results-enumeration"></a><span data-ttu-id="e3297-105">\_ \_ \_ Enumerazione dei risultati della query consentita azione DRM \_</span><span class="sxs-lookup"><span data-stu-id="e3297-105">DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS enumeration</span></span>

<span data-ttu-id="e3297-106">Il tipo di enumerazione dei **\_ \_ \_ \_ risultati delle query consentiti per l'azione DRM** viene usato dall'interfaccia [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) per specificare il motivo per cui non è consentita un'azione.</span><span class="sxs-lookup"><span data-stu-id="e3297-106">The **DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS** enumeration type is used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3297-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3297-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="e3297-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="e3297-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e3297-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**\_ \_ query consentita azione DRM \_ \_ non \_ abilitata**</span><span class="sxs-lookup"><span data-stu-id="e3297-109"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED"></span><span id="drm_action_allowed_query_not_enabled"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-110">Specifica che l'azione query non è consentita.</span><span class="sxs-lookup"><span data-stu-id="e3297-110">Specifies that the queries action is not allowed.</span></span> <span data-ttu-id="e3297-111">Per le azioni non consentite, il valore restituito è questo valore combinato utilizzando un operatore OR bit per bit con uno o più degli altri valori di questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e3297-111">For actions that are not allowed, the returned value is this value combined by using a bitwise OR with one or more of the other values in this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**\_query di azione DRM \_ consentita \_ \_ non \_ abilitata \_ senza \_ licenza**</span><span class="sxs-lookup"><span data-stu-id="e3297-112"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_LICENSE"></span><span id="drm_action_allowed_query_not_enabled_no_license"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-113">Specifica che non esiste una licenza per il contenuto richiesto.</span><span class="sxs-lookup"><span data-stu-id="e3297-113">Specifies that a license does not exist for the requested content.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**\_query di azione DRM \_ consentita \_ \_ non \_ abilitata \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3297-114"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_RIGHT"></span><span id="drm_action_allowed_query_not_enabled_no_right"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-115">Specifica che esiste una licenza per il contenuto, ma che il diritto sottoposto a query non è consentito.</span><span class="sxs-lookup"><span data-stu-id="e3297-115">Specifies that a license exists for the content, but that the queried right is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**\_non è \_ stata \_ \_ \_ ABILITAta la query azione \_ DRM consentita**</span><span class="sxs-lookup"><span data-stu-id="e3297-116"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXHAUSTED"></span><span id="drm_action_allowed_query_not_enabled_exhausted"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXHAUSTED**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-117">Specifica che il diritto sottoposto a query è limitato da un conteggio e che non viene più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e3297-117">Specifies that the queried right is restricted by a count, and that no more uses remain.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ \_ scaduta**</span><span class="sxs-lookup"><span data-stu-id="e3297-118"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_EXPIRED"></span><span id="drm_action_allowed_query_not_enabled_expired"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-119">Specifica che il diritto sottoposto a query è limitato a una data di scadenza precedente alla data corrente.</span><span class="sxs-lookup"><span data-stu-id="e3297-119">Specifies that the queried right is restricted with an expiration date that is earlier than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**\_query di azione DRM \_ consentita \_ \_ non \_ abilitata \_ non \_ avviata**</span><span class="sxs-lookup"><span data-stu-id="e3297-120"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NOT_STARTED"></span><span id="drm_action_allowed_query_not_enabled_not_started"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NOT\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-121">Specifica che il diritto sottoposto a query è limitato a una data di inizio successiva alla data corrente.</span><span class="sxs-lookup"><span data-stu-id="e3297-121">Specifies that the queried right is restricted with a start date that is later than the current date.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ abilitata \_ appsec \_ troppo \_ bassa**</span><span class="sxs-lookup"><span data-stu-id="e3297-122"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_APPSEC_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_appsec_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_APPSEC\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-123">Specifica che esiste una licenza per il contenuto e che la licenza consente il diritto di query, ma che il livello di sicurezza dell'applicazione chiamante non è sufficientemente elevato.</span><span class="sxs-lookup"><span data-stu-id="e3297-123">Specifies that a license exists for the content and that the license allows the queried right, but that the security level of the calling application is not high enough.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**\_richiesta di azione DRM \_ \_ \_ non \_ abilitata per la \_ \_ indiv req**</span><span class="sxs-lookup"><span data-stu-id="e3297-124"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_REQ_INDIV"></span><span id="drm_action_allowed_query_not_enabled_req_indiv"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_REQ\_INDIV**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-125">Specifica che esiste una licenza per il contenuto e che la licenza consente il diritto sottoposto a query, ma che il sottosistema DRM deve essere individualizzato.</span><span class="sxs-lookup"><span data-stu-id="e3297-125">Specifies that a license exists for the content and that the license allows the queried right, but that the DRM subsystem must be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ abilitata \_ Copia \_ OPL \_ troppo \_ bassa**</span><span class="sxs-lookup"><span data-stu-id="e3297-126"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_TOO_LOW"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_too_low"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_TOO\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-127">Specifica che il livello di protezione dell'output del client è troppo basso.</span><span class="sxs-lookup"><span data-stu-id="e3297-127">Specifies that the output protection level of the client is too low.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**\_azione DRM \_ consentita di \_ query \_ non \_ abilitata \_ Copia \_ OPL \_ esclusa**</span><span class="sxs-lookup"><span data-stu-id="e3297-128"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_COPY_OPL_EXCLUDED"></span><span id="drm_action_allowed_query_not_enabled_copy_opl_excluded"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_COPY\_OPL\_EXCLUDED**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-129">Specifica che il livello di protezione dell'output del client si trova nell'elenco di esclusione.</span><span class="sxs-lookup"><span data-stu-id="e3297-129">Specifies that the output protection level of the client is on the exclusion list.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ abilitata \_ senza \_ \_ supporto Clock**</span><span class="sxs-lookup"><span data-stu-id="e3297-130"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_CLOCK_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_clock_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_CLOCK\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-131">Specifica che la licenza richiede il supporto del clock protetto e che il client non lo fornisce.</span><span class="sxs-lookup"><span data-stu-id="e3297-131">Specifies that the license requires secure clock support and that the client does not provide it.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**la \_ query di azione DRM \_ consentita \_ \_ non è \_ abilitata \_ senza \_ supporto di misurazione \_**</span><span class="sxs-lookup"><span data-stu-id="e3297-132"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_NO_METERING_SUPPORT"></span><span id="drm_action_allowed_query_not_enabled_no_metering_support"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_NO\_METERING\_SUPPORT**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-133">Specifica che l'azione sottoposta a query è consentita da una licenza, ma tale misurazione è obbligatoria e il client non supporta la misurazione.</span><span class="sxs-lookup"><span data-stu-id="e3297-133">Specifies that the queried action is allowed by a license, but that metering is required and the client does not support metering.</span></span>

</dd> <dt>

<span data-ttu-id="e3297-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**azione DRM la \_ \_ query consentita \_ non è \_ \_ abilitata \_ profondità della catena \_ \_ troppo \_ elevata**</span><span class="sxs-lookup"><span data-stu-id="e3297-134"><span id="DRM_ACTION_ALLOWED_QUERY_NOT_ENABLED_CHAIN_DEPTH_TOO_HIGH"></span><span id="drm_action_allowed_query_not_enabled_chain_depth_too_high"></span>**DRM\_ACTION\_ALLOWED\_QUERY\_NOT\_ENABLED\_CHAIN\_DEPTH\_TOO\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="e3297-135">Specifica che i diritti per l'azione sottoposta a query non possono essere determinati perché il contenuto è coperto da una licenza concatenata e la licenza foglia è mancante.</span><span class="sxs-lookup"><span data-stu-id="e3297-135">Specifies that the rights for the queried action cannot be determined because the content is covered by a chained license and the leaf license is missing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3297-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3297-136">Remarks</span></span>

<span data-ttu-id="e3297-137">I valori di questo tipo di enumerazione indicano che un'azione non è consentita.</span><span class="sxs-lookup"><span data-stu-id="e3297-137">The values of this enumeration type indicate that an action is not allowed.</span></span> <span data-ttu-id="e3297-138">Un valore pari a zero indica che l'azione è consentita.</span><span class="sxs-lookup"><span data-stu-id="e3297-138">A value of zero indicates that the action is allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3297-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3297-139">Requirements</span></span>



| <span data-ttu-id="e3297-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3297-140">Requirement</span></span> | <span data-ttu-id="e3297-141">Valore</span><span class="sxs-lookup"><span data-stu-id="e3297-141">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3297-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3297-142">Header</span></span><br/> | <dl> <span data-ttu-id="e3297-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3297-143"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3297-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3297-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3297-145">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="e3297-145">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





