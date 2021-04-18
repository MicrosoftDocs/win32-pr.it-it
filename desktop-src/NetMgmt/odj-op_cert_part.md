---
title: OP_CERT_PART
description: Definizione di OP_CERT_PART IDL
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "106300651"
---
# <a name="op_cert_part-structure"></a><span data-ttu-id="fe4b8-103">Struttura OP_CERT_PART</span><span class="sxs-lookup"><span data-stu-id="fe4b8-103">OP_CERT_PART structure</span></span>

<span data-ttu-id="fe4b8-104">Contiene i file PFX serializzati e gli archivi certificati.</span><span class="sxs-lookup"><span data-stu-id="fe4b8-104">Contains serialized PFX and certificate stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4b8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe4b8-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a><span data-ttu-id="fe4b8-106">Members</span><span class="sxs-lookup"><span data-stu-id="fe4b8-106">Members</span></span>

### <a name="cpfxstores"></a><span data-ttu-id="fe4b8-107">cPfxStores</span><span class="sxs-lookup"><span data-stu-id="fe4b8-107">cPfxStores</span></span>

<span data-ttu-id="fe4b8-108">Contiene il numero di elementi in pPfxStores.</span><span class="sxs-lookup"><span data-stu-id="fe4b8-108">Contains the number of elements in pPfxStores.</span></span>

### <a name="ppfxstores"></a><span data-ttu-id="fe4b8-109">pPfxStores</span><span class="sxs-lookup"><span data-stu-id="fe4b8-109">pPfxStores</span></span>

<span data-ttu-id="fe4b8-110">Contiene una matrice di strutture di OP_CERT_PFX_STORE.</span><span class="sxs-lookup"><span data-stu-id="fe4b8-110">Contains an array of OP_CERT_PFX_STORE structures.</span></span>

### <a name="csststores"></a><span data-ttu-id="fe4b8-111">cSstStores</span><span class="sxs-lookup"><span data-stu-id="fe4b8-111">cSstStores</span></span>

<span data-ttu-id="fe4b8-112">Contiene il numero di elementi in pSstStores.</span><span class="sxs-lookup"><span data-stu-id="fe4b8-112">Contains the number of elements in pSstStores.</span></span>

### <a name="psststores"></a><span data-ttu-id="fe4b8-113">pSstStores</span><span class="sxs-lookup"><span data-stu-id="fe4b8-113">pSstStores</span></span>

<span data-ttu-id="fe4b8-114">Contiene una matrice di strutture di OP_CERT_SST_STORE.</span><span class="sxs-lookup"><span data-stu-id="fe4b8-114">Contains an array of OP_CERT_SST_STORE structures.</span></span>

### <a name="extension"></a><span data-ttu-id="fe4b8-115">Estensione</span><span class="sxs-lookup"><span data-stu-id="fe4b8-115">Extension</span></span>

<span data-ttu-id="fe4b8-116">Riservato per usi futuri e deve contenere tutti zeri.</span><span class="sxs-lookup"><span data-stu-id="fe4b8-116">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe4b8-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe4b8-117">See also</span></span>

[<span data-ttu-id="fe4b8-118">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="fe4b8-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="fe4b8-119">**\_ \_ Archivio pfx del certificato op \_**</span><span class="sxs-lookup"><span data-stu-id="fe4b8-119">**OP\_CERT\_PFX\_STORE**</span></span>](odj-op_cert_pfx_store.md)

[<span data-ttu-id="fe4b8-120">**\_Archivio di \_ SST del certificato op \_**</span><span class="sxs-lookup"><span data-stu-id="fe4b8-120">**OP\_CERT\_SST\_STORE**</span></span>](odj-op_cert_sst_store.md)

[<span data-ttu-id="fe4b8-121">**\_BLOB op**</span><span class="sxs-lookup"><span data-stu-id="fe4b8-121">**OP\_BLOB**</span></span>](odj-op_blob.md)

