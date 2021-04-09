---
description: Recupera una descrizione indipendente dal computer di un'eccezione e le informazioni sullo stato del computer esistente per il thread quando si verifica l'eccezione. Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro di un gestore di eccezioni.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation (macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748890"
---
# <a name="getexceptioninformation-macro"></a><span data-ttu-id="91af0-104">GetExceptionInformation (macro)</span><span class="sxs-lookup"><span data-stu-id="91af0-104">GetExceptionInformation macro</span></span>

<span data-ttu-id="91af0-105">Recupera una descrizione indipendente dal computer di un'eccezione e le informazioni sullo stato del computer esistente per il thread quando si verifica l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="91af0-105">Retrieves a computer-independent description of an exception, and information about the computer state that exists for the thread when the exception occurs.</span></span> <span data-ttu-id="91af0-106">Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro di un gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="91af0-106">This function can be called only from within the filter expression of an exception handler.</span></span>

> [!Note]  
> <span data-ttu-id="91af0-107">Il compilatore di ottimizzazione di Microsoft C/C++ interpreta questa funzione come una parola chiave e il suo utilizzo al di fuori della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore.</span><span class="sxs-lookup"><span data-stu-id="91af0-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="91af0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91af0-108">Syntax</span></span>


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a><span data-ttu-id="91af0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="91af0-109">Parameters</span></span>

<span data-ttu-id="91af0-110">Questa macro non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="91af0-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91af0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91af0-111">Return value</span></span>

<span data-ttu-id="91af0-112">Puntatore a una struttura [**di \_ puntatori di eccezione**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) che contiene puntatori alle due strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="91af0-112">A pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure that contains pointers to the following two structures:</span></span>

-   <span data-ttu-id="91af0-113">[**Eccezione \_ di**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Struttura di record che contiene una descrizione dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="91af0-113">[**EXCEPTION\_RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record) structure that contains a description of the exception.</span></span>
-   <span data-ttu-id="91af0-114">Struttura del [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) che contiene le informazioni sullo stato del computer.</span><span class="sxs-lookup"><span data-stu-id="91af0-114">[**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure that contains the computer state information.</span></span>

## <a name="remarks"></a><span data-ttu-id="91af0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="91af0-115">Remarks</span></span>

<span data-ttu-id="91af0-116">L'espressione di filtro (da cui viene chiamata la funzione) viene valutata se si verifica un'eccezione durante l'esecuzione del blocco **\_ \_ try** e determina se il blocco **\_ \_ except** viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91af0-116">The filter expression (from which the function is called) is evaluated if an exception occurs during execution of the **\_\_try** block, and it determines whether or not the **\_\_except** block is executed.</span></span>

<span data-ttu-id="91af0-117">L'espressione di filtro può richiamare una funzione di filtro.</span><span class="sxs-lookup"><span data-stu-id="91af0-117">The filter expression can invoke a filter function.</span></span> <span data-ttu-id="91af0-118">La funzione Filter non può chiamare **GetExceptionInformation**.</span><span class="sxs-lookup"><span data-stu-id="91af0-118">The filter function cannot call **GetExceptionInformation**.</span></span> <span data-ttu-id="91af0-119">Tuttavia, il valore restituito di **GetExceptionInformation** può essere passato come parametro a una funzione di filtro.</span><span class="sxs-lookup"><span data-stu-id="91af0-119">However, the return value of **GetExceptionInformation** can be passed as a parameter to a filter function.</span></span>

<span data-ttu-id="91af0-120">Per passare le informazioni sui [**\_ puntatori di eccezione**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) al blocco del gestore di eccezioni, l'espressione di filtro o la funzione di filtro deve copiare il puntatore o i dati nell'archiviazione sicura a cui il gestore può accedere in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="91af0-120">To pass the [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) information to the exception-handler block, the filter expression or filter function must copy the pointer or the data to safe storage that the handler can later access.</span></span>

<span data-ttu-id="91af0-121">Nel caso di gestori annidati, ogni espressione di filtro viene valutata fino a quando non viene valutata come **\_ \_ gestore di esecuzione delle eccezioni** oppure **\_ \_ l'esecuzione dell'eccezione continua**.</span><span class="sxs-lookup"><span data-stu-id="91af0-121">In the case of nested handlers, each filter expression is evaluated until one is evaluated as **EXCEPTION\_EXECUTE\_HANDLER** or **EXCEPTION\_CONTINUE\_EXECUTION**.</span></span> <span data-ttu-id="91af0-122">Ogni espressione di filtro può richiamare **GetExceptionInformation** per ottenere informazioni sull'eccezione.</span><span class="sxs-lookup"><span data-stu-id="91af0-122">Each filter expression can invoke **GetExceptionInformation** to get exception information.</span></span>

## <a name="requirements"></a><span data-ttu-id="91af0-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91af0-123">Requirements</span></span>



| <span data-ttu-id="91af0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="91af0-124">Requirement</span></span> | <span data-ttu-id="91af0-125">Valore</span><span class="sxs-lookup"><span data-stu-id="91af0-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91af0-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91af0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="91af0-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="91af0-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="91af0-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91af0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="91af0-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91af0-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91af0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91af0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91af0-131">**CONTESTO**</span><span class="sxs-lookup"><span data-stu-id="91af0-131">**CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[<span data-ttu-id="91af0-132">**\_puntatori di eccezione**</span><span class="sxs-lookup"><span data-stu-id="91af0-132">**EXCEPTION\_POINTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[<span data-ttu-id="91af0-133">**RECORD di eccezione \_**</span><span class="sxs-lookup"><span data-stu-id="91af0-133">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="91af0-134">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="91af0-134">**GetExceptionCode**</span></span>](getexceptioncode.md)
</dt> <dt>

[<span data-ttu-id="91af0-135">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="91af0-135">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[<span data-ttu-id="91af0-136">Funzioni di gestione delle eccezioni strutturate</span><span class="sxs-lookup"><span data-stu-id="91af0-136">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="91af0-137">Cenni preliminari sulla gestione delle eccezioni strutturata</span><span class="sxs-lookup"><span data-stu-id="91af0-137">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> <dt>

[<span data-ttu-id="91af0-138">Abilita il supporto di Windows per Intel AVX</span><span class="sxs-lookup"><span data-stu-id="91af0-138">Enable Windows Support for Intel AVX</span></span>](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
