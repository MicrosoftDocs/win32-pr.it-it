---
title: Proprietà IResultsViewer SortProperty (WdsView. h)
description: Questa proprietà consente di impostare o restituire l'IndexColumn della proprietà per ordinare i risultati in base a.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà SortProperty
- Proprietà SortProperty caratteristiche dell'ambiente Windows legacy, interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, proprietà SortProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb75b98f1f0a726ef0d61b5c476df1485ba7189
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873733"
---
# <a name="iresultsviewersortproperty-property"></a><span data-ttu-id="829d9-106">Proprietà IResultsViewer:: SortProperty</span><span class="sxs-lookup"><span data-stu-id="829d9-106">IResultsViewer::SortProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="829d9-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="829d9-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="829d9-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="829d9-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="829d9-109">Questa proprietà consente di impostare o restituire l'IndexColumn della proprietà per ordinare i risultati in base a.</span><span class="sxs-lookup"><span data-stu-id="829d9-109">This property will set or return the IndexColumn of the property to sort results by.</span></span>

<span data-ttu-id="829d9-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="829d9-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="829d9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="829d9-111">Syntax</span></span>


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="829d9-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="829d9-112">Property value</span></span>

<span data-ttu-id="829d9-113">Imposta la proprietà IndexColumn.</span><span class="sxs-lookup"><span data-stu-id="829d9-113">Sets the IndexColumn property.</span></span>

## <a name="requirements"></a><span data-ttu-id="829d9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="829d9-114">Requirements</span></span>



| <span data-ttu-id="829d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="829d9-115">Requirement</span></span> | <span data-ttu-id="829d9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="829d9-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="829d9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="829d9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="829d9-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="829d9-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="829d9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="829d9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="829d9-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="829d9-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="829d9-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="829d9-121">Redistributable</span></span><br/>          | <span data-ttu-id="829d9-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="829d9-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="829d9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="829d9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="829d9-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="829d9-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





