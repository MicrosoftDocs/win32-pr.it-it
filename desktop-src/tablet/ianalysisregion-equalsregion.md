---
description: Determina se il IAnalysisRegion specificato contiene lo stesso valore dell'oggetto IAnalysisRegion corrente.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'Metodo IAnalysisRegion:: EqualsRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129523"
---
# <a name="ianalysisregionequalsregion-method"></a><span data-ttu-id="35820-103">Metodo IAnalysisRegion:: EqualsRegion</span><span class="sxs-lookup"><span data-stu-id="35820-103">IAnalysisRegion::EqualsRegion method</span></span>

<span data-ttu-id="35820-104">Determina se il [**IAnalysisRegion**](ianalysisregion.md) specificato contiene lo stesso valore dell'oggetto **IAnalysisRegion** corrente.</span><span class="sxs-lookup"><span data-stu-id="35820-104">Determines whether the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current **IAnalysisRegion** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="35820-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35820-105">Syntax</span></span>


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a><span data-ttu-id="35820-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35820-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35820-107">*pOtherRegion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35820-107">*pOtherRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35820-108">Oggetto [**IAnalysisRegion**](ianalysisregion.md) da confrontare con il **IAnalysisRegion** corrente.</span><span class="sxs-lookup"><span data-stu-id="35820-108">The [**IAnalysisRegion**](ianalysisregion.md) object to compare with the current **IAnalysisRegion**.</span></span>

</dd> <dt>

<span data-ttu-id="35820-109">*pfRegionsEqual* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35820-109">*pfRegionsEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35820-110">**Variante \_ TRUE** se l'oggetto [**IAnalysisRegion**](ianalysisregion.md) specificato contiene lo stesso valore dell'oggetto IAnalysisRegion corrente. in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="35820-110">**VARIANT\_TRUE** if the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current IAnalysisRegion; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35820-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35820-111">Return value</span></span>

<span data-ttu-id="35820-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="35820-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35820-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35820-113">Requirements</span></span>



| <span data-ttu-id="35820-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="35820-114">Requirement</span></span> | <span data-ttu-id="35820-115">Valore</span><span class="sxs-lookup"><span data-stu-id="35820-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35820-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35820-116">Minimum supported client</span></span><br/> | <span data-ttu-id="35820-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="35820-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="35820-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35820-118">Minimum supported server</span></span><br/> | <span data-ttu-id="35820-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="35820-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="35820-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35820-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="35820-121"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="35820-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="35820-122">DLL</span><span class="sxs-lookup"><span data-stu-id="35820-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35820-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35820-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="35820-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35820-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35820-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="35820-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> </dl>

 

 




