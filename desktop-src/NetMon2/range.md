---
description: La struttura di intervallo definisce un intervallo di valori di proprietà validi.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Struttura RANGE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310959"
---
# <a name="range-structure"></a><span data-ttu-id="a0cf9-103">Struttura di intervallo</span><span class="sxs-lookup"><span data-stu-id="a0cf9-103">RANGE structure</span></span>

<span data-ttu-id="a0cf9-104">La struttura di **intervallo** definisce un intervallo di valori di proprietà validi.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-104">The **RANGE** structure defines a range of valid property values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0cf9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0cf9-105">Syntax</span></span>


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a><span data-ttu-id="a0cf9-106">Members</span><span class="sxs-lookup"><span data-stu-id="a0cf9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0cf9-107">**MinValue**</span><span class="sxs-lookup"><span data-stu-id="a0cf9-107">**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="a0cf9-108">Valore minimo possibile in un intervallo.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-108">Lowest possible value in a range.</span></span>

</dd> <dt>

<span data-ttu-id="a0cf9-109">**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="a0cf9-109">**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="a0cf9-110">Valore massimo possibile in un intervallo.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-110">Highest possible value in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0cf9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0cf9-111">Remarks</span></span>

<span data-ttu-id="a0cf9-112">La struttura di **intervallo** viene utilizzata per specificare un intervallo di numeri validi per una proprietà del protocollo.</span><span class="sxs-lookup"><span data-stu-id="a0cf9-112">The **RANGE** structure is used to specify a valid range of numbers for a protocol property.</span></span> <span data-ttu-id="a0cf9-113">Se il membro **dataqualifier** della struttura **PropertyInfo** è impostato su **prop \_ qual \_ Range**, il membro **lpRange** della struttura [PropertyInfo](propertyinfo.md) deve fornire un puntatore a una struttura di **intervallo** .</span><span class="sxs-lookup"><span data-stu-id="a0cf9-113">If the **DataQualifier** member of the **PROPERTYINFO** structure is set to **PROP\_QUAL\_RANGE**, the **lpRange** member of the [PROPERTYINFO](propertyinfo.md) structure must provide a pointer to a **RANGE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0cf9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0cf9-114">Requirements</span></span>



| <span data-ttu-id="a0cf9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0cf9-115">Requirement</span></span> | <span data-ttu-id="a0cf9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a0cf9-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cf9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0cf9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a0cf9-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0cf9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a0cf9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0cf9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a0cf9-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0cf9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a0cf9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0cf9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0cf9-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0cf9-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0cf9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0cf9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0cf9-124">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="a0cf9-124">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




