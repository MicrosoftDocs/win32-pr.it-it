---
description: Indica se il \_ \_ blocco try di un gestore di terminazione è terminato normalmente. La funzione può essere chiamata solo dall'interno del \_ \_ blocco finally di un gestore di terminazione.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: AbnormalTermination (macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966286"
---
# <a name="abnormaltermination-macro"></a><span data-ttu-id="41411-104">AbnormalTermination (macro)</span><span class="sxs-lookup"><span data-stu-id="41411-104">AbnormalTermination macro</span></span>

<span data-ttu-id="41411-105">Indica se il blocco **\_ \_ try** di un gestore di terminazione è terminato normalmente.</span><span class="sxs-lookup"><span data-stu-id="41411-105">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span> <span data-ttu-id="41411-106">La funzione può essere chiamata solo dall'interno del blocco **\_ \_ finally** di un gestore di terminazione.</span><span class="sxs-lookup"><span data-stu-id="41411-106">The function can be called only from within the **\_\_finally** block of a termination handler.</span></span>

> [!Note]  
> <span data-ttu-id="41411-107">Il compilatore di ottimizzazione di Microsoft C/C++ interpreta questa funzione come una parola chiave e il suo utilizzo al di fuori della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore.</span><span class="sxs-lookup"><span data-stu-id="41411-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="41411-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41411-108">Syntax</span></span>


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a><span data-ttu-id="41411-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="41411-109">Parameters</span></span>

<span data-ttu-id="41411-110">Questa macro non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="41411-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41411-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41411-111">Return value</span></span>

<span data-ttu-id="41411-112">Se il blocco **\_ \_ try** termina in modo anomalo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="41411-112">If the **\_\_try** block terminated abnormally, the return value is nonzero.</span></span>

<span data-ttu-id="41411-113">Se il blocco **\_ \_ try** termina normalmente, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="41411-113">If the **\_\_try** block terminated normally, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="41411-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="41411-114">Remarks</span></span>

<span data-ttu-id="41411-115">Il blocco **\_ \_ try** termina normalmente solo se l'esecuzione lascia il blocco in sequenza dopo l'esecuzione dell'ultima istruzione nel blocco.</span><span class="sxs-lookup"><span data-stu-id="41411-115">The **\_\_try** block terminates normally only if execution leaves the block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="41411-116">Le istruzioni, ad esempio **return**, **goto**, **continue** o **break**, che fanno sì che l'esecuzione lasci il blocco **\_ \_ try** causando una chiusura anomala del blocco.</span><span class="sxs-lookup"><span data-stu-id="41411-116">Statements (such as **return**, **goto**, **continue**, or **break**) that cause execution to leave the **\_\_try** block result in abnormal termination of the block.</span></span> <span data-ttu-id="41411-117">Questa situazione si verifica anche se tale istruzione rappresenta l'ultima istruzione nel blocco **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="41411-117">This is the case even if such a statement is the last statement in the **\_\_try** block.</span></span>

<span data-ttu-id="41411-118">Una chiusura anomala di un blocco **\_ \_ try** causa la ricerca all'indietro di tutti gli stack frame da parte del sistema per determinare se è necessario chiamare i gestori di terminazione.</span><span class="sxs-lookup"><span data-stu-id="41411-118">Abnormal termination of a **\_\_try** block causes the system to search backward through all stack frames to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="41411-119">Questo può comportare l'esecuzione di centinaia di istruzioni, quindi è importante evitare la chiusura anomala di un blocco **\_ \_ try** a causa di un'istruzione **return**, **goto**, **continue** o **break** .</span><span class="sxs-lookup"><span data-stu-id="41411-119">This can result in the execution of hundreds of instructions, so it is important to avoid abnormal termination of a **\_\_try** block due to a **return**, **goto**, **continue**, or **break** statement.</span></span> <span data-ttu-id="41411-120">Si noti che queste istruzioni non generano un'eccezione, anche se la chiusura è anomala.</span><span class="sxs-lookup"><span data-stu-id="41411-120">Note that these statements do not generate an exception, even though the termination is abnormal.</span></span>

<span data-ttu-id="41411-121">Per evitare la chiusura anomala, l'esecuzione deve proseguire fino alla fine del blocco.</span><span class="sxs-lookup"><span data-stu-id="41411-121">To avoid abnormal termination, execution should continue to the end of the block.</span></span> <span data-ttu-id="41411-122">È anche possibile eseguire l'istruzione **\_ \_ Leave** .</span><span class="sxs-lookup"><span data-stu-id="41411-122">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="41411-123">L'istruzione **\_ \_ Leave** consente la chiusura immediata del blocco **\_ \_ try** senza causare la terminazione anomala e la riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="41411-123">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="41411-124">Controllare la documentazione del compilatore per determinare se l'istruzione **\_ \_ Leave** è supportata.</span><span class="sxs-lookup"><span data-stu-id="41411-124">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="41411-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41411-125">Requirements</span></span>



| <span data-ttu-id="41411-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="41411-126">Requirement</span></span> | <span data-ttu-id="41411-127">Valore</span><span class="sxs-lookup"><span data-stu-id="41411-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41411-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41411-128">Minimum supported client</span></span><br/> | <span data-ttu-id="41411-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="41411-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="41411-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41411-130">Minimum supported server</span></span><br/> | <span data-ttu-id="41411-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41411-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41411-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41411-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41411-133">Funzioni di gestione delle eccezioni strutturate</span><span class="sxs-lookup"><span data-stu-id="41411-133">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="41411-134">Cenni preliminari sulla gestione delle eccezioni strutturata</span><span class="sxs-lookup"><span data-stu-id="41411-134">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> </dl>

 

 




