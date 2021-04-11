---
description: Indica la fine della frase finale in una sequenza di frasi alternative generate da un Word breaker in fase di indicizzazione.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'Metodo IWordSink:: EndAltPhrase (search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225942"
---
# <a name="iwordsinkendaltphrase-method"></a><span data-ttu-id="6d842-103">Metodo IWordSink:: EndAltPhrase</span><span class="sxs-lookup"><span data-stu-id="6d842-103">IWordSink::EndAltPhrase method</span></span>

<span data-ttu-id="6d842-104">Indica la fine della frase finale in una sequenza di frasi alternative generate da un Word breaker in fase di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="6d842-104">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d842-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d842-105">Syntax</span></span>


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="6d842-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d842-106">Parameters</span></span>

<span data-ttu-id="6d842-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6d842-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d842-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d842-108">Return value</span></span>

<span data-ttu-id="6d842-109">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="6d842-109">This method can return one of these values.</span></span>



| <span data-ttu-id="6d842-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6d842-110">Return code</span></span>                                                                                           | <span data-ttu-id="6d842-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d842-111">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d842-112"><dt>**\_ \_ solo query WBREAK \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="6d842-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="6d842-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) viene chiamato durante la fase di query.</span><span class="sxs-lookup"><span data-stu-id="6d842-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d842-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d842-114">Remarks</span></span>

<span data-ttu-id="6d842-115">Le implementazioni [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) chiamano **IWordSink:: EndAltPhrase** dal metodo [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) per terminare una sequenza di frasi alternative.</span><span class="sxs-lookup"><span data-stu-id="6d842-115">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations call **IWordSink::EndAltPhrase** from the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method to terminate a sequence of alternative phrases.</span></span> <span data-ttu-id="6d842-116">Il metodo [**IWordSink:: StartAltPhrase**](iwordsink-startaltphrase.md) viene chiamato per indicare la fine di una frase e l'inizio di un altro oggetto in una sequenza di frasi.</span><span class="sxs-lookup"><span data-stu-id="6d842-116">The [**IWordSink::StartAltPhrase**](iwordsink-startaltphrase.md) method is called to indicate the end of one phrase and the beginning of another in a sequence of phrases.</span></span> <span data-ttu-id="6d842-117">Solo l'ultima frase in una sequenza viene terminata con una chiamata a **EndAltPhrase**.</span><span class="sxs-lookup"><span data-stu-id="6d842-117">Only the last phrase in a sequence is terminated with a call to **EndAltPhrase**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d842-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d842-118">Requirements</span></span>



| <span data-ttu-id="6d842-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d842-119">Requirement</span></span> | <span data-ttu-id="6d842-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6d842-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6d842-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d842-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6d842-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6d842-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6d842-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d842-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6d842-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6d842-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6d842-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d842-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d842-126"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d842-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d842-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d842-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d842-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="6d842-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
