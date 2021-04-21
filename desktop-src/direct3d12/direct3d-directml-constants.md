---
title: Costanti DirectML
description: Le costanti seguenti vengono dichiarate in `DirectML.h` .
keywords:
- Costanti
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803404"
---
# <a name="directml-constants"></a><span data-ttu-id="defba-104">Costanti DirectML</span><span class="sxs-lookup"><span data-stu-id="defba-104">DirectML constants</span></span>

<span data-ttu-id="defba-105">Le costanti seguenti vengono dichiarate in `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="defba-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="defba-106">Costante</span><span class="sxs-lookup"><span data-stu-id="defba-106">Constant</span></span> | <span data-ttu-id="defba-107">Valore</span><span class="sxs-lookup"><span data-stu-id="defba-107">Value</span></span> | <span data-ttu-id="defba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="defba-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="defba-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="defba-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="defba-110">5</span><span class="sxs-lookup"><span data-stu-id="defba-110">5</span></span> | <span data-ttu-id="defba-111">I tensori DirectML supportano un massimo di 5 dimensioni per DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="defba-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="defba-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="defba-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="defba-113">8</span><span class="sxs-lookup"><span data-stu-id="defba-113">8</span></span> | <span data-ttu-id="defba-114">I tensori DirectML supportano un massimo di 8 dimensioni per DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="defba-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="defba-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="defba-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="defba-116">256</span><span class="sxs-lookup"><span data-stu-id="defba-116">256</span></span> | <span data-ttu-id="defba-117">I buffer temporanei e persistenti devono avere un indirizzo di base allineato a 256 byte.</span><span class="sxs-lookup"><span data-stu-id="defba-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="defba-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="defba-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="defba-119">256</span><span class="sxs-lookup"><span data-stu-id="defba-119">256</span></span> | <span data-ttu-id="defba-120">I buffer temporanei e persistenti devono avere un indirizzo di base allineato a 256 byte.</span><span class="sxs-lookup"><span data-stu-id="defba-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="defba-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="defba-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="defba-122">16</span><span class="sxs-lookup"><span data-stu-id="defba-122">16</span></span> | <span data-ttu-id="defba-123">I tensori del buffer hanno un requisito minimo di allineamento degli indirizzi di base di 16 byte.</span><span class="sxs-lookup"><span data-stu-id="defba-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="defba-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="defba-124">Requirements</span></span>

| <span data-ttu-id="defba-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="defba-125">Requirement</span></span> | <span data-ttu-id="defba-126">Valore</span><span class="sxs-lookup"><span data-stu-id="defba-126">Value</span></span> |
|-|-|
| <span data-ttu-id="defba-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="defba-127">Header</span></span> | <span data-ttu-id="defba-128">DirectML.h</span><span class="sxs-lookup"><span data-stu-id="defba-128">DirectML.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="defba-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="defba-129">See also</span></span>

* [<span data-ttu-id="defba-130">Informazioni di riferimento su DirectML</span><span class="sxs-lookup"><span data-stu-id="defba-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="defba-131">Informazioni di riferimento di base</span><span class="sxs-lookup"><span data-stu-id="defba-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="defba-132">Informazioni di riferimento su Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="defba-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
