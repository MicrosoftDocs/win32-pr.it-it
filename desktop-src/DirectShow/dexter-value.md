---
description: Identifica una proprietà che deve essere impostata su una transizione o un effetto, insieme al numero di valori distinct che la proprietà presuppone per la durata della transizione o dell'effetto.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: Struttura DEXTER_VALUE (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329146"
---
# <a name="dexter_value-structure"></a><span data-ttu-id="5b846-103">\_Struttura del valore Dexter</span><span class="sxs-lookup"><span data-stu-id="5b846-103">DEXTER\_VALUE structure</span></span>

> [!Note]  
> <span data-ttu-id="5b846-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5b846-104">\[Deprecated.</span></span> <span data-ttu-id="5b846-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5b846-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5b846-106">Identifica una proprietà che deve essere impostata su una transizione o un effetto, insieme al numero di valori distinct che la proprietà presuppone per la durata della transizione o dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="5b846-106">Identifies a property that is to be set on a transition or effect, along with the number of distinct values that the property assumes over the duration of the transition or effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b846-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b846-107">Syntax</span></span>


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a><span data-ttu-id="5b846-108">Members</span><span class="sxs-lookup"><span data-stu-id="5b846-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b846-109">**v**</span><span class="sxs-lookup"><span data-stu-id="5b846-109">**v**</span></span>
</dt> <dd>

<span data-ttu-id="5b846-110">Valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b846-110">Value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="5b846-111">**RT**</span><span class="sxs-lookup"><span data-stu-id="5b846-111">**rt**</span></span>
</dt> <dd>

<span data-ttu-id="5b846-112">Tempo in cui la proprietà presuppone il valore, relativo all'inizio della transizione o dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="5b846-112">Time at which the property assumes the value, relative to the start of the transition or effect.</span></span>

</dd> <dt>

<span data-ttu-id="5b846-113">**dwInterp**</span><span class="sxs-lookup"><span data-stu-id="5b846-113">**dwInterp**</span></span>
</dt> <dd>

<span data-ttu-id="5b846-114">Flag che indica il modo in cui la proprietà avanza dal valore precedente a questo valore.</span><span class="sxs-lookup"><span data-stu-id="5b846-114">Flag indicating how the property progresses from the previous value to this value.</span></span> <span data-ttu-id="5b846-115">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b846-115">Must be one of the following:</span></span>



| <span data-ttu-id="5b846-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5b846-116">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="5b846-117">Significato</span><span class="sxs-lookup"><span data-stu-id="5b846-117">Meaning</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <span data-ttu-id="5b846-118"><dt>**DEXTERF \_ Jump**</dt></span><span class="sxs-lookup"><span data-stu-id="5b846-118"><dt>**DEXTERF\_JUMP**</dt></span></span> </dl>                      | <span data-ttu-id="5b846-119">La proprietà passa immediatamente al nuovo valore all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="5b846-119">The property jumps instantly to the new value at the specified time.</span></span><br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <span data-ttu-id="5b846-120"><dt>**\_interpolazione DEXTERF**</dt></span><span class="sxs-lookup"><span data-stu-id="5b846-120"><dt>**DEXTERF\_INTERPOLATE**</dt></span></span> </dl> | <span data-ttu-id="5b846-121">La proprietà viene interpolata in modo lineare nel tempo rispetto al valore precedente.</span><span class="sxs-lookup"><span data-stu-id="5b846-121">The property is interpolated linearly over time from the previous value.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b846-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b846-122">Requirements</span></span>



| <span data-ttu-id="5b846-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b846-123">Requirement</span></span> | <span data-ttu-id="5b846-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5b846-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b846-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b846-125">Header</span></span><br/> | <dl> <span data-ttu-id="5b846-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b846-126"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b846-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b846-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b846-128">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="5b846-128">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="5b846-129">**\_param Dexter**</span><span class="sxs-lookup"><span data-stu-id="5b846-129">**DEXTER\_PARAM**</span></span>](dexter-param.md)
</dt> </dl>

 

 




