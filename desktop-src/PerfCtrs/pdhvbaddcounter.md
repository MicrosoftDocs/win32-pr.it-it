---
description: La funzione PdhVbAddCounter crea una voce del contatore nell'oggetto query specificato e restituisce un handle al contatore al termine del completamento.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: PdhVbAddCounter (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312154"
---
# <a name="pdhvbaddcounter-function"></a><span data-ttu-id="522e9-103">PdhVbAddCounter (funzione)</span><span class="sxs-lookup"><span data-stu-id="522e9-103">PdhVbAddCounter function</span></span>

<span data-ttu-id="522e9-104">La funzione **PdhVbAddCounter** crea una voce del contatore nell'oggetto query specificato e restituisce un handle al contatore al termine del completamento.</span><span class="sxs-lookup"><span data-stu-id="522e9-104">The **PdhVbAddCounter** function creates a counter entry in the specified query object, and returns a handle to that counter upon successful completion.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="522e9-105">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="522e9-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="522e9-106">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="522e9-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="522e9-107">Funzione PdhVbAddCounter ( \_ ByVal QueryHandle Long, \_ ByVal CounterPath As String, \_ ByVal CounterHandle Long \_ ) Long</span><span class="sxs-lookup"><span data-stu-id="522e9-107">Function PdhVbAddCounter( \_ ByVal QueryHandle As Long, \_ ByVal CounterPath As String, \_ ByVal CounterHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="522e9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="522e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="522e9-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="522e9-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="522e9-110">ID della query a cui deve essere assegnato questo contatore.</span><span class="sxs-lookup"><span data-stu-id="522e9-110">ID of the query to which this counter is to be assigned.</span></span> <span data-ttu-id="522e9-111">Questo valore viene restituito dalla funzione [**PdhVbOpenQuery**](pdhvbopenquery.md) .</span><span class="sxs-lookup"><span data-stu-id="522e9-111">This value is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="522e9-112">*CounterPath*</span><span class="sxs-lookup"><span data-stu-id="522e9-112">*CounterPath*</span></span> 
</dt> <dd>

<span data-ttu-id="522e9-113">Stringa di testo che specifica il nome del percorso del contatore da aggiungere alla query.</span><span class="sxs-lookup"><span data-stu-id="522e9-113">Text string that specifies the name of the counter path to add to the query.</span></span> <span data-ttu-id="522e9-114">Il contenuto di questa stringa deve essere un percorso di contatore valido, come ottenuto dal browser del contatore o da un'altra origine.</span><span class="sxs-lookup"><span data-stu-id="522e9-114">The contents of this string must be a valid counter path, as obtained from the counter browser or other source.</span></span>

</dd> <dt>

<span data-ttu-id="522e9-115">*CounterHandle*</span><span class="sxs-lookup"><span data-stu-id="522e9-115">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="522e9-116">Riferimento univoco che identifica questo contatore nella query.</span><span class="sxs-lookup"><span data-stu-id="522e9-116">Unique reference that identifies this counter in the query.</span></span> <span data-ttu-id="522e9-117">Questa variabile deve essere inizializzata su zero prima della chiamata della funzione.</span><span class="sxs-lookup"><span data-stu-id="522e9-117">This variable must be initialized to zero before the function is called.</span></span> <span data-ttu-id="522e9-118">Contiene un valore valido per return solo se la funzione viene completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="522e9-118">It contains a valid value on return only if the function completes successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="522e9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="522e9-119">Return value</span></span>

<span data-ttu-id="522e9-120">Se la funzione ha esito positivo, restituisce un **Long** Integer uguale a Error \_ Success e un nuovo handle nella variabile *CounterHandle* .</span><span class="sxs-lookup"><span data-stu-id="522e9-120">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *CounterHandle* variable.</span></span>

<span data-ttu-id="522e9-121">Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="522e9-121">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="522e9-122">Di seguito sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="522e9-122">The following are possible values.</span></span>



| <span data-ttu-id="522e9-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="522e9-123">Return code</span></span>                                                                                                     | <span data-ttu-id="522e9-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="522e9-124">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="522e9-125"><dt>**\_argomento PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="522e9-126">Uno o più argomenti non sono validi o sono errati.</span><span class="sxs-lookup"><span data-stu-id="522e9-126">One or more of the arguments is invalid or incorrect.</span></span><br/>              |
| <dl> <span data-ttu-id="522e9-127"><dt>**\_errore di \_ allocazione della memoria PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-127"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="522e9-128">Impossibile allocare un buffer di memoria.</span><span class="sxs-lookup"><span data-stu-id="522e9-128">A memory buffer could not be allocated.</span></span><br/>                            |
| <dl> <span data-ttu-id="522e9-129"><dt>**\_handle PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-129"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>             | <span data-ttu-id="522e9-130">Handle di query non valido.</span><span class="sxs-lookup"><span data-stu-id="522e9-130">The query handle is not valid.</span></span><br/>                                     |
| <dl> <span data-ttu-id="522e9-131"><dt>**PDH \_ CSTATUS \_ senza \_ contatore**</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-131"><dt>**PDH\_CSTATUS\_NO\_COUNTER**</dt></span></span> </dl>        | <span data-ttu-id="522e9-132">Il contatore specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="522e9-132">The specified counter was not found.</span></span><br/>                               |
| <dl> <span data-ttu-id="522e9-133"><dt>**PDH \_ CSTATUS \_ nessun \_ oggetto**</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-133"><dt>**PDH\_CSTATUS\_NO\_OBJECT**</dt></span></span> </dl>         | <span data-ttu-id="522e9-134">Impossibile trovare l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="522e9-134">The specified object could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="522e9-135"><dt>**PDH \_ CSTATUS \_ nessun \_ computer**</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-135"><dt>**PDH\_CSTATUS\_NO\_MACHINE**</dt></span></span> </dl>        | <span data-ttu-id="522e9-136">Non è stato possibile creare una voce del computer.</span><span class="sxs-lookup"><span data-stu-id="522e9-136">A computer entry could not be created.</span></span><br/>                             |
| <dl> <span data-ttu-id="522e9-137"><dt>**PDH \_ CSTATUS \_ - \_ counterName non valido**</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-137"><dt>**PDH\_CSTATUS\_BAD\_COUNTERNAME**</dt></span></span> </dl>   | <span data-ttu-id="522e9-138">È stata passata una stringa vuota del percorso del nome del contatore.</span><span class="sxs-lookup"><span data-stu-id="522e9-138">An empty counter name path string was passed in.</span></span><br/>                   |
| <dl> <span data-ttu-id="522e9-139"><dt>**\_funzione PDH \_ non \_ trovata**</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-139"><dt>**PDH\_FUNCTION\_NOT\_FOUND**</dt></span></span> </dl>        | <span data-ttu-id="522e9-140">Impossibile determinare la funzione di calcolo per questo contatore.</span><span class="sxs-lookup"><span data-stu-id="522e9-140">The calculation function for this counter could not be determined.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="522e9-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="522e9-141">Requirements</span></span>



| <span data-ttu-id="522e9-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="522e9-142">Requirement</span></span> | <span data-ttu-id="522e9-143">Valore</span><span class="sxs-lookup"><span data-stu-id="522e9-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="522e9-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="522e9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="522e9-145">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="522e9-145">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="522e9-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="522e9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="522e9-147">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="522e9-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="522e9-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="522e9-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="522e9-149"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-149"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="522e9-150">DLL</span><span class="sxs-lookup"><span data-stu-id="522e9-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="522e9-151"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="522e9-151"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="522e9-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="522e9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522e9-153">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="522e9-153">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
</dt> </dl>

 

