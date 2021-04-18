---
title: Enumerazione DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
description: Il \_ \_ tipo di enumerazione dello stato di individualizzazione DRM definisce gli stati validi per l'individualizzazione DRM. | Enumerazione DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- Formato Windows Media enumerazione DRM_INDIVIDUALIZATION_STATUS
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331989"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="d811e-106">Enumerazione DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="d811e-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="d811e-107">Il tipo di enumerazione **\_ \_ dello stato di individualizzazione DRM** definisce gli stati validi per l'individualizzazione DRM.</span><span class="sxs-lookup"><span data-stu-id="d811e-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM individualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="d811e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d811e-108">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="d811e-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="d811e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d811e-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI non \_ definito**</span><span class="sxs-lookup"><span data-stu-id="d811e-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="d811e-111">Questo valore è riservato per l'uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d811e-111">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="d811e-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**\_inizio indi**</span><span class="sxs-lookup"><span data-stu-id="d811e-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="d811e-113">Indica l'inizio del processo di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d811e-113">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="d811e-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**operazione INDI \_ riuscita**</span><span class="sxs-lookup"><span data-stu-id="d811e-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="d811e-115">Indica che il processo di individualizzazione è stato completato.</span><span class="sxs-lookup"><span data-stu-id="d811e-115">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="d811e-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**\_errore indi**</span><span class="sxs-lookup"><span data-stu-id="d811e-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="d811e-117">Indica che il processo di individualizzazione non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d811e-117">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="d811e-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**\_Annulla indi**</span><span class="sxs-lookup"><span data-stu-id="d811e-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="d811e-119">Indica che il processo di individualizzazione è stato annullato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d811e-119">Indicates that the individualization process was canceled by the application.</span></span>

</dd> <dt>

<span data-ttu-id="d811e-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**\_download indi**</span><span class="sxs-lookup"><span data-stu-id="d811e-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="d811e-121">Indica che è in corso il download dell'aggiornamento della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d811e-121">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="d811e-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**\_installazione indi**</span><span class="sxs-lookup"><span data-stu-id="d811e-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="d811e-123">Indica che è in corso l'installazione dell'aggiornamento della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d811e-123">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d811e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="d811e-124">Remarks</span></span>

<span data-ttu-id="d811e-125">Questa enumerazione viene utilizzata dalla struttura [**di \_ \_ stato di personalizzazione WM**](drmwm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="d811e-125">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d811e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d811e-126">Requirements</span></span>



| <span data-ttu-id="d811e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d811e-127">Requirement</span></span> | <span data-ttu-id="d811e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="d811e-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d811e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d811e-129">Header</span></span><br/> | <dl> <span data-ttu-id="d811e-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d811e-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d811e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d811e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d811e-132">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="d811e-132">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





