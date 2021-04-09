---
description: Recupera una matrice di intervalli di caratteri che rappresenta gli intervalli di caratteri Unicode supportati.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'Metodo IInkAnalysisRecognizer:: GetUnicodeRanges (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879350"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a><span data-ttu-id="a3f4d-103">Metodo IInkAnalysisRecognizer:: GetUnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="a3f4d-103">IInkAnalysisRecognizer::GetUnicodeRanges method</span></span>

<span data-ttu-id="a3f4d-104">Recupera una matrice di intervalli di caratteri che rappresenta gli intervalli di caratteri Unicode supportati.</span><span class="sxs-lookup"><span data-stu-id="a3f4d-104">Retrieves an array of character ranges representing the supported Unicode character ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f4d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3f4d-105">Syntax</span></span>


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a><span data-ttu-id="a3f4d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3f4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f4d-107">*pulNumberOfRanges* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a3f4d-107">*pulNumberOfRanges* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f4d-108">Numero di intervalli di caratteri a cui punta *ppulLowUnicode*.</span><span class="sxs-lookup"><span data-stu-id="a3f4d-108">The number of character ranges pointed to by *ppulLowUnicode*.</span></span>

</dd> <dt>

<span data-ttu-id="a3f4d-109">*ppulLowUnicode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3f4d-109">*ppulLowUnicode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f4d-110">Puntatore a una matrice di intervalli di caratteri che rappresenta gli intervalli di caratteri Unicode supportati.</span><span class="sxs-lookup"><span data-stu-id="a3f4d-110">Pointer to an array of character ranges representing the supported Unicode character ranges.</span></span>

</dd> <dt>

<span data-ttu-id="a3f4d-111">*ppusUnicodeRangeLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3f4d-111">*ppusUnicodeRangeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f4d-112">Puntatore a una matrice di valori che indica la lunghezza di ogni matrice puntata da *ppulLowUnicode*.</span><span class="sxs-lookup"><span data-stu-id="a3f4d-112">Pointer to an array of values indicating the length of each array point to by *ppulLowUnicode*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f4d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3f4d-113">Return value</span></span>

<span data-ttu-id="a3f4d-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a3f4d-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f4d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3f4d-115">Requirements</span></span>



| <span data-ttu-id="a3f4d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f4d-116">Requirement</span></span> | <span data-ttu-id="a3f4d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a3f4d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f4d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3f4d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f4d-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a3f4d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a3f4d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3f4d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f4d-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a3f4d-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a3f4d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3f4d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3f4d-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a3f4d-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a3f4d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a3f4d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3f4d-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3f4d-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a3f4d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3f4d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f4d-127">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="a3f4d-127">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




