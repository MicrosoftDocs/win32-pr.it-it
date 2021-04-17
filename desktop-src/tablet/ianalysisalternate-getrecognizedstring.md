---
description: Ottiene il valore stringa riconosciuto dell'oggetto IAnalysisAlternate.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'Metodo IAnalysisAlternate:: GetRecognizedString (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526569"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a><span data-ttu-id="539dd-103">Metodo IAnalysisAlternate:: GetRecognizedString</span><span class="sxs-lookup"><span data-stu-id="539dd-103">IAnalysisAlternate::GetRecognizedString method</span></span>

<span data-ttu-id="539dd-104">Ottiene il valore stringa riconosciuto dell'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) .</span><span class="sxs-lookup"><span data-stu-id="539dd-104">Gets the recognized string value of the [**IAnalysisAlternate**](ianalysisalternate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="539dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="539dd-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="539dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="539dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="539dd-107">*pbstrRecognizedString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="539dd-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="539dd-108">Puntatore a **BSTR** impostato sul valore stringa riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="539dd-108">A pointer to the **BSTR** that is set to the recognized string value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="539dd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="539dd-109">Return value</span></span>

<span data-ttu-id="539dd-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="539dd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="539dd-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="539dd-111">Requirements</span></span>



| <span data-ttu-id="539dd-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="539dd-112">Requirement</span></span> | <span data-ttu-id="539dd-113">Valore</span><span class="sxs-lookup"><span data-stu-id="539dd-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="539dd-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="539dd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="539dd-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="539dd-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="539dd-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="539dd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="539dd-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="539dd-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="539dd-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="539dd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="539dd-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="539dd-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="539dd-120">DLL</span><span class="sxs-lookup"><span data-stu-id="539dd-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="539dd-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="539dd-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="539dd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="539dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="539dd-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="539dd-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="539dd-124">**Metodo IInkAnalyzer:: GetRecognizedString**</span><span class="sxs-lookup"><span data-stu-id="539dd-124">**IInkAnalyzer::GetRecognizedString Method**</span></span>](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




