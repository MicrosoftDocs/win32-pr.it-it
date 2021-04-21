---
UID: NE:directml.DML_RANDOM_GENERATOR_TYPE
title: DML_RANDOM_GENERATOR_TYPE
description: Definisce costanti che specificano tipi di generatore di numeri casuali.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_TYPE
- DML_RANDOM_GENERATOR_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_RANDOM_GENERATOR_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_TYPE, DML_RANDOM_GENERATOR_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_RANDOM_GENERATOR_TYPE
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
- DML_RANDOM_GENERATOR_TYPE
- directml/DML_RANDOM_GENERATOR_TYPE
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
- DML_RANDOM_GENERATOR_TYPE
ms.openlocfilehash: c08b5cdc07280a2851636a555415ecce515fa79b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803761"
---
# <a name="dml_random_generator_type-enumeration-directmlh"></a><span data-ttu-id="16868-103">DML_RANDOM_GENERATOR_TYPE enumerazione (directml.h)</span><span class="sxs-lookup"><span data-stu-id="16868-103">DML_RANDOM_GENERATOR_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="16868-104">Definisce costanti che specificano tipi di generatore di numeri casuali.</span><span class="sxs-lookup"><span data-stu-id="16868-104">Defines constants that specify types of random random-number generator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16868-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="16868-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="16868-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="16868-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="16868-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16868-107">Syntax</span></span>
```cpp
enum DML_RANDOM_GENERATOR_TYPE
{
  DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10
};
```

## <a name="constants"></a><span data-ttu-id="16868-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="16868-108">Constants</span></span>

| <span data-ttu-id="16868-109">Nome</span><span class="sxs-lookup"><span data-stu-id="16868-109">Name</span></span> | <span data-ttu-id="16868-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16868-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="16868-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span><span class="sxs-lookup"><span data-stu-id="16868-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span></span> | <span data-ttu-id="16868-112">Specifica un generatore per i numeri pseudo-casuali in base [all'algoritmo 4x32-10 di Philox.](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)</span><span class="sxs-lookup"><span data-stu-id="16868-112">Specifies a generator for pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span> |


## <a name="requirements"></a><span data-ttu-id="16868-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16868-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="16868-114">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="16868-114">**Header**</span></span> | <span data-ttu-id="16868-115">directml.h</span><span class="sxs-lookup"><span data-stu-id="16868-115">directml.h</span></span> |