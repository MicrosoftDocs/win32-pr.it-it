---
description: Recupera le funzionalità del riconoscimento.
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'Metodo IInkAnalysisRecognizer:: GetCapabilities (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129478"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a><span data-ttu-id="70c15-103">Metodo IInkAnalysisRecognizer:: GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="70c15-103">IInkAnalysisRecognizer::GetCapabilities method</span></span>

<span data-ttu-id="70c15-104">Recupera le funzionalità del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="70c15-104">Retrieves the capabilities of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="70c15-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70c15-105">Syntax</span></span>


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="70c15-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="70c15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70c15-107">*pCapabilities* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="70c15-107">*pCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70c15-108">Combinazione bit per bit dei valori [**RecognizerCapabilities**](recognizercapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="70c15-108">A bitwise combination of [**RecognizerCapabilities**](recognizercapabilities.md) values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70c15-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70c15-109">Return value</span></span>

<span data-ttu-id="70c15-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="70c15-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70c15-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="70c15-111">Remarks</span></span>

<span data-ttu-id="70c15-112">Questo valore è costante per ogni [ **IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span><span class="sxs-lookup"><span data-stu-id="70c15-112">This value is constant for each [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="70c15-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70c15-113">Requirements</span></span>



| <span data-ttu-id="70c15-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c15-114">Requirement</span></span> | <span data-ttu-id="70c15-115">Valore</span><span class="sxs-lookup"><span data-stu-id="70c15-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70c15-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70c15-116">Minimum supported client</span></span><br/> | <span data-ttu-id="70c15-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="70c15-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70c15-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70c15-118">Minimum supported server</span></span><br/> | <span data-ttu-id="70c15-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="70c15-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="70c15-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70c15-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c15-121"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="70c15-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="70c15-122">DLL</span><span class="sxs-lookup"><span data-stu-id="70c15-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70c15-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70c15-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="70c15-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70c15-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c15-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="70c15-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="70c15-126">**RecognizerCapabilities**</span><span class="sxs-lookup"><span data-stu-id="70c15-126">**RecognizerCapabilities**</span></span>](recognizercapabilities.md)
</dt> <dt>

[<span data-ttu-id="70c15-127">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="70c15-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




