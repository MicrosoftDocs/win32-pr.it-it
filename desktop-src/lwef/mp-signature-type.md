---
title: Enumerazione MP_SIGNATURE_TYPE (MpClient. h)
description: Tipi di firma possibili.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MP_SIGNATURE_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMP_SIGNATURE_TYPE
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476504"
---
# <a name="mp_signature_type-enumeration"></a><span data-ttu-id="274f1-105">Enumerazione del tipo di \_ firma MP \_</span><span class="sxs-lookup"><span data-stu-id="274f1-105">MP\_SIGNATURE\_TYPE enumeration</span></span>

<span data-ttu-id="274f1-106">Tipi di firma possibili.</span><span class="sxs-lookup"><span data-stu-id="274f1-106">Possible signature types.</span></span>

## <a name="syntax"></a><span data-ttu-id="274f1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="274f1-107">Syntax</span></span>


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="274f1-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="274f1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="274f1-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**\_antimalware firma MP \_**</span><span class="sxs-lookup"><span data-stu-id="274f1-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP\_SIGNATURE\_ANTIMALWARE**</span></span>
</dt> <dd>

<span data-ttu-id="274f1-110">Firme antivirus e antispyware.</span><span class="sxs-lookup"><span data-stu-id="274f1-110">Both antivirus and antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="274f1-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**ANTIVIRUS per la \_ firma MP \_**</span><span class="sxs-lookup"><span data-stu-id="274f1-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP\_SIGNATURE\_ANTIVIRUS**</span></span>
</dt> <dd>

<span data-ttu-id="274f1-112">Solo le firme antivirus.</span><span class="sxs-lookup"><span data-stu-id="274f1-112">Only antivirus signatures.</span></span>

</dd> <dt>

<span data-ttu-id="274f1-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**\_antispyware firma MP \_**</span><span class="sxs-lookup"><span data-stu-id="274f1-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP\_SIGNATURE\_ANTISPYWARE**</span></span>
</dt> <dd>

<span data-ttu-id="274f1-114">Solo le firme antispyware.</span><span class="sxs-lookup"><span data-stu-id="274f1-114">Only antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="274f1-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**\_NIS firma \_ MP**</span><span class="sxs-lookup"><span data-stu-id="274f1-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP\_SIGNATURE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="274f1-116">Firme NIS.</span><span class="sxs-lookup"><span data-stu-id="274f1-116">NIS signatures.</span></span>

</dd> <dt>

<span data-ttu-id="274f1-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**\_tipi di firma MP \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="274f1-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MP\_SIGNATURE\_TYPES\_MAXVALUE**</span></span>
<span data-ttu-id="274f1-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="274f1-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="274f1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="274f1-119">Requirements</span></span>



| <span data-ttu-id="274f1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="274f1-120">Requirement</span></span> | <span data-ttu-id="274f1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="274f1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="274f1-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="274f1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="274f1-123">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="274f1-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="274f1-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="274f1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="274f1-125">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="274f1-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="274f1-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="274f1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="274f1-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="274f1-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





