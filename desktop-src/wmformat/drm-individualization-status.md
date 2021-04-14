---
title: Enumerazione DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
description: Il \_ \_ tipo di enumerazione dello stato di individualizzazione DRM definisce gli stati validi per l'individualizzazione DRM. | Enumerazione DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- Formato Windows Media enumerazione DRM_INDIVIDUALIZATION_STATUS
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401911"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a><span data-ttu-id="74e3f-106">Enumerazione DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="74e3f-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="74e3f-107">Il tipo di enumerazione **\_ \_ dello stato di individualizzazione DRM** definisce gli stati validi per l' [*individualizzazione*](wmformat-glossary.md)DRM.</span><span class="sxs-lookup"><span data-stu-id="74e3f-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM [*individualization*](wmformat-glossary.md).</span></span> <span data-ttu-id="74e3f-108">Quando un'applicazione avvia l'individualizzazione con una chiamata a [**IWMDRMReader:: individualizzato**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), lo stato di avanzamento della richiesta di individualizzazione viene trasmesso all'applicazione tramite chiamate al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="74e3f-108">When an application initiates individualization with a call to [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), the progress of the individualization request is conveyed to the application through calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="74e3f-109">I messaggi di stato di individualizzazione utilizzeranno tutti il \_ membro WMT di individuazione del tipo di enumerazione [**\_ stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) come parametro *status* .</span><span class="sxs-lookup"><span data-stu-id="74e3f-109">Individualization status messages will all use the WMT\_INDIVIDUALIZE member of the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type as the *Status* parameter.</span></span> <span data-ttu-id="74e3f-110">Lo stato della individualizzazione viene passato a **OnStatus** nel parametro *pValue* .</span><span class="sxs-lookup"><span data-stu-id="74e3f-110">The status of the individualization is passed to **OnStatus** in the *pValue* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="74e3f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74e3f-111">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="74e3f-112">Costanti</span><span class="sxs-lookup"><span data-stu-id="74e3f-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="74e3f-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI non \_ definito**</span><span class="sxs-lookup"><span data-stu-id="74e3f-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="74e3f-114">Questo valore è riservato per l'uso futuro.</span><span class="sxs-lookup"><span data-stu-id="74e3f-114">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="74e3f-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**\_inizio indi**</span><span class="sxs-lookup"><span data-stu-id="74e3f-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="74e3f-116">Indica l'inizio del processo di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="74e3f-116">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="74e3f-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**operazione INDI \_ riuscita**</span><span class="sxs-lookup"><span data-stu-id="74e3f-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="74e3f-118">Indica che il processo di individualizzazione è stato completato.</span><span class="sxs-lookup"><span data-stu-id="74e3f-118">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="74e3f-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**\_errore indi**</span><span class="sxs-lookup"><span data-stu-id="74e3f-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="74e3f-120">Indica che il processo di individualizzazione non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="74e3f-120">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="74e3f-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**\_Annulla indi**</span><span class="sxs-lookup"><span data-stu-id="74e3f-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="74e3f-122">Indica che il processo di individualizzazione è stato annullato in seguito a una chiamata a [**IWMDRMReader:: CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span><span class="sxs-lookup"><span data-stu-id="74e3f-122">Indicates that the individualization process was canceled as the result of a call to [**IWMDRMReader::CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span></span>

</dd> <dt>

<span data-ttu-id="74e3f-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**\_download indi**</span><span class="sxs-lookup"><span data-stu-id="74e3f-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="74e3f-124">Indica che è in corso il download dell'aggiornamento della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="74e3f-124">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="74e3f-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**\_installazione indi**</span><span class="sxs-lookup"><span data-stu-id="74e3f-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="74e3f-126">Indica che è in corso l'installazione dell'aggiornamento della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="74e3f-126">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74e3f-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="74e3f-127">Remarks</span></span>

<span data-ttu-id="74e3f-128">Questa enumerazione viene utilizzata dalla struttura [**di \_ \_ stato di personalizzazione WM**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="74e3f-128">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="74e3f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74e3f-129">Requirements</span></span>



| <span data-ttu-id="74e3f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="74e3f-130">Requirement</span></span> | <span data-ttu-id="74e3f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="74e3f-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="74e3f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74e3f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="74e3f-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74e3f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74e3f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74e3f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="74e3f-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74e3f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="74e3f-136">Versione</span><span class="sxs-lookup"><span data-stu-id="74e3f-136">Version</span></span><br/>                  | <span data-ttu-id="74e3f-137">Windows Media Format 7 SDK o versioni successive dell'SDK</span><span class="sxs-lookup"><span data-stu-id="74e3f-137">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="74e3f-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74e3f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="74e3f-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="74e3f-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74e3f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74e3f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e3f-141">**\_stato http \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="74e3f-141">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="74e3f-142">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="74e3f-142">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





