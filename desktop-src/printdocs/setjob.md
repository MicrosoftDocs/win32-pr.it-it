---
description: La funzione SetJob sospende, riprende, Annulla o riavvia un processo di stampa su una stampante specificata. È inoltre possibile utilizzare la funzione SetJob per impostare i parametri del processo di stampa, ad esempio la priorità del processo di stampa e il nome del documento.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Funzione SetJob (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314979"
---
# <a name="setjob-function"></a><span data-ttu-id="d1596-104">SetJob (funzione)</span><span class="sxs-lookup"><span data-stu-id="d1596-104">SetJob function</span></span>

<span data-ttu-id="d1596-105">La funzione **SetJob** sospende, riprende, Annulla o riavvia un processo di stampa su una stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="d1596-105">The **SetJob** function pauses, resumes, cancels, or restarts a print job on a specified printer.</span></span> <span data-ttu-id="d1596-106">È inoltre possibile utilizzare la funzione **SetJob** per impostare i parametri del processo di stampa, ad esempio la priorità del processo di stampa e il nome del documento.</span><span class="sxs-lookup"><span data-stu-id="d1596-106">You can also use the **SetJob** function to set print job parameters, such as the print job priority and the document name.</span></span>

<span data-ttu-id="d1596-107">È possibile utilizzare la funzione **SetJob** per fornire un comando a un processo di stampa o per impostare i parametri del processo di stampa oppure per eseguire entrambe le operazioni nella stessa chiamata.</span><span class="sxs-lookup"><span data-stu-id="d1596-107">You can use the **SetJob** function to give a command to a print job, or to set print job parameters, or to do both in the same call.</span></span> <span data-ttu-id="d1596-108">Il valore del parametro *Command* non influisce sul modo in cui la funzione usa i parametri *Level* e *pJob* .</span><span class="sxs-lookup"><span data-stu-id="d1596-108">The value of the *Command* parameter does not affect how the function uses the *Level* and *pJob* parameters.</span></span> <span data-ttu-id="d1596-109">Inoltre, è possibile usare **SetJob** con [**informazioni sul processo \_ \_ 3**](job-info-3.md) per collegare insieme un set di processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-109">Also, you can use **SetJob** with [**JOB\_INFO\_3**](job-info-3.md) to link together a set of print jobs.</span></span> <span data-ttu-id="d1596-110">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d1596-110">See Remarks for more information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1596-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1596-111">Syntax</span></span>


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="d1596-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1596-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1596-113">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1596-113">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1596-114">Handle per l'oggetto stampante di interesse.</span><span class="sxs-lookup"><span data-stu-id="d1596-114">A handle to the printer object of interest.</span></span> <span data-ttu-id="d1596-115">Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="d1596-115">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="d1596-116">*JobID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1596-116">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1596-117">Identificatore che specifica il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-117">Identifier that specifies the print job.</span></span> <span data-ttu-id="d1596-118">È possibile ottenere un identificatore del processo di stampa chiamando la funzione [**AddJob**](addjob.md) o [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .</span><span class="sxs-lookup"><span data-stu-id="d1596-118">You obtain a print job identifier by calling the [**AddJob**](addjob.md) function or the [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function.</span></span>

<span data-ttu-id="d1596-119">Se il parametro *Level* è impostato su 3, il parametro *JobID* deve corrispondere al membro **JobID** della struttura [**Job \_ info \_ 3**](job-info-3.md) a cui punta *pJob*</span><span class="sxs-lookup"><span data-stu-id="d1596-119">If the *Level* parameter is set to 3, the *JobId* parameter must match the **JobId** member of the [**JOB\_INFO\_3**](job-info-3.md) structure pointed to by *pJob*</span></span>

</dd> <dt>

<span data-ttu-id="d1596-120">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d1596-120">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1596-121">Tipo di struttura delle informazioni sul processo a cui punta il parametro *pJob* .</span><span class="sxs-lookup"><span data-stu-id="d1596-121">The type of job information structure pointed to by the *pJob* parameter.</span></span>

<span data-ttu-id="d1596-122">**Tutte le versioni di Windows**: è possibile impostare il parametro *Level* su 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="d1596-122">**All versions of Windows**: You can set the *Level* parameter to 0, 1, or 2.</span></span> <span data-ttu-id="d1596-123">Quando si imposta *Level* su 0, *PJob* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d1596-123">When you set *Level* to 0, *pJob* should be **NULL**.</span></span> <span data-ttu-id="d1596-124">Usare questi valori quando non si imposta alcun parametro del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-124">Use these values when you are not setting any print job parameters.</span></span>

<span data-ttu-id="d1596-125">È anche possibile impostare il parametro *Level* su 3.</span><span class="sxs-lookup"><span data-stu-id="d1596-125">You can also set the *Level* parameter to 3.</span></span>

<span data-ttu-id="d1596-126">A partire da **Windows Vista**: è anche possibile impostare il parametro *Level* su 4.</span><span class="sxs-lookup"><span data-stu-id="d1596-126">Starting with **Windows Vista**: You can also set the *Level* parameter to 4.</span></span>

</dd> <dt>

<span data-ttu-id="d1596-127">*pJob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1596-127">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1596-128">Puntatore a una struttura che imposta i parametri del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-128">A pointer to a structure that sets the print job parameters.</span></span>

<span data-ttu-id="d1596-129">**Tutte le versioni di Windows**: *pJob* può puntare a una struttura di job info [**\_ \_ 1**](job-info-1.md) o [**Job \_ info \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="d1596-129">**All versions of Windows**: *pJob* can point to a [**JOB\_INFO\_1**](job-info-1.md) or [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

<span data-ttu-id="d1596-130">*pJob* può puntare anche a una struttura di [**informazioni sul processo \_ \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="d1596-130">*pJob* can also point to a [**JOB\_INFO\_3**](job-info-3.md) structure.</span></span> <span data-ttu-id="d1596-131">È necessario disporre dell'autorizzazione di accesso per l' **\_ \_ Amministrazione** dell'accesso ai processi specificati dai membri **JobID** e **NextJobId** della struttura di **informazioni sul processo \_ \_ 3** .</span><span class="sxs-lookup"><span data-stu-id="d1596-131">You must have **JOB\_ACCESS\_ADMINISTER** access permission for the jobs specified by the **JobId** and **NextJobId** members of the **JOB\_INFO\_3** structure.</span></span>

<span data-ttu-id="d1596-132">A partire da **Windows Vista**: *pJob* può puntare anche a una struttura di [**informazioni sul processo \_ \_ 4**](job-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="d1596-132">Starting with **Windows Vista**: *pJob* can also point to a [**JOB\_INFO\_4**](job-info-4.md) structure.</span></span>

<span data-ttu-id="d1596-133">Se il parametro *Level* è 0, *PJob* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d1596-133">If the *Level* parameter is 0, *pJob* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d1596-134">*Comando* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1596-134">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1596-135">Operazione di stampa del processo da eseguire.</span><span class="sxs-lookup"><span data-stu-id="d1596-135">The print job operation to perform.</span></span> <span data-ttu-id="d1596-136">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d1596-136">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d1596-137">Valore</span><span class="sxs-lookup"><span data-stu-id="d1596-137">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="d1596-138">Significato</span><span class="sxs-lookup"><span data-stu-id="d1596-138">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <span data-ttu-id="d1596-139"><dt>**\_annullamento controllo \_ processo**</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-139"><dt>**JOB\_CONTROL\_CANCEL**</dt></span></span> </dl>                                    | <span data-ttu-id="d1596-140">Non usare.</span><span class="sxs-lookup"><span data-stu-id="d1596-140">Do not use.</span></span> <span data-ttu-id="d1596-141">Per eliminare un processo di stampa, utilizzare il **controllo del processo \_ \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="d1596-141">To delete a print job, use **JOB\_CONTROL\_DELETE**.</span></span><br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <span data-ttu-id="d1596-142"><dt>**\_pausa controllo \_ processo**</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-142"><dt>**JOB\_CONTROL\_PAUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="d1596-143">Sospendere il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-143">Pause the print job.</span></span><br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <span data-ttu-id="d1596-144"><dt>**\_riavvio del controllo processo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-144"><dt>**JOB\_CONTROL\_RESTART**</dt></span></span> </dl>                                 | <span data-ttu-id="d1596-145">Riavviare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-145">Restart the print job.</span></span> <span data-ttu-id="d1596-146">Un processo può essere riavviato solo se è stato stampato.</span><span class="sxs-lookup"><span data-stu-id="d1596-146">A job can only be restarted if it was printing.</span></span><br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <span data-ttu-id="d1596-147"><dt>**\_ripresa controllo \_ processo**</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-147"><dt>**JOB\_CONTROL\_RESUME**</dt></span></span> </dl>                                    | <span data-ttu-id="d1596-148">Riprendere un processo di stampa in pausa.</span><span class="sxs-lookup"><span data-stu-id="d1596-148">Resume a paused print job.</span></span><br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <span data-ttu-id="d1596-149"><dt>**\_eliminazione controllo \_ processo**</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-149"><dt>**JOB\_CONTROL\_DELETE**</dt></span></span> </dl>                                    | <span data-ttu-id="d1596-150">Eliminare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-150">Delete the print job.</span></span><br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <span data-ttu-id="d1596-151"><dt>**\_controllo processo \_ inviato \_ alla \_ stampante**</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-151"><dt>**JOB\_CONTROL\_SENT\_TO\_PRINTER**</dt></span></span> </dl>       | <span data-ttu-id="d1596-152">Utilizzato dai monitoraggi porta per terminare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-152">Used by port monitors to end the print job.</span></span><br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <span data-ttu-id="d1596-153"><dt>**\_ultima pagina di controllo processo \_ \_ \_ espellata**</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-153"><dt>**JOB\_CONTROL\_LAST\_PAGE\_EJECTED**</dt></span></span> </dl> | <span data-ttu-id="d1596-154">Utilizzato dai monitoraggi della lingua per terminare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-154">Used by language monitors to end the print job.</span></span><br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <span data-ttu-id="d1596-155"><dt>**\_mantenimento del controllo del processo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-155"><dt>**JOB\_CONTROL\_RETAIN**</dt></span></span> </dl>                                    | <span data-ttu-id="d1596-156">**Windows Vista e versioni successive**: Mantieni il processo nella coda dopo la stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-156">**Windows Vista and later**: Keep the job in the queue after it prints.</span></span><br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <span data-ttu-id="d1596-157"><dt>**\_versione controllo \_ processo**</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-157"><dt>**JOB\_CONTROL\_RELEASE**</dt></span></span> </dl>                                 | <span data-ttu-id="d1596-158">**Windows Vista e versioni successive**: rilasciare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-158">**Windows Vista and later**: Release the print job.</span></span><br/>                     |



 

<span data-ttu-id="d1596-159">È possibile utilizzare la stessa chiamata alla funzione **SetJob** per impostare i parametri del processo di stampa e per fornire un comando a un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d1596-159">You can use the same call to the **SetJob** function to set print job parameters and to give a command to a print job.</span></span> <span data-ttu-id="d1596-160">Pertanto, il *comando* non deve essere 0 se si imposta i parametri del processo di stampa, sebbene possa essere.</span><span class="sxs-lookup"><span data-stu-id="d1596-160">Thus, *Command* does not need to be 0 if you are setting print job parameters, although it can be.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1596-161">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1596-161">Return value</span></span>

<span data-ttu-id="d1596-162">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="d1596-162">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d1596-163">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="d1596-163">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1596-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1596-164">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d1596-165">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="d1596-165">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d1596-166">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1596-166">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d1596-167">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="d1596-167">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d1596-168">È possibile utilizzare la **funzione SetJob** per impostare vari parametri del processo di stampa fornendo un puntatore a un [**processo di \_ informazioni \_ 1**](job-info-1.md), informazioni sul processo [**\_ \_ 2**](job-info-2.md), informazioni sul [**processo \_ \_ 3**](job-info-3.md)o struttura di informazioni sul [**processo \_ \_ 4**](job-info-4.md) contenente i dati necessari.</span><span class="sxs-lookup"><span data-stu-id="d1596-168">You can use the **SetJob** function to set various print job parameters by supplying a pointer to a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), [**JOB\_INFO\_3**](job-info-3.md), or [**JOB\_INFO\_4**](job-info-4.md) structure that contains the necessary data.</span></span>

<span data-ttu-id="d1596-169">Per rimuovere o eliminare tutti i processi di stampa per una particolare stampante, chiamare la funzione [**Seprinter**](setprinter.md) con il parametro *Command* impostato sul **controllo della stampante \_ \_ Purge**.</span><span class="sxs-lookup"><span data-stu-id="d1596-169">To remove or delete all of the print jobs for a particular printer, call the [**SetPrinter**](setprinter.md) function with its *Command* parameter set to **PRINTER\_CONTROL\_PURGE**.</span></span>

<span data-ttu-id="d1596-170">I membri seguenti di una struttura di informazioni sul processo [**\_ \_ 1**](job-info-1.md), [**informazioni sul processo \_ \_ 2**](job-info-2.md)o [**informazioni sul processo \_ \_ 4**](job-info-4.md) vengono ignorati in una chiamata a **SetJob**: **JobID**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **size**, **inviato**, **ora** e **TotalPages**.</span><span class="sxs-lookup"><span data-stu-id="d1596-170">The following members of a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure are ignored on a call to **SetJob**: **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted**, **Time**, and **TotalPages**.</span></span>

<span data-ttu-id="d1596-171">Per modificare la posizione di un processo di stampa nella coda di stampa, è necessario disporre dell'autorizzazione di accesso per **la stampante. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d1596-171">You must have **PRINTER\_ACCESS\_ADMINISTER** access permission for a printer in order to change a print job's position in the print queue.</span></span>

<span data-ttu-id="d1596-172">Se non si desidera impostare la posizione di un processo di stampa nella coda di stampa, è necessario impostare il membro **position** della struttura [**Job \_ info \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 4**](job-info-4.md) sulla posizione del processo non **\_ \_ specificata**.</span><span class="sxs-lookup"><span data-stu-id="d1596-172">If you do not want to set a print job's position in the print queue, you should set the **Position** member of the [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure to **JOB\_POSITION\_UNSPECIFIED**.</span></span>

<span data-ttu-id="d1596-173">Usare la funzione **SetJob** con la struttura [**Job \_ info \_ 3**](job-info-3.md) per collegare un set di processi di stampa (noto anche come catena).</span><span class="sxs-lookup"><span data-stu-id="d1596-173">Use the **SetJob** function with the [**JOB\_INFO\_3**](job-info-3.md) structure to link together a set of print jobs (also known as a chain).</span></span> <span data-ttu-id="d1596-174">Questa operazione è utile nelle situazioni in cui un singolo documento è costituito da diverse parti di cui si desidera eseguire il rendering separatamente.</span><span class="sxs-lookup"><span data-stu-id="d1596-174">This is useful in situations where a single document consists of several parts that you want to render separately.</span></span> <span data-ttu-id="d1596-175">Per stampare i processi a, B, C e D in ordine, chiamare **SetJob** con [**informazioni sul processo \_ \_ 4**](job-info-4.md) per collegare da a a b, da b a c e da C a d.</span><span class="sxs-lookup"><span data-stu-id="d1596-175">To print jobs A, B, C, and D in order, call **SetJob** with [**JOB\_INFO\_4**](job-info-4.md) to link A to B, B to C, and C to D.</span></span>

<span data-ttu-id="d1596-176">Se si collegano i processi di stampa, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d1596-176">If you link print jobs, note the following:</span></span>

-   <span data-ttu-id="d1596-177">I processi possono essere aggiunti all'inizio o alla fine di una catena.</span><span class="sxs-lookup"><span data-stu-id="d1596-177">Jobs can be added to the beginning or end of a chain.</span></span>
-   <span data-ttu-id="d1596-178">Tutti i processi nella catena devono avere lo stesso tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="d1596-178">All jobs in the chain must have the same data type.</span></span>
-   <span data-ttu-id="d1596-179">La catena deve essere completamente collegata prima che lo spooling venga avviato. in caso contrario, lo spooler potrebbe stampare ed eliminare i processi di spooling prima di collegarli tutti.</span><span class="sxs-lookup"><span data-stu-id="d1596-179">The chain must be completely linked before spooling begins, otherwise the spooler may print and delete spooled jobs before you link them all.</span></span> <span data-ttu-id="d1596-180">Esistono due modi per impedire la stampa della catena in modo anomalo:</span><span class="sxs-lookup"><span data-stu-id="d1596-180">There are two ways to keep the chain from printing prematurely:</span></span>

    -   <span data-ttu-id="d1596-181">Sospende il primo processo nella catena finché la catena non è completamente collegata.</span><span class="sxs-lookup"><span data-stu-id="d1596-181">Pause the first job in the chain until the chain is completely linked.</span></span> <span data-ttu-id="d1596-182">Lo stato di sospensione del primo processo determina lo stato di tutti i processi nella catena.</span><span class="sxs-lookup"><span data-stu-id="d1596-182">The paused state of the first job governs the state of all jobs in the chain.</span></span>
    -   <span data-ttu-id="d1596-183">Lasciare incompleto il primo processo, ovvero non chiamare [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) o [**ScheduleJob**](schedulejob.md) per il primo processo.</span><span class="sxs-lookup"><span data-stu-id="d1596-183">Keep the first job incomplete, that is, do not call [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) or [**ScheduleJob**](schedulejob.md) for the first job.</span></span> <span data-ttu-id="d1596-184">Tuttavia, se l'opzione ' stampa durante lo spooling ' è abilitata (impostazione predefinita), questo metodo blocca la porta mentre viene compilata la catena, che impedisce anche la stampa di processi non correlati.</span><span class="sxs-lookup"><span data-stu-id="d1596-184">However, if 'print while spooling' is enabled (the default), this method blocks the port while the chain is built, which also prevents the printing of non-related jobs.</span></span>

-   <span data-ttu-id="d1596-185">L'applicazione deve gestire il caso in cui l'utente elimina un processo nella catena prima del completamento della stampa della catena.</span><span class="sxs-lookup"><span data-stu-id="d1596-185">The application must handle the case where the user deletes a job in the chain before the chain finishes printing.</span></span> <span data-ttu-id="d1596-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **un \_ parametro non valido** quando JobID non esiste.</span><span class="sxs-lookup"><span data-stu-id="d1596-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **INVALID\_PARAMETER** when a JobID does not exist.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1596-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1596-187">Requirements</span></span>



| <span data-ttu-id="d1596-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1596-188">Requirement</span></span> | <span data-ttu-id="d1596-189">Valore</span><span class="sxs-lookup"><span data-stu-id="d1596-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1596-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1596-190">Minimum supported client</span></span><br/> | <span data-ttu-id="d1596-191">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d1596-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d1596-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1596-192">Minimum supported server</span></span><br/> | <span data-ttu-id="d1596-193">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d1596-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d1596-194">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1596-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1596-195"><dt>WinSpool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-195"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d1596-196">Libreria</span><span class="sxs-lookup"><span data-stu-id="d1596-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1596-197"><dt>WinSpool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-197"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d1596-198">DLL</span><span class="sxs-lookup"><span data-stu-id="d1596-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1596-199"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d1596-199"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d1596-200">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d1596-200">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d1596-201">**SetJobW** (Unicode) e **SetJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d1596-201">**SetJobW** (Unicode) and **SetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="d1596-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1596-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1596-203">Stampa</span><span class="sxs-lookup"><span data-stu-id="d1596-203">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d1596-204">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="d1596-204">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d1596-205">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="d1596-205">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="d1596-206">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="d1596-206">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="d1596-207">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d1596-207">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="d1596-208">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="d1596-208">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="d1596-209">**\_Informazioni processo \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d1596-209">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="d1596-210">**Informazioni sul processo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d1596-210">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="d1596-211">**Informazioni sul processo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="d1596-211">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="d1596-212">**Informazioni sul processo \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="d1596-212">**JOB\_INFO\_4**</span></span>](job-info-4.md)
</dt> </dl>

 

