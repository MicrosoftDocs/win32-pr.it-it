---
description: Restituisce l'identificatore delle impostazioni locali del tratto specificato.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'Metodo IInkAnalyzer:: GetStrokeLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751802"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a><span data-ttu-id="7321c-103">Metodo IInkAnalyzer:: GetStrokeLanguageId</span><span class="sxs-lookup"><span data-stu-id="7321c-103">IInkAnalyzer::GetStrokeLanguageId method</span></span>

<span data-ttu-id="7321c-104">Restituisce l'identificatore delle impostazioni locali del tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="7321c-104">Returns the locale identifier of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="7321c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7321c-105">Syntax</span></span>


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="7321c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7321c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7321c-107">*lStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7321c-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7321c-108">Identificatore del tratto.</span><span class="sxs-lookup"><span data-stu-id="7321c-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7321c-109">*lStrokeLCID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7321c-109">*lStrokeLCID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7321c-110">Identificatore delle impostazioni locali per il tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="7321c-110">The locale identifier for the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7321c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7321c-111">Return value</span></span>

<span data-ttu-id="7321c-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7321c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7321c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7321c-113">Remarks</span></span>

<span data-ttu-id="7321c-114">Le impostazioni locali del tratto vengono impostate quando si aggiunge il tratto chiamando il metodo [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), [**IInkAnalyzer:: AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes Method**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="7321c-114">The stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="7321c-115">Per modificare le impostazioni locali del tratto, usare il metodo [**IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) o [**IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="7321c-115">To change the stroke's locale, use [**IInkAnalyzer::SetStrokeLanguageId Method**](iinkanalyzer-setstrokelanguageid.md) or [**IInkAnalyzer::SetStrokesLanguageId Method**](iinkanalyzer-setstrokeslanguageid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7321c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7321c-116">Requirements</span></span>



| <span data-ttu-id="7321c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7321c-117">Requirement</span></span> | <span data-ttu-id="7321c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7321c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7321c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7321c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7321c-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7321c-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7321c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7321c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7321c-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7321c-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7321c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7321c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7321c-124"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7321c-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7321c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7321c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7321c-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7321c-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7321c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7321c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7321c-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="7321c-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7321c-129">**Metodo IInkAnalyzer:: SetStrokeLanguageId**</span><span class="sxs-lookup"><span data-stu-id="7321c-129">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="7321c-130">**Metodo IInkAnalyzer:: SetStrokesLanguageId**</span><span class="sxs-lookup"><span data-stu-id="7321c-130">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="7321c-131">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="7321c-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




