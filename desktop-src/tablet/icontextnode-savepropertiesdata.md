---
description: Recupera una matrice di byte che contiene i dati della proprietà interna e specifici dell'applicazione per questo IContextNode.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'Metodo IContextNode:: SavePropertiesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966726"
---
# <a name="icontextnodesavepropertiesdata-method"></a><span data-ttu-id="6f1ac-103">Metodo IContextNode:: SavePropertiesData</span><span class="sxs-lookup"><span data-stu-id="6f1ac-103">IContextNode::SavePropertiesData method</span></span>

<span data-ttu-id="6f1ac-104">Recupera una matrice di byte che contiene i dati della proprietà interna e specifici dell'applicazione per questo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="6f1ac-104">Retrieves an array of bytes that contains the application-specific and internal property data for this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1ac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f1ac-105">Syntax</span></span>


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="6f1ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f1ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f1ac-107">*pulPropertiesDataSize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6f1ac-107">*pulPropertiesDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1ac-108">Dimensioni della matrice di dati contenente le informazioni sulla proprietà.</span><span class="sxs-lookup"><span data-stu-id="6f1ac-108">The size of the data array containing the property information.</span></span> <span data-ttu-id="6f1ac-109">Il valore passato non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="6f1ac-109">The value passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6f1ac-110">*ppbPropertiesData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6f1ac-110">*ppbPropertiesData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1ac-111">Puntatore a una matrice di Unsigned Integer a 8 bit che contiene i dati della proprietà interna e specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f1ac-111">A pointer to an 8-bit unsigned integer array that contains the application-specific and internal property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f1ac-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f1ac-112">Return value</span></span>

<span data-ttu-id="6f1ac-113">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6f1ac-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f1ac-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f1ac-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6f1ac-115">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppbPropertiesData* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="6f1ac-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertiesData* when you no longer need the information.</span></span>

 

<span data-ttu-id="6f1ac-116">Utilizzare questo metodo quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="6f1ac-116">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="6f1ac-117">Questo metodo salva i dati della proprietà impostati da **IInkAnalyzer** in [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="6f1ac-117">This method saves the property data that the **IInkAnalyzer** has set on the [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="6f1ac-118">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6f1ac-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f1ac-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f1ac-119">Requirements</span></span>



| <span data-ttu-id="6f1ac-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f1ac-120">Requirement</span></span> | <span data-ttu-id="6f1ac-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6f1ac-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1ac-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f1ac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6f1ac-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6f1ac-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6f1ac-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f1ac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6f1ac-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6f1ac-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6f1ac-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f1ac-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f1ac-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6f1ac-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6f1ac-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6f1ac-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f1ac-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f1ac-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6f1ac-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f1ac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f1ac-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="6f1ac-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6f1ac-132">**IContextNode:: LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="6f1ac-132">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="6f1ac-133">**IContextNode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6f1ac-133">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="6f1ac-134">**IContextNode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6f1ac-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="6f1ac-135">**IContextNode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="6f1ac-135">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="6f1ac-136">**IContextNode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="6f1ac-136">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="6f1ac-137">**IContextNode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6f1ac-137">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="6f1ac-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="6f1ac-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

