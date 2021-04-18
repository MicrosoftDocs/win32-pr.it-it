---
title: Enumerazione DRM_HTTP_STATUS (wmdrmsdk. h)
description: Il \_ \_ tipo di enumerazione stato http DRM definisce un intervallo di stati http per una richiesta DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- Formato Windows Media enumerazione DRM_HTTP_STATUS
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331990"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="892ff-105">Enumerazione DRM_HTTP_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="892ff-105">DRM_HTTP_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="892ff-106">Il tipo di enumerazione **\_ \_ stato http DRM** definisce un intervallo di stati http per una richiesta DRM.</span><span class="sxs-lookup"><span data-stu-id="892ff-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of HTTP states for a DRM request.</span></span>

## <a name="syntax"></a><span data-ttu-id="892ff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="892ff-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="892ff-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="892ff-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="892ff-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_NOTINITIATED http**</span><span class="sxs-lookup"><span data-stu-id="892ff-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="892ff-110">Le operazioni HTTP non sono state avviate.</span><span class="sxs-lookup"><span data-stu-id="892ff-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="892ff-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_connessione http**</span><span class="sxs-lookup"><span data-stu-id="892ff-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="892ff-112">Viene stabilita la connessione.</span><span class="sxs-lookup"><span data-stu-id="892ff-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="892ff-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_richiesta http**</span><span class="sxs-lookup"><span data-stu-id="892ff-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="892ff-114">I dati sono richiesti.</span><span class="sxs-lookup"><span data-stu-id="892ff-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="892ff-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_ricezione http**</span><span class="sxs-lookup"><span data-stu-id="892ff-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="892ff-116">Sono in corso la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="892ff-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="892ff-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ completato**</span><span class="sxs-lookup"><span data-stu-id="892ff-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="892ff-118">Le operazioni HTTP sono state completate.</span><span class="sxs-lookup"><span data-stu-id="892ff-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="892ff-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="892ff-119">Remarks</span></span>

<span data-ttu-id="892ff-120">Questa enumerazione viene utilizzata dalla struttura [**di \_ \_ stato di personalizzazione WM**](drmwm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="892ff-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="892ff-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="892ff-121">Requirements</span></span>



| <span data-ttu-id="892ff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="892ff-122">Requirement</span></span> | <span data-ttu-id="892ff-123">Valore</span><span class="sxs-lookup"><span data-stu-id="892ff-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="892ff-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="892ff-124">Header</span></span><br/> | <dl> <span data-ttu-id="892ff-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="892ff-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="892ff-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="892ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="892ff-127">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="892ff-127">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





