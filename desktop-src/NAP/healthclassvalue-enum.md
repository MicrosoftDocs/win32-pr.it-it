---
title: Enumerazione HealthClassValue (NapProtocol. h)
description: Indica il valore della classe di integrità TLV.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- HealthClassValue enumerazione NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ade44b74d03a69d6ccf410a042adf3819b8cc782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475070"
---
# <a name="healthclassvalue-enumeration"></a><span data-ttu-id="9ddcc-104">Enumerazione HealthClassValue</span><span class="sxs-lookup"><span data-stu-id="9ddcc-104">HealthClassValue enumeration</span></span>

> [!Note]  
> <span data-ttu-id="9ddcc-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="9ddcc-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9ddcc-106">Il tipo di enumerazione **HealthClassValue** indica il valore della classe di integrità TLV.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-106">The **HealthClassValue** enumeration type indicates the value of the health class TLV.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ddcc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ddcc-107">Syntax</span></span>


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a><span data-ttu-id="9ddcc-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="9ddcc-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9ddcc-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span><span class="sxs-lookup"><span data-stu-id="9ddcc-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span></span>
</dt> <dd>

<span data-ttu-id="9ddcc-110">La classe di integrità TLV è il firewall.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-110">The health class TLV is firewall.</span></span>

</dd> <dt>

<span data-ttu-id="9ddcc-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span><span class="sxs-lookup"><span data-stu-id="9ddcc-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span></span>
</dt> <dd>

<span data-ttu-id="9ddcc-112">La classe di integrità TLV è a livello di patch.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-112">The health class TLV is patch level.</span></span>

</dd> <dt>

<span data-ttu-id="9ddcc-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span><span class="sxs-lookup"><span data-stu-id="9ddcc-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span></span>
</dt> <dd>

<span data-ttu-id="9ddcc-114">La classe di integrità TLV è un antivirus.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-114">The health class TLV is antivirus.</span></span>

</dd> <dt>

<span data-ttu-id="9ddcc-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span><span class="sxs-lookup"><span data-stu-id="9ddcc-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="9ddcc-116">La classe di integrità TLV è un aggiornamento critico.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-116">The health class TLV is critical update.</span></span>

</dd> <dt>

<span data-ttu-id="9ddcc-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span><span class="sxs-lookup"><span data-stu-id="9ddcc-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span></span>
</dt> <dd>

<span data-ttu-id="9ddcc-118">Riservato solo per uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-118">Reserved for system use only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ddcc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ddcc-119">Requirements</span></span>



| <span data-ttu-id="9ddcc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ddcc-120">Requirement</span></span> | <span data-ttu-id="9ddcc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9ddcc-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ddcc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ddcc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9ddcc-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ddcc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ddcc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ddcc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9ddcc-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ddcc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9ddcc-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ddcc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ddcc-127"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ddcc-127"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ddcc-128">IDL</span><span class="sxs-lookup"><span data-stu-id="9ddcc-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ddcc-129"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ddcc-129"><dt>NapProtocol.idl</dt></span></span> </dl> |



 

 





