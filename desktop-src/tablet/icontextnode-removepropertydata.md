---
description: Rimuove una parte di dati specifici dell'applicazione.
ms.assetid: 41077c2f-39e3-4069-ac05-97f1785e37b7
title: 'Metodo IContextNode:: RemovePropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.RemovePropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4c2fd5924b206ee296c066a908d2a59b02019f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526515"
---
# <a name="icontextnoderemovepropertydata-method"></a><span data-ttu-id="0e5fa-103">Metodo IContextNode:: RemovePropertyData</span><span class="sxs-lookup"><span data-stu-id="0e5fa-103">IContextNode::RemovePropertyData method</span></span>

<span data-ttu-id="0e5fa-104">Rimuove una parte di dati specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-104">Removes a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e5fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e5fa-105">Syntax</span></span>


```C++
HRESULT RemovePropertyData(
  [in] const GUID *pPropertyDataId
);
```



## <a name="parameters"></a><span data-ttu-id="0e5fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e5fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e5fa-107">*pPropertyDataId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e5fa-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e5fa-108">Identificatore dei dati da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-108">The identifier of the data to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e5fa-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e5fa-109">Return value</span></span>

<span data-ttu-id="0e5fa-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0e5fa-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e5fa-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e5fa-111">Remarks</span></span>

<span data-ttu-id="0e5fa-112">**E \_ INVALIDARG** viene restituito se il parametro *pPropertyDataId* è una delle costanti delle [proprietà del nodo di contesto](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="0e5fa-112">**E\_INVALIDARG** is returned if the *pPropertyDataId* parameter is one of the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e5fa-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e5fa-113">Requirements</span></span>



| <span data-ttu-id="0e5fa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e5fa-114">Requirement</span></span> | <span data-ttu-id="0e5fa-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0e5fa-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e5fa-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e5fa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0e5fa-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0e5fa-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0e5fa-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e5fa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0e5fa-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0e5fa-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0e5fa-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e5fa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e5fa-121"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0e5fa-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0e5fa-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0e5fa-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e5fa-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e5fa-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0e5fa-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e5fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e5fa-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="0e5fa-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="0e5fa-126">**IContextNode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0e5fa-126">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="0e5fa-127">**IContextNode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0e5fa-127">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="0e5fa-128">**IContextNode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0e5fa-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="0e5fa-129">**IContextNode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="0e5fa-129">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="0e5fa-130">**IContextNode:: LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="0e5fa-130">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="0e5fa-131">**IContextNode:: SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="0e5fa-131">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="0e5fa-132">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="0e5fa-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




