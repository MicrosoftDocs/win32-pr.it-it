---
description: La funzione PdhVbGetCounterPathElements analizza una stringa di percorso del contatore delle prestazioni completo nei singoli elementi.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: PdhVbGetCounterPathElements (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312152"
---
# <a name="pdhvbgetcounterpathelements-function"></a><span data-ttu-id="b6b90-103">PdhVbGetCounterPathElements (funzione)</span><span class="sxs-lookup"><span data-stu-id="b6b90-103">PdhVbGetCounterPathElements function</span></span>

<span data-ttu-id="b6b90-104">La funzione **PdhVbGetCounterPathElements** analizza una stringa di percorso del contatore delle prestazioni completo nei singoli elementi.</span><span class="sxs-lookup"><span data-stu-id="b6b90-104">The **PdhVbGetCounterPathElements** function parses a fully qualified performance counter path string into its individual elements.</span></span> <span data-ttu-id="b6b90-105">Ogni variabile di tipo stringa deve avere la stessa dimensione (*bufferSize*) e dimensionata e inizializzata prima di essere utilizzata in questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b6b90-105">Each of the string variables must be the same size (*BufferSize*) and dimensioned and initialized before it is used in this function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6b90-106">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="b6b90-106">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="b6b90-107">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b6b90-107">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="b6b90-108">Funzione PdhVbGetCounterPathElements ( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal nomeoggetto As String, \_ ByVal NomeIstanza As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal bufferSize Long \_ ) Long</span><span class="sxs-lookup"><span data-stu-id="b6b90-108">Function PdhVbGetCounterPathElements( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal InstanceName As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal BufferSize As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="b6b90-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6b90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b90-110">*PathString*</span><span class="sxs-lookup"><span data-stu-id="b6b90-110">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b90-111">Stringa del percorso del contatore che deve essere suddivisa nei singoli elementi.</span><span class="sxs-lookup"><span data-stu-id="b6b90-111">Counter path string that is to be broken up into its individual elements.</span></span>

</dd> <dt>

<span data-ttu-id="b6b90-112">*MachineName*</span><span class="sxs-lookup"><span data-stu-id="b6b90-112">*MachineName*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b90-113">Stringa per la ricezione del nome del computer.</span><span class="sxs-lookup"><span data-stu-id="b6b90-113">String to receive the computer name.</span></span>

</dd> <dt>

<span data-ttu-id="b6b90-114">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="b6b90-114">*ObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b90-115">Stringa che consente di ricevere il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b6b90-115">String to receive the object name.</span></span>

</dd> <dt>

<span data-ttu-id="b6b90-116">*InstanceName*</span><span class="sxs-lookup"><span data-stu-id="b6b90-116">*InstanceName*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b90-117">Stringa in cui ricevere il nome dell'istanza, se utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b6b90-117">String to receive the instance name, if used.</span></span>

</dd> <dt>

<span data-ttu-id="b6b90-118">*ParentInstance*</span><span class="sxs-lookup"><span data-stu-id="b6b90-118">*ParentInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b90-119">Stringa per la ricezione dell'istanza padre, se utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b6b90-119">String to receive the parent instance, if used.</span></span>

</dd> <dt>

<span data-ttu-id="b6b90-120">*CounterName*</span><span class="sxs-lookup"><span data-stu-id="b6b90-120">*CounterName*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b90-121">Stringa per la ricezione del nome del contatore.</span><span class="sxs-lookup"><span data-stu-id="b6b90-121">String to receive the counter name.</span></span>

</dd> <dt>

<span data-ttu-id="b6b90-122">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="b6b90-122">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b90-123">Dimensione massima di ogni variabile di stringa utilizzata come parametro per la chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="b6b90-123">Maximum size of each string variable used as a parameter to this function call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b90-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6b90-124">Return value</span></span>

<span data-ttu-id="b6b90-125">Se la funzione ha esito positivo, restituisce un **Long** Integer uguale a Error \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b6b90-125">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b6b90-126">Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b6b90-126">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="b6b90-127">Di seguito sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="b6b90-127">The following are possible values.</span></span>



| <span data-ttu-id="b6b90-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b6b90-128">Return code</span></span>                                                                                                     | <span data-ttu-id="b6b90-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6b90-129">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6b90-130"><dt>**\_argomento PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b90-130"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="b6b90-131">La dimensione di uno o più buffer di stringa non è corretta.</span><span class="sxs-lookup"><span data-stu-id="b6b90-131">One or more of the string buffers is not the correct size.</span></span><br/>                          |
| <dl> <span data-ttu-id="b6b90-132"><dt>**PDH \_ altri \_ dati**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b90-132"><dt>**PDH\_MORE\_DATA**</dt></span></span> </dl>                  | <span data-ttu-id="b6b90-133">Uno o più elementi del percorso del contatore sono troppo grandi per la lunghezza del buffer di ritorno.</span><span class="sxs-lookup"><span data-stu-id="b6b90-133">One or more of the counter path elements is too large for the return buffer length.</span></span><br/> |
| <dl> <span data-ttu-id="b6b90-134"><dt>**\_errore di \_ allocazione della memoria PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b90-134"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="b6b90-135">Impossibile allocare un buffer di memoria temporaneo.</span><span class="sxs-lookup"><span data-stu-id="b6b90-135">A temporary memory buffer could not be allocated.</span></span><br/>                                   |



 

## <a name="requirements"></a><span data-ttu-id="b6b90-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6b90-136">Requirements</span></span>



| <span data-ttu-id="b6b90-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6b90-137">Requirement</span></span> | <span data-ttu-id="b6b90-138">Valore</span><span class="sxs-lookup"><span data-stu-id="b6b90-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b90-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6b90-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b90-140">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b6b90-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6b90-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6b90-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b90-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6b90-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b6b90-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6b90-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6b90-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6b90-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6b90-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b90-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b90-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6b90-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6b90-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6b90-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b90-148">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="b6b90-148">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="b6b90-149">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="b6b90-149">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="b6b90-150">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="b6b90-150">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

