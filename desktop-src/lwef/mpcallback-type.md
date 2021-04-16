---
title: Enumerazione MPCALLBACK_TYPE (MpClient. h)
description: Tipi di callback possibili.
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPCALLBACK_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPCALLBACK_TYPE
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3fd310f3733d36dd92ace1c7a5286bcf73a75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476121"
---
# <a name="mpcallback_type-enumeration"></a><span data-ttu-id="14902-105">\_Enumerazione del tipo MPCALLBACK</span><span class="sxs-lookup"><span data-stu-id="14902-105">MPCALLBACK\_TYPE enumeration</span></span>

<span data-ttu-id="14902-106">Tipi di callback possibili.</span><span class="sxs-lookup"><span data-stu-id="14902-106">Possible callback types.</span></span>

## <a name="syntax"></a><span data-ttu-id="14902-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14902-107">Syntax</span></span>


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="14902-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="14902-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="14902-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="14902-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**\_stato MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**MPCALLBACK\_STATUS**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**\_minaccia MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**MPCALLBACK\_THREAT**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**\_analisi MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**MPCALLBACK\_SCAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**\_Pulisci MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**\_Verifica MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**MPCALLBACK\_PRECHECK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**\_SIGUPDATE MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK\_SIGUPDATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**\_esempio MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**MPCALLBACK\_SAMPLE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK \_ riservato**</span><span class="sxs-lookup"><span data-stu-id="14902-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK\_RESERVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**\_notifica della configurazione di MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="14902-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**MPCALLBACK\_CONFIGURATION\_NOTIFICATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**\_FastPath MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK\_FASTPATH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**\_scadenza del prodotto MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="14902-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**MPCALLBACK\_PRODUCT\_EXPIRATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK \_ NIS \_ privato**</span><span class="sxs-lookup"><span data-stu-id="14902-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK\_NIS\_PRIVATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**\_stato MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**MPCALLBACK\_HEALTH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**\_ENDOFLIFE MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK\_ENDOFLIFE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**\_MALWARETOAST MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="14902-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK\_MALWARETOAST**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="14902-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="14902-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK\_MAXVALUE**</span></span>
<span data-ttu-id="14902-126"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="14902-126"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="14902-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14902-127">Requirements</span></span>



| <span data-ttu-id="14902-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="14902-128">Requirement</span></span> | <span data-ttu-id="14902-129">Valore</span><span class="sxs-lookup"><span data-stu-id="14902-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14902-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14902-130">Minimum supported client</span></span><br/> | <span data-ttu-id="14902-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="14902-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="14902-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14902-132">Minimum supported server</span></span><br/> | <span data-ttu-id="14902-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="14902-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14902-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14902-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="14902-135"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="14902-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





