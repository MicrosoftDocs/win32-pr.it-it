---
title: Proprietà IResultsViewer itemStore sconosciuta (WdsView. h)
description: Questa proprietà consente di impostare o restituire il nome dell'archivio in base al quale filtrare i risultati.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà itemStore sconosciuta
- Proprietà itemStore sconosciuta caratteristiche dell'ambiente Windows legacy, interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, proprietà itemStore sconosciuta
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99abd4ef7ee36a0c76efa391d98a9fdb1d75f34e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476505"
---
# <a name="iresultsvieweritemstore-property"></a><span data-ttu-id="c65de-106">Proprietà IResultsViewer:: itemStore sconosciuta</span><span class="sxs-lookup"><span data-stu-id="c65de-106">IResultsViewer::ItemStore property</span></span>

> [!NOTE]
> <span data-ttu-id="c65de-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c65de-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c65de-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="c65de-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c65de-109">Questa proprietà consente di impostare o restituire il nome dell'archivio in base al quale filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="c65de-109">This property will set or return the name of the store to filter results by.</span></span>

<span data-ttu-id="c65de-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c65de-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c65de-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c65de-111">Syntax</span></span>


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="c65de-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c65de-112">Property value</span></span>

<span data-ttu-id="c65de-113">Imposta i nomi dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="c65de-113">Sets the names of the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="c65de-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c65de-114">Requirements</span></span>



| <span data-ttu-id="c65de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c65de-115">Requirement</span></span> | <span data-ttu-id="c65de-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c65de-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c65de-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65de-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c65de-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c65de-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c65de-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65de-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c65de-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="c65de-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="c65de-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c65de-121">Redistributable</span></span><br/>          | <span data-ttu-id="c65de-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="c65de-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="c65de-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c65de-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c65de-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="c65de-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





