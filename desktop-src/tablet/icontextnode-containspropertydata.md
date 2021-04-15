---
description: Determina se l'oggetto IContextNode contiene dati archiviati con l'identificatore specificato.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'Metodo IContextNode:: ContainsPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485116"
---
# <a name="icontextnodecontainspropertydata-method"></a><span data-ttu-id="a7d07-103">Metodo IContextNode:: ContainsPropertyData</span><span class="sxs-lookup"><span data-stu-id="a7d07-103">IContextNode::ContainsPropertyData method</span></span>

<span data-ttu-id="a7d07-104">Determina se l'oggetto [**IContextNode**](icontextnode.md) contiene dati archiviati con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="a7d07-104">Determines whether the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d07-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7d07-105">Syntax</span></span>


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a><span data-ttu-id="a7d07-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7d07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d07-107">*pPropertyDataId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7d07-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d07-108">Identificatore per i dati.</span><span class="sxs-lookup"><span data-stu-id="a7d07-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="a7d07-109">*pbContains* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a7d07-109">*pbContains* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d07-110">**Variante \_ TRUE** se l'oggetto [**IContextNode**](icontextnode.md) contiene dati archiviati con l'identificatore specificato. in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a7d07-110">**VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d07-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7d07-111">Return value</span></span>

<span data-ttu-id="a7d07-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a7d07-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7d07-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7d07-113">Remarks</span></span>

<span data-ttu-id="a7d07-114">Oltre ai dati specifici dell'applicazione, è anche possibile usare questo metodo per determinare se questo [**IContextNode**](icontextnode.md) contiene altri dati interni (vedere [proprietà hint di analisi](analysis-hint-properties.md) e [proprietà del nodo di contesto](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="a7d07-114">In addition to application-specific data, you can also use this method to determine whether this [**IContextNode**](icontextnode.md) contains other internal data (see [Analysis Hint Properties](analysis-hint-properties.md) and [Context Node Properties](context-node-properties.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d07-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7d07-115">Requirements</span></span>



| <span data-ttu-id="a7d07-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d07-116">Requirement</span></span> | <span data-ttu-id="a7d07-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a7d07-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d07-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7d07-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d07-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a7d07-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a7d07-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7d07-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d07-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a7d07-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a7d07-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7d07-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7d07-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d07-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a7d07-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a7d07-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7d07-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7d07-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a7d07-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7d07-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d07-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="a7d07-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a7d07-128">**IContextNode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a7d07-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="a7d07-129">**IContextNode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a7d07-129">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="a7d07-130">**IContextNode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="a7d07-130">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="a7d07-131">**IContextNode:: LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="a7d07-131">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="a7d07-132">**IContextNode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="a7d07-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="a7d07-133">**IContextNode:: SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="a7d07-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="a7d07-134">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="a7d07-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




