---
title: Enumerazione MPDETECTION_ORIGIN (MpClient. h)
description: Origine del rilevamento.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPDETECTION_ORIGIN
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPDETECTION_ORIGIN
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301410"
---
# <a name="mpdetection_origin-enumeration"></a><span data-ttu-id="ca5df-105">\_Enumerazione MPDETECTION Origin</span><span class="sxs-lookup"><span data-stu-id="ca5df-105">MPDETECTION\_ORIGIN enumeration</span></span>

<span data-ttu-id="ca5df-106">Origine del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="ca5df-106">Detection origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca5df-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca5df-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a><span data-ttu-id="ca5df-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="ca5df-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ca5df-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**\_origine MPDETECTION \_ sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="ca5df-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION\_ORIGIN\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ca5df-110">Origine rilevata minaccia sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="ca5df-110">Threat detected origin unknown.</span></span>

</dd> <dt>

<span data-ttu-id="ca5df-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**\_ \_ computer locale di origine MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="ca5df-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MPDETECTION\_ORIGIN\_LOCAL\_MACHINE**</span></span>
</dt> <dd>

<span data-ttu-id="ca5df-112">Minaccia rilevata nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="ca5df-112">Threat detected on local machine.</span></span>

</dd> <dt>

<span data-ttu-id="ca5df-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ Origin \_ NETWORKSHARE**</span><span class="sxs-lookup"><span data-stu-id="ca5df-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION\_ORIGIN\_NETWORKSHARE**</span></span>
</dt> <dd>

<span data-ttu-id="ca5df-114">Minaccia rilevata nella condivisione di rete.</span><span class="sxs-lookup"><span data-stu-id="ca5df-114">Threat detected on network share.</span></span>

</dd> <dt>

<span data-ttu-id="ca5df-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**\_Internet di origine MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="ca5df-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION\_ORIGIN\_INTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="ca5df-116">Minaccia rilevata in Internet.</span><span class="sxs-lookup"><span data-stu-id="ca5df-116">Threat detected on internet.</span></span>

</dd> <dt>

<span data-ttu-id="ca5df-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**origine MPDETECTION in \_ \_ uscita**</span><span class="sxs-lookup"><span data-stu-id="ca5df-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION\_ORIGIN\_OUTBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="ca5df-118">Minaccia rilevata in una connessione in uscita.</span><span class="sxs-lookup"><span data-stu-id="ca5df-118">Threat detected on an outbound connection.</span></span>

</dd> <dt>

<span data-ttu-id="ca5df-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**origine MPDETECTION in \_ \_ ingresso**</span><span class="sxs-lookup"><span data-stu-id="ca5df-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION\_ORIGIN\_INBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="ca5df-120">Minaccia rilevata in una connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="ca5df-120">Threat detected on an inbound connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca5df-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca5df-121">Requirements</span></span>



| <span data-ttu-id="ca5df-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca5df-122">Requirement</span></span> | <span data-ttu-id="ca5df-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ca5df-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5df-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca5df-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ca5df-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ca5df-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ca5df-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca5df-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ca5df-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ca5df-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca5df-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca5df-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca5df-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca5df-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





