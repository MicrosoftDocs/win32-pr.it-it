---
title: Struttura DRM_OUTPUT_PROTECTION_EX (wmdrmsdk. h)
description: La \_ \_ struttura ex protezione dell'output DRM \_ include informazioni su una tecnologia di protezione dell'output. Questa struttura estende \_ \_ la protezione dell'output DRM aggiungendo un numero di versione.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- Formato di Windows Media per la struttura DRM_OUTPUT_PROTECTION_EX
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332661"
---
# <a name="drm_output_protection_ex-structure"></a><span data-ttu-id="67706-106">\_ \_ Struttura ex protezione dell'output DRM \_</span><span class="sxs-lookup"><span data-stu-id="67706-106">DRM\_OUTPUT\_PROTECTION\_EX structure</span></span>

<span data-ttu-id="67706-107">La **struttura \_ \_ \_ ex protezione dell'output DRM** include informazioni su una tecnologia di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="67706-107">The **DRM\_OUTPUT\_PROTECTION\_EX** structure holds information about an output protection technology.</span></span> <span data-ttu-id="67706-108">Questa struttura estende **la \_ \_ protezione dell'output DRM** aggiungendo un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="67706-108">This structure extends **DRM\_OUTPUT\_PROTECTION** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="67706-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67706-109">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="67706-110">Members</span><span class="sxs-lookup"><span data-stu-id="67706-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="67706-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="67706-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="67706-112">Numero di versione.</span><span class="sxs-lookup"><span data-stu-id="67706-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="67706-113">**guidId**</span><span class="sxs-lookup"><span data-stu-id="67706-113">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="67706-114">GUID che identifica la tecnologia di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="67706-114">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="67706-115">**dwConfigData**</span><span class="sxs-lookup"><span data-stu-id="67706-115">**dwConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="67706-116">Dati di configurazione per la tecnologia.</span><span class="sxs-lookup"><span data-stu-id="67706-116">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67706-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="67706-117">Remarks</span></span>

<span data-ttu-id="67706-118">**DRM \_ La protezione output AUDIO \_ \_ \_ ex** e **DRM \_ video \_ \_ \_** , ad esempio, sono entrambi definiti come **\_ \_ protezione dell'output DRM** nelle istruzioni **typedef** .</span><span class="sxs-lookup"><span data-stu-id="67706-118">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** and **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="67706-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67706-119">Requirements</span></span>



| <span data-ttu-id="67706-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="67706-120">Requirement</span></span> | <span data-ttu-id="67706-121">Valore</span><span class="sxs-lookup"><span data-stu-id="67706-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67706-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67706-122">Header</span></span><br/> | <dl> <span data-ttu-id="67706-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="67706-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67706-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67706-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67706-125">**\_protezione dell'output DRM \_**</span><span class="sxs-lookup"><span data-stu-id="67706-125">**DRM\_OUTPUT\_PROTECTION**</span></span>](drm-output-protection.md)
</dt> <dt>

[<span data-ttu-id="67706-126">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="67706-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





