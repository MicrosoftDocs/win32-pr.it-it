---
title: Proprietà IResultProperty DisplayState (WdsSharedIDL. h)
description: Visibilità della proprietà.
ms.assetid: 4fdf6cdb-30bd-4582-a573-a1cc9f4052e6
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà DisplayState
- Proprietà DisplayState caratteristiche dell'ambiente Windows legacy, interfaccia IResultProperty
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty, proprietà DisplayState
topic_type:
- apiref
api_name:
- IResultProperty.DisplayState
- IResultProperty.get_DisplayState
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85634441a38c2cb2130010c79f8ee3ebcb78a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301948"
---
# <a name="iresultpropertydisplaystate-property"></a><span data-ttu-id="894aa-106">IResultProperty::D Proprietà isplayState</span><span class="sxs-lookup"><span data-stu-id="894aa-106">IResultProperty::DisplayState property</span></span>

> [!NOTE]
> <span data-ttu-id="894aa-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="894aa-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="894aa-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="894aa-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="894aa-109">Visibilità della proprietà.</span><span class="sxs-lookup"><span data-stu-id="894aa-109">Visability of the property.</span></span>

<span data-ttu-id="894aa-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="894aa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="894aa-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="894aa-111">Syntax</span></span>


```C++
HRESULT get_DisplayState(
  [out, retval] PropertyDisplayState *state
);
```



## <a name="property-value"></a><span data-ttu-id="894aa-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="894aa-112">Property value</span></span>

<span data-ttu-id="894aa-113">Restituisce un puntatore al valore dello stato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="894aa-113">returns a pointer to the display state value.</span></span>

## <a name="requirements"></a><span data-ttu-id="894aa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="894aa-114">Requirements</span></span>



| <span data-ttu-id="894aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="894aa-115">Requirement</span></span> | <span data-ttu-id="894aa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="894aa-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="894aa-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="894aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="894aa-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="894aa-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="894aa-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="894aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="894aa-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="894aa-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="894aa-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="894aa-121">Redistributable</span></span><br/>          | <span data-ttu-id="894aa-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="894aa-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="894aa-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="894aa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="894aa-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="894aa-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





