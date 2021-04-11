---
description: Recupera il tipo del tratto specificato.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'Metodo IInkAnalyzer:: GetStrokeType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226153"
---
# <a name="iinkanalyzergetstroketype-method"></a><span data-ttu-id="a3f25-103">Metodo IInkAnalyzer:: GetStrokeType</span><span class="sxs-lookup"><span data-stu-id="a3f25-103">IInkAnalyzer::GetStrokeType method</span></span>

<span data-ttu-id="a3f25-104">Recupera il tipo del tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="a3f25-104">Retrieves the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f25-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3f25-105">Syntax</span></span>


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="a3f25-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3f25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f25-107">*lStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3f25-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f25-108">Identificatore del tratto.</span><span class="sxs-lookup"><span data-stu-id="a3f25-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a3f25-109">*pStrokeType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3f25-109">*pStrokeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f25-110">Classificazione del tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="a3f25-110">The classification of the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f25-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3f25-111">Return value</span></span>

<span data-ttu-id="a3f25-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a3f25-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f25-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3f25-113">Remarks</span></span>

<span data-ttu-id="a3f25-114">Se il tipo del tratto è il valore [**StrokeType**](stroketype.md) StrokeType \_ unclassifiedd, [**IInkAnalyzer**](iinkanalyzer.md) classifica il tratto durante l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="a3f25-114">If the stroke's type is the [**StrokeType**](stroketype.md) value StrokeType\_Unclassified, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="a3f25-115">In caso contrario, **IInkAnalyzer** usa il tipo impostato sul tratto.</span><span class="sxs-lookup"><span data-stu-id="a3f25-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="a3f25-116">[**IInkAnalyzer**](iinkanalyzer.md) non imposta il valore del tipo di tratto come parte dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="a3f25-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="a3f25-117">Per specificare o modificare il tipo di tratto, usare il metodo [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="a3f25-117">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f25-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3f25-118">Requirements</span></span>



| <span data-ttu-id="a3f25-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f25-119">Requirement</span></span> | <span data-ttu-id="a3f25-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a3f25-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f25-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3f25-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f25-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a3f25-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a3f25-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3f25-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f25-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a3f25-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a3f25-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3f25-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3f25-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a3f25-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a3f25-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a3f25-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3f25-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3f25-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a3f25-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3f25-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f25-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a3f25-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a3f25-131">**Metodo IInkAnalyzer:: SetStrokeType**</span><span class="sxs-lookup"><span data-stu-id="a3f25-131">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="a3f25-132">**Metodo IInkAnalyzer:: SetStrokesType**</span><span class="sxs-lookup"><span data-stu-id="a3f25-132">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="a3f25-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="a3f25-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




