---
description: Recupera una raccolta di oggetti IContextNode che sono rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'Metodo IInkAnalyzer:: GetNodesFromTextRange (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751810"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a><span data-ttu-id="52443-103">Metodo IInkAnalyzer:: GetNodesFromTextRange</span><span class="sxs-lookup"><span data-stu-id="52443-103">IInkAnalyzer::GetNodesFromTextRange method</span></span>

<span data-ttu-id="52443-104">Recupera una raccolta di oggetti [**IContextNode**](icontextnode.md) che sono rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.</span><span class="sxs-lookup"><span data-stu-id="52443-104">Retrieves a collection of [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="52443-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52443-105">Syntax</span></span>


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a><span data-ttu-id="52443-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52443-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52443-107">*plStart* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="52443-107">*plStart* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52443-108">Un riferimento all'inizio dell'intervallo di testo nella parte *pNodesToSearch* della stringa riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="52443-108">A reference to the start of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="52443-109">*plLength* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="52443-109">*plLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52443-110">Riferimento alla lunghezza dell'intervallo di testo nella parte *pNodesToSearch* della stringa riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="52443-110">A reference to the length of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="52443-111">*ppContextNodes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52443-111">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52443-112">Puntatore agli oggetti [**IContextNode**](icontextnode.md) rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.</span><span class="sxs-lookup"><span data-stu-id="52443-112">A pointer to the [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

</dd> <dt>

<span data-ttu-id="52443-113">*pNodesToSearch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52443-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52443-114">Oggetti [**IContextNode**](icontextnode.md) a cui limitare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="52443-114">The [**IContextNode**](icontextnode.md) objects to which to limit the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52443-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52443-115">Return value</span></span>

<span data-ttu-id="52443-116">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="52443-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52443-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="52443-117">Remarks</span></span>

<span data-ttu-id="52443-118">L'intervallo di testo specificato deve essere relativo alla parte *pNodesToSearch* della stringa riconosciuta di [**IInkAnalyzer**](iinkanalyzer.md), anziché alla stringa riconosciuta dell'intero **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="52443-118">The specified text range should be relative to the *pNodesToSearch* portion of the recognized string of the [**IInkAnalyzer**](iinkanalyzer.md), rather than to the recognized string of the entire **IInkAnalyzer**.</span></span>

<span data-ttu-id="52443-119">Questo metodo consente di modificare i valori dei parametri *plStart* e *plLength* espandendo l'intervallo di testo ai limiti di parola più vicini.</span><span class="sxs-lookup"><span data-stu-id="52443-119">This method modifies the values of the *plStart* and *plLength* parameters by expanding the text range to the nearest word boundaries.</span></span>

<span data-ttu-id="52443-120">Se, ad esempio, la stringa riconosciuta è "sono tardi" e si chiama questo metodo usando i valori di parametro 6 per *plStart* e 1 per *plLength*, che corrisponde alla lettera "a" in "late", questo metodo restituisce una raccolta che contiene un singolo [**IContextNode**](icontextnode.md), InkWord o TextWord che corrisponde alla parola "tardiva".</span><span class="sxs-lookup"><span data-stu-id="52443-120">For example, if the recognized string is "I am late" and you call this method using the parameter values of 6 for *plStart* and 1 for *plLength*, which corresponds to the letter "a" in "late", this method returns a collection containing a single [**IContextNode**](icontextnode.md), the InkWord or TextWord that corresponds to the word "late".</span></span> <span data-ttu-id="52443-121">Per questo esempio, questo metodo modifica anche il valore di *plStart* in 5 e il valore di *plLength* su 4, che corrisponde alla parola "tardiva".</span><span class="sxs-lookup"><span data-stu-id="52443-121">For this example, this method also modifies the value of *plStart* to 5 and the value of *plLength* to 4, which corresponds to the word "late".</span></span>

> [!Note]  
> <span data-ttu-id="52443-122">Il parametro *plStart* è relativo alla stringa riconosciuta del parametro *pNodesToSearch* .</span><span class="sxs-lookup"><span data-stu-id="52443-122">The *plStart* parameter is relative to the recognized string of the *pNodesToSearch* parameter.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52443-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52443-123">Requirements</span></span>



| <span data-ttu-id="52443-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="52443-124">Requirement</span></span> | <span data-ttu-id="52443-125">Valore</span><span class="sxs-lookup"><span data-stu-id="52443-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52443-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52443-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52443-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="52443-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="52443-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52443-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52443-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="52443-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="52443-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52443-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="52443-131"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="52443-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="52443-132">DLL</span><span class="sxs-lookup"><span data-stu-id="52443-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52443-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52443-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="52443-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52443-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52443-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="52443-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




