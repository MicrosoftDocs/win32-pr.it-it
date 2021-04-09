---
title: Enumerazione MP_FASTPATH_TYPE (MpClient. h)
description: Tipo FastPath.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MP_FASTPATH_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMP_FASTPATH_TYPE
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89db79c54b166a833369ff52e47473463e0a2b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121170"
---
# <a name="mp_fastpath_type-enumeration"></a><span data-ttu-id="d3847-105">\_Enumerazione del \_ tipo MP FastPath</span><span class="sxs-lookup"><span data-stu-id="d3847-105">MP\_FASTPATH\_TYPE enumeration</span></span>

<span data-ttu-id="d3847-106">Tipo FastPath.</span><span class="sxs-lookup"><span data-stu-id="d3847-106">FastPath type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3847-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3847-107">Syntax</span></span>


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="d3847-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="d3847-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d3847-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP \_ FastPath \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="d3847-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP\_FASTPATH\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="d3847-110">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d3847-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="d3847-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**\_VDM FastPath \_ MP**</span><span class="sxs-lookup"><span data-stu-id="d3847-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP\_FASTPATH\_VDM**</span></span>
</dt> <dd>

<span data-ttu-id="d3847-112">Aggiornamento di VDM.</span><span class="sxs-lookup"><span data-stu-id="d3847-112">VDM update.</span></span>

</dd> <dt>

<span data-ttu-id="d3847-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**\_FastPath MP \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="d3847-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP\_FASTPATH\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="d3847-114">Notifica di disabilitazione della firma.</span><span class="sxs-lookup"><span data-stu-id="d3847-114">Signature disable notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3847-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3847-115">Requirements</span></span>



| <span data-ttu-id="d3847-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3847-116">Requirement</span></span> | <span data-ttu-id="d3847-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d3847-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3847-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3847-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d3847-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d3847-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d3847-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3847-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d3847-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d3847-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3847-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3847-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3847-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3847-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





