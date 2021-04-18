---
description: Specifica il valore che una proprietà presuppone in un determinato momento.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: Struttura DEXTER_PARAM (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329147"
---
# <a name="dexter_param-structure"></a><span data-ttu-id="8be09-103">\_Struttura param di Dexter</span><span class="sxs-lookup"><span data-stu-id="8be09-103">DEXTER\_PARAM structure</span></span>

> [!Note]  
> <span data-ttu-id="8be09-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8be09-104">\[Deprecated.</span></span> <span data-ttu-id="8be09-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8be09-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8be09-106">Specifica il valore che una proprietà presuppone in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="8be09-106">Specifies the value that a property assumes at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be09-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8be09-107">Syntax</span></span>


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a><span data-ttu-id="8be09-108">Members</span><span class="sxs-lookup"><span data-stu-id="8be09-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8be09-109">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8be09-109">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="8be09-110">Nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8be09-110">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="8be09-111">**dispID**</span><span class="sxs-lookup"><span data-stu-id="8be09-111">**dispID**</span></span>
</dt> <dd>

<span data-ttu-id="8be09-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="8be09-112">Reserved.</span></span> <span data-ttu-id="8be09-113">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="8be09-113">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8be09-114">**nValori**</span><span class="sxs-lookup"><span data-stu-id="8be09-114">**nValues**</span></span>
</dt> <dd>

<span data-ttu-id="8be09-115">Numero di valori assunti dalla proprietà.</span><span class="sxs-lookup"><span data-stu-id="8be09-115">Number of values that the property assumes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8be09-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8be09-116">Remarks</span></span>

<span data-ttu-id="8be09-117">L'oggetto deve supportare l'interfaccia **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="8be09-117">The object must support the **IDispatch** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be09-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8be09-118">Requirements</span></span>



| <span data-ttu-id="8be09-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be09-119">Requirement</span></span> | <span data-ttu-id="8be09-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8be09-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8be09-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8be09-121">Header</span></span><br/> | <dl> <span data-ttu-id="8be09-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8be09-122"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be09-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8be09-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be09-124">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="8be09-124">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="8be09-125">**\_valore Dexter**</span><span class="sxs-lookup"><span data-stu-id="8be09-125">**DEXTER\_VALUE**</span></span>](dexter-value.md)
</dt> </dl>

 

 




