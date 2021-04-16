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
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a><span data-ttu-id="78595-105">Enumerazione DRM_LICENSE_STATE_CATEGORY (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="78595-105">DRM_LICENSE_STATE_CATEGORY enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="78595-106">Il tipo di enumerazione di **\_ \_ \_ Categoria stato licenze DRM** definisce le categorie per le stringhe di [*licenza*](wmformat-glossary.md) DRM visualizzate all'utente.</span><span class="sxs-lookup"><span data-stu-id="78595-106">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type defines the categories for DRM [*license*](wmformat-glossary.md) strings that are displayed to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="78595-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78595-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="78595-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="78595-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="78595-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**stato della licenza di WM \_ DRM \_ \_ \_ noright**</span><span class="sxs-lookup"><span data-stu-id="78595-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="78595-110">Indica che la stringa ha il formato "riproduzione non consentita".</span><span class="sxs-lookup"><span data-stu-id="78595-110">Indicates the string will take the form "Playback not permitted."</span></span>

</dd> <dt>

<span data-ttu-id="78595-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**\_ \_ \_ UNLIM stato licenza WM \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="78595-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="78595-112">Indica che la stringa ha il formato "playback Unlimited".</span><span class="sxs-lookup"><span data-stu-id="78595-112">Indicates the string will take the form "Playback unlimited."</span></span>

</dd> <dt>

<span data-ttu-id="78595-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**\_ \_ \_ conteggio stato licenze WM \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="78595-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="78595-114">Indica che la stringa ha il formato "riproduzione valida 5 volte".</span><span class="sxs-lookup"><span data-stu-id="78595-114">Indicates the string will take the form "Playback valid 5 times."</span></span>

</dd> <dt>

<span data-ttu-id="78595-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**\_ \_ stato della licenza WM DRM \_ \_ da**</span><span class="sxs-lookup"><span data-stu-id="78595-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="78595-116">Indica che la stringa prende il formato "riproduzione valida da 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="78595-116">Indicates the string will take the form "Playback valid from 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="78595-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**\_stato della licenza WM DRM \_ \_ \_ fino a**</span><span class="sxs-lookup"><span data-stu-id="78595-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="78595-118">Indica che il formato della stringa sarà "riproduzione valida fino a 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="78595-118">Indicates the string will take the form "Playback valid until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="78595-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**\_ \_ stato della licenza WM DRM \_ \_ da \_ fino a**</span><span class="sxs-lookup"><span data-stu-id="78595-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="78595-120">Indica che la stringa deve avere il formato "riproduzione valida da 5/12 a 9/12".</span><span class="sxs-lookup"><span data-stu-id="78595-120">Indicates the string will take the form "Playback valid from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="78595-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_ \_ \_ conteggio dello stato di licenza WM DRM \_ \_ da**</span><span class="sxs-lookup"><span data-stu-id="78595-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="78595-122">Indica che la stringa deve avere il formato "riproduzione valida 5 volte da 5/12 a 9/12".</span><span class="sxs-lookup"><span data-stu-id="78595-122">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="78595-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**\_ \_ conteggio stato licenze WM DRM \_ \_ \_ fino a**</span><span class="sxs-lookup"><span data-stu-id="78595-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="78595-124">Indica che il formato della stringa sarà "riproduzione valida 5 volte fino a 7/12/00".</span><span class="sxs-lookup"><span data-stu-id="78595-124">Indicates the string will take the form "Playback valid 5 times until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="78595-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**\_ \_ conteggio stato licenze WM DRM \_ \_ \_ da \_ fino a**</span><span class="sxs-lookup"><span data-stu-id="78595-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="78595-126">Indica che la stringa deve avere il formato "riproduzione valida 5 volte da 5/12 a 9/12".</span><span class="sxs-lookup"><span data-stu-id="78595-126">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="78595-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**\_ \_ scadenza dello stato della licenza WM DRM \_ \_ \_ dopo \_ FIRSTUSE**</span><span class="sxs-lookup"><span data-stu-id="78595-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="78595-128">Indica che la stringa ha il formato "riproduzione valida per 24 ore dal primo utilizzo".</span><span class="sxs-lookup"><span data-stu-id="78595-128">Indicates the string will take the form "Playback valid for 24 hours from first use."</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78595-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="78595-129">Remarks</span></span>

<span data-ttu-id="78595-130">Questa enumerazione indica la categoria per ogni possibile stringa di output da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="78595-130">This enumeration indicates the category for each possible output string to be displayed.</span></span> <span data-ttu-id="78595-131">Si tratta di un membro della struttura dei [**\_ dati di \_ stato \_ delle licenze DRM**](drm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="78595-131">It is a member of the [**DRM\_LICENSE\_STATE\_DATA**](drm-license-state-data.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="78595-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78595-132">Requirements</span></span>



| <span data-ttu-id="78595-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="78595-133">Requirement</span></span> | <span data-ttu-id="78595-134">Valore</span><span class="sxs-lookup"><span data-stu-id="78595-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="78595-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78595-135">Minimum supported client</span></span><br/> | <span data-ttu-id="78595-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78595-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="78595-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78595-137">Minimum supported server</span></span><br/> | <span data-ttu-id="78595-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78595-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="78595-139">Versione</span><span class="sxs-lookup"><span data-stu-id="78595-139">Version</span></span><br/>                  | <span data-ttu-id="78595-140">Windows Media Format 7 SDK o versioni successive dell'SDK</span><span class="sxs-lookup"><span data-stu-id="78595-140">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="78595-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78595-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="78595-142"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="78595-142"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78595-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78595-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78595-144">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="78595-144">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





