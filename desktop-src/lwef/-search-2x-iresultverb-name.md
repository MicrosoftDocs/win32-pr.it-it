---
title: Proprietà Name di IResultVerb (WdsSharedIDL. h)
description: Questa proprietà restituisce un puntatore al nome cononical per il verbo, ad esempio Print, Open e così via.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- Proprietà nome caratteristiche ambiente Windows legacy
- Proprietà nome ambiente Windows legacy funzionalità, interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, proprietà Name
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c831ea0dad36f733995062d8a76fc27d4cc837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963815"
---
# <a name="iresultverbname-property"></a><span data-ttu-id="4d4eb-106">Proprietà IResultVerb:: Name</span><span class="sxs-lookup"><span data-stu-id="4d4eb-106">IResultVerb::Name property</span></span>

> [!NOTE]
> <span data-ttu-id="4d4eb-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4d4eb-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4d4eb-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="4d4eb-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="4d4eb-109">Questa proprietà restituisce un puntatore al nome cononical per il verbo, ad esempio Print, Open e così via.</span><span class="sxs-lookup"><span data-stu-id="4d4eb-109">This property returns a pointer to the cononical name for the verb such as print, open, etc.</span></span>

<span data-ttu-id="4d4eb-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4d4eb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d4eb-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d4eb-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="4d4eb-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4d4eb-112">Property value</span></span>

<span data-ttu-id="4d4eb-113">Name è un puntatore al nome cononical per il verbo.</span><span class="sxs-lookup"><span data-stu-id="4d4eb-113">name is a pointer to the cononical name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d4eb-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d4eb-114">Requirements</span></span>



| <span data-ttu-id="4d4eb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d4eb-115">Requirement</span></span> | <span data-ttu-id="4d4eb-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4d4eb-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4eb-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d4eb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4d4eb-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d4eb-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4d4eb-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d4eb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4d4eb-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="4d4eb-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4d4eb-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4d4eb-121">Redistributable</span></span><br/>          | <span data-ttu-id="4d4eb-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="4d4eb-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="4d4eb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d4eb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d4eb-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d4eb-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





