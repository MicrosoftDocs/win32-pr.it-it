---
title: OP_PACKAGE_PART_COLLECTION
description: Definizione di OP_PACKAGE_PART_COLLECTION IDL
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104047549"
---
# <a name="op_package_part_collection-structure"></a><span data-ttu-id="4a665-103">Struttura OP_PACKAGE_PART_COLLECTION</span><span class="sxs-lookup"><span data-stu-id="4a665-103">OP_PACKAGE_PART_COLLECTION structure</span></span>

<span data-ttu-id="4a665-104">Specifica una struttura che contiene una matrice di strutture di OP_PACKAGE_PART.</span><span class="sxs-lookup"><span data-stu-id="4a665-104">Specifies a structure that contains an array of OP_PACKAGE_PART structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a665-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a665-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a><span data-ttu-id="4a665-106">Members</span><span class="sxs-lookup"><span data-stu-id="4a665-106">Members</span></span>

### <a name="cparts"></a><span data-ttu-id="4a665-107">cParts</span><span class="sxs-lookup"><span data-stu-id="4a665-107">cParts</span></span>

<span data-ttu-id="4a665-108">Contiene il numero di elementi in pParts.</span><span class="sxs-lookup"><span data-stu-id="4a665-108">Contains the number of elements in pParts.</span></span>

### <a name="pparts"></a><span data-ttu-id="4a665-109">pParts</span><span class="sxs-lookup"><span data-stu-id="4a665-109">pParts</span></span>

<span data-ttu-id="4a665-110">Contiene una matrice di strutture di OP_PACKAGE_PART.</span><span class="sxs-lookup"><span data-stu-id="4a665-110">Contains an array of OP_PACKAGE_PART structures.</span></span>

### <a name="extension"></a><span data-ttu-id="4a665-111">Estensione</span><span class="sxs-lookup"><span data-stu-id="4a665-111">Extension</span></span>

<span data-ttu-id="4a665-112">Riservato per utilizzi futuri e deve essere impostato su tutti zeri.</span><span class="sxs-lookup"><span data-stu-id="4a665-112">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a665-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a665-113">See also</span></span>

[<span data-ttu-id="4a665-114">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="4a665-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="4a665-115">**\_parte pacchetto \_ op**</span><span class="sxs-lookup"><span data-stu-id="4a665-115">**OP\_PACKAGE\_PART**</span></span>](odj-op_package_part.md)

[<span data-ttu-id="4a665-116">**\_BLOB op**</span><span class="sxs-lookup"><span data-stu-id="4a665-116">**OP\_BLOB**</span></span>](odj-op_blob.md)

