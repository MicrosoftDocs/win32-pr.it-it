---
description: Aggiunge un elemento di dati specifici dell'applicazione.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'Metodo IContextNode:: AddPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129507"
---
# <a name="icontextnodeaddpropertydata-method"></a><span data-ttu-id="dbef3-103">Metodo IContextNode:: AddPropertyData</span><span class="sxs-lookup"><span data-stu-id="dbef3-103">IContextNode::AddPropertyData method</span></span>

<span data-ttu-id="dbef3-104">Aggiunge un elemento di dati specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dbef3-104">Adds a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbef3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbef3-105">Syntax</span></span>


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="dbef3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbef3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbef3-107">*pPropertyDataId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbef3-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbef3-108">Identificatore univoco globale (GUID) utilizzato per identificare il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="dbef3-108">A globally unique identifier (GUID) that is used to identify the type of data.</span></span>

</dd> <dt>

<span data-ttu-id="dbef3-109">*ulPropertyDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbef3-109">*ulPropertyDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbef3-110">Dimensioni dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="dbef3-110">The size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dbef3-111">*pbPropertiesData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbef3-111">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbef3-112">\[in, Size \_ è (ulPropertyDataSize)\]</span><span class="sxs-lookup"><span data-stu-id="dbef3-112">\[in, size\_is(ulPropertyDataSize)\]</span></span>

<span data-ttu-id="dbef3-113">Matrice di Unsigned Integer a 8 bit contenente le informazioni sulle proprietà da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="dbef3-113">An 8-bit unsigned integer array containing the property information to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbef3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbef3-114">Return value</span></span>

<span data-ttu-id="dbef3-115">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dbef3-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dbef3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbef3-116">Remarks</span></span>

<span data-ttu-id="dbef3-117">Usare **IContextNode:: AddPropertyData** per associare i dati a un nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="dbef3-117">Use **IContextNode::AddPropertyData** to associate data with a context node.</span></span> <span data-ttu-id="dbef3-118">Per recuperare i dati in un secondo momento, utilizzare [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="dbef3-118">To retrieve the data later, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

<span data-ttu-id="dbef3-119">Ink Analyzer può eliminare il nodo come parte dell'analisi dell'input penna, a meno che il nodo di contesto non sia confermato (vedere [**IContextNode:: Confirm**](icontextnode-confirm.md)).</span><span class="sxs-lookup"><span data-stu-id="dbef3-119">The ink analyzer may delete the node as part of ink analysis, unless the context node is confirmed (see [**IContextNode::Confirm**](icontextnode-confirm.md)).</span></span> <span data-ttu-id="dbef3-120">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dbef3-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbef3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbef3-121">Requirements</span></span>



| <span data-ttu-id="dbef3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbef3-122">Requirement</span></span> | <span data-ttu-id="dbef3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="dbef3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbef3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbef3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dbef3-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dbef3-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dbef3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbef3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dbef3-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dbef3-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dbef3-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbef3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbef3-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dbef3-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dbef3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="dbef3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbef3-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbef3-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dbef3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbef3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbef3-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="dbef3-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="dbef3-134">**IContextNode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="dbef3-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="dbef3-135">**IContextNode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="dbef3-135">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="dbef3-136">**IContextNode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="dbef3-136">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="dbef3-137">**IContextNode:: LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="dbef3-137">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="dbef3-138">**IContextNode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="dbef3-138">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="dbef3-139">**IContextNode:: SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="dbef3-139">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




