---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: Unione di tipi scalari.
helpviewer_keywords:
- DML_SCALAR_UNION
- DML_SCALAR_UNION structure
- direct3d12.dml_scalar_union
- directml/DML_SCALAR_UNION
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
ms.keywords: DML_SCALAR_UNION, DML_SCALAR_UNION structure, direct3d12.dml_scalar_union, directml/DML_SCALAR_UNION
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
- DML_SCALAR_UNION
- directml/DML_SCALAR_UNION
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
- DML_SCALAR_UNION
ms.openlocfilehash: d53ec7025d3da5a07a648849e366d436755ad3f1
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803948"
---
# <a name="dml_scalar_union-union-directmlh"></a><span data-ttu-id="bbfca-103">DML_SCALAR_UNION union (directml.h)</span><span class="sxs-lookup"><span data-stu-id="bbfca-103">DML_SCALAR_UNION union (directml.h)</span></span>
<span data-ttu-id="bbfca-104">Unione di tipi scalari.</span><span class="sxs-lookup"><span data-stu-id="bbfca-104">A union of scalar types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bbfca-105">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="bbfca-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="bbfca-106">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="bbfca-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bbfca-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbfca-107">Syntax</span></span>
```cpp
union DML_SCALAR_UNION {
  BYTE   Bytes[8];
  INT8   Int8;
  UINT8  UInt8;
  INT16  Int16;
  UINT16 UInt16;
  INT32  Int32;
  UINT32 UInt32;
  INT64  Int64;
  UINT64 UInt64;
  FLOAT  Float32;
  DOUBLE Float64;
};
```



## <a name="members"></a><span data-ttu-id="bbfca-108">Members</span><span class="sxs-lookup"><span data-stu-id="bbfca-108">Members</span></span>

`Bytes`

<span data-ttu-id="bbfca-109">Matrice a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="bbfca-109">An 8-byte array.</span></span>


`Int8`

<span data-ttu-id="bbfca-110">Numero intero con segno a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="bbfca-110">An 8-bit signed integer.</span></span>


`UInt8`

<span data-ttu-id="bbfca-111">Intero senza segno a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="bbfca-111">An 8-bit unsigned integer.</span></span>


`Int16`

<span data-ttu-id="bbfca-112">Intero con segno a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="bbfca-112">A 16-bit signed integer.</span></span>


`UInt16`

<span data-ttu-id="bbfca-113">Numero intero non firmato a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="bbfca-113">A 16-bit unsigned integer.</span></span>


`Int32`

<span data-ttu-id="bbfca-114">Intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="bbfca-114">A 32-bit signed integer.</span></span>


`UInt32`

<span data-ttu-id="bbfca-115">Intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="bbfca-115">A 32-bit unsigned integer.</span></span>


`Int64`

<span data-ttu-id="bbfca-116">Intero con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="bbfca-116">A 64-bit signed integer.</span></span>


`UInt64`

<span data-ttu-id="bbfca-117">Intero senza segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="bbfca-117">A 64-bit unsigned integer.</span></span>


`Float32`

<span data-ttu-id="bbfca-118">Numero a virgola mobile e precisione singola.</span><span class="sxs-lookup"><span data-stu-id="bbfca-118">A single precision floating-point number.</span></span>


`Float64`

<span data-ttu-id="bbfca-119">Numero a virgola mobile e precisione doppia.</span><span class="sxs-lookup"><span data-stu-id="bbfca-119">A double precision floating-point number.</span></span>



## <a name="requirements"></a><span data-ttu-id="bbfca-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbfca-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bbfca-121">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="bbfca-121">**Header**</span></span> | <span data-ttu-id="bbfca-122">directml.h</span><span class="sxs-lookup"><span data-stu-id="bbfca-122">directml.h</span></span> |