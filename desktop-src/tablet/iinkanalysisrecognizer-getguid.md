---
description: Recupera l'identificatore univoco globale (GUID) del riconoscimento.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: 'Metodo IInkAnalysisRecognizer:: GetGuid (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879354"
---
# <a name="iinkanalysisrecognizergetguid-method"></a><span data-ttu-id="c9ace-103">Metodo IInkAnalysisRecognizer:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="c9ace-103">IInkAnalysisRecognizer::GetGuid method</span></span>

<span data-ttu-id="c9ace-104">Recupera l'identificatore univoco globale (GUID) del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="c9ace-104">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ace-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9ace-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="c9ace-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9ace-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ace-107">*PID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c9ace-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ace-108">GUID che identifica questo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="c9ace-108">The GUID that identifies this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ace-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9ace-109">Return value</span></span>

<span data-ttu-id="c9ace-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c9ace-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ace-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9ace-111">Requirements</span></span>



| <span data-ttu-id="c9ace-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9ace-112">Requirement</span></span> | <span data-ttu-id="c9ace-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c9ace-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ace-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9ace-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c9ace-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c9ace-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c9ace-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9ace-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c9ace-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c9ace-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c9ace-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9ace-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9ace-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c9ace-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c9ace-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c9ace-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9ace-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9ace-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c9ace-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9ace-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ace-123">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="c9ace-123">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="c9ace-124">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="c9ace-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




