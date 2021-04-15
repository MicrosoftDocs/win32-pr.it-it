---
description: Recupera l'oggetto IInkAnalysisRecognizer in corrispondenza dell'indice specificato.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'Metodo IInkAnalysisRecognizers:: GetInkAnalysisRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485092"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a><span data-ttu-id="f5696-103">Metodo IInkAnalysisRecognizers:: GetInkAnalysisRecognizer</span><span class="sxs-lookup"><span data-stu-id="f5696-103">IInkAnalysisRecognizers::GetInkAnalysisRecognizer method</span></span>

<span data-ttu-id="f5696-104">Recupera l'oggetto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="f5696-104">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5696-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5696-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="f5696-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5696-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5696-107">*ulIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5696-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5696-108">Indice in base zero dell'oggetto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f5696-108">The zero-based index of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="f5696-109">*ppInkAnalysisRecognizer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f5696-109">*ppInkAnalysisRecognizer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5696-110">Puntatore a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="f5696-110">A pointer to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5696-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5696-111">Return value</span></span>

<span data-ttu-id="f5696-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f5696-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5696-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5696-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f5696-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppInkAnalysisRecognizer* quando non è più necessario usare il sistema di riconoscimento dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="f5696-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppInkAnalysisRecognizer* when you no longer need to use the ink analysis recognizer.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5696-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5696-115">Requirements</span></span>



| <span data-ttu-id="f5696-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5696-116">Requirement</span></span> | <span data-ttu-id="f5696-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f5696-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5696-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5696-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5696-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f5696-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f5696-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5696-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5696-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f5696-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f5696-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5696-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5696-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f5696-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f5696-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f5696-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5696-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5696-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f5696-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5696-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5696-127">**InkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="f5696-127">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="f5696-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="f5696-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

