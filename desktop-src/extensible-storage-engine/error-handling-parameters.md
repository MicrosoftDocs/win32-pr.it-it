---
description: 'Altre informazioni su: parametri di gestione degli errori'
title: Parametri di gestione degli errori
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885378"
---
# <a name="error-handling-parameters"></a><span data-ttu-id="417e2-103">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="417e2-103">Error Handling Parameters</span></span>


<span data-ttu-id="417e2-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="417e2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="error-handling-parameters"></a><span data-ttu-id="417e2-105">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="417e2-105">Error Handling Parameters</span></span>

<span data-ttu-id="417e2-106">Questo argomento contiene i parametri utilizzati per la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="417e2-106">This topic contains parameters that are used for error handling.</span></span>

<span data-ttu-id="417e2-107">*JET_paramErrorToString* 70</span><span class="sxs-lookup"><span data-stu-id="417e2-107">*JET_paramErrorToString* 70</span></span>  

<span data-ttu-id="417e2-108">Questo parametro può essere usato per convertire un [JET_ERR](./jet-err.md) in una stringa.</span><span class="sxs-lookup"><span data-stu-id="417e2-108">This parameter can be used to convert a [JET_ERR](./jet-err.md) into a string.</span></span> <span data-ttu-id="417e2-109">Questa operazione viene eseguita tramite una chiamata speciale a [JetGetSystemParameter](./jetgetsystemparameter-function.md) in cui il buffer di output Integer contiene il valore [JET_ERR](./jet-err.md) da convertire (come parametro di input) e il buffer di output della stringa restituisce la stringa di errore corrispondente.</span><span class="sxs-lookup"><span data-stu-id="417e2-109">This is done using a special call to [JetGetSystemParameter](./jetgetsystemparameter-function.md) where the integer output buffer contains the [JET_ERR](./jet-err.md) value to be converted (as an input parameter) and the string output buffer returns the matching error string.</span></span> <span data-ttu-id="417e2-110">La stringa avrà un aspetto simile al seguente: "JET_errSuccess, operazione riuscita".</span><span class="sxs-lookup"><span data-stu-id="417e2-110">The string will look something like this: "JET_errSuccess,Successful Operation".</span></span> <span data-ttu-id="417e2-111">La stringa è costituita dal nome simbolico della stringa, quindi da una virgola e quindi da una semplice descrizione di testo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="417e2-111">The string is composed of the symbolic name for the string, then a comma, and then a simple text description of the error.</span></span> <span data-ttu-id="417e2-112">La stringa di descrizione può contenere virgole.</span><span class="sxs-lookup"><span data-stu-id="417e2-112">The description string may itself contain commas.</span></span> <span data-ttu-id="417e2-113">Se l'errore non viene riconosciuto, la stringa sarà "errore sconosciuto, errore sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="417e2-113">If the error is not recognized then the string will be "Unknown Error,Unknown Error".</span></span>

<span data-ttu-id="417e2-114">**Nota**  Questo parametro è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="417e2-114">**Note**  This parameter is read only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="417e2-115">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="417e2-115">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="417e2-116">Speciali</span><span class="sxs-lookup"><span data-stu-id="417e2-116">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-117">Digitare:</span><span class="sxs-lookup"><span data-stu-id="417e2-117">Type:</span></span></p></td>
<td><p><span data-ttu-id="417e2-118">Speciali</span><span class="sxs-lookup"><span data-stu-id="417e2-118">Special</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-119">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="417e2-119">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="417e2-120">Speciali</span><span class="sxs-lookup"><span data-stu-id="417e2-120">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-121">Ambito:</span><span class="sxs-lookup"><span data-stu-id="417e2-121">Scope:</span></span></p></td>
<td><p><span data-ttu-id="417e2-122">Globale</span><span class="sxs-lookup"><span data-stu-id="417e2-122">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-123">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="417e2-123">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="417e2-124">No</span><span class="sxs-lookup"><span data-stu-id="417e2-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-125">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="417e2-125">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="417e2-126">No</span><span class="sxs-lookup"><span data-stu-id="417e2-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-127">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="417e2-127">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="417e2-128">No</span><span class="sxs-lookup"><span data-stu-id="417e2-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-129">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="417e2-129">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="417e2-130">No</span><span class="sxs-lookup"><span data-stu-id="417e2-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-131">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="417e2-131">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="417e2-132">No</span><span class="sxs-lookup"><span data-stu-id="417e2-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-133">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="417e2-133">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="417e2-134">No</span><span class="sxs-lookup"><span data-stu-id="417e2-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-135">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="417e2-135">Availability:</span></span></p></td>
<td><p><span data-ttu-id="417e2-136">Tutti</span><span class="sxs-lookup"><span data-stu-id="417e2-136">All</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="417e2-137">*JET_paramExceptionAction*</span><span class="sxs-lookup"><span data-stu-id="417e2-137">*JET_paramExceptionAction*</span></span>  
<span data-ttu-id="417e2-138">98</span><span class="sxs-lookup"><span data-stu-id="417e2-138">98</span></span>  

<span data-ttu-id="417e2-139">Questo parametro controlla ciò che accade quando un'eccezione viene generata dal motore di database o dal codice chiamato dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="417e2-139">This parameter controls what happens when an exception is thrown by the database engine or code that is called by the database engine.</span></span> <span data-ttu-id="417e2-140">Se impostato su JET_ExceptionMsgBox, qualsiasi eccezione verrà generata al filtro eccezioni non gestite di Windows.</span><span class="sxs-lookup"><span data-stu-id="417e2-140">When set to JET_ExceptionMsgBox, any exception will be thrown to the Windows unhandled exception filter.</span></span> <span data-ttu-id="417e2-141">In questo modo l'eccezione viene gestita come un errore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="417e2-141">This will result in the exception being handled as an application failure.</span></span> <span data-ttu-id="417e2-142">Lo scopo è impedire che il codice dell'applicazione tenti erroneamente di rilevare e ignorare un'eccezione generata dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="417e2-142">The intent is to prevent application code from erroneously trying to catch and ignore an exception generated by the database engine.</span></span> <span data-ttu-id="417e2-143">Questa operazione non può essere consentita perché potrebbe verificarsi un danneggiamento del database.</span><span class="sxs-lookup"><span data-stu-id="417e2-143">This cannot be allowed because database corruption could occur.</span></span> <span data-ttu-id="417e2-144">Se l'applicazione desidera gestire correttamente queste eccezioni, è possibile disabilitare la protezione impostando questo parametro su JET_ExceptionNone.</span><span class="sxs-lookup"><span data-stu-id="417e2-144">If the application wishes to properly handle these exceptions then the protection can be disabled by setting this parameter to JET_ExceptionNone.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="417e2-145">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="417e2-145">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="417e2-146">JET_ExceptionMsgBox</span><span class="sxs-lookup"><span data-stu-id="417e2-146">JET_ExceptionMsgBox</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-147">Digitare:</span><span class="sxs-lookup"><span data-stu-id="417e2-147">Type:</span></span></p></td>
<td><p><span data-ttu-id="417e2-148">Integer</span><span class="sxs-lookup"><span data-stu-id="417e2-148">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-149">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="417e2-149">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="417e2-150">JET_ExceptionMsgBox, JET_ExceptionNone</span><span class="sxs-lookup"><span data-stu-id="417e2-150">JET_ExceptionMsgBox, JET_ExceptionNone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-151">Ambito:</span><span class="sxs-lookup"><span data-stu-id="417e2-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="417e2-152">Globale</span><span class="sxs-lookup"><span data-stu-id="417e2-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-153">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="417e2-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="417e2-154"><strong>Windows 2000, Windows XP e Windows Server 2003:  </strong>  No</span><span class="sxs-lookup"><span data-stu-id="417e2-154"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="417e2-155"><strong>Windows Vista:</strong>  Sì</span><span class="sxs-lookup"><span data-stu-id="417e2-155"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-156">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="417e2-156">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="417e2-157"><strong>Windows 2000, Windows XP e Windows Server 2003:  </strong>  No</span><span class="sxs-lookup"><span data-stu-id="417e2-157"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="417e2-158"><strong>Windows Vista:</strong>  Sì</span><span class="sxs-lookup"><span data-stu-id="417e2-158"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-159">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="417e2-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="417e2-160">No</span><span class="sxs-lookup"><span data-stu-id="417e2-160">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-161">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="417e2-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="417e2-162">Sì</span><span class="sxs-lookup"><span data-stu-id="417e2-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-163">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="417e2-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="417e2-164">No</span><span class="sxs-lookup"><span data-stu-id="417e2-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-165">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="417e2-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="417e2-166">No</span><span class="sxs-lookup"><span data-stu-id="417e2-166">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-167">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="417e2-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="417e2-168">Tutti</span><span class="sxs-lookup"><span data-stu-id="417e2-168">All</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="requirements"></a><span data-ttu-id="417e2-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="417e2-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="417e2-170"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="417e2-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="417e2-171">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="417e2-171">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="417e2-172"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="417e2-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="417e2-173">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="417e2-173">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="417e2-174"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="417e2-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="417e2-175">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="417e2-175">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a><span data-ttu-id="417e2-176">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="417e2-176">See Also</span></span>

[<span data-ttu-id="417e2-177">Costanti di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="417e2-177">Error Handling Constants</span></span>](./error-handling-constants.md)  
[<span data-ttu-id="417e2-178">Codici di errore di Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="417e2-178">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="417e2-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="417e2-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="417e2-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="417e2-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="417e2-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="417e2-181">JetInit</span></span>](./jetinit-function.md)
