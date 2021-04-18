---
title: Proprietà DisplayName IResultsViewer (WdsView. h)
description: Nome visualizzato localizzato del tipo.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy, interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, proprietà DisplayName
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5ba65729fb238dbed57b71d893a9814c8ac8f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301543"
---
# <a name="iresultsviewerdisplayname-property"></a><span data-ttu-id="76471-106">IResultsViewer::D proprietà di riproduzione</span><span class="sxs-lookup"><span data-stu-id="76471-106">IResultsViewer::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="76471-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="76471-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="76471-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="76471-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="76471-109">Nome visualizzato localizzato del tipo.</span><span class="sxs-lookup"><span data-stu-id="76471-109">Localized display name of the type.</span></span>

<span data-ttu-id="76471-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="76471-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="76471-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76471-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="76471-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="76471-112">Property value</span></span>

<span data-ttu-id="76471-113">Puntatore a un valore che riceve il nome visualizzato localizzato per il tipo.</span><span class="sxs-lookup"><span data-stu-id="76471-113">Pointer to a value that receives the localized display name for the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="76471-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76471-114">Requirements</span></span>



| <span data-ttu-id="76471-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="76471-115">Requirement</span></span> | <span data-ttu-id="76471-116">Valore</span><span class="sxs-lookup"><span data-stu-id="76471-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76471-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76471-117">Minimum supported client</span></span><br/> | <span data-ttu-id="76471-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="76471-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76471-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76471-119">Minimum supported server</span></span><br/> | <span data-ttu-id="76471-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="76471-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="76471-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="76471-121">Redistributable</span></span><br/>          | <span data-ttu-id="76471-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="76471-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="76471-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76471-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="76471-124"><dt>WdsView. h</dt></span><span class="sxs-lookup"><span data-stu-id="76471-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





