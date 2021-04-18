---
description: Definisce lo stato di output Protection Manager (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: Enumerazione MF_MEDIA_ENGINE_OPM_STATUS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320545"
---
# <a name="mf_media_engine_opm_status-enumeration"></a><span data-ttu-id="ed1d2-103">\_ \_ \_ Enumerazione stato OPM del motore multimediale MF \_</span><span class="sxs-lookup"><span data-stu-id="ed1d2-103">MF\_MEDIA\_ENGINE\_OPM\_STATUS enumeration</span></span>

<span data-ttu-id="ed1d2-104">Definisce lo stato di [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="ed1d2-104">Defines the status of the [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed1d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed1d2-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a><span data-ttu-id="ed1d2-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="ed1d2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ed1d2-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF \_ media \_ Engine \_ OPM \_ non \_ richiesto**</span><span class="sxs-lookup"><span data-stu-id="ed1d2-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF\_MEDIA\_ENGINE\_OPM\_NOT\_REQUESTED**</span></span>
</dt> <dd>

<span data-ttu-id="ed1d2-108">Stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="ed1d2-108">Default status.</span></span> <span data-ttu-id="ed1d2-109">Utilizzato per restituire lo stato corretto quando il contenuto non è protetto.</span><span class="sxs-lookup"><span data-stu-id="ed1d2-109">Used to return the correct status when the content is unprotected.</span></span>

</dd> <dt>

<span data-ttu-id="ed1d2-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF \_ media \_ Engine \_ OPM \_ stabilito**</span><span class="sxs-lookup"><span data-stu-id="ed1d2-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF\_MEDIA\_ENGINE\_OPM\_ESTABLISHED**</span></span>
</dt> <dd>

<span data-ttu-id="ed1d2-111">La creazione di OPM è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ed1d2-111">OPM successfully established.</span></span>

</dd> <dt>

<span data-ttu-id="ed1d2-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**\_ \_ \_ \_ VM non riuscita del motore multimediale MF \_**</span><span class="sxs-lookup"><span data-stu-id="ed1d2-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="ed1d2-113">OPM non riuscito perché è in esecuzione in una macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="ed1d2-113">OPM failed because running in a virtual machined (VM).</span></span>

</dd> <dt>

<span data-ttu-id="ed1d2-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF \_ media \_ Engine \_ OPM \_ non riuscito \_ BDA**</span><span class="sxs-lookup"><span data-stu-id="ed1d2-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_BDA**</span></span>
</dt> <dd>

<span data-ttu-id="ed1d2-115">OPM non riuscito perché non è presente alcun driver grafico e il sistema usa la scheda di visualizzazione di base (BDA).</span><span class="sxs-lookup"><span data-stu-id="ed1d2-115">OPM failed because there is no graphics driver and the system is using Basic Display Adapter (BDA).</span></span>

</dd> <dt>

<span data-ttu-id="ed1d2-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**\_ \_ \_ \_ \_ driver non firmato \_ per MF Media Engine OPM**</span><span class="sxs-lookup"><span data-stu-id="ed1d2-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_UNSIGNED\_DRIVER**</span></span>
</dt> <dd>

<span data-ttu-id="ed1d2-117">L'accesso ad OPM non è riuscito perché il driver di grafica non è firmato PE e viene eseguito il fallback a WARP.</span><span class="sxs-lookup"><span data-stu-id="ed1d2-117">OPM failed because the graphics driver is not PE signed, falling back to WARP.</span></span>

</dd> <dt>

<span data-ttu-id="ed1d2-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF \_ media \_ Engine \_ OPM \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="ed1d2-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="ed1d2-119">OPM non riuscito per altri motivi.</span><span class="sxs-lookup"><span data-stu-id="ed1d2-119">OPM failed for other reasons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed1d2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed1d2-120">Requirements</span></span>



| <span data-ttu-id="ed1d2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed1d2-121">Requirement</span></span> | <span data-ttu-id="ed1d2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ed1d2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1d2-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed1d2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ed1d2-124">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed1d2-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ed1d2-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed1d2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ed1d2-126">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed1d2-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ed1d2-127">IDL</span><span class="sxs-lookup"><span data-stu-id="ed1d2-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed1d2-128"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed1d2-128"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed1d2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed1d2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1d2-130">Enumerazioni di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ed1d2-130">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




