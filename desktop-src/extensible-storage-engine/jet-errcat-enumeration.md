---
description: 'Altre informazioni su: Enumerazione JET_ERRCAT'
title: Enumerazione JET_ERRCAT (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231812"
---
# <a name="jet_errcat-enumeration"></a><span data-ttu-id="d13fc-103">Enumerazione JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="d13fc-103">JET_ERRCAT enumeration</span></span>

<span data-ttu-id="d13fc-104">Categoria dell'errore.</span><span class="sxs-lookup"><span data-stu-id="d13fc-104">The error category.</span></span> <span data-ttu-id="d13fc-105">La gerarchia è la seguente: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//problemi di IO non sono temporanei.</span><span class="sxs-lookup"><span data-stu-id="d13fc-105">The hierarchy is as follows: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // bad IO issues, may or may not be transient.</span></span> <span data-ttu-id="d13fc-106">| |--JET_errcatResource | |--JET_errcatMemory//memoria insufficiente (tutte le varianti) | |--JET_errcatQuota | |--JET_errcatDisk//spazio su disco insufficiente (tutte le varianti) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//in genere causati da utenti malgestiti | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete</span><span class="sxs-lookup"><span data-stu-id="d13fc-106">| |-- JET_errcatResource | |-- JET_errcatMemory // out of memory (all variants) | |-- JET_errcatQuota | |-- JET_errcatDisk // out of disk space (all variants) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // typically caused by user Mishandling | |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete</span></span>

<span data-ttu-id="d13fc-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d13fc-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="d13fc-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d13fc-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d13fc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d13fc-109">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a><span data-ttu-id="d13fc-110">Members</span><span class="sxs-lookup"><span data-stu-id="d13fc-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d13fc-111">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="d13fc-111">Member name</span></span></th>
<th><span data-ttu-id="d13fc-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d13fc-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d13fc-113">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="d13fc-113">Unknown</span></span></td>
<td><span data-ttu-id="d13fc-114">Categoria sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="d13fc-114">Unknown category.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d13fc-115">Errore</span><span class="sxs-lookup"><span data-stu-id="d13fc-115">Error</span></span></td>
<td><span data-ttu-id="d13fc-116">Categoria generica.</span><span class="sxs-lookup"><span data-stu-id="d13fc-116">A generic category.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d13fc-117">Operazione</span><span class="sxs-lookup"><span data-stu-id="d13fc-117">Operation</span></span></td>
<td><span data-ttu-id="d13fc-118">Errori che in genere possono verificarsi in qualsiasi momento a causa di condizioni incontrollabili.</span><span class="sxs-lookup"><span data-stu-id="d13fc-118">Errors that can usually happen any time due to uncontrollable conditions.</span></span> <span data-ttu-id="d13fc-119">Spesso temporanea, ma non sempre.</span><span class="sxs-lookup"><span data-stu-id="d13fc-119">Frequently temporary, but not always.</span></span> <span data-ttu-id="d13fc-120">Ripristino: è probabile che venga effettuato un nuovo tentativo o alla fine di informare l'operatore.</span><span class="sxs-lookup"><span data-stu-id="d13fc-120">Recovery: Probably retry, or eventually inform the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d13fc-121">Fatal</span><span class="sxs-lookup"><span data-stu-id="d13fc-121">Fatal</span></span></td>
<td><span data-ttu-id="d13fc-122">Questo errore di ordinamento si verifica solo quando ESE rileva una condizione di errore così grave, che non è possibile continuare in un modo sicuro (spesso transazionale) e invece che i dati danneggiati generano errori di questa categoria.</span><span class="sxs-lookup"><span data-stu-id="d13fc-122">This sort error happens only when ESE encounters an error condition so grave, that we can not continue on in a safe (often transactional) way, and rather than corrupt data we throw errors of this category.</span></span> <span data-ttu-id="d13fc-123">Ripristino: riavviare l'istanza o il processo.</span><span class="sxs-lookup"><span data-stu-id="d13fc-123">Recovery: Restart the instance or process.</span></span> <span data-ttu-id="d13fc-124">Se il problema persiste, informare l'operatore.</span><span class="sxs-lookup"><span data-stu-id="d13fc-124">If the problem persists inform the operator.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d13fc-125">IO</span><span class="sxs-lookup"><span data-stu-id="d13fc-125">IO</span></span></td>
<td><span data-ttu-id="d13fc-126">O gli errori provengono dal sistema operativo e sono fuori dal controllo di ESE, questo tipo di errore è probabilmente temporaneo, probabilmente non.</span><span class="sxs-lookup"><span data-stu-id="d13fc-126">O errors come from the OS, and are out of ESE's control, this sort of error is possibly temporary, possibly not.</span></span> <span data-ttu-id="d13fc-127">Ripristino: Riprova.</span><span class="sxs-lookup"><span data-stu-id="d13fc-127">Recovery: Retry.</span></span> <span data-ttu-id="d13fc-128">Se non viene risolto, richiedere all'operatore il problema del disco.</span><span class="sxs-lookup"><span data-stu-id="d13fc-128">If not resolved, ask operator about disk issue.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d13fc-129">Risorsa</span><span class="sxs-lookup"><span data-stu-id="d13fc-129">Resource</span></span></td>
<td><span data-ttu-id="d13fc-130">Si tratta di una categoria che indica una delle numerose condizioni possibili di esaurimento delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d13fc-130">This is a category that indicates one of many potential out-of-resource conditions.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d13fc-131">Memoria</span><span class="sxs-lookup"><span data-stu-id="d13fc-131">Memory</span></span></td>
<td><span data-ttu-id="d13fc-132">Condizione di memoria esaurita classica.</span><span class="sxs-lookup"><span data-stu-id="d13fc-132">Classic out of memory condition.</span></span> <span data-ttu-id="d13fc-133">Ripristino: attendere qualche minuto e riprovare, liberare memoria o uscire.</span><span class="sxs-lookup"><span data-stu-id="d13fc-133">Recovery: Wait a while and retry, free up memory, or quit.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d13fc-134">Quota</span><span class="sxs-lookup"><span data-stu-id="d13fc-134">Quota</span></span></td>
<td><span data-ttu-id="d13fc-135">Alcune &quot; &quot; risorse speciali sono in pool di una determinata dimensione, semplificando il rilevamento delle perdite di queste risorse.</span><span class="sxs-lookup"><span data-stu-id="d13fc-135">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span> <span data-ttu-id="d13fc-136">Ripristino: potrebbe richiedere modifiche minime al codice.</span><span class="sxs-lookup"><span data-stu-id="d13fc-136">Recovery: Might require some minor code changes.</span></span> <span data-ttu-id="d13fc-137">Per poter essere rilevati durante lo sviluppo, l'applicazione deve avere un'azione di solo debug, ad esempio un'asserzione.</span><span class="sxs-lookup"><span data-stu-id="d13fc-137">Your application should have a debug only action, such as an Assert, on these conditions in order to detect them during development.</span></span> <span data-ttu-id="d13fc-138">Per il codice per la vendita al dettaglio, è consigliabile considerare questo errore, ad esempio l'errore della categoria di memoria e riprovare, liberare memoria o uscire dall'operazione.</span><span class="sxs-lookup"><span data-stu-id="d13fc-138">For retail code, we recommend that you treat this error like the Memory category error and either retry, free up memory, or quit the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d13fc-139">Disco</span><span class="sxs-lookup"><span data-stu-id="d13fc-139">Disk</span></span></td>
<td><span data-ttu-id="d13fc-140">Condizioni del disco insufficiente.</span><span class="sxs-lookup"><span data-stu-id="d13fc-140">Out of disk conditions.</span></span> <span data-ttu-id="d13fc-141">Ripristino: è possibile riprovare più tardi nella speranza che lo spazio sia disponibile o richiedere all'operatore di liberare spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="d13fc-141">Recovery: Can retry later in the hope more space is available, or ask the operator to free some disk space.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d13fc-142">Data</span><span class="sxs-lookup"><span data-stu-id="d13fc-142">Data</span></span></td>
<td><span data-ttu-id="d13fc-143">Errore relativo ai dati.</span><span class="sxs-lookup"><span data-stu-id="d13fc-143">A data-related error.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d13fc-144">Danneggiamento</span><span class="sxs-lookup"><span data-stu-id="d13fc-144">Corruption</span></span></td>
<td><span data-ttu-id="d13fc-145">Ho mangiato il mio disco rigido.</span><span class="sxs-lookup"><span data-stu-id="d13fc-145">My hard drive ate my homework.</span></span> <span data-ttu-id="d13fc-146">Problemi di danneggiamento classici, spesso permanenti senza azioni correttive.</span><span class="sxs-lookup"><span data-stu-id="d13fc-146">Classic corruption issues, frequently permanent without corrective action.</span></span> <span data-ttu-id="d13fc-147">Ripristino: eseguire il ripristino da un backup, ad esempio l'operazione di ripristino delle utilità ESE, che consente di recuperare solo i dati a sinistra/con perdita di dati. Inoltre, nel caso del ripristino (JetInit), potrebbe essere possibile eseguire il ripristino consentendo la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="d13fc-147">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy) .Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d13fc-148">Incoerente</span><span class="sxs-lookup"><span data-stu-id="d13fc-148">Inconsistent</span></span></td>
<td><span data-ttu-id="d13fc-149">Si tratta di un problema simile al danneggiamento in quanto i file di database e/o di log si trovano in uno stato incoerente e non riconciliabile tra loro.</span><span class="sxs-lookup"><span data-stu-id="d13fc-149">This is similar to Corruption in that the database and/or log files are in a state that is inconsistent and unreconcilable with each other.</span></span> <span data-ttu-id="d13fc-150">Questo problema è spesso dovuto a una gestione non gestita da parte dell'applicazione o dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="d13fc-150">Often this is caused by application/administrator mishandling.</span></span> <span data-ttu-id="d13fc-151">Ripristino: eseguire il ripristino da un backup, ad esempio l'operazione di ripristino delle utilità ESE, che consente di recuperare solo i dati a sinistra/con perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="d13fc-151">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy).</span></span> <span data-ttu-id="d13fc-152">Inoltre, nel caso del ripristino (JetInit), potrebbe essere possibile eseguire il ripristino consentendo la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="d13fc-152">Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d13fc-153">Frammentazione</span><span class="sxs-lookup"><span data-stu-id="d13fc-153">Fragmentation</span></span></td>
<td><span data-ttu-id="d13fc-154">Si tratta di una classe di errori in cui è stata eseguita una risorsa interna permanente. Ripristino: per gli errori del database, la deframmentazione non in linea risolverà il problema. per i file di log è necessario _innanzitutto_ ripristinare tutti i database collegati a una chiusura normale e quindi eliminare tutti i file di log e il checkpoint.</span><span class="sxs-lookup"><span data-stu-id="d13fc-154">This is a class of errors where some persisted internal resource ran out. Recovery: For database errors, offline defragmentation will rectify the problem, for the log files _first_ recover all attached databases to a clean shutdown, and then delete all the log files and checkpoint.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d13fc-155">API</span><span class="sxs-lookup"><span data-stu-id="d13fc-155">Api</span></span></td>
<td><span data-ttu-id="d13fc-156">Contenitore per l'utilizzo e lo stato.</span><span class="sxs-lookup"><span data-stu-id="d13fc-156">A container for Usage and State.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d13fc-157">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d13fc-157">Usage</span></span></td>
<td><span data-ttu-id="d13fc-158">Errore di utilizzo classico. questo significa che il codice client non ha passato gli argomenti corretti all'API JET.</span><span class="sxs-lookup"><span data-stu-id="d13fc-158">Classic usage error, this means the client code did not pass correct arguments to the JET API.</span></span> <span data-ttu-id="d13fc-159">Questo errore probabilmente non verrà ritentato.</span><span class="sxs-lookup"><span data-stu-id="d13fc-159">This error will likely not go away with retry.</span></span> <span data-ttu-id="d13fc-160">Recupero: in genere il codice client deve dichiarare () questa classe di errori non viene restituita, quindi i problemi possono essere rilevati durante lo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="d13fc-160">Recovery: Generally speaking client code should Assert() this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="d13fc-161">Nella vendita al dettaglio, l'app avrà probabilmente una piccola opzione, ma restituirà il problema all'operatore.</span><span class="sxs-lookup"><span data-stu-id="d13fc-161">In retail, the app will probably have little option but to return the issue up to the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d13fc-162">State</span><span class="sxs-lookup"><span data-stu-id="d13fc-162">State</span></span></td>
<td><span data-ttu-id="d13fc-163">Si tratta della classificazione per i diversi segnali che possono essere restituiti dall'API per descrivere lo stato del database. un caso classico è JET_errRecordNotFound, che può essere restituito da JetSeek () quando il record richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="d13fc-163">This is the classification for different signals the API could return describe the state of the database, a classic case is JET_errRecordNotFound which can be returned by JetSeek() when the record you asked for was not found.</span></span> <span data-ttu-id="d13fc-164">Ripristino: non è rilevante, dipende in larga misura dall'API.</span><span class="sxs-lookup"><span data-stu-id="d13fc-164">Recovery: Not really relevant, depends greatly on the API.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d13fc-165">Obsoleti</span><span class="sxs-lookup"><span data-stu-id="d13fc-165">Obsolete</span></span></td>
<td><span data-ttu-id="d13fc-166">L'errore viene riconosciuto come un errore valido, ma non è previsto che venga restituito da questa versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="d13fc-166">The error is recognized as a valid error, but is not expected to be returned by this version of the API.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d13fc-167">Max</span><span class="sxs-lookup"><span data-stu-id="d13fc-167">Max</span></span></td>
<td><span data-ttu-id="d13fc-168">Valore massimo per l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="d13fc-168">The maximum value for the enum.</span></span> <span data-ttu-id="d13fc-169">Questa operazione non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d13fc-169">This should not be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d13fc-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d13fc-170">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d13fc-171">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d13fc-171">Reference</span></span>

[<span data-ttu-id="d13fc-172">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="d13fc-172">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
