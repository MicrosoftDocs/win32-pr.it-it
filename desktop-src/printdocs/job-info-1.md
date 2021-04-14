---
description: La \_ struttura info processo \_ 1 specifica le informazioni sul processo di stampa, ad esempio il valore dell'identificatore del processo, il nome della stampante per cui viene eseguito lo spooling del processo, il nome del computer in cui è stato creato il processo di stampa, il nome dell'utente proprietario del processo di stampa e così via.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: Struttura JOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349081"
---
# <a name="job_info_1-structure"></a><span data-ttu-id="ce2e7-103">Struttura di informazioni sul processo \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="ce2e7-103">JOB\_INFO\_1 structure</span></span>

<span data-ttu-id="ce2e7-104">La **struttura \_ info processo \_ 1** specifica le informazioni sul processo di stampa, ad esempio il valore dell'identificatore del processo, il nome della stampante per cui viene eseguito lo spooling del processo, il nome del computer in cui è stato creato il processo di stampa, il nome dell'utente proprietario del processo di stampa e così via.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-104">The **JOB\_INFO\_1** structure specifies print-job information such as the job-identifier value, the name of the printer for which the job is spooled, the name of the machine that created the print job, the name of the user that owns the print job, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce2e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce2e7-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="ce2e7-106">Members</span><span class="sxs-lookup"><span data-stu-id="ce2e7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce2e7-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-108">Identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-108">A job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-110">Puntatore a una stringa con terminazione null che specifica il nome della stampante per cui viene eseguito lo spooling del processo.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-112">Puntatore a una stringa con terminazione null che specifica il nome del computer in cui è stato creato il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-114">Puntatore a una stringa con terminazione null che specifica il nome dell'utente proprietario del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-114">A pointer to a null-terminated string that specifies the name of the user that owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-116">Puntatore a una stringa con terminazione null che specifica il nome del processo di stampa, ad esempio "MS-WORD: Review.doc".</span><span class="sxs-lookup"><span data-stu-id="ce2e7-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-117">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-117">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-118">Puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzati per registrare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-118">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-119">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-119">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-120">Puntatore a una stringa con terminazione null che specifica lo stato del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-120">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="ce2e7-121">Questo membro deve essere controllato prima *dello stato* e, se *pStatus* è **null**, lo stato viene definito dal contenuto del membro di stato.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-121">This member should be checked prior to *Status* and, if *pStatus* is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-122">**Status**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-122">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-123">Stato del processo.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-123">The job status.</span></span> <span data-ttu-id="ce2e7-124">Il valore di questo membro può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-124">The value of this member can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="ce2e7-125">Un valore pari a zero indica che la coda di stampa è stata sospesa al termine dello spooling del documento.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-125">A value of zero indicates that the print queue was paused after the document finished spooling.</span></span>



| <span data-ttu-id="ce2e7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ce2e7-126">Value</span></span>                           | <span data-ttu-id="ce2e7-127">Significato</span><span class="sxs-lookup"><span data-stu-id="ce2e7-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2e7-128">\_stato processo \_ bloccato \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="ce2e7-128">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="ce2e7-129">Il driver non è in grado di stampare il processo.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-129">The driver cannot print the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ce2e7-130">\_stato processo \_ completato</span><span class="sxs-lookup"><span data-stu-id="ce2e7-130">JOB\_STATUS\_COMPLETE</span></span>           | <span data-ttu-id="ce2e7-131">**Windows XP e versioni successive:** Il processo viene inviato alla stampante, ma il processo potrebbe non essere ancora stampato.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-131">**Windows XP and later:** Job is sent to the printer, but the job may not be printed yet.</span></span><br/> <span data-ttu-id="ce2e7-132">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-132">See Remarks for more information.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ce2e7-133">\_stato processo \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="ce2e7-133">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="ce2e7-134">Il processo è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-134">Job has been deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ce2e7-135">\_eliminazione dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="ce2e7-135">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="ce2e7-136">È in corso l'eliminazione del processo.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-136">Job is being deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ce2e7-137">\_errore di stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="ce2e7-137">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="ce2e7-138">Un errore è associato al processo.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-138">An error is associated with the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ce2e7-139">stato del processo \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="ce2e7-139">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="ce2e7-140">La stampante è offline.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-140">Printer is offline.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ce2e7-141">\_carta dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="ce2e7-141">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="ce2e7-142">Stampante esaurita.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-142">Printer is out of paper.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ce2e7-143">\_stato processo \_ sospeso</span><span class="sxs-lookup"><span data-stu-id="ce2e7-143">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="ce2e7-144">Il processo è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-144">Job is paused.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ce2e7-145">stato del processo \_ \_ stampato</span><span class="sxs-lookup"><span data-stu-id="ce2e7-145">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="ce2e7-146">Il processo è stato stampato.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-146">Job has printed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ce2e7-147">\_stampa dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="ce2e7-147">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="ce2e7-148">Il processo viene stampato.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-148">Job is printing.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ce2e7-149">\_riavvio stato \_ processo</span><span class="sxs-lookup"><span data-stu-id="ce2e7-149">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="ce2e7-150">Il processo è stato riavviato.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-150">Job has been restarted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ce2e7-151">stato del processo \_ \_ mantenuto</span><span class="sxs-lookup"><span data-stu-id="ce2e7-151">JOB\_STATUS\_RETAINED</span></span>           | <span data-ttu-id="ce2e7-152">**Windows Vista e versioni successive:** Il processo è stato mantenuto nella coda di stampa e non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-152">**Windows Vista and later:** Job has been retained in the print queue and cannot be deleted.</span></span> <span data-ttu-id="ce2e7-153">Ciò può essere causato dai seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="ce2e7-153">This can be caused by the following:</span></span><br/> <span data-ttu-id="ce2e7-154">1) il processo è stato mantenuto manualmente da una chiamata a SetJob e lo spooler è in attesa del rilascio del processo.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-154">1) The job was manually retained by a call to SetJob and the spooler is waiting for the job to be released.</span></span><br/> <span data-ttu-id="ce2e7-155">2) il processo non ha completato la stampa e deve terminare la stampa prima di poter essere eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-155">2) The job has not finished printing and must finish printing before it can be automatically deleted.</span></span><br/> <span data-ttu-id="ce2e7-156">Per ulteriori informazioni sui comandi dei processi di stampa, vedere [**SetJob**](setjob.md) .</span><span class="sxs-lookup"><span data-stu-id="ce2e7-156">See [**SetJob**](setjob.md) for more information about print job commands.</span></span><br/> |
| <span data-ttu-id="ce2e7-157">\_spooling dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="ce2e7-157">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="ce2e7-158">Il processo sta effettuando lo spooling.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-158">Job is spooling.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ce2e7-159">\_ \_ intervento dell'utente sullo stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="ce2e7-159">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="ce2e7-160">La stampante presenta un errore che richiede all'utente di eseguire un'operazione.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-160">Printer has an error that requires the user to do something.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="ce2e7-161">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-161">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-162">Priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-162">The job priority.</span></span> <span data-ttu-id="ce2e7-163">Questo membro può essere uno dei valori seguenti o compreso tra 1 e 99 ( \_ priorità minima tramite \_ priorità massima).</span><span class="sxs-lookup"><span data-stu-id="ce2e7-163">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="ce2e7-164">Valore</span><span class="sxs-lookup"><span data-stu-id="ce2e7-164">Value</span></span>         | <span data-ttu-id="ce2e7-165">Significato</span><span class="sxs-lookup"><span data-stu-id="ce2e7-165">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="ce2e7-166">\_priorità minima</span><span class="sxs-lookup"><span data-stu-id="ce2e7-166">MIN\_PRIORITY</span></span> | <span data-ttu-id="ce2e7-167">Priorità minima.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-167">Minimum priority.</span></span> |
| <span data-ttu-id="ce2e7-168">\_priorità massima</span><span class="sxs-lookup"><span data-stu-id="ce2e7-168">MAX\_PRIORITY</span></span> | <span data-ttu-id="ce2e7-169">Priorità massima.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-169">Maximum priority.</span></span> |
| <span data-ttu-id="ce2e7-170">\_priorità def</span><span class="sxs-lookup"><span data-stu-id="ce2e7-170">DEF\_PRIORITY</span></span> | <span data-ttu-id="ce2e7-171">Priorità predefinita.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-171">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ce2e7-172">**Position**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-172">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-173">Posizione del processo nella coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-173">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-174">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-174">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-175">Numero totale di pagine contenute nel documento.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-175">The total number of pages that the document contains.</span></span> <span data-ttu-id="ce2e7-176">Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-176">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-177">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-177">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-178">Numero di pagine stampate.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-178">The number of pages that have printed.</span></span> <span data-ttu-id="ce2e7-179">Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-179">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="ce2e7-180">**Inviata**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-180">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="ce2e7-181">Struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora in cui è stato eseguito lo spooling del documento.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-181">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time that this document was spooled.</span></span>

<span data-ttu-id="ce2e7-182">Questo valore di ora è in formato UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="ce2e7-182">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="ce2e7-183">È necessario convertirlo in un valore di ora locale prima di visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-183">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="ce2e7-184">Per eseguire la conversione, è possibile usare la funzione [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) .</span><span class="sxs-lookup"><span data-stu-id="ce2e7-184">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce2e7-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce2e7-185">Remarks</span></span>

<span data-ttu-id="ce2e7-186">I monitoraggi porta che non supportano TrueEndOfJob imposteranno il processo in modo che lo stato del processo \_ \_ venga stampato subito dopo l'invio del processo alla stampante.</span><span class="sxs-lookup"><span data-stu-id="ce2e7-186">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce2e7-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce2e7-187">Requirements</span></span>



| <span data-ttu-id="ce2e7-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce2e7-188">Requirement</span></span> | <span data-ttu-id="ce2e7-189">Valore</span><span class="sxs-lookup"><span data-stu-id="ce2e7-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2e7-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce2e7-190">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2e7-191">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce2e7-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ce2e7-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce2e7-192">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2e7-193">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce2e7-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce2e7-194">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce2e7-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce2e7-195"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce2e7-195"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ce2e7-196">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ce2e7-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce2e7-197">**\_ \_ Info processo \_ 1W** (Unicode) e **\_ informazioni sul processo \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ce2e7-197">**\_JOB\_INFO\_1W** (Unicode) and **\_JOB\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="ce2e7-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce2e7-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce2e7-199">Stampa</span><span class="sxs-lookup"><span data-stu-id="ce2e7-199">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ce2e7-200">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="ce2e7-200">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ce2e7-201">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-201">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="ce2e7-202">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-202">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="ce2e7-203">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="ce2e7-203">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

