---
description: Indica il limite tra le frasi in una sequenza di frasi alternative generate da un Word breaker durante l'esecuzione dell'indice.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'Metodo IWordSink:: StartAltPhrase (search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225941"
---
# <a name="iwordsinkstartaltphrase-method"></a><span data-ttu-id="7188b-103">Metodo IWordSink:: StartAltPhrase</span><span class="sxs-lookup"><span data-stu-id="7188b-103">IWordSink::StartAltPhrase method</span></span>

<span data-ttu-id="7188b-104">Indica il limite tra le frasi in una sequenza di frasi alternative generate da un Word breaker durante l'esecuzione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="7188b-104">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7188b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7188b-105">Syntax</span></span>


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="7188b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7188b-106">Parameters</span></span>

<span data-ttu-id="7188b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7188b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7188b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7188b-108">Return value</span></span>

<span data-ttu-id="7188b-109">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7188b-109">This method can return one of these values.</span></span>



| <span data-ttu-id="7188b-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7188b-110">Return code</span></span>                                                                                           | <span data-ttu-id="7188b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7188b-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7188b-112"><dt>**\_ \_ solo query WBREAK \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="7188b-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="7188b-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) viene chiamato durante la fase di query.</span><span class="sxs-lookup"><span data-stu-id="7188b-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7188b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7188b-114">Remarks</span></span>

<span data-ttu-id="7188b-115">Ogni frase alternativa inizia con una chiamata **StartAltPhrase** .</span><span class="sxs-lookup"><span data-stu-id="7188b-115">Each alternative phrase starts with a **StartAltPhrase** call.</span></span> <span data-ttu-id="7188b-116">La frase viene inserita nell'oggetto [**IWordSink**](iwordsink.md) tramite chiamate successive al metodo [**IWordSink::P utword**](iwordsink-putword.md) o [**IWordSink::P utaltword**](iwordsink-putaltword.md) .</span><span class="sxs-lookup"><span data-stu-id="7188b-116">The phrase is put in the [**IWordSink**](iwordsink.md) object through subsequent calls to the [**IWordSink::PutWord**](iwordsink-putword.md) or [**IWordSink::PutAltWord**](iwordsink-putaltword.md) method.</span></span> <span data-ttu-id="7188b-117">La frase alternativa finale in una sequenza di frasi viene terminata con una chiamata al metodo [**IWordSink:: EndAltPhrase**](iwordsink-endaltphrase.md) .</span><span class="sxs-lookup"><span data-stu-id="7188b-117">The final alternative phrase in a sequence of phrases is terminated with a call to the [**IWordSink::EndAltPhrase**](iwordsink-endaltphrase.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7188b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7188b-118">Requirements</span></span>



| <span data-ttu-id="7188b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7188b-119">Requirement</span></span> | <span data-ttu-id="7188b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7188b-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7188b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7188b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7188b-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7188b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7188b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7188b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7188b-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7188b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7188b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7188b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7188b-126"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="7188b-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7188b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7188b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7188b-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="7188b-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 




