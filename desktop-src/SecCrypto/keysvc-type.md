---
description: L' \_ enumerazione del tipo KEYSVC definisce se una chiave viene applicata a un computer o a un servizio.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: Enumerazione KEYSVC_TYPE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 71d6724f7bae78a3c1ac4da83289c151b7ec1a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968656"
---
# <a name="keysvc_type-enumeration"></a><span data-ttu-id="8fbf7-103">\_Enumerazione del tipo KEYSVC</span><span class="sxs-lookup"><span data-stu-id="8fbf7-103">KEYSVC\_TYPE enumeration</span></span>

<span data-ttu-id="8fbf7-104">L'enumerazione del **\_ tipo KEYSVC** definisce se una chiave viene applicata a un computer o a un servizio.</span><span class="sxs-lookup"><span data-stu-id="8fbf7-104">The **KEYSVC\_TYPE** enumeration defines whether a key applies to a computer or a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbf7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fbf7-105">Syntax</span></span>


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a><span data-ttu-id="8fbf7-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="8fbf7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8fbf7-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span><span class="sxs-lookup"><span data-stu-id="8fbf7-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span></span>
</dt> <dd>

<span data-ttu-id="8fbf7-108">La chiave è per un computer.</span><span class="sxs-lookup"><span data-stu-id="8fbf7-108">The key is for a computer.</span></span>

</dd> <dt>

<span data-ttu-id="8fbf7-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span><span class="sxs-lookup"><span data-stu-id="8fbf7-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span></span>
</dt> <dd>

<span data-ttu-id="8fbf7-110">La chiave è per un servizio.</span><span class="sxs-lookup"><span data-stu-id="8fbf7-110">The key is for a service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fbf7-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fbf7-111">Requirements</span></span>



| <span data-ttu-id="8fbf7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fbf7-112">Requirement</span></span> | <span data-ttu-id="8fbf7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="8fbf7-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbf7-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fbf7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8fbf7-115">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8fbf7-115">None supported</span></span><br/>                                                             |
| <span data-ttu-id="8fbf7-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fbf7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8fbf7-117">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8fbf7-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8fbf7-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fbf7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fbf7-119"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fbf7-119"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fbf7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fbf7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbf7-121">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="8fbf7-121">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




