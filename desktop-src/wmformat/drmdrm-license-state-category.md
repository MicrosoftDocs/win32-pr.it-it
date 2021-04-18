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
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a><span data-ttu-id="98644-104">Enumerazione DRM_LICENSE_STATE_CATEGORY (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="98644-104">DRM_LICENSE_STATE_CATEGORY enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="98644-105">Il tipo di enumerazione **\_ \_ dello stato \_** della licenza DRM specifica il tipo di restrizione della licenza descritta dalla struttura [**\_ \_ \_ dei dati dello stato delle licenze DRM**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="98644-105">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="98644-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98644-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="98644-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="98644-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="98644-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**stato della licenza di WM \_ DRM \_ \_ \_ noright**</span><span class="sxs-lookup"><span data-stu-id="98644-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="98644-109">Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** non è consentita.</span><span class="sxs-lookup"><span data-stu-id="98644-109">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="98644-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_ \_ \_ UNLIM stato licenza WM \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="98644-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="98644-111">Specifica che l'azione per cui sono stati ricevuti i **\_ dati di \_ stato \_ della licenza DRM** è consentita senza restrizioni.</span><span class="sxs-lookup"><span data-stu-id="98644-111">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="98644-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_ \_ \_ conteggio stato licenze WM \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="98644-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="98644-113">Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita, ma solo un numero di volte.</span><span class="sxs-lookup"><span data-stu-id="98644-113">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times.</span></span>

</dd> <dt>

<span data-ttu-id="98644-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ stato della licenza WM DRM \_ \_ da**</span><span class="sxs-lookup"><span data-stu-id="98644-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="98644-115">Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita dopo una data impostata.</span><span class="sxs-lookup"><span data-stu-id="98644-115">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="98644-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**\_stato della licenza WM DRM \_ \_ \_ fino a**</span><span class="sxs-lookup"><span data-stu-id="98644-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="98644-117">Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita fino a una data impostata.</span><span class="sxs-lookup"><span data-stu-id="98644-117">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="98644-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ stato della licenza WM DRM \_ \_ da \_ fino a**</span><span class="sxs-lookup"><span data-stu-id="98644-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="98644-119">Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita tra due date impostate.</span><span class="sxs-lookup"><span data-stu-id="98644-119">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="98644-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da**</span><span class="sxs-lookup"><span data-stu-id="98644-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="98644-121">Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita, ma solo per un numero di volte successivo a una data impostata.</span><span class="sxs-lookup"><span data-stu-id="98644-121">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="98644-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_ \_ conteggio stato licenze WM DRM \_ \_ \_ fino a**</span><span class="sxs-lookup"><span data-stu-id="98644-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="98644-123">Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita, ma solo un numero di volte fino a una data impostata.</span><span class="sxs-lookup"><span data-stu-id="98644-123">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="98644-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ conteggio stato licenze WM DRM \_ \_ \_ da \_ fino a**</span><span class="sxs-lookup"><span data-stu-id="98644-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="98644-125">Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita, ma solo un numero impostato di volte tra due date impostate.</span><span class="sxs-lookup"><span data-stu-id="98644-125">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="98644-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_ \_ scadenza dello stato della licenza WM DRM \_ \_ \_ dopo \_ FIRSTUSE**</span><span class="sxs-lookup"><span data-stu-id="98644-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="98644-127">Specifica che l'azione per cui sono stati ricevuti i **\_ \_ \_ dati relativi allo stato della licenza DRM** è consentita per un periodo di tempo impostato a partire dal primo utilizzo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="98644-127">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed for a set amount of time beginning with the first use of the action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98644-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="98644-128">Remarks</span></span>

<span data-ttu-id="98644-129">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="98644-129">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="98644-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98644-130">Requirements</span></span>



| <span data-ttu-id="98644-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="98644-131">Requirement</span></span> | <span data-ttu-id="98644-132">Valore</span><span class="sxs-lookup"><span data-stu-id="98644-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98644-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98644-133">Header</span></span><br/> | <dl> <span data-ttu-id="98644-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="98644-134"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98644-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98644-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98644-136">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="98644-136">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





