---
title: Proprietà IResultProperty IndexColumn (WdsSharedIDL. h)
description: Nome della colonna proprietà nell'indice.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- Funzionalità dell'ambiente Windows legacy della Proprietà IndexColumn
- Proprietà IndexColumn caratteristiche dell'ambiente Windows legacy, interfaccia IResultProperty
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty, Proprietà IndexColumn
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4749f9ba1200f1af8ba202056e48f0123e8402
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873605"
---
# <a name="iresultpropertyindexcolumn-property"></a><span data-ttu-id="567d6-106">Proprietà IResultProperty:: IndexColumn</span><span class="sxs-lookup"><span data-stu-id="567d6-106">IResultProperty::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="567d6-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="567d6-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="567d6-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="567d6-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="567d6-109">Nome della colonna proprietà nell'indice.</span><span class="sxs-lookup"><span data-stu-id="567d6-109">Properties column name in the index.</span></span>

<span data-ttu-id="567d6-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="567d6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="567d6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="567d6-111">Syntax</span></span>


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="567d6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="567d6-112">Property value</span></span>

<span data-ttu-id="567d6-113">Restituisce un puntatore al nome della colonna nell'indice.</span><span class="sxs-lookup"><span data-stu-id="567d6-113">returns a pointer to the column name in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="567d6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="567d6-114">Requirements</span></span>



| <span data-ttu-id="567d6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="567d6-115">Requirement</span></span> | <span data-ttu-id="567d6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="567d6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="567d6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="567d6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="567d6-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="567d6-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="567d6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="567d6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="567d6-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="567d6-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="567d6-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="567d6-121">Redistributable</span></span><br/>          | <span data-ttu-id="567d6-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="567d6-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="567d6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="567d6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="567d6-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="567d6-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





