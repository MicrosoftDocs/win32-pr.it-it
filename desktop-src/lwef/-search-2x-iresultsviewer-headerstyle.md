---
title: Proprietà HeaderStyle IResultsViewer (WdsView. h)
description: Stile dell'intestazione visualizzata nella visualizzazione.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà Header
- Proprietà Header, funzionalità dell'ambiente Windows legacy, interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, proprietà Header
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc4d0ad56e1303914af712e2a9b6fa0fd416785
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741594"
---
# <a name="iresultsviewerheaderstyle-property"></a><span data-ttu-id="8c3c0-106">Proprietà IResultsViewer:: header</span><span class="sxs-lookup"><span data-stu-id="8c3c0-106">IResultsViewer::HeaderStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="8c3c0-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8c3c0-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8c3c0-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8c3c0-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8c3c0-109">Stile dell'intestazione visualizzata nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c3c0-109">The style of header displayed in the view.</span></span>

<span data-ttu-id="8c3c0-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8c3c0-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3c0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c3c0-111">Syntax</span></span>


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="8c3c0-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8c3c0-112">Property value</span></span>

<span data-ttu-id="8c3c0-113">Imposta lo stile dell'intestazione visualizzata.</span><span class="sxs-lookup"><span data-stu-id="8c3c0-113">Sets the style of the header displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c3c0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c3c0-114">Requirements</span></span>



| <span data-ttu-id="8c3c0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c3c0-115">Requirement</span></span> | <span data-ttu-id="8c3c0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8c3c0-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3c0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c3c0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c3c0-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c3c0-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8c3c0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c3c0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c3c0-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="8c3c0-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="8c3c0-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="8c3c0-121">Redistributable</span></span><br/>          | <span data-ttu-id="8c3c0-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="8c3c0-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="8c3c0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c3c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c3c0-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c3c0-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





