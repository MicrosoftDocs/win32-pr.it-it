---
title: Proprietà DataType IResultProperty (WdsSharedIDL. h)
description: Tipo di dati Properties.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- Caratteristiche dell'ambiente Windows legacy della proprietà DataType
- Proprietà DataType caratteristiche ambiente Windows legacy, interfaccia IResultProperty
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty, proprietà DataType
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d887642594ed5ac7f78de1d4eac76fb4709f0dfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301952"
---
# <a name="iresultpropertydatatype-property"></a><span data-ttu-id="7aa92-106">IResultProperty::D Proprietà ataType</span><span class="sxs-lookup"><span data-stu-id="7aa92-106">IResultProperty::DataType property</span></span>

> [!NOTE]
> <span data-ttu-id="7aa92-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7aa92-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7aa92-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="7aa92-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7aa92-109">Tipo di dati Properties.</span><span class="sxs-lookup"><span data-stu-id="7aa92-109">A properties data type.</span></span>

<span data-ttu-id="7aa92-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7aa92-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa92-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7aa92-111">Syntax</span></span>


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a><span data-ttu-id="7aa92-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7aa92-112">Property value</span></span>

<span data-ttu-id="7aa92-113">Restituisce un puntatore al tipo di dati Properties.</span><span class="sxs-lookup"><span data-stu-id="7aa92-113">returns a pointer to the properties data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aa92-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7aa92-114">Requirements</span></span>



| <span data-ttu-id="7aa92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aa92-115">Requirement</span></span> | <span data-ttu-id="7aa92-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7aa92-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa92-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7aa92-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7aa92-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7aa92-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7aa92-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7aa92-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7aa92-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="7aa92-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7aa92-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7aa92-121">Redistributable</span></span><br/>          | <span data-ttu-id="7aa92-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="7aa92-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="7aa92-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7aa92-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aa92-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aa92-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





