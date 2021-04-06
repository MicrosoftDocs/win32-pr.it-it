---
title: Enumerazione MP_REMOVAL_REASON (MpClient. h)
description: Motivo della rimozione della firma FastPath.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MP_REMOVAL_REASON
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMP_REMOVAL_REASON
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ce70f46bd95d4183343990b40594326ed5d3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743186"
---
# <a name="mp_removal_reason-enumeration"></a><span data-ttu-id="7074c-105">Enumerazione del motivo della \_ rimozione MP \_</span><span class="sxs-lookup"><span data-stu-id="7074c-105">MP\_REMOVAL\_REASON enumeration</span></span>

<span data-ttu-id="7074c-106">Motivo della rimozione della firma FastPath.</span><span class="sxs-lookup"><span data-stu-id="7074c-106">FastPath signature removal reason.</span></span>

## <a name="syntax"></a><span data-ttu-id="7074c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7074c-107">Syntax</span></span>


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a><span data-ttu-id="7074c-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="7074c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7074c-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**\_rimozione MP \_ sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="7074c-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**MP\_REMOVAL\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="7074c-110">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="7074c-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="7074c-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**\_Manuale di rimozione MP \_**</span><span class="sxs-lookup"><span data-stu-id="7074c-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**MP\_REMOVAL\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="7074c-112">manuale.</span><span class="sxs-lookup"><span data-stu-id="7074c-112">Manual.</span></span>

</dd> <dt>

<span data-ttu-id="7074c-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**\_rimozione MP \_ automatica**</span><span class="sxs-lookup"><span data-stu-id="7074c-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**MP\_REMOVAL\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="7074c-114">Automatico.</span><span class="sxs-lookup"><span data-stu-id="7074c-114">Automatic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7074c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7074c-115">Requirements</span></span>



| <span data-ttu-id="7074c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7074c-116">Requirement</span></span> | <span data-ttu-id="7074c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7074c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7074c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7074c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7074c-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7074c-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7074c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7074c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7074c-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7074c-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7074c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7074c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7074c-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7074c-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





