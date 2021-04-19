---
description: 'Altre informazioni su: funzione JetEnableMultiInstance'
title: JetEnableMultiInstance (funzione)
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319635"
---
# <a name="jetenablemultiinstance-function"></a><span data-ttu-id="216e9-103">JetEnableMultiInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="216e9-103">JetEnableMultiInstance Function</span></span>


<span data-ttu-id="216e9-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="216e9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenablemultiinstance-function"></a><span data-ttu-id="216e9-105">JetEnableMultiInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="216e9-105">JetEnableMultiInstance Function</span></span>

<span data-ttu-id="216e9-106">La funzione **JetEnableMultiInstance** configura il motore di database per l'utilizzo con più istanze nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="216e9-106">The **JetEnableMultiInstance** function configures the database engine for use with multiple instances in the same process.</span></span> <span data-ttu-id="216e9-107">Una matrice facoltativa di parametri di sistema globale è disponibile per il primo chiamante che consente la modifica alla modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="216e9-107">An optional array of global system parameters is available to the first caller allowing for the change to multi-instance mode.</span></span>

<span data-ttu-id="216e9-108">**Windows XP: JetEnableMultiInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="216e9-108">**Windows XP:  JetEnableMultiInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a><span data-ttu-id="216e9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="216e9-109">Parameters</span></span>

<span data-ttu-id="216e9-110">*psetsysparam*</span><span class="sxs-lookup"><span data-stu-id="216e9-110">*psetsysparam*</span></span>

<span data-ttu-id="216e9-111">Matrice di parametri di sistema globale da impostare se e solo se il motore entra in modalità a istanze diverse in seguito a questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="216e9-111">An array of global system parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="216e9-112">Se *csetsysparam* è zero, *psetsysparam* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="216e9-112">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="216e9-113">*csetsysparam*</span><span class="sxs-lookup"><span data-stu-id="216e9-113">*csetsysparam*</span></span>

<span data-ttu-id="216e9-114">Il numero di elementi per la matrice di parametri globali da impostare se e solo se il motore entra in modalità a istanze diverse in seguito a questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="216e9-114">The count of elements for the array of global parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="216e9-115">Se *csetsysparam* è zero, *psetsysparam* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="216e9-115">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="216e9-116">*pcsetsucceed*</span><span class="sxs-lookup"><span data-stu-id="216e9-116">*pcsetsucceed*</span></span>

<span data-ttu-id="216e9-117">Puntatore al numero di parametri di sistema globale configurati correttamente in seguito a questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="216e9-117">A pointer to the count of global system parameters that were successfully configured as a result of this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="216e9-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="216e9-118">Return Value</span></span>

<span data-ttu-id="216e9-119">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="216e9-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="216e9-120">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="216e9-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="216e9-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="216e9-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="216e9-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="216e9-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="216e9-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="216e9-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="216e9-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="216e9-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="216e9-125">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="216e9-125">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="216e9-126">I parametri specificati per l'indice tupla non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="216e9-126">The specified tuple index parameters were not allowed.</span></span> <span data-ttu-id="216e9-127">Questo errore può essere restituito da <strong>JetEnableMultiInstance</strong> solo quando si imposta <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> su un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="216e9-127">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="216e9-128"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="216e9-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="216e9-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="216e9-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="216e9-130">Il percorso di file system specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="216e9-130">The specified file system path was invalid.</span></span> <span data-ttu-id="216e9-131">Questo errore può essere restituito da <strong>JetEnableMultiInstance</strong> solo quando si impostano parametri di sistema che rappresentano file System percorsi.</span><span class="sxs-lookup"><span data-stu-id="216e9-131">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="216e9-132">Ad esempio, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> possibile restituire l'errore.</span><span class="sxs-lookup"><span data-stu-id="216e9-132">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> can return this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="216e9-133">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="216e9-133">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="216e9-134">L'operazione non è riuscita perché non è valida quando il motore di database funziona in modalità a istanza singola (modalità di compatibilità di Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="216e9-134">The operation failed because it is illegal when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="216e9-135">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="216e9-135">JET_errSystemParamsAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="216e9-136"><strong>JetEnableMultiInstance</strong> non riuscito perché il motore è già in modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="216e9-136"><strong>JetEnableMultiInstance</strong> failed because the engine is already in multi-instance mode.</span></span></p>
<p><span data-ttu-id="216e9-137"><strong>Nota  </strong> Questa operazione si verificherà anche se non viene specificato alcun parametro di sistema.</span><span class="sxs-lookup"><span data-stu-id="216e9-137"><strong>Note  </strong>This will happen even if no system parameters are specified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="216e9-138">Se questa funzione ha esito positivo, il motore di database verrà configurato per l'esecuzione in modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="216e9-138">If this function succeeds, the database engine will be configured to run in multi-instance mode.</span></span> <span data-ttu-id="216e9-139">Anche il motore è stato configurato correttamente con l'elenco facoltativo di parametri di sistema globali.</span><span class="sxs-lookup"><span data-stu-id="216e9-139">The engine was also successfully configured with the optional list of global system parameters.</span></span>

<span data-ttu-id="216e9-140">Se questa funzione ha esito negativo, il motore di database rimarrà nella modalità corrente.</span><span class="sxs-lookup"><span data-stu-id="216e9-140">If this function fails, the database engine will remain in the current mode.</span></span> <span data-ttu-id="216e9-141">Se *pcsetsucceed* è diverso da zero, il numero di parametri di sistema rimarrà impostato.</span><span class="sxs-lookup"><span data-stu-id="216e9-141">If *pcsetsucceed* is non-zero, that number of system parameters will remain set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="216e9-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="216e9-142">Remarks</span></span>

<span data-ttu-id="216e9-143">Questa funzione deve essere utilizzata solo se l'applicazione deve configurare un determinato set di parametri di sistema in modo atomico quando si configura il motore di database per l'utilizzo in uno scenario multiutente nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="216e9-143">This function should only be used if the application must configure a given set of system parameters atomically when setting up the database engine for use in a multi-user scenario in the same process.</span></span> <span data-ttu-id="216e9-144">Se è disponibile un altro metodo di sincronizzazione, è preferibile chiamare [JetCreateInstance](./jetcreateinstance-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md) separatamente.</span><span class="sxs-lookup"><span data-stu-id="216e9-144">If another method of synchronization is available, it is preferable to call [JetCreateInstance](./jetcreateinstance-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) separately.</span></span>

#### <a name="requirements"></a><span data-ttu-id="216e9-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="216e9-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="216e9-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="216e9-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="216e9-147">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="216e9-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="216e9-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="216e9-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="216e9-149">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="216e9-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="216e9-150"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="216e9-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="216e9-151">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="216e9-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="216e9-152"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="216e9-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="216e9-153">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="216e9-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="216e9-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="216e9-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="216e9-155">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="216e9-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="216e9-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="216e9-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="216e9-157">Implementato come <strong>JetEnableMultiInstanceW</strong> (Unicode) e <strong>JetEnableMultiInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="216e9-157">Implemented as <strong>JetEnableMultiInstanceW</strong> (Unicode) and <strong>JetEnableMultiInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="216e9-158">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="216e9-158">See Also</span></span>

[<span data-ttu-id="216e9-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="216e9-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="216e9-160">JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="216e9-160">JET_SETSYSPARAM</span></span>](./jet-setsysparam-structure.md)  
[<span data-ttu-id="216e9-161">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="216e9-161">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="216e9-162">JetInit</span><span class="sxs-lookup"><span data-stu-id="216e9-162">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="216e9-163">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="216e9-163">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
