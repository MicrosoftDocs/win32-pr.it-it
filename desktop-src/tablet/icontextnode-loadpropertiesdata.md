---
description: "Ricrea i dati delle proprietà specifiche dell'applicazione e interni per una matrice di byte creata in precedenza con IContextNode:: SavePropertiesData."
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'Metodo IContextNode:: LoadPropertiesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307422"
---
# <a name="icontextnodeloadpropertiesdata-method"></a><span data-ttu-id="4ab82-103">Metodo IContextNode:: LoadPropertiesData</span><span class="sxs-lookup"><span data-stu-id="4ab82-103">IContextNode::LoadPropertiesData method</span></span>

<span data-ttu-id="4ab82-104">Ricrea i dati delle proprietà specifiche dell'applicazione e interni per una matrice di byte creata in precedenza con [**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md).</span><span class="sxs-lookup"><span data-stu-id="4ab82-104">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ab82-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ab82-105">Syntax</span></span>


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="4ab82-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ab82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ab82-107">*cbPropertiesDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ab82-107">*cbPropertiesDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ab82-108">Dimensioni della matrice di dati delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="4ab82-108">The size of the properties data array.</span></span>

</dd> <dt>

<span data-ttu-id="4ab82-109">*pbPropertiesData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ab82-109">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ab82-110">Matrice Unsigned Integer a 8 bit contenente le informazioni sulle proprietà da caricare.</span><span class="sxs-lookup"><span data-stu-id="4ab82-110">The 8-bit unsigned integer array containing property information to load.</span></span>

</dd> <dt>

<span data-ttu-id="4ab82-111">*pfSuccessful* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4ab82-111">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ab82-112">**Variante \_ TRUE** se i dati della proprietà sono stati caricati correttamente; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="4ab82-112">**VARIANT\_TRUE** if the property data loaded successfully; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ab82-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ab82-113">Return value</span></span>

<span data-ttu-id="4ab82-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4ab82-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ab82-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ab82-115">Requirements</span></span>



| <span data-ttu-id="4ab82-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ab82-116">Requirement</span></span> | <span data-ttu-id="4ab82-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab82-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab82-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ab82-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4ab82-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4ab82-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ab82-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ab82-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4ab82-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4ab82-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4ab82-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ab82-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ab82-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4ab82-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4ab82-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4ab82-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ab82-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ab82-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4ab82-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ab82-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ab82-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="4ab82-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4ab82-128">**IContextNode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="4ab82-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="4ab82-129">**IContextNode:: ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="4ab82-129">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="4ab82-130">**IContextNode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="4ab82-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="4ab82-131">**IContextNode:: GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="4ab82-131">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="4ab82-132">**IContextNode:: RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="4ab82-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="4ab82-133">**IContextNode:: SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="4ab82-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="4ab82-134">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="4ab82-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




