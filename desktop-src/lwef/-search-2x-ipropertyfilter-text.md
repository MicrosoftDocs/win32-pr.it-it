---
title: Proprietà Text IPropertyFilter (WdsSharedIDL. h)
description: Testo del filtro.
ms.assetid: 1e0bf432-6d6b-4c29-bb2f-64fb91f5faaf
keywords:
- Proprietà testo funzionalità legacy ambiente Windows
- Proprietà Text funzionalità dell'ambiente Windows legacy, interfaccia IPropertyFilter
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilter, proprietà Text
topic_type:
- apiref
api_name:
- IPropertyFilter.Text
- IPropertyFilter.get_Text
- IPropertyFilter.put_Text
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b30614f63cbcd766ca843f1b793632502f8e114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518315"
---
# <a name="ipropertyfiltertext-property"></a><span data-ttu-id="9c378-106">Proprietà IPropertyFilter:: Text</span><span class="sxs-lookup"><span data-stu-id="9c378-106">IPropertyFilter::Text property</span></span>

> [!NOTE]
> <span data-ttu-id="9c378-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9c378-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9c378-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="9c378-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9c378-109">Testo del filtro.</span><span class="sxs-lookup"><span data-stu-id="9c378-109">Text of the filter.</span></span>

<span data-ttu-id="9c378-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9c378-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c378-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c378-111">Syntax</span></span>


```C++
HRESULT put_Text(
  [in]          BSTR text
);

HRESULT get_Text(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="9c378-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9c378-112">Property value</span></span>

<span data-ttu-id="9c378-113">Imposta il testo del filtro.</span><span class="sxs-lookup"><span data-stu-id="9c378-113">Sets the filter text.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c378-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c378-114">Requirements</span></span>



| <span data-ttu-id="9c378-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c378-115">Requirement</span></span> | <span data-ttu-id="9c378-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9c378-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c378-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c378-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c378-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c378-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9c378-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c378-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c378-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="9c378-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9c378-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9c378-121">Redistributable</span></span><br/>          | <span data-ttu-id="9c378-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="9c378-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="9c378-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c378-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c378-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c378-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





