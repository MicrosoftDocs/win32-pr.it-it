---
title: Proprietà IPropertyFilter NestingDepth (WdsSharedIDL. h)
description: Filtra la profondità all'interno di un set annidato di parentesi.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà NestingDepth
- Proprietà NestingDepth caratteristiche dell'ambiente Windows legacy, interfaccia IPropertyFilter
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilter, proprietà NestingDepth
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bda4e12bb68b501fa42003ac145113dade3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400597"
---
# <a name="ipropertyfilternestingdepth-property"></a><span data-ttu-id="c1dba-106">Proprietà IPropertyFilter:: NestingDepth</span><span class="sxs-lookup"><span data-stu-id="c1dba-106">IPropertyFilter::NestingDepth property</span></span>

> [!NOTE]
> <span data-ttu-id="c1dba-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c1dba-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c1dba-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="c1dba-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c1dba-109">Filtra la profondità all'interno di un set annidato di parentesi.</span><span class="sxs-lookup"><span data-stu-id="c1dba-109">Filters depth within a nested set of parentheses.</span></span>

<span data-ttu-id="c1dba-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c1dba-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1dba-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1dba-111">Syntax</span></span>


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a><span data-ttu-id="c1dba-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c1dba-112">Property value</span></span>

<span data-ttu-id="c1dba-113">Imposta il numero che indica la profondità delle parentesi nidificate.</span><span class="sxs-lookup"><span data-stu-id="c1dba-113">Sets the number indicating the depth of nested parentheses.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1dba-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1dba-114">Requirements</span></span>



| <span data-ttu-id="c1dba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1dba-115">Requirement</span></span> | <span data-ttu-id="c1dba-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c1dba-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dba-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1dba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c1dba-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1dba-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c1dba-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1dba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c1dba-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="c1dba-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c1dba-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c1dba-121">Redistributable</span></span><br/>          | <span data-ttu-id="c1dba-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="c1dba-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="c1dba-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1dba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1dba-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1dba-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





