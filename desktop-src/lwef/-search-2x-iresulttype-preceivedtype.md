---
title: Proprietà IResultType PreceivedType (WdsSharedIDL. h)
description: Questa proprietà contiene la stringa utilizzata per identificare il tipo nell'indice.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà PreceivedType
- Proprietà PreceivedType caratteristiche dell'ambiente Windows legacy, interfaccia IResultType
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType, proprietà PreceivedType
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873601"
---
# <a name="iresulttypepreceivedtype-property"></a><span data-ttu-id="00de1-106">IResultType::P proprietà receivedType</span><span class="sxs-lookup"><span data-stu-id="00de1-106">IResultType::PreceivedType property</span></span>

> [!NOTE]
> <span data-ttu-id="00de1-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="00de1-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="00de1-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="00de1-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="00de1-109">Questa proprietà contiene la stringa utilizzata per identificare il tipo nell'indice.</span><span class="sxs-lookup"><span data-stu-id="00de1-109">This property contains the string used to identify the type in the index.</span></span>

<span data-ttu-id="00de1-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="00de1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="00de1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00de1-111">Syntax</span></span>


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="00de1-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="00de1-112">Property value</span></span>

<span data-ttu-id="00de1-113">Restituisce l'indirizzo della stringa identifyint il tipo nell'indice.</span><span class="sxs-lookup"><span data-stu-id="00de1-113">returns the address of the string identifyint the type in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="00de1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00de1-114">Requirements</span></span>



| <span data-ttu-id="00de1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="00de1-115">Requirement</span></span> | <span data-ttu-id="00de1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="00de1-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="00de1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00de1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="00de1-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="00de1-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="00de1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00de1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="00de1-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="00de1-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="00de1-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="00de1-121">Redistributable</span></span><br/>          | <span data-ttu-id="00de1-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="00de1-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="00de1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00de1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="00de1-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="00de1-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





