---
description: La \_ struttura di informazioni sul processo \_ 2 descrive un set completo di valori associati a un processo.
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: Struttura JOB_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_2
- _JOB_INFO_2A
- _JOB_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d6b582267afceb01fd7ced7d6d46144664bb9d2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233723"
---
# <a name="job_info_2-structure"></a><span data-ttu-id="8a7c2-103">Struttura di informazioni sul processo \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="8a7c2-103">JOB\_INFO\_2 structure</span></span>

<span data-ttu-id="8a7c2-104">La struttura di **informazioni sul processo \_ \_ 2** descrive un set completo di valori associati a un processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-104">The **JOB\_INFO\_2** structure describes a full set of values associated with a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7c2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a7c2-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_2 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
} JOB_INFO_2, *PJOB_INFO_2;
```



## <a name="members"></a><span data-ttu-id="8a7c2-106">Members</span><span class="sxs-lookup"><span data-stu-id="8a7c2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a7c2-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-108">Valore dell'identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-110">Puntatore a una stringa con terminazione null che specifica il nome della stampante per cui viene eseguito lo spooling del processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-112">Puntatore a una stringa con terminazione null che specifica il nome del computer in cui è stato creato il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-114">Puntatore a una stringa con terminazione null che specifica il nome dell'utente proprietario del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-116">Puntatore a una stringa con terminazione null che specifica il nome del processo di stampa, ad esempio "MS-WORD: Review.doc".</span><span class="sxs-lookup"><span data-stu-id="8a7c2-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-117">**pNotifyName**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-118">Puntatore a una stringa con terminazione null che specifica il nome dell'utente che deve ricevere una notifica quando il processo è stato stampato o quando si verifica un errore durante la stampa del processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-119">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-120">Puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzati per registrare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-121">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-122">Puntatore a una stringa con terminazione null che specifica il nome del processore di stampa da utilizzare per stampare il processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-123">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-124">Puntatore a una stringa con terminazione null che specifica i parametri del processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-125">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-126">Puntatore a una stringa con terminazione null che specifica il nome del driver della stampante da utilizzare per elaborare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-127">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-128">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati dell'ambiente e dell'inizializzazione del dispositivo per il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-129">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-130">Puntatore a una stringa con terminazione null che specifica lo stato del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="8a7c2-131">Questo membro deve essere controllato prima **dello stato** e, se **pStatus** è **null**, lo stato viene definito dal contenuto del membro di stato.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-132">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-133">Il valore di questo membro è **null**.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="8a7c2-134">Il recupero e l'impostazione dei descrittori di sicurezza del documento non sono supportati in questa versione.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-136">Stato del processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-136">The job status.</span></span> <span data-ttu-id="8a7c2-137">Il membro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-137">This member can be one or more of the following values.</span></span>

| <span data-ttu-id="8a7c2-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7c2-138">Value</span></span>                           | <span data-ttu-id="8a7c2-139">Significato</span><span class="sxs-lookup"><span data-stu-id="8a7c2-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8a7c2-140">\_stato processo \_ bloccato \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="8a7c2-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="8a7c2-141">Il driver non è in grado di stampare il processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="8a7c2-142">\_stato processo \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="8a7c2-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="8a7c2-143">Il processo è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="8a7c2-144">\_eliminazione dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="8a7c2-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="8a7c2-145">È in corso l'eliminazione del processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="8a7c2-146">\_errore di stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="8a7c2-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="8a7c2-147">Un errore è associato al processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="8a7c2-148">stato del processo \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="8a7c2-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="8a7c2-149">La stampante è offline.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="8a7c2-150">\_carta dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="8a7c2-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="8a7c2-151">Stampante esaurita.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="8a7c2-152">\_stato processo \_ sospeso</span><span class="sxs-lookup"><span data-stu-id="8a7c2-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="8a7c2-153">Il processo è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="8a7c2-154">stato del processo \_ \_ stampato</span><span class="sxs-lookup"><span data-stu-id="8a7c2-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="8a7c2-155">Il processo è stato stampato.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="8a7c2-156">\_stampa dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="8a7c2-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="8a7c2-157">Il processo viene stampato.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="8a7c2-158">\_riavvio stato \_ processo</span><span class="sxs-lookup"><span data-stu-id="8a7c2-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="8a7c2-159">Il processo è stato riavviato.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="8a7c2-160">\_spooling dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="8a7c2-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="8a7c2-161">Il processo sta effettuando lo spooling.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="8a7c2-162">\_ \_ intervento dell'utente sullo stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="8a7c2-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="8a7c2-163">La stampante presenta un errore che richiede all'utente di eseguire un'operazione.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="8a7c2-164">In Windows XP e nelle versioni successive di Windows è possibile utilizzare anche i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a7c2-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="8a7c2-165">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7c2-165">Value</span></span>                 | <span data-ttu-id="8a7c2-166">Significato</span><span class="sxs-lookup"><span data-stu-id="8a7c2-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7c2-167">\_stato processo \_ completato</span><span class="sxs-lookup"><span data-stu-id="8a7c2-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="8a7c2-168">Il processo viene inviato alla stampante, ma potrebbe non essere ancora stampato.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="8a7c2-169">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="8a7c2-170">stato del processo \_ \_ mantenuto</span><span class="sxs-lookup"><span data-stu-id="8a7c2-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="8a7c2-171">Il processo è stato mantenuto nella coda di stampa che segue la stampa.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="8a7c2-172">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-173">Priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-173">The job priority.</span></span> <span data-ttu-id="8a7c2-174">Questo membro può essere uno dei valori seguenti o compreso tra 1 e 99 ( \_ priorità minima tramite \_ priorità massima).</span><span class="sxs-lookup"><span data-stu-id="8a7c2-174">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="8a7c2-175">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7c2-175">Value</span></span>         | <span data-ttu-id="8a7c2-176">Significato</span><span class="sxs-lookup"><span data-stu-id="8a7c2-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="8a7c2-177">\_priorità minima</span><span class="sxs-lookup"><span data-stu-id="8a7c2-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="8a7c2-178">Priorità minima.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-178">Minimum priority.</span></span> |
| <span data-ttu-id="8a7c2-179">\_priorità massima</span><span class="sxs-lookup"><span data-stu-id="8a7c2-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="8a7c2-180">Priorità massima.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-180">Maximum priority.</span></span> |
| <span data-ttu-id="8a7c2-181">\_priorità def</span><span class="sxs-lookup"><span data-stu-id="8a7c2-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="8a7c2-182">Priorità predefinita.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8a7c2-183">**Position**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-184">Posizione del processo nella coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-186">La prima volta che il processo può essere stampato.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-187">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-188">Ora più recente in cui è possibile stampare il processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-190">Numero di pagine necessarie per il processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-190">The number of pages required for the job.</span></span> <span data-ttu-id="8a7c2-191">Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-192">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-193">Dimensione, in byte, del processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-193">The size, in bytes, of the job.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-194">**Inviata**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-194">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-195">Struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora in cui il processo è stato inviato.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-195">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="8a7c2-196">Questo valore di ora è in formato UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="8a7c2-196">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="8a7c2-197">È necessario convertirlo in un valore di ora locale prima di visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-197">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="8a7c2-198">Per eseguire la conversione, è possibile usare la funzione [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) .</span><span class="sxs-lookup"><span data-stu-id="8a7c2-198">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-199">**Time**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-199">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-200">Tempo totale, in millisecondi, trascorso dall'inizio della stampa del processo.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-200">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="8a7c2-201">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-201">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="8a7c2-202">Numero di pagine stampate.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-202">The number of pages that have printed.</span></span> <span data-ttu-id="8a7c2-203">Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-203">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a7c2-204">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a7c2-204">Remarks</span></span>

<span data-ttu-id="8a7c2-205">I monitoraggi porta che non supportano TrueEndOfJob imposteranno il processo in modo che lo stato del processo \_ \_ venga stampato subito dopo l'invio del processo alla stampante.</span><span class="sxs-lookup"><span data-stu-id="8a7c2-205">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a7c2-206">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a7c2-206">Requirements</span></span>



| <span data-ttu-id="8a7c2-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a7c2-207">Requirement</span></span> | <span data-ttu-id="8a7c2-208">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7c2-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7c2-209">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a7c2-209">Minimum supported client</span></span><br/> | <span data-ttu-id="8a7c2-210">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8a7c2-210">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8a7c2-211">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a7c2-211">Minimum supported server</span></span><br/> | <span data-ttu-id="8a7c2-212">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8a7c2-212">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8a7c2-213">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a7c2-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a7c2-214"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a7c2-214"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8a7c2-215">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8a7c2-215">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8a7c2-216">**\_ \_ Info processo \_ 2W** (Unicode) e **\_ informazioni sul processo \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8a7c2-216">**\_JOB\_INFO\_2W** (Unicode) and **\_JOB\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="8a7c2-217">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a7c2-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7c2-218">Stampa</span><span class="sxs-lookup"><span data-stu-id="8a7c2-218">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8a7c2-219">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="8a7c2-219">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="8a7c2-220">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-220">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="8a7c2-221">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-221">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="8a7c2-222">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-222">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="8a7c2-223">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="8a7c2-223">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

