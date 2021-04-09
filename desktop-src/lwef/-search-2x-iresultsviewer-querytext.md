---
title: Proprietà IResultsViewer QueryText (WdsView. h)
description: Ottiene o imposta il testo della query corrente.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- Funzionalità dell'ambiente Windows legacy della Proprietà QueryText
- Proprietà QueryText caratteristiche dell'ambiente Windows legacy, interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, Proprietà QueryText
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98450114ad64ec0209b14041b8f2516dc6884b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121171"
---
# <a name="iresultsviewerquerytext-property"></a><span data-ttu-id="34d88-106">Proprietà IResultsViewer:: QueryText</span><span class="sxs-lookup"><span data-stu-id="34d88-106">IResultsViewer::QueryText property</span></span>

> [!NOTE]
> <span data-ttu-id="34d88-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="34d88-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="34d88-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="34d88-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="34d88-109">Ottiene o imposta il testo della query corrente.</span><span class="sxs-lookup"><span data-stu-id="34d88-109">Gets or sets the current query text.</span></span>

<span data-ttu-id="34d88-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="34d88-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d88-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34d88-111">Syntax</span></span>


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a><span data-ttu-id="34d88-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="34d88-112">Property value</span></span>

<span data-ttu-id="34d88-113">Imposta il testo della query corrente.</span><span class="sxs-lookup"><span data-stu-id="34d88-113">Sets the current query text.</span></span>

## <a name="requirements"></a><span data-ttu-id="34d88-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34d88-114">Requirements</span></span>



| <span data-ttu-id="34d88-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="34d88-115">Requirement</span></span> | <span data-ttu-id="34d88-116">Valore</span><span class="sxs-lookup"><span data-stu-id="34d88-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="34d88-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34d88-117">Minimum supported client</span></span><br/> | <span data-ttu-id="34d88-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="34d88-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="34d88-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34d88-119">Minimum supported server</span></span><br/> | <span data-ttu-id="34d88-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="34d88-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="34d88-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="34d88-121">Redistributable</span></span><br/>          | <span data-ttu-id="34d88-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="34d88-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="34d88-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34d88-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="34d88-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="34d88-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





