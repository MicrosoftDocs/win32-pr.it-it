---
description: 'Altre informazioni su: funzione JetSetSystemParameter'
title: JetSetSystemParameter (funzione)
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226248"
---
# <a name="jetsetsystemparameter-function"></a><span data-ttu-id="873fa-103">JetSetSystemParameter (funzione)</span><span class="sxs-lookup"><span data-stu-id="873fa-103">JetSetSystemParameter Function</span></span>


<span data-ttu-id="873fa-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="873fa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsystemparameter-function"></a><span data-ttu-id="873fa-105">JetSetSystemParameter (funzione)</span><span class="sxs-lookup"><span data-stu-id="873fa-105">JetSetSystemParameter Function</span></span>

<span data-ttu-id="873fa-106">La funzione **JetSetSystemParameter** viene utilizzata per impostare le numerose impostazioni di configurazione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="873fa-106">The **JetSetSystemParameter** function is used to set the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a><span data-ttu-id="873fa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="873fa-107">Parameters</span></span>

<span data-ttu-id="873fa-108">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="873fa-108">*pinstance*</span></span>

<span data-ttu-id="873fa-109">Specifica l'istanza di da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="873fa-109">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="873fa-110">**Windows 2000:**  Per Windows 2000, questo parametro viene ignorato e deve essere sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="873fa-110">**Windows 2000:**  For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="873fa-111">**Windows XP:**  Per Windows XP e versioni successive, questo parametro è leggermente sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="873fa-111">**Windows XP:**  For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="873fa-112">Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro può essere **null** o può contenere l'istanza effettiva restituita da [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="873fa-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="873fa-113">In entrambi i casi, tutte le impostazioni dei parametri di sistema vengono lette da un'istanza.</span><span class="sxs-lookup"><span data-stu-id="873fa-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="873fa-114">Se il motore funziona in modalità a istanze diverse, questo parametro può essere **null** o un puntatore a un'istanza creata usando [JetInit](./jetinit-function.md) o [JetCreateIndex](./jetcreateindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="873fa-114">If the engine is operating in multi-instance mode, then this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateIndex](./jetcreateindex-function.md).</span></span> <span data-ttu-id="873fa-115">Se questo parametro è **null** , viene letta l'impostazione del parametro di sistema globale (o default).</span><span class="sxs-lookup"><span data-stu-id="873fa-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="873fa-116">Quando questo parametro è un'istanza, viene letta l'impostazione del parametro di sistema per tale istanza.</span><span class="sxs-lookup"><span data-stu-id="873fa-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="873fa-117">Anche se si tratta tecnicamente di un parametro out, questa API non modifica mai il contenuto del buffer fornito.</span><span class="sxs-lookup"><span data-stu-id="873fa-117">Even though this is technically an out parameter, this API never modifies the contents of the provided buffer.</span></span>

<span data-ttu-id="873fa-118">*sesid*</span><span class="sxs-lookup"><span data-stu-id="873fa-118">*sesid*</span></span>

<span data-ttu-id="873fa-119">Specifica la sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="873fa-119">Specifies the session to use for this call.</span></span>

<span data-ttu-id="873fa-120">Quando specificato, l'istanza specificata viene ignorata e viene utilizzata l'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="873fa-120">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="873fa-121">*paramid*</span><span class="sxs-lookup"><span data-stu-id="873fa-121">*paramid*</span></span>

<span data-ttu-id="873fa-122">ID del parametro di sistema che verrà impostato.</span><span class="sxs-lookup"><span data-stu-id="873fa-122">The ID of the system parameter that will be set.</span></span> <span data-ttu-id="873fa-123">Per un elenco completo dei parametri di sistema e delle relative proprietà, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="873fa-123">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="873fa-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="873fa-124">*lParam*</span></span>

<span data-ttu-id="873fa-125">Fornisce il valore da impostare per il parametro di sistema selezionato se il parametro di sistema è di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="873fa-125">Provides the value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="873fa-126">*szParam*</span><span class="sxs-lookup"><span data-stu-id="873fa-126">*szParam*</span></span>

<span data-ttu-id="873fa-127">Fornisce il valore per il parametro di sistema selezionato se il parametro di sistema è di tipo String.</span><span class="sxs-lookup"><span data-stu-id="873fa-127">Provides the value for the selected system parameter if that system parameter is of a string type.</span></span>

### <a name="return-value"></a><span data-ttu-id="873fa-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="873fa-128">Return Value</span></span>

<span data-ttu-id="873fa-129">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="873fa-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="873fa-130">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="873fa-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="873fa-131">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="873fa-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="873fa-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="873fa-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="873fa-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="873fa-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="873fa-134">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="873fa-134">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="873fa-135"><strong>Windows Vista:</strong>  In Windows Vista e versioni successive, è possibile restituire un esito positivo senza modificare il valore del parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="873fa-135"><strong>Windows Vista:</strong>  On Windows Vista and later releases, success can be returned without a change to the system parameter's value.</span></span> <span data-ttu-id="873fa-136">Per ulteriori informazioni, vedere il JET_paramEnableAdvanced parametro System nell'argomento <a href="gg269346(v=exchg.10).md">meta Parameters</a> .</span><span class="sxs-lookup"><span data-stu-id="873fa-136">See the JET_paramEnableAdvanced system parameter in the <a href="gg269346(v=exchg.10).md">Meta Parameters</a> topic for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="873fa-137">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="873fa-137">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="873fa-138">L'istanza è stata inizializzata tramite una chiamata a <a href="gg294068(v=exchg.10).md">JetInit</a> e non è possibile eseguire l'operazione di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="873fa-138">The instance has been initialized using a call to <a href="gg294068(v=exchg.10).md">JetInit</a> and this operation cannot be performed as a result.</span></span> <span data-ttu-id="873fa-139">Questa situazione può verificarsi per <strong>JetSetSystemParameter</strong> quando viene effettuato un tentativo di configurare un parametro di sistema dopo che una modifica nel suo valore non può influire sullo stato del motore di database.</span><span class="sxs-lookup"><span data-stu-id="873fa-139">This can happen for <strong>JetSetSystemParameter</strong> when an attempt is made to configure a system parameter after a change in its value cannot affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="873fa-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="873fa-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="873fa-141">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="873fa-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="873fa-142">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="873fa-142">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="873fa-143">I parametri specificati per l'indice di tupla non sono validi.</span><span class="sxs-lookup"><span data-stu-id="873fa-143">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="873fa-144">Questo errore può essere restituito da <strong>JetSetSystemParameter</strong> solo quando si imposta <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> su un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="873fa-144">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="873fa-145"><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può essere eseguita solo in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="873fa-145"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="873fa-146">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="873fa-146">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="873fa-147">Non è possibile completare l'operazione perché è in corso l'inizializzazione dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="873fa-147">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="873fa-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="873fa-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="873fa-149">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="873fa-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="873fa-150"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="873fa-150"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="873fa-151">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="873fa-151">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="873fa-152">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="873fa-152">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="873fa-153">Questo problema può verificarsi per <strong>JetSetSystemParameter</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="873fa-153">This can happen for <strong>JetSetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="873fa-154">L'ID parametro di sistema specificato non è valido o non è supportato.</span><span class="sxs-lookup"><span data-stu-id="873fa-154">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="873fa-155">È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con una stringa la cui lunghezza non rientra nell'intervallo valido per il parametro.</span><span class="sxs-lookup"><span data-stu-id="873fa-155">An attempt was made to set a string-valued system parameter with a string whose length was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="873fa-156">È stato effettuato un tentativo di impostare un parametro di sistema con valori di stringa con un percorso di file in cui la lunghezza della rappresentazione del percorso assoluto non rientra nell'intervallo valido per il parametro.</span><span class="sxs-lookup"><span data-stu-id="873fa-156">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p>
<p><span data-ttu-id="873fa-157"><strong>Windows Vista:</strong>  Questa operazione può essere eseguita solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="873fa-157"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="873fa-158">È stato effettuato un tentativo di impostare un parametro di sistema con valori integer con un numero intero non compreso nell'intervallo valido per il parametro.</span><span class="sxs-lookup"><span data-stu-id="873fa-158">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="873fa-159">È stato effettuato un tentativo di impostare JET_paramUnicodeIndexDefault con un puntatore <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> <strong>null</strong> , un LCID non valido o un set di flag LCMapString non supportato.</span><span class="sxs-lookup"><span data-stu-id="873fa-159">An attempt was made to set JET_paramUnicodeIndexDefault with a <strong>NULL</strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of LCMapString flags.</span></span></p>
<p><span data-ttu-id="873fa-160"><strong>Windows Vista:</strong>  Questa operazione può essere eseguita solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="873fa-160"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="873fa-161">Impossibile impostare il parametro di sistema specificato perché è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="873fa-161">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="873fa-162">È stato effettuato un tentativo di impostare un parametro di sistema dopo la chiamata di <a href="gg294068(v=exchg.10).md">JetInit</a> , il motore di database è in modalità a istanza singola e non è stata specificata una sessione.</span><span class="sxs-lookup"><span data-stu-id="873fa-162">An attempt was made to set a system parameter after <a href="gg294068(v=exchg.10).md">JetInit</a> was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p>
<p><span data-ttu-id="873fa-163"><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può essere eseguita solo in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="873fa-163"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="873fa-164">Il parametro di sistema specificato è solo globale ed è stato effettuato un tentativo di impostare un valore specifico dell'istanza per il parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="873fa-164">The specified system parameter is global only and an attempt was made to set an instance specific value for that system parameter.</span></span></p>
<p><span data-ttu-id="873fa-165"><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può essere eseguita solo in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="873fa-165"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="873fa-166">Il parametro di sistema specificato è solo per istanza ed è stato effettuato un tentativo di impostare il valore globale per il parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="873fa-166">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p>
<p><span data-ttu-id="873fa-167"><strong>Windows XP e Windows Server 2003:</strong>  Questa operazione può essere eseguita solo in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="873fa-167"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="873fa-168">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="873fa-168">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="873fa-169">Il percorso di file system specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="873fa-169">The specified file system path was invalid.</span></span> <span data-ttu-id="873fa-170">Questo errore può essere restituito da <strong>JetSetSystemParameter</strong> solo quando si impostano parametri di sistema che rappresentano file System percorsi.</span><span class="sxs-lookup"><span data-stu-id="873fa-170">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="873fa-171">Ad esempio, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> possibile che questo errore venga restituito.</span><span class="sxs-lookup"><span data-stu-id="873fa-171">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> may return this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="873fa-172">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="873fa-172">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="873fa-173">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="873fa-173">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="873fa-174">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="873fa-174">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="873fa-175">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="873fa-175">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="873fa-176">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="873fa-176">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="873fa-177">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="873fa-177">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="873fa-178">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="873fa-178">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="873fa-179">L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</span><span class="sxs-lookup"><span data-stu-id="873fa-179">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="873fa-180">Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="873fa-180">This error is not returned under all circumstances.</span></span> <span data-ttu-id="873fa-181">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="873fa-181">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="873fa-182">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="873fa-182">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="873fa-183">L'handle dell'istanza non è valido o fa riferimento a un'istanza di che è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="873fa-183">The instance handle is invalid or refers to an instance that has been shutdown.</span></span></p>
<p><span data-ttu-id="873fa-184">Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="873fa-184">This error is not returned under all circumstances.</span></span> <span data-ttu-id="873fa-185">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="873fa-185">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="873fa-186"><strong>Windows Vista:</strong>  Questo errore verrà restituito solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="873fa-186"><strong>Windows Vista:</strong>  This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="873fa-187">In seguito all'esito positivo, l'impostazione per il parametro di sistema verrà impostata sul valore fornito.</span><span class="sxs-lookup"><span data-stu-id="873fa-187">On success, the setting for the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="873fa-188">In caso di errore, l'impostazione per il parametro di sistema rimarrà invariata.</span><span class="sxs-lookup"><span data-stu-id="873fa-188">On failure, the setting for the system parameter will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="873fa-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="873fa-189">Remarks</span></span>

<span data-ttu-id="873fa-190">**JetSetSystemParameter** esegue un processo insufficiente per convalidare l'impostazione scelta per ogni parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="873fa-190">**JetSetSystemParameter** does a poor job of validating the chosen setting for each system parameter.</span></span> <span data-ttu-id="873fa-191">È necessario prestare attenzione a non basarsi su questa convalida per applicare impostazioni valide.</span><span class="sxs-lookup"><span data-stu-id="873fa-191">Care must be taken to not rely on this validation to enforce good settings.</span></span> <span data-ttu-id="873fa-192">Prestare particolare attenzione alla descrizione di ogni parametro di sistema e attenersi alle linee guida per una corretta impostazione del parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="873fa-192">Please pay close attention to the description of each system parameter and follow those guidelines for a good system parameter setting.</span></span>

<span data-ttu-id="873fa-193">È necessario impostare sempre un set di parametri di sistema per garantire che il motore di database funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="873fa-193">There are a set of system parameters that should always be set to guarantee that the database engine works as intended.</span></span> <span data-ttu-id="873fa-194">In particolare, tutti i parametri di sistema che influiscono sul layout fisico dei file utilizzati dal motore di database devono essere sempre impostati.</span><span class="sxs-lookup"><span data-stu-id="873fa-194">Specifically, any system parameters that affect the physical layout of the files used by the database engine should always be set.</span></span> <span data-ttu-id="873fa-195">Per ulteriori informazioni, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="873fa-195">For more information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="873fa-196">Ogni parametro di sistema ha un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="873fa-196">Every system parameter has a default value.</span></span> <span data-ttu-id="873fa-197">Questi valori predefiniti si sono evoluti nel tempo e sono piuttosto arbitrari.</span><span class="sxs-lookup"><span data-stu-id="873fa-197">These default values have evolved over time and are quite arbitrary.</span></span> <span data-ttu-id="873fa-198">Si consiglia vivamente che un'applicazione valuti tutti i valori predefiniti per assicurarsi che siano appropriati.</span><span class="sxs-lookup"><span data-stu-id="873fa-198">It is highly recommended that an application evaluate all the default values to ensure that they are appropriate.</span></span> <span data-ttu-id="873fa-199">Se non sono appropriati, devono essere configurati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="873fa-199">If they are not appropriate, then they should be configured by the application.</span></span> <span data-ttu-id="873fa-200">Questo è importante poiché molti di questi parametri possono avere un notevole effetto sull'affidabilità, sulle prestazioni e sull'utilizzo delle risorse del motore di database.</span><span class="sxs-lookup"><span data-stu-id="873fa-200">This is important as many of these parameters can greatly impact the reliability, performance, and resource utilization of the database engine.</span></span>

#### <a name="requirements"></a><span data-ttu-id="873fa-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="873fa-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="873fa-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="873fa-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="873fa-203">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="873fa-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="873fa-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="873fa-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="873fa-205">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="873fa-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="873fa-206"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="873fa-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="873fa-207">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="873fa-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="873fa-208"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="873fa-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="873fa-209">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="873fa-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="873fa-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="873fa-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="873fa-211">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="873fa-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="873fa-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="873fa-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="873fa-213">Implementato come <strong>JetSetSystemParameterW</strong> (Unicode) e <strong>JetSetSystemParameterA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="873fa-213">Implemented as <strong>JetSetSystemParameterW</strong> (Unicode) and <strong>JetSetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="873fa-214">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="873fa-214">See Also</span></span>

[<span data-ttu-id="873fa-215">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="873fa-215">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="873fa-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="873fa-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="873fa-217">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="873fa-217">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="873fa-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="873fa-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="873fa-219">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="873fa-219">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="873fa-220">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="873fa-220">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="873fa-221">JetInit</span><span class="sxs-lookup"><span data-stu-id="873fa-221">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="873fa-222">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="873fa-222">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
