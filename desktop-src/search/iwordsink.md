---
description: Gestisce le parole identificate da interruzioni di parola durante il tempo di indicizzazione e di query.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Interfaccia IWordSink (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306094"
---
# <a name="iwordsink-interface"></a><span data-ttu-id="ed6e3-103">Interfaccia IWordSink</span><span class="sxs-lookup"><span data-stu-id="ed6e3-103">IWordSink interface</span></span>

<span data-ttu-id="ed6e3-104">Gestisce le parole identificate da interruzioni di parola durante il tempo di indicizzazione e di query.</span><span class="sxs-lookup"><span data-stu-id="ed6e3-104">Handles words identified by word breaks during both index time and query time.</span></span>

## <a name="members"></a><span data-ttu-id="ed6e3-105">Membri</span><span class="sxs-lookup"><span data-stu-id="ed6e3-105">Members</span></span>

<span data-ttu-id="ed6e3-106">L'interfaccia **IWordSink** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ed6e3-106">The **IWordSink** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ed6e3-107">**IWordSink** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ed6e3-107">**IWordSink** also has these types of members:</span></span>

-   [<span data-ttu-id="ed6e3-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="ed6e3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ed6e3-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ed6e3-109">Methods</span></span>

<span data-ttu-id="ed6e3-110">L'interfaccia **IWordSink** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ed6e3-110">The **IWordSink** interface has these methods.</span></span>



| <span data-ttu-id="ed6e3-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="ed6e3-111">Method</span></span>                                             | <span data-ttu-id="ed6e3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed6e3-112">Description</span></span>                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed6e3-113">**EndAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="ed6e3-113">**EndAltPhrase**</span></span>](iwordsink-endaltphrase.md)     | <span data-ttu-id="ed6e3-114">Indica la fine della frase finale in una sequenza di frasi alternative generate da un Word breaker in fase di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="ed6e3-114">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/>  |
| [<span data-ttu-id="ed6e3-115">**PutAltWord**</span><span class="sxs-lookup"><span data-stu-id="ed6e3-115">**PutAltWord**</span></span>](iwordsink-putaltword.md)         | <span data-ttu-id="ed6e3-116">Inserisce una parola alternativa e la relativa posizione nell'oggetto **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="ed6e3-116">Puts an alternative word and its position in the **IWordSink** object.</span></span><br/>                                                       |
| [<span data-ttu-id="ed6e3-117">**PutBreak**</span><span class="sxs-lookup"><span data-stu-id="ed6e3-117">**PutBreak**</span></span>](iwordsink-putbreak.md)             | <span data-ttu-id="ed6e3-118">Inserisce un'interruzioni dopo la parola precedente.</span><span class="sxs-lookup"><span data-stu-id="ed6e3-118">Puts a break after the preceding word.</span></span><br/>                                                                                       |
| [<span data-ttu-id="ed6e3-119">**PutWord**</span><span class="sxs-lookup"><span data-stu-id="ed6e3-119">**PutWord**</span></span>](iwordsink-putword.md)               | <span data-ttu-id="ed6e3-120">Inserisce una parola e la relativa posizione nell'oggetto **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="ed6e3-120">Puts a word and its position in the **IWordSink** object.</span></span><br/>                                                                    |
| [<span data-ttu-id="ed6e3-121">**StartAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="ed6e3-121">**StartAltPhrase**</span></span>](iwordsink-startaltphrase.md) | <span data-ttu-id="ed6e3-122">Indica il limite tra le frasi in una sequenza di frasi alternative generate da un Word breaker durante l'esecuzione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="ed6e3-122">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed6e3-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed6e3-123">Remarks</span></span>

<span data-ttu-id="ed6e3-124">Windows Search crea e inizializza le istanze dell'oggetto **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="ed6e3-124">Windows Search creates and initializes instances of the **IWordSink** object.</span></span> <span data-ttu-id="ed6e3-125">L'oggetto **IWordSink** riceve il parametro *fQuery* durante l'inizializzazione e usa questo parametro per determinare il contesto di suddivisione delle parole in cui viene usato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ed6e3-125">The **IWordSink** object receives the *fQuery* parameter during initialization and uses this parameter to determine the word-breaking context in which the object is used.</span></span>

<span data-ttu-id="ed6e3-126">Le implementazioni [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) ricevono un puntatore all'oggetto **IWordSink** nel metodo [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .</span><span class="sxs-lookup"><span data-stu-id="ed6e3-126">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations receive a pointer to the **IWordSink** object in the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed6e3-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed6e3-127">Requirements</span></span>



| <span data-ttu-id="ed6e3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed6e3-128">Requirement</span></span> | <span data-ttu-id="ed6e3-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ed6e3-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed6e3-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed6e3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed6e3-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed6e3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ed6e3-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed6e3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed6e3-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ed6e3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ed6e3-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed6e3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed6e3-135"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed6e3-135"><dt>Search.h</dt></span></span> </dl> |



 

 
