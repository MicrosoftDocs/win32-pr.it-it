---
title: Enumerazione DRM_HTTP_STATUS (Drmexternals. h)
description: Il \_ \_ tipo di enumerazione stato http DRM definisce un intervallo di stati per una richiesta DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- Formato Windows Media enumerazione DRM_HTTP_STATUS
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302064"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a><span data-ttu-id="163dd-105">Enumerazione DRM_HTTP_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="163dd-105">DRM_HTTP_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="163dd-106">Il tipo di enumerazione **\_ \_ stato http DRM** definisce un intervallo di stati per una richiesta [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="163dd-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of states for a [*DRM*](wmformat-glossary.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="163dd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="163dd-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="163dd-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="163dd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="163dd-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_NOTINITIATED http**</span><span class="sxs-lookup"><span data-stu-id="163dd-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="163dd-110">Le operazioni HTTP non sono state avviate.</span><span class="sxs-lookup"><span data-stu-id="163dd-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="163dd-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_connessione http**</span><span class="sxs-lookup"><span data-stu-id="163dd-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="163dd-112">Viene stabilita la connessione.</span><span class="sxs-lookup"><span data-stu-id="163dd-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="163dd-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_richiesta http**</span><span class="sxs-lookup"><span data-stu-id="163dd-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="163dd-114">I dati sono richiesti.</span><span class="sxs-lookup"><span data-stu-id="163dd-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="163dd-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_ricezione http**</span><span class="sxs-lookup"><span data-stu-id="163dd-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="163dd-116">Sono in corso la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="163dd-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="163dd-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ completato**</span><span class="sxs-lookup"><span data-stu-id="163dd-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="163dd-118">Le operazioni HTTP sono state completate.</span><span class="sxs-lookup"><span data-stu-id="163dd-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="163dd-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="163dd-119">Remarks</span></span>

<span data-ttu-id="163dd-120">Questa enumerazione viene utilizzata dalla struttura [**di \_ \_ stato di personalizzazione WM**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="163dd-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="163dd-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="163dd-121">Requirements</span></span>



| <span data-ttu-id="163dd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="163dd-122">Requirement</span></span> | <span data-ttu-id="163dd-123">Valore</span><span class="sxs-lookup"><span data-stu-id="163dd-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="163dd-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="163dd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="163dd-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="163dd-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="163dd-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="163dd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="163dd-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="163dd-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="163dd-128">Versione</span><span class="sxs-lookup"><span data-stu-id="163dd-128">Version</span></span><br/>                  | <span data-ttu-id="163dd-129">Windows Media Format 7 SDK o versioni successive dell'SDK</span><span class="sxs-lookup"><span data-stu-id="163dd-129">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="163dd-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="163dd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="163dd-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="163dd-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="163dd-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="163dd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="163dd-133">**\_stato di individualizzazione DRM \_**</span><span class="sxs-lookup"><span data-stu-id="163dd-133">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drm-individualization-status.md)
</dt> <dt>

[<span data-ttu-id="163dd-134">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="163dd-134">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





