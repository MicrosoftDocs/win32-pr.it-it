---
title: Struttura MrmResourceIndexerHandle (MrmResourceIndexer. h)
description: Rappresenta un handle opaco per un oggetto indicizzatore di risorse. L'handle è gestito dal sistema operativo. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- Menu struttura MrmResourceIndexerHandle e altre risorse
- Menu puntatore struttura PMrmResourceIndexerHandle e altre risorse
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5786585597b5d23a6f6c0cd6842b655727c3ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400920"
---
# <a name="mrmresourceindexerhandle-structure"></a><span data-ttu-id="afa9b-107">Struttura MrmResourceIndexerHandle</span><span class="sxs-lookup"><span data-stu-id="afa9b-107">MrmResourceIndexerHandle structure</span></span>

<span data-ttu-id="afa9b-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="afa9b-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="afa9b-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="afa9b-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="afa9b-110">Rappresenta un handle opaco per un oggetto indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="afa9b-110">Represents an opaque handle to a resource indexer object.</span></span> <span data-ttu-id="afa9b-111">L'handle è gestito dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="afa9b-111">The handle is managed by the operating system.</span></span> <span data-ttu-id="afa9b-112">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="afa9b-112">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="afa9b-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afa9b-113">Syntax</span></span>


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a><span data-ttu-id="afa9b-114">Members</span><span class="sxs-lookup"><span data-stu-id="afa9b-114">Members</span></span>

<dl> <dt>

<span data-ttu-id="afa9b-115">**gestire**</span><span class="sxs-lookup"><span data-stu-id="afa9b-115">**handle**</span></span>
</dt> <dd>

<span data-ttu-id="afa9b-116">Tipo: **PVOID**</span><span class="sxs-lookup"><span data-stu-id="afa9b-116">Type: **PVOID**</span></span>

</dd> <dd>

<span data-ttu-id="afa9b-117">Handle opaco per un oggetto indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="afa9b-117">An opaque handle to a resource indexer object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afa9b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afa9b-118">Requirements</span></span>



| <span data-ttu-id="afa9b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="afa9b-119">Requirement</span></span> | <span data-ttu-id="afa9b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="afa9b-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa9b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afa9b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="afa9b-122">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="afa9b-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="afa9b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afa9b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="afa9b-124">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="afa9b-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="afa9b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afa9b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="afa9b-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="afa9b-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afa9b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afa9b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa9b-128">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="afa9b-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

