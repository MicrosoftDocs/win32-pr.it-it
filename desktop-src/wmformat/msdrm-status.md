---
title: Enumerazione MSDRM_STATUS (wmdrmsdk. h)
description: Il \_ tipo di enumerazione dello stato MSDRM definisce le condizioni di stato per il sottosistema DRM.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- Formato Windows Media enumerazione MSDRM_STATUS
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2a73de9e33216e22a01966be8f2ed6a3185fdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326960"
---
# <a name="msdrm_status-enumeration"></a><span data-ttu-id="7d995-105">\_Enumerazione stato msdrm</span><span class="sxs-lookup"><span data-stu-id="7d995-105">MSDRM\_STATUS enumeration</span></span>

<span data-ttu-id="7d995-106">Il tipo di enumerazione **\_ dello stato MSDRM** definisce le condizioni di stato per il sottosistema DRM.</span><span class="sxs-lookup"><span data-stu-id="7d995-106">The **MSDRM\_STATUS** enumeration type defines status conditions for the DRM subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d995-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d995-107">Syntax</span></span>


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a><span data-ttu-id="7d995-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="7d995-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7d995-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**\_errore DRM**</span><span class="sxs-lookup"><span data-stu-id="7d995-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-110">Specifica che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="7d995-110">Specifies that an error has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**\_informazioni DRM**</span><span class="sxs-lookup"><span data-stu-id="7d995-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM\_INFORMATION**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-112">Specifica che sono presenti informazioni aggiuntive sullo stato.</span><span class="sxs-lookup"><span data-stu-id="7d995-112">Specifies that there is additional status information.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**\_inizio BACKUPRESTORE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="7d995-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM\_BACKUPRESTORE\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-114">Specifica l'inizio di un'operazione di backup o ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="7d995-114">Specifies that a license backup or restore operation has begun.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**\_fine BACKUPRESTORE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="7d995-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM\_BACKUPRESTORE\_END**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-116">Specifica che è stata terminata un'operazione di backup o ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="7d995-116">Specifies that a license backup or restore operation has ended.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**\_connessione DRM BACKUPRESTORE \_**</span><span class="sxs-lookup"><span data-stu-id="7d995-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM\_BACKUPRESTORE\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-118">Specifica che è in corso un'operazione di backup o ripristino della licenza e che il computer client si connette al server di backup.</span><span class="sxs-lookup"><span data-stu-id="7d995-118">Specifies that a license backup or restore operation is in progress and that the client computer is connecting with the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**disconnessione di \_ BACKUPRESTORE DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7d995-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM\_BACKUPRESTORE\_DISCONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-120">Specifica che è in corso un'operazione di backup o ripristino della licenza e che il computer client si sta disconnettendo dal server di backup.</span><span class="sxs-lookup"><span data-stu-id="7d995-120">Specifies that a license backup or restore operation is in progress and that the client computer is disconnecting from the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**\_errore DRM \_ WITHURL**</span><span class="sxs-lookup"><span data-stu-id="7d995-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM\_ERROR\_WITHURL**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-122">Specifica che l'operazione DRM ha rilevato un URL non valido.</span><span class="sxs-lookup"><span data-stu-id="7d995-122">Specifies that the DRM operation has encountered a bad URL.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_licenza con restrizioni DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7d995-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**DRM\_RESTRICTED\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-124">Specifica che l'operazione di DRM non può continuare perché non è presente alcuna licenza che conceda il diritto richiesto nel computer client.</span><span class="sxs-lookup"><span data-stu-id="7d995-124">Specifies that the DRM operation cannot continue because no license granting the required right exists on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ necessita di un' \_ individualizzazione**</span><span class="sxs-lookup"><span data-stu-id="7d995-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM\_NEEDS\_INDIVIDUALIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-126">Specifica che l'operazione DRM non può continuare perché il sottosistema DRM deve essere individualizzato.</span><span class="sxs-lookup"><span data-stu-id="7d995-126">Specifies that the DRM operation cannot continue because the DRM subsystem needs to be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**\_ \_ notifica OPL di riproduzione DRM \_**</span><span class="sxs-lookup"><span data-stu-id="7d995-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM\_PLAY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-128">Specifica che non è possibile completare un'operazione di riproduzione perché non è stato soddisfatto un requisito del livello di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="7d995-128">Specifies that a playback operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**\_ \_ notifica OPL copia \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="7d995-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM\_COPY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-130">Specifica che non è possibile completare un'operazione di copia perché non è stato soddisfatto un requisito del livello di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="7d995-130">Specifies that a copy operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="7d995-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**\_REFRESHCRL DRM \_ completato**</span><span class="sxs-lookup"><span data-stu-id="7d995-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM\_REFRESHCRL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="7d995-132">Specifica che una chiamata a [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) ha completato l'aggiornamento di un elenco di revoche.</span><span class="sxs-lookup"><span data-stu-id="7d995-132">Specifies that a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) has completed refreshing a revocation list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d995-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d995-133">Remarks</span></span>

<span data-ttu-id="7d995-134">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="7d995-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d995-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d995-135">Requirements</span></span>



| <span data-ttu-id="7d995-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d995-136">Requirement</span></span> | <span data-ttu-id="7d995-137">Valore</span><span class="sxs-lookup"><span data-stu-id="7d995-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d995-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d995-138">Header</span></span><br/> | <dl> <span data-ttu-id="7d995-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d995-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d995-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d995-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d995-141">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="7d995-141">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





