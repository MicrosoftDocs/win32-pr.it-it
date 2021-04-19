---
title: Struttura DRM_OUTPUT_PROTECTION (wmdrmsdk. h)
description: La \_ \_ struttura di protezione dell'output DRM include informazioni su una tecnologia di protezione dell'output.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- Formato di Windows Media per la struttura DRM_OUTPUT_PROTECTION
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329055"
---
# <a name="drm_output_protection-structure"></a><span data-ttu-id="74bff-105">Struttura di protezione dell' \_ output DRM \_</span><span class="sxs-lookup"><span data-stu-id="74bff-105">DRM\_OUTPUT\_PROTECTION structure</span></span>

<span data-ttu-id="74bff-106">La struttura di **\_ \_ protezione dell'output DRM** include informazioni su una tecnologia di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="74bff-106">The **DRM\_OUTPUT\_PROTECTION** structure holds information about an output protection technology.</span></span>

## <a name="syntax"></a><span data-ttu-id="74bff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74bff-107">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="74bff-108">Members</span><span class="sxs-lookup"><span data-stu-id="74bff-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="74bff-109">**guidId**</span><span class="sxs-lookup"><span data-stu-id="74bff-109">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="74bff-110">GUID che identifica la tecnologia di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="74bff-110">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="74bff-111">**bConfigData**</span><span class="sxs-lookup"><span data-stu-id="74bff-111">**bConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="74bff-112">Dati di configurazione per la tecnologia.</span><span class="sxs-lookup"><span data-stu-id="74bff-112">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74bff-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="74bff-113">Remarks</span></span>

<span data-ttu-id="74bff-114">**DRM \_ La \_ \_** protezione dell'output audio e la **\_ \_ \_ protezione dell'output video DRM** sono entrambe definite come **\_ \_ protezione dell'output DRM** nelle istruzioni **typedef** .</span><span class="sxs-lookup"><span data-stu-id="74bff-114">**DRM\_AUDIO\_OUTPUT\_PROTECTION** and **DRM\_VIDEO\_OUTPUT\_PROTECTION** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="74bff-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74bff-115">Requirements</span></span>



| <span data-ttu-id="74bff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="74bff-116">Requirement</span></span> | <span data-ttu-id="74bff-117">Valore</span><span class="sxs-lookup"><span data-stu-id="74bff-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74bff-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74bff-118">Header</span></span><br/> | <dl> <span data-ttu-id="74bff-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="74bff-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74bff-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74bff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bff-121">**protezione dell'output DRM, ad \_ \_ \_ esempio**</span><span class="sxs-lookup"><span data-stu-id="74bff-121">**DRM\_OUTPUT\_PROTECTION\_EX**</span></span>](drm-output-protection-ex.md)
</dt> <dt>

[<span data-ttu-id="74bff-122">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="74bff-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





