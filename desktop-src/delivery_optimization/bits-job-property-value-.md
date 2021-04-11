---
title: Struttura BITS_JOB_PROPERTY_VALUE (Deliveryoptimization. h)
description: Il BITS_JOB_PROPERTY_VALUE Unione fornisce il valore della proprietà del processo DO in base al valore dell'enumerazione BITS_JOB_PROPERTY_ID.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- Struttura BITS_JOB_PROPERTY_VALUE
- Struttura BITS_JOB_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119759"
---
# <a name="bits_job_property_value-structure"></a><span data-ttu-id="47482-105">Struttura BITS_JOB_PROPERTY_VALUE</span><span class="sxs-lookup"><span data-stu-id="47482-105">BITS_JOB_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="47482-106">Il **BITS_JOB_PROPERTY_VALUE** Unione fornisce il valore della proprietà del processo do in base al valore dell'enumerazione [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="47482-106">The **BITS_JOB_PROPERTY_VALUE** union provides the property value of the DO job based on the value of the [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="47482-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47482-107">Syntax</span></span>


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="47482-108">Members</span><span class="sxs-lookup"><span data-stu-id="47482-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="47482-109">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="47482-109">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="47482-110">Questo valore viene restituito quando si usa l'ID della proprietà enum **BITS_JOB_PROPERTY_ID_COST_FLAGS** e viene applicato come [criterio di trasferimento](https://www.bing.com/search?q=transfer+policy) nel processo do.</span><span class="sxs-lookup"><span data-stu-id="47482-110">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_ID_COST_FLAGS** and is applied as the [transfer policy](https://www.bing.com/search?q=transfer+policy) on the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="47482-111">**ClsID**</span><span class="sxs-lookup"><span data-stu-id="47482-111">**ClsID**</span></span>
</dt> <dd>

<span data-ttu-id="47482-112">Questo valore viene restituito quando si usa l'ID della proprietà enum **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** e rappresenta il CLSID dell'oggetto callback da registrare con il processo do.</span><span class="sxs-lookup"><span data-stu-id="47482-112">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** and represents the CLSID of the callback object to register with the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="47482-113">**Attiva**</span><span class="sxs-lookup"><span data-stu-id="47482-113">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="47482-114">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="47482-114">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="47482-115">**UInt64**</span><span class="sxs-lookup"><span data-stu-id="47482-115">**Uint64**</span></span>
</dt> <dd>

<span data-ttu-id="47482-116">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="47482-116">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="47482-117">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="47482-117">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="47482-118">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="47482-118">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47482-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47482-119">Requirements</span></span>



| <span data-ttu-id="47482-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="47482-120">Requirement</span></span> | <span data-ttu-id="47482-121">Valore</span><span class="sxs-lookup"><span data-stu-id="47482-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47482-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47482-122">Minimum supported client</span></span><br/> | <span data-ttu-id="47482-123">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="47482-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="47482-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47482-124">Minimum supported server</span></span><br/> | <span data-ttu-id="47482-125">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="47482-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="47482-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47482-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="47482-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="47482-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47482-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47482-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47482-129">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="47482-129">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="47482-130">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="47482-130">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





