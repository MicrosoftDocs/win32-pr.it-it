---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Definisce le costanti che controllano la trasformazione applicata negli operatori DirectML DML_OPERATOR_DEPTH_TO_SPACE1 [e](/windows/win32/api/directml/ne-directml-dml_operator_type) **DML_OPERATOR_SPACE_TO_DEPTH1**.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803537"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a><span data-ttu-id="140d7-103">DML_DEPTH_SPACE_ORDER enumerazione (directml.h)</span><span class="sxs-lookup"><span data-stu-id="140d7-103">DML_DEPTH_SPACE_ORDER enumeration (directml.h)</span></span>

<span data-ttu-id="140d7-104">Definisce le costanti che controllano la trasformazione applicata negli operatori DirectML DML_OPERATOR_DEPTH_TO_SPACE1 [e](/windows/win32/api/directml/ne-directml-dml_operator_type) **DML_OPERATOR_SPACE_TO_DEPTH1**.</span><span class="sxs-lookup"><span data-stu-id="140d7-104">Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**.</span></span> <span data-ttu-id="140d7-105">Questi vengono usati all'interno [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) strutture.</span><span class="sxs-lookup"><span data-stu-id="140d7-105">These are used within the [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) structures.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="140d7-106">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="140d7-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="140d7-107">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="140d7-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="140d7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="140d7-108">Syntax</span></span>
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a><span data-ttu-id="140d7-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="140d7-109">Constants</span></span>

| <span data-ttu-id="140d7-110">Nome</span><span class="sxs-lookup"><span data-stu-id="140d7-110">Name</span></span> | <span data-ttu-id="140d7-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="140d7-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="140d7-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span><span class="sxs-lookup"><span data-stu-id="140d7-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span></span> | <span data-ttu-id="140d7-113">Fa sì che [](./ns-directml-dml_depth_to_space1_operator_desc.md) i tensori DML_DEPTH_TO_SPACE1_OPERATOR_DESC e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) siano interpretati con i layout seguenti, in cui le dimensioni tra parentesi vengono appiattite insieme.</span><span class="sxs-lookup"><span data-stu-id="140d7-113">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="140d7-114">- **Versione di profondità:**[Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span><span class="sxs-lookup"><span data-stu-id="140d7-114">- **Depth version**: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span></span><br><span data-ttu-id="140d7-115">- **Versione spazio:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="140d7-115">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |
| <span data-ttu-id="140d7-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span><span class="sxs-lookup"><span data-stu-id="140d7-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span></span> | <span data-ttu-id="140d7-117">Fa sì che [](./ns-directml-dml_depth_to_space1_operator_desc.md) i tensori usati DML_DEPTH_TO_SPACE1_OPERATOR_DESC e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) siano interpretati con i layout seguenti, in cui le dimensioni tra parentesi vengono appiattite insieme.</span><span class="sxs-lookup"><span data-stu-id="140d7-117">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="140d7-118">- **Versione di profondità:**[Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span><span class="sxs-lookup"><span data-stu-id="140d7-118">- **Depth version**: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span></span><br><span data-ttu-id="140d7-119">- **Versione spazio:**[Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="140d7-119">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |

## <a name="remarks"></a><span data-ttu-id="140d7-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="140d7-120">Remarks</span></span>

<span data-ttu-id="140d7-121">Vedere [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) per esempi che illustrano l'effetto di questi valori.</span><span class="sxs-lookup"><span data-stu-id="140d7-121">See [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) documentation for examples showing the effect of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="140d7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="140d7-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="140d7-123">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="140d7-123">**Header**</span></span> | <span data-ttu-id="140d7-124">directml.h</span><span class="sxs-lookup"><span data-stu-id="140d7-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="140d7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="140d7-125">See also</span></span>

* [<span data-ttu-id="140d7-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="140d7-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span></span>](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [<span data-ttu-id="140d7-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="140d7-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a><span data-ttu-id="140d7-128">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="140d7-128">Availability</span></span>
<span data-ttu-id="140d7-129">Questa enumerazione è stata introdotta in `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="140d7-129">This enumeration was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>