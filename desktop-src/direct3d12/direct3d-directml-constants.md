---
title: Costanti DirectML
description: Le costanti seguenti sono dichiarate in `DirectML.h` .
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
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322164"
---
# <a name="directml-constants"></a><span data-ttu-id="3c411-104">Costanti DirectML</span><span class="sxs-lookup"><span data-stu-id="3c411-104">DirectML constants</span></span>

<span data-ttu-id="3c411-105">Le costanti seguenti sono dichiarate in `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="3c411-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="3c411-106">Costante</span><span class="sxs-lookup"><span data-stu-id="3c411-106">Constant</span></span> | <span data-ttu-id="3c411-107">Valore</span><span class="sxs-lookup"><span data-stu-id="3c411-107">Value</span></span> | <span data-ttu-id="3c411-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c411-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="3c411-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="3c411-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="3c411-110">5</span><span class="sxs-lookup"><span data-stu-id="3c411-110">5</span></span> | <span data-ttu-id="3c411-111">I tensori DirectML supportano un massimo di 5 dimensioni per DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="3c411-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="3c411-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="3c411-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="3c411-113">8</span><span class="sxs-lookup"><span data-stu-id="3c411-113">8</span></span> | <span data-ttu-id="3c411-114">I tensori DirectML supportano un massimo di 8 dimensioni per DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="3c411-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="3c411-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="3c411-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="3c411-116">256</span><span class="sxs-lookup"><span data-stu-id="3c411-116">256</span></span> | <span data-ttu-id="3c411-117">I buffer temporanei e permanenti devono avere un indirizzo di base allineato a 256 byte.</span><span class="sxs-lookup"><span data-stu-id="3c411-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="3c411-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="3c411-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="3c411-119">256</span><span class="sxs-lookup"><span data-stu-id="3c411-119">256</span></span> | <span data-ttu-id="3c411-120">I buffer temporanei e permanenti devono avere un indirizzo di base allineato a 256 byte.</span><span class="sxs-lookup"><span data-stu-id="3c411-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="3c411-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="3c411-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="3c411-122">16</span><span class="sxs-lookup"><span data-stu-id="3c411-122">16</span></span> | <span data-ttu-id="3c411-123">I tempi di risoluzione del buffer hanno un requisito minimo di allineamento degli indirizzi di base di 16 byte.</span><span class="sxs-lookup"><span data-stu-id="3c411-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="3c411-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c411-124">Requirements</span></span>

| <span data-ttu-id="3c411-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c411-125">Requirement</span></span> | <span data-ttu-id="3c411-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3c411-126">Value</span></span> |
|-|-|
| <span data-ttu-id="3c411-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c411-127">Header</span></span> | <span data-ttu-id="3c411-128">D3D12. h</span><span class="sxs-lookup"><span data-stu-id="3c411-128">D3D12.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="3c411-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c411-129">See also</span></span>

* [<span data-ttu-id="3c411-130">Riferimento a DirectML</span><span class="sxs-lookup"><span data-stu-id="3c411-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="3c411-131">Riferimento principale</span><span class="sxs-lookup"><span data-stu-id="3c411-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="3c411-132">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3c411-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
