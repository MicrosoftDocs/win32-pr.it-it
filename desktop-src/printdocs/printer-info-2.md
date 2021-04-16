---
description: La \_ struttura Printer Info \_ 2 specifica informazioni dettagliate sulla stampante.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: Struttura PRINTER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529755"
---
# <a name="printer_info_2-structure"></a><span data-ttu-id="f4c78-103">\_Struttura Info stampante \_ 2</span><span class="sxs-lookup"><span data-stu-id="f4c78-103">PRINTER\_INFO\_2 structure</span></span>

<span data-ttu-id="f4c78-104">La struttura **Printer \_ info \_ 2** specifica informazioni dettagliate sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-104">The **PRINTER\_INFO\_2** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c78-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4c78-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="f4c78-106">Members</span><span class="sxs-lookup"><span data-stu-id="f4c78-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4c78-107">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="f4c78-107">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-108">Puntatore a una stringa con terminazione null che identifica il server che controlla la stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-108">A pointer to a null-terminated string identifying the server that controls the printer.</span></span> <span data-ttu-id="f4c78-109">Se la stringa è **null**, la stampante viene controllata localmente.</span><span class="sxs-lookup"><span data-stu-id="f4c78-109">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-110">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="f4c78-110">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-111">Puntatore a una stringa con terminazione null che specifica il nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-111">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-112">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="f4c78-112">**pShareName**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-113">Puntatore a una stringa con terminazione null che identifica il punto di condivisione per la stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-113">A pointer to a null-terminated string that identifies the share point for the printer.</span></span> <span data-ttu-id="f4c78-114">Questa stringa viene utilizzata solo se la stampante \_ \_Per il membro **Attributes** è stata impostata la costante condivisa dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="f4c78-114">(This string is used only if the PRINTER\_ATTRIBUTE\_SHARED constant was set for the **Attributes** member.)</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-115">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="f4c78-115">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-116">Puntatore a una stringa con terminazione null che identifica la porta o le porte utilizzate per trasmettere i dati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-116">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="f4c78-117">Se una stampante è connessa a più di una porta, i nomi di ogni porta devono essere separati da virgole (ad esempio, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="f4c78-117">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-118">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="f4c78-118">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-119">Puntatore a una stringa con terminazione null che specifica il nome del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-119">A pointer to a null-terminated string that specifies the name of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-120">**pComment**</span><span class="sxs-lookup"><span data-stu-id="f4c78-120">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-121">Puntatore a una stringa con terminazione null che fornisce una breve descrizione della stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-121">A pointer to a null-terminated string that provides a brief description of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-122">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="f4c78-122">**pLocation**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-123">Puntatore a una stringa con terminazione null che specifica la posizione fisica della stampante, ad esempio "Bldg.</span><span class="sxs-lookup"><span data-stu-id="f4c78-123">A pointer to a null-terminated string that specifies the physical location of the printer (for example, "Bldg.</span></span> <span data-ttu-id="f4c78-124">38, stanza 1164 ").</span><span class="sxs-lookup"><span data-stu-id="f4c78-124">38, Room 1164").</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-125">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="f4c78-125">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-126">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che definisce i dati predefiniti della stampante, ad esempio l'orientamento della carta e la risoluzione.</span><span class="sxs-lookup"><span data-stu-id="f4c78-126">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines default printer data such as the paper orientation and the resolution.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-127">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="f4c78-127">**pSepFile**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-128">Puntatore a una stringa con terminazione null che specifica il nome del file utilizzato per creare la pagina separatore.</span><span class="sxs-lookup"><span data-stu-id="f4c78-128">A pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="f4c78-129">Questa pagina viene utilizzata per separare i processi di stampa inviati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-129">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-130">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="f4c78-130">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-131">Puntatore a una stringa con terminazione null che specifica il nome del processore di stampa utilizzato dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-131">A pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span> <span data-ttu-id="f4c78-132">È possibile utilizzare la funzione [**EnumPrintProcessors**](enumprintprocessors.md) per ottenere un elenco dei processori di stampa installati in un server.</span><span class="sxs-lookup"><span data-stu-id="f4c78-132">You can use the [**EnumPrintProcessors**](enumprintprocessors.md) function to obtain a list of print processors installed on a server.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-133">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="f4c78-133">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-134">Puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzato per registrare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-134">A pointer to a null-terminated string that specifies the data type used to record the print job.</span></span> <span data-ttu-id="f4c78-135">È possibile utilizzare la funzione [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) per ottenere un elenco dei tipi di dati supportati da uno specifico processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-135">You can use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to obtain a list of data types supported by a specific print processor.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-136">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="f4c78-136">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-137">Puntatore a una stringa con terminazione null che specifica i parametri predefiniti del processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-137">A pointer to a null-terminated string that specifies the default print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-138">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f4c78-138">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-139">Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) per la stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-139">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure for the printer.</span></span> <span data-ttu-id="f4c78-140">Questo membro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="f4c78-140">This member may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-141">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="f4c78-141">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-142">Attributi della stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-142">The printer attributes.</span></span> <span data-ttu-id="f4c78-143">Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f4c78-143">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="f4c78-144">Valore</span><span class="sxs-lookup"><span data-stu-id="f4c78-144">Value</span></span>                                   | <span data-ttu-id="f4c78-145">Significato</span><span class="sxs-lookup"><span data-stu-id="f4c78-145">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c78-146">\_attributo stampante \_ diretto</span><span class="sxs-lookup"><span data-stu-id="f4c78-146">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="f4c78-147">Il processo viene inviato direttamente alla stampante, ovvero non è stato eseguito lo spooling.</span><span class="sxs-lookup"><span data-stu-id="f4c78-147">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="f4c78-148">\_prima operazione di attributo stampante \_ \_ completata \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-148">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="f4c78-149">Se set e Printer sono impostati per lo spooling di stampa, tutti i processi che hanno completato lo spooling sono pianificati per la stampa prima dei processi che non hanno completato lo spooling.</span><span class="sxs-lookup"><span data-stu-id="f4c78-149">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="f4c78-150">\_attributo stampante \_ Abilita \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="f4c78-150">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="f4c78-151">Se impostato, viene chiamato **DevQueryPrint** .</span><span class="sxs-lookup"><span data-stu-id="f4c78-151">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="f4c78-152">**DevQueryPrint** può avere esito negativo se le configurazioni di documento e stampante non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="f4c78-152">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="f4c78-153">Impostando questo flag, i documenti non corrispondenti verranno mantenuti nella coda.</span><span class="sxs-lookup"><span data-stu-id="f4c78-153">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="f4c78-154">attributo della stampante \_ \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="f4c78-154">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="f4c78-155">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f4c78-155">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="f4c78-156">\_KEEPPRINTEDJOBS attributo \_ stampante</span><span class="sxs-lookup"><span data-stu-id="f4c78-156">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="f4c78-157">Se impostata, i processi vengono conservati dopo la stampa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-157">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="f4c78-158">Se non impostata, i processi vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="f4c78-158">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="f4c78-159">\_attributo stampante \_ locale</span><span class="sxs-lookup"><span data-stu-id="f4c78-159">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="f4c78-160">La stampante è una stampante locale.</span><span class="sxs-lookup"><span data-stu-id="f4c78-160">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="f4c78-161">\_rete attributi \_ stampante</span><span class="sxs-lookup"><span data-stu-id="f4c78-161">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="f4c78-162">La stampante è una connessione alla stampante di rete.</span><span class="sxs-lookup"><span data-stu-id="f4c78-162">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="f4c78-163">\_attributo Printer \_ pubblicato</span><span class="sxs-lookup"><span data-stu-id="f4c78-163">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="f4c78-164">Indica se la stampante è pubblicata nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="f4c78-164">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="f4c78-165">attributo stampante in \_ \_ coda</span><span class="sxs-lookup"><span data-stu-id="f4c78-165">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="f4c78-166">Se impostato, lo spooler della stampante e la stampa viene avviata dopo lo spooling dell'ultima pagina.</span><span class="sxs-lookup"><span data-stu-id="f4c78-166">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="f4c78-167">Se non è impostato e \_ l'attributo della stampante \_ Direct non è impostato, la stampante esegue lo spooling e la stampa durante lo spooling.</span><span class="sxs-lookup"><span data-stu-id="f4c78-167">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="f4c78-168">\_attributo stampante \_ \_ solo RAW</span><span class="sxs-lookup"><span data-stu-id="f4c78-168">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="f4c78-169">Indica che è possibile spoolare solo i processi di stampa con tipi di dati non elaborati.</span><span class="sxs-lookup"><span data-stu-id="f4c78-169">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="f4c78-170">\_attributo stampante \_ condiviso</span><span class="sxs-lookup"><span data-stu-id="f4c78-170">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="f4c78-171">La stampante è condivisa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-171">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="f4c78-172">In Windows XP e nelle versioni successive di Windows è possibile utilizzare anche il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="f4c78-172">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="f4c78-173">Valore</span><span class="sxs-lookup"><span data-stu-id="f4c78-173">Value</span></span>                   | <span data-ttu-id="f4c78-174">Significato</span><span class="sxs-lookup"><span data-stu-id="f4c78-174">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c78-175">\_Fax attributo \_ stampante</span><span class="sxs-lookup"><span data-stu-id="f4c78-175">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="f4c78-176">Se impostato, Printer è una stampante fax.</span><span class="sxs-lookup"><span data-stu-id="f4c78-176">If set, printer is a fax printer.</span></span> <span data-ttu-id="f4c78-177">Questo può essere impostato solo da [**AddPrinter**](addprinter.md), ma può essere recuperato da [**EnumPrinters**](enumprinters.md) e [**GetPrinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="f4c78-177">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="f4c78-178">In Windows Vista e nelle versioni successive di Windows è possibile utilizzare anche i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f4c78-178">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="f4c78-179">Valore</span><span class="sxs-lookup"><span data-stu-id="f4c78-179">Value</span></span>                               | <span data-ttu-id="f4c78-180">Significato</span><span class="sxs-lookup"><span data-stu-id="f4c78-180">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f4c78-181">\_ \_ nome descrittivo dell'attributo Printer \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-181">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="f4c78-182">Un computer si è connesso a questa stampante e ne è stato assegnato un nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="f4c78-182">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="f4c78-183">\_computer attributo \_ stampante</span><span class="sxs-lookup"><span data-stu-id="f4c78-183">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="f4c78-184">La stampante è una connessione per computer.</span><span class="sxs-lookup"><span data-stu-id="f4c78-184">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="f4c78-185">\_ \_ utente push attributo \_ stampante</span><span class="sxs-lookup"><span data-stu-id="f4c78-185">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="f4c78-186">La stampante è stata installata usando i criteri utente per le connessioni push Printer.</span><span class="sxs-lookup"><span data-stu-id="f4c78-186">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="f4c78-187">\_ \_ computer push degli attributi stampante \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-187">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="f4c78-188">La stampante è stata installata usando i criteri del computer connessioni stampante push.</span><span class="sxs-lookup"><span data-stu-id="f4c78-188">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

<span data-ttu-id="f4c78-189">In Windows Server 2003 è possibile usare anche il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="f4c78-189">In Windows Server 2003, the following value can also be used.</span></span>

| <span data-ttu-id="f4c78-190">Valore</span><span class="sxs-lookup"><span data-stu-id="f4c78-190">Value</span></span>                  | <span data-ttu-id="f4c78-191">Significato</span><span class="sxs-lookup"><span data-stu-id="f4c78-191">Meaning</span></span>                                                                 |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f4c78-192">\_attributo stampante \_ TS</span><span class="sxs-lookup"><span data-stu-id="f4c78-192">PRINTER\_ATTRIBUTE\_TS</span></span> | <span data-ttu-id="f4c78-193">Indica che la stampante è attualmente connessa tramite un server terminal.</span><span class="sxs-lookup"><span data-stu-id="f4c78-193">Indicates the printer is currently connected through a terminal server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f4c78-194">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="f4c78-194">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-195">Valore di priorità utilizzato dallo spooler per instradare i processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-195">A priority value that the spooler uses to route print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-196">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="f4c78-196">**DefaultPriority**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-197">Valore di priorità predefinito assegnato a ogni processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-197">The default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-198">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="f4c78-198">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-199">Data e ora della prima stampa di un processo da parte della stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-199">The earliest time at which the printer will print a job.</span></span> <span data-ttu-id="f4c78-200">Questo valore è espresso come minuti trascorsi dall'ora 12:00 GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="f4c78-200">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-201">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="f4c78-201">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-202">Ora più recente in cui la stampante stampa un processo.</span><span class="sxs-lookup"><span data-stu-id="f4c78-202">The latest time at which the printer will print a job.</span></span> <span data-ttu-id="f4c78-203">Questo valore è espresso come minuti trascorsi dall'ora 12:00 GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="f4c78-203">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-204">**Status**</span><span class="sxs-lookup"><span data-stu-id="f4c78-204">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-205">Stato della stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-205">The printer status.</span></span> <span data-ttu-id="f4c78-206">Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f4c78-206">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="f4c78-207">Valore</span><span class="sxs-lookup"><span data-stu-id="f4c78-207">Value</span></span>                               | <span data-ttu-id="f4c78-208">Significato</span><span class="sxs-lookup"><span data-stu-id="f4c78-208">Meaning</span></span>                                                          |
|-------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f4c78-209">stato della stampante \_ \_ occupato</span><span class="sxs-lookup"><span data-stu-id="f4c78-209">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="f4c78-210">La stampante è occupata.</span><span class="sxs-lookup"><span data-stu-id="f4c78-210">The printer is busy.</span></span>                                             |
| <span data-ttu-id="f4c78-211">\_sportello dello stato della stampante \_ \_ aperto</span><span class="sxs-lookup"><span data-stu-id="f4c78-211">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="f4c78-212">Lo sportello della stampante è aperto.</span><span class="sxs-lookup"><span data-stu-id="f4c78-212">The printer door is open.</span></span>                                        |
| <span data-ttu-id="f4c78-213">\_errore di stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-213">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="f4c78-214">La stampante è in uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="f4c78-214">The printer is in an error state.</span></span>                                |
| <span data-ttu-id="f4c78-215">\_inizializzazione dello stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-215">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="f4c78-216">È in corso l'inizializzazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-216">The printer is initializing.</span></span>                                     |
| <span data-ttu-id="f4c78-217">\_io stato \_ stampante \_ attivo</span><span class="sxs-lookup"><span data-stu-id="f4c78-217">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="f4c78-218">La stampante è in uno stato di input/output attivo</span><span class="sxs-lookup"><span data-stu-id="f4c78-218">The printer is in an active input/output state</span></span>                   |
| <span data-ttu-id="f4c78-219">\_feed manuale dello stato della stampante \_ \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-219">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="f4c78-220">La stampante è in uno stato di avanzamento manuale.</span><span class="sxs-lookup"><span data-stu-id="f4c78-220">The printer is in a manual feed state.</span></span>                           |
| <span data-ttu-id="f4c78-221">\_stato stampante \_ senza \_ toner</span><span class="sxs-lookup"><span data-stu-id="f4c78-221">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="f4c78-222">La stampante ha esaurito il toner.</span><span class="sxs-lookup"><span data-stu-id="f4c78-222">The printer is out of toner.</span></span>                                     |
| <span data-ttu-id="f4c78-223">stato della stampante \_ \_ non \_ disponibile</span><span class="sxs-lookup"><span data-stu-id="f4c78-223">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="f4c78-224">La stampante non è disponibile per la stampa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-224">The printer is not available for printing.</span></span>                       |
| <span data-ttu-id="f4c78-225">stato della stampante \_ \_ offline</span><span class="sxs-lookup"><span data-stu-id="f4c78-225">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="f4c78-226">La stampante non è in linea.</span><span class="sxs-lookup"><span data-stu-id="f4c78-226">The printer is offline.</span></span>                                          |
| <span data-ttu-id="f4c78-227">\_ \_ \_ \_ memoria insufficiente per lo stato della stampante</span><span class="sxs-lookup"><span data-stu-id="f4c78-227">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="f4c78-228">Memoria esaurita per la stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-228">The printer has run out of memory.</span></span>                               |
| <span data-ttu-id="f4c78-229">\_Cestino di \_ output stato stampante \_ \_ completo</span><span class="sxs-lookup"><span data-stu-id="f4c78-229">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="f4c78-230">Il cassetto di uscita della stampante è pieno.</span><span class="sxs-lookup"><span data-stu-id="f4c78-230">The printer's output bin is full.</span></span>                                |
| <span data-ttu-id="f4c78-231">pagina di stato della stampante \_ \_ \_ Punt</span><span class="sxs-lookup"><span data-stu-id="f4c78-231">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="f4c78-232">La stampante non è in grado di stampare la pagina corrente.</span><span class="sxs-lookup"><span data-stu-id="f4c78-232">The printer cannot print the current page.</span></span>                       |
| <span data-ttu-id="f4c78-233">\_ \_ inceppamento carta stato stampante \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-233">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="f4c78-234">La carta è bloccata nella stampante</span><span class="sxs-lookup"><span data-stu-id="f4c78-234">Paper is jammed in the printer</span></span>                                   |
| <span data-ttu-id="f4c78-235">\_carta dello stato della stampante in \_ \_ uscita</span><span class="sxs-lookup"><span data-stu-id="f4c78-235">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="f4c78-236">La stampante ha esaurito la carta.</span><span class="sxs-lookup"><span data-stu-id="f4c78-236">The printer is out of paper.</span></span>                                     |
| <span data-ttu-id="f4c78-237">\_ \_ problema relativo alla carta di stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-237">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="f4c78-238">La stampante presenta un problema relativo alla carta.</span><span class="sxs-lookup"><span data-stu-id="f4c78-238">The printer has a paper problem.</span></span>                                 |
| <span data-ttu-id="f4c78-239">stato della stampante \_ \_ sospeso</span><span class="sxs-lookup"><span data-stu-id="f4c78-239">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="f4c78-240">La stampante è sospesa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-240">The printer is paused.</span></span>                                           |
| <span data-ttu-id="f4c78-241">\_stato stampante \_ in attesa di \_ eliminazione</span><span class="sxs-lookup"><span data-stu-id="f4c78-241">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="f4c78-242">È in corso l'eliminazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-242">The printer is being deleted.</span></span>                                    |
| <span data-ttu-id="f4c78-243">\_risparmio di stato della stampante \_ \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-243">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="f4c78-244">La stampante è in modalità risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="f4c78-244">The printer is in power save mode.</span></span>                               |
| <span data-ttu-id="f4c78-245">\_stampa dello stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-245">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="f4c78-246">Viene stampata la stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-246">The printer is printing.</span></span>                                         |
| <span data-ttu-id="f4c78-247">\_elaborazione dello stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-247">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="f4c78-248">La stampante sta elaborando un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-248">The printer is processing a print job.</span></span>                           |
| <span data-ttu-id="f4c78-249">\_Server stato \_ stampante \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="f4c78-249">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="f4c78-250">Lo stato della stampante è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f4c78-250">The printer status is unknown.</span></span>                                   |
| <span data-ttu-id="f4c78-251">\_ \_ toner stato stampante \_ basso</span><span class="sxs-lookup"><span data-stu-id="f4c78-251">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="f4c78-252">Il toner della stampante è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f4c78-252">The printer is low on toner.</span></span>                                     |
| <span data-ttu-id="f4c78-253">\_ \_ intervento dell'utente sullo stato della stampante \_</span><span class="sxs-lookup"><span data-stu-id="f4c78-253">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="f4c78-254">La stampante presenta un errore che richiede all'utente di eseguire un'operazione.</span><span class="sxs-lookup"><span data-stu-id="f4c78-254">The printer has an error that requires the user to do something.</span></span> |
| <span data-ttu-id="f4c78-255">stato della stampante \_ \_ in attesa</span><span class="sxs-lookup"><span data-stu-id="f4c78-255">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="f4c78-256">La stampante è in attesa.</span><span class="sxs-lookup"><span data-stu-id="f4c78-256">The printer is waiting.</span></span>                                          |
| <span data-ttu-id="f4c78-257">\_stato della \_ stampante \_ attivo</span><span class="sxs-lookup"><span data-stu-id="f4c78-257">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="f4c78-258">La stampante è in fase di riscaldamento.</span><span class="sxs-lookup"><span data-stu-id="f4c78-258">The printer is warming up.</span></span>                                       |



 

</dd> <dt>

<span data-ttu-id="f4c78-259">**cJobs**</span><span class="sxs-lookup"><span data-stu-id="f4c78-259">**cJobs**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-260">Numero di processi di stampa accodati per la stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-260">The number of print jobs that have been queued for the printer.</span></span>

</dd> <dt>

<span data-ttu-id="f4c78-261">**AveragePPM**</span><span class="sxs-lookup"><span data-stu-id="f4c78-261">**AveragePPM**</span></span>
</dt> <dd>

<span data-ttu-id="f4c78-262">Numero medio di pagine al minuto stampate sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="f4c78-262">The average number of pages per minute that have been printed on the printer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4c78-263">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4c78-263">Requirements</span></span>



| <span data-ttu-id="f4c78-264">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4c78-264">Requirement</span></span> | <span data-ttu-id="f4c78-265">Valore</span><span class="sxs-lookup"><span data-stu-id="f4c78-265">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c78-266">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4c78-266">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c78-267">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f4c78-267">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f4c78-268">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4c78-268">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c78-269">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f4c78-269">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f4c78-270">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4c78-270">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4c78-271"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4c78-271"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f4c78-272">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f4c78-272">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f4c78-273">**\_ \_ Info stampante \_ 2W** (Unicode) e **\_ \_ Info stampante \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f4c78-273">**\_PRINTER\_INFO\_2W** (Unicode) and **\_PRINTER\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="f4c78-274">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4c78-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c78-275">Stampa</span><span class="sxs-lookup"><span data-stu-id="f4c78-275">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f4c78-276">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="f4c78-276">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f4c78-277">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="f4c78-277">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="f4c78-278">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="f4c78-278">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="f4c78-279">**\_Informazioni stampante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f4c78-279">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="f4c78-280">**\_Informazioni stampante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="f4c78-280">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="f4c78-281">**\_Informazioni stampante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="f4c78-281">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="f4c78-282">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="f4c78-282">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

