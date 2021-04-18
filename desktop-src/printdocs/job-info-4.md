---
description: Descrive un set completo di valori associati a un processo e supporta file di spooling di grandi dimensioni con dimensioni espresse con 64 bit.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: Struttura JOB_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5a6ccd7bf589ed341c9aceab86205cd9852c0896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318370"
---
# <a name="job_info_4-structure"></a><span data-ttu-id="87ce8-103">Struttura delle informazioni sul processo \_ \_ 4</span><span class="sxs-lookup"><span data-stu-id="87ce8-103">JOB\_INFO\_4 structure</span></span>

<span data-ttu-id="87ce8-104">Descrive un set completo di valori associati a un processo e supporta file di spooling di grandi dimensioni con dimensioni espresse con 64 bit.</span><span class="sxs-lookup"><span data-stu-id="87ce8-104">Describes a full set of values associated with a job and supports large spool files with sizes expressed with 64 bits.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ce8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87ce8-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_4 {
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
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a><span data-ttu-id="87ce8-106">Members</span><span class="sxs-lookup"><span data-stu-id="87ce8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="87ce8-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="87ce8-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-108">Valore dell'identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="87ce8-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-110">Puntatore a una stringa con terminazione null che specifica il nome della stampante per cui viene eseguito lo spooling del processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="87ce8-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-112">Puntatore a una stringa con terminazione null che specifica il nome del computer in cui è stato creato il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="87ce8-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="87ce8-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-114">Puntatore a una stringa con terminazione null che specifica il nome dell'utente proprietario del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="87ce8-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="87ce8-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-116">Puntatore a una stringa con terminazione null che specifica il nome del processo di stampa, ad esempio "MS-WORD: Review.doc".</span><span class="sxs-lookup"><span data-stu-id="87ce8-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-117">**pNotifyName**</span><span class="sxs-lookup"><span data-stu-id="87ce8-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-118">Puntatore a una stringa con terminazione null che specifica il nome dell'utente a cui deve essere inviata una notifica quando il processo è stato stampato oppure quando si verifica un errore durante la stampa del processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed, or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-119">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="87ce8-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-120">Puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzati per registrare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="87ce8-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-121">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="87ce8-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-122">Puntatore a una stringa con terminazione null che specifica il nome del processore di stampa da utilizzare per stampare il processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-123">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="87ce8-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-124">Puntatore a una stringa con terminazione null che specifica i parametri del processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="87ce8-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-125">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="87ce8-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-126">Puntatore a una stringa con terminazione null che specifica il nome del driver della stampante da utilizzare per elaborare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="87ce8-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-127">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="87ce8-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-128">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati dell'ambiente e dell'inizializzazione del dispositivo per il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="87ce8-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-129">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="87ce8-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-130">Puntatore a una stringa con terminazione null che specifica lo stato del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="87ce8-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="87ce8-131">Questo membro deve essere controllato prima **dello stato** e, se **pStatus** è **null**, lo stato viene definito dal contenuto del membro di stato.</span><span class="sxs-lookup"><span data-stu-id="87ce8-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-132">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="87ce8-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-133">Il valore di questo membro è **null**.</span><span class="sxs-lookup"><span data-stu-id="87ce8-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="87ce8-134">Il recupero e l'impostazione dei descrittori di sicurezza del documento non sono supportati in questa versione.</span><span class="sxs-lookup"><span data-stu-id="87ce8-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-135">**Status**</span><span class="sxs-lookup"><span data-stu-id="87ce8-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-136">Stato del processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-136">The job status.</span></span> <span data-ttu-id="87ce8-137">Il membro può essere costituito da uno o più dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="87ce8-137">This member can be one or more of the following values:</span></span>

| <span data-ttu-id="87ce8-138">Valore</span><span class="sxs-lookup"><span data-stu-id="87ce8-138">Value</span></span>                           | <span data-ttu-id="87ce8-139">Significato</span><span class="sxs-lookup"><span data-stu-id="87ce8-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="87ce8-140">\_stato processo \_ bloccato \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="87ce8-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="87ce8-141">Il driver non è in grado di stampare il processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="87ce8-142">\_stato processo \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="87ce8-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="87ce8-143">Il processo è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="87ce8-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="87ce8-144">\_eliminazione dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="87ce8-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="87ce8-145">È in corso l'eliminazione del processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="87ce8-146">\_errore di stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="87ce8-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="87ce8-147">Un errore è associato al processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="87ce8-148">stato del processo \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="87ce8-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="87ce8-149">La stampante è offline.</span><span class="sxs-lookup"><span data-stu-id="87ce8-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="87ce8-150">\_carta dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="87ce8-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="87ce8-151">Stampante esaurita.</span><span class="sxs-lookup"><span data-stu-id="87ce8-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="87ce8-152">\_stato processo \_ sospeso</span><span class="sxs-lookup"><span data-stu-id="87ce8-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="87ce8-153">Il processo è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="87ce8-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="87ce8-154">stato del processo \_ \_ stampato</span><span class="sxs-lookup"><span data-stu-id="87ce8-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="87ce8-155">Il processo è stato stampato.</span><span class="sxs-lookup"><span data-stu-id="87ce8-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="87ce8-156">\_stampa dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="87ce8-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="87ce8-157">Il processo viene stampato.</span><span class="sxs-lookup"><span data-stu-id="87ce8-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="87ce8-158">\_riavvio stato \_ processo</span><span class="sxs-lookup"><span data-stu-id="87ce8-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="87ce8-159">Il processo è stato riavviato.</span><span class="sxs-lookup"><span data-stu-id="87ce8-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="87ce8-160">\_spooling dello stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="87ce8-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="87ce8-161">Il processo sta effettuando lo spooling.</span><span class="sxs-lookup"><span data-stu-id="87ce8-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="87ce8-162">\_ \_ intervento dell'utente sullo stato del processo \_</span><span class="sxs-lookup"><span data-stu-id="87ce8-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="87ce8-163">La stampante presenta un errore che richiede all'utente di eseguire un'operazione.</span><span class="sxs-lookup"><span data-stu-id="87ce8-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="87ce8-164">In Windows XP e nelle versioni successive di Windows è possibile utilizzare anche i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="87ce8-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="87ce8-165">Valore</span><span class="sxs-lookup"><span data-stu-id="87ce8-165">Value</span></span>                 | <span data-ttu-id="87ce8-166">Significato</span><span class="sxs-lookup"><span data-stu-id="87ce8-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ce8-167">\_stato processo \_ completato</span><span class="sxs-lookup"><span data-stu-id="87ce8-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="87ce8-168">Il processo viene inviato alla stampante, ma potrebbe non essere ancora stampato.</span><span class="sxs-lookup"><span data-stu-id="87ce8-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="87ce8-169">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="87ce8-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="87ce8-170">stato del processo \_ \_ mantenuto</span><span class="sxs-lookup"><span data-stu-id="87ce8-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="87ce8-171">Il processo è stato mantenuto nella coda di stampa che segue la stampa.</span><span class="sxs-lookup"><span data-stu-id="87ce8-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="87ce8-172">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="87ce8-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-173">Priorità del processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-173">The job priority.</span></span> <span data-ttu-id="87ce8-174">Questo membro può essere uno dei valori seguenti o compreso tra 1 e 99 ( \_ priorità minima fino alla \_ priorità massima).</span><span class="sxs-lookup"><span data-stu-id="87ce8-174">This member can be one of the following values, or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="87ce8-175">Valore</span><span class="sxs-lookup"><span data-stu-id="87ce8-175">Value</span></span>         | <span data-ttu-id="87ce8-176">Significato</span><span class="sxs-lookup"><span data-stu-id="87ce8-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="87ce8-177">\_priorità minima</span><span class="sxs-lookup"><span data-stu-id="87ce8-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="87ce8-178">Priorità minima.</span><span class="sxs-lookup"><span data-stu-id="87ce8-178">Minimum priority.</span></span> |
| <span data-ttu-id="87ce8-179">\_priorità massima</span><span class="sxs-lookup"><span data-stu-id="87ce8-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="87ce8-180">Priorità massima.</span><span class="sxs-lookup"><span data-stu-id="87ce8-180">Maximum priority.</span></span> |
| <span data-ttu-id="87ce8-181">\_priorità def</span><span class="sxs-lookup"><span data-stu-id="87ce8-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="87ce8-182">Priorità predefinita.</span><span class="sxs-lookup"><span data-stu-id="87ce8-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="87ce8-183">**Position**</span><span class="sxs-lookup"><span data-stu-id="87ce8-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-184">Posizione del processo nella coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="87ce8-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="87ce8-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-186">La prima volta che il processo può essere stampato.</span><span class="sxs-lookup"><span data-stu-id="87ce8-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-187">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="87ce8-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-188">Ora più recente in cui è possibile stampare il processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="87ce8-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-190">Numero di pagine necessarie per il processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-190">The number of pages required for the job.</span></span> <span data-ttu-id="87ce8-191">Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.</span><span class="sxs-lookup"><span data-stu-id="87ce8-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-192">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="87ce8-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-193">I quattro byte inferiori delle dimensioni del processo, in byte.</span><span class="sxs-lookup"><span data-stu-id="87ce8-193">The lower four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="87ce8-194">Vedere anche il membro **SizeHigh** di seguito.</span><span class="sxs-lookup"><span data-stu-id="87ce8-194">See also the **SizeHigh** member below.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-195">**Inviata**</span><span class="sxs-lookup"><span data-stu-id="87ce8-195">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-196">Struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora in cui il processo è stato inviato.</span><span class="sxs-lookup"><span data-stu-id="87ce8-196">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="87ce8-197">Questo valore di ora è in formato UTC (Universal Time Coordinate).</span><span class="sxs-lookup"><span data-stu-id="87ce8-197">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="87ce8-198">È necessario convertirlo in un valore di ora locale prima di visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-198">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="87ce8-199">Per eseguire la conversione, è possibile usare la funzione [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) .</span><span class="sxs-lookup"><span data-stu-id="87ce8-199">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-200">**Time**</span><span class="sxs-lookup"><span data-stu-id="87ce8-200">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-201">Tempo totale, in millisecondi, trascorso dall'inizio della stampa del processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-201">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-202">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="87ce8-202">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-203">Numero di pagine stampate.</span><span class="sxs-lookup"><span data-stu-id="87ce8-203">The number of pages that have printed.</span></span> <span data-ttu-id="87ce8-204">Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.</span><span class="sxs-lookup"><span data-stu-id="87ce8-204">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="87ce8-205">**SizeHigh**</span><span class="sxs-lookup"><span data-stu-id="87ce8-205">**SizeHigh**</span></span>
</dt> <dd>

<span data-ttu-id="87ce8-206">I quattro byte più elevati della dimensione, in byte, del processo.</span><span class="sxs-lookup"><span data-stu-id="87ce8-206">The higher four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="87ce8-207">Vedere anche il membro delle **dimensioni** sopra riportato.</span><span class="sxs-lookup"><span data-stu-id="87ce8-207">See also the **Size** member above.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87ce8-208">Commenti</span><span class="sxs-lookup"><span data-stu-id="87ce8-208">Remarks</span></span>

<span data-ttu-id="87ce8-209">I monitoraggi porta che non supportano TrueEndOfJob imposteranno il processo quando lo \_ stato del processo verrà \_ stampato immediatamente dopo l'invio del processo alla stampante.</span><span class="sxs-lookup"><span data-stu-id="87ce8-209">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED immediately after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ce8-210">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87ce8-210">Requirements</span></span>



| <span data-ttu-id="87ce8-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ce8-211">Requirement</span></span> | <span data-ttu-id="87ce8-212">Valore</span><span class="sxs-lookup"><span data-stu-id="87ce8-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87ce8-213">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87ce8-213">Minimum supported client</span></span><br/> | <span data-ttu-id="87ce8-214">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87ce8-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="87ce8-215">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87ce8-215">Minimum supported server</span></span><br/> | <span data-ttu-id="87ce8-216">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87ce8-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87ce8-217">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87ce8-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ce8-218"><dt>Winspool. h</dt></span><span class="sxs-lookup"><span data-stu-id="87ce8-218"><dt>Winspool.h</dt></span></span> </dl> |
| <span data-ttu-id="87ce8-219">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="87ce8-219">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="87ce8-220">**\_ \_ Info processo \_ 4W** (Unicode) e **\_ informazioni sul processo \_ \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="87ce8-220">**\_JOB\_INFO\_4W** (Unicode) and **\_JOB\_INFO\_4A** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="87ce8-221">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87ce8-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ce8-222">Stampa</span><span class="sxs-lookup"><span data-stu-id="87ce8-222">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="87ce8-223">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="87ce8-223">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="87ce8-224">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="87ce8-224">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="87ce8-225">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="87ce8-225">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="87ce8-226">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="87ce8-226">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="87ce8-227">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="87ce8-227">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

