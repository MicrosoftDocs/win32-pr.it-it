---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Definisce le costanti che specificano la direzione di un'operazione lungo l'asse specificato per l'operatore (ad esempio, somma, selezione degli elementi top-k, selezione dell'elemento minimo).
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
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
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
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
- DML_AXIS_DIRECTION
ms.openlocfilehash: e54d2abed3843ea9b2a22cb3c385f9edd1541ba5
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803782"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a><span data-ttu-id="468e4-103">DML_AXIS_DIRECTION enumerazione (directml.h)</span><span class="sxs-lookup"><span data-stu-id="468e4-103">DML_AXIS_DIRECTION enumeration (directml.h)</span></span>

<span data-ttu-id="468e4-104">Definisce le costanti che specificano la direzione di un'operazione lungo l'asse specificato per l'operatore (ad esempio, somma, selezione degli elementi top-k, selezione dell'elemento minimo).</span><span class="sxs-lookup"><span data-stu-id="468e4-104">Defines constants that specify the direction of an operation along the given axis for the operator (for example, summation, selecting the top-k elements, selecting the minimum element).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="468e4-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="468e4-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="468e4-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="468e4-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="468e4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="468e4-107">Syntax</span></span>
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a><span data-ttu-id="468e4-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="468e4-108">Constants</span></span>

| <span data-ttu-id="468e4-109">Nome</span><span class="sxs-lookup"><span data-stu-id="468e4-109">Name</span></span> | <span data-ttu-id="468e4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="468e4-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="468e4-111">DML_AXIS_DIRECTION_INCREASING</span><span class="sxs-lookup"><span data-stu-id="468e4-111">DML_AXIS_DIRECTION_INCREASING</span></span> | <span data-ttu-id="468e4-112">Specifica l'ordine crescente (dall'indice basso all'indice alto).</span><span class="sxs-lookup"><span data-stu-id="468e4-112">Specifies increasing order (from the low index to the high index).</span></span> |
| <span data-ttu-id="468e4-113">DML_AXIS_DIRECTION_DECREASING</span><span class="sxs-lookup"><span data-stu-id="468e4-113">DML_AXIS_DIRECTION_DECREASING</span></span> | <span data-ttu-id="468e4-114">Specifica l'ordine decrescente (dall'indice alto all'indice basso).</span><span class="sxs-lookup"><span data-stu-id="468e4-114">Specifies decreasing order (from the high index to the low index).</span></span> |


## <a name="requirements"></a><span data-ttu-id="468e4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="468e4-115">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="468e4-116">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="468e4-116">**Header**</span></span> | <span data-ttu-id="468e4-117">directml.h</span><span class="sxs-lookup"><span data-stu-id="468e4-117">directml.h</span></span> |