---
description: La \_ struttura Info stampante \_ 5 specifica informazioni dettagliate sulla stampante.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: Struttura PRINTER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314990"
---
# <a name="printer_info_5-structure"></a><span data-ttu-id="ea6af-103">\_Struttura Info stampante \_ 5</span><span class="sxs-lookup"><span data-stu-id="ea6af-103">PRINTER\_INFO\_5 structure</span></span>

<span data-ttu-id="ea6af-104">La **struttura \_ Info stampante \_ 5** specifica informazioni dettagliate sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="ea6af-104">The **PRINTER\_INFO\_5** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea6af-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea6af-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="ea6af-106">Members</span><span class="sxs-lookup"><span data-stu-id="ea6af-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ea6af-107">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="ea6af-107">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="ea6af-108">Puntatore a una stringa con terminazione null che specifica il nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="ea6af-108">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="ea6af-109">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="ea6af-109">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="ea6af-110">Puntatore a una stringa con terminazione null che identifica la porta o le porte utilizzate per trasmettere i dati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="ea6af-110">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="ea6af-111">Se una stampante è connessa a più di una porta, i nomi di ogni porta devono essere separati da virgole (ad esempio, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="ea6af-111">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="ea6af-112">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="ea6af-112">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="ea6af-113">Attributi della stampante.</span><span class="sxs-lookup"><span data-stu-id="ea6af-113">The printer attributes.</span></span> <span data-ttu-id="ea6af-114">Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea6af-114">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="ea6af-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ea6af-115">Value</span></span>                                   | <span data-ttu-id="ea6af-116">Significato</span><span class="sxs-lookup"><span data-stu-id="ea6af-116">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6af-117">\_attributo stampante \_ diretto</span><span class="sxs-lookup"><span data-stu-id="ea6af-117">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="ea6af-118">Il processo viene inviato direttamente alla stampante, ovvero non è stato eseguito lo spooling.</span><span class="sxs-lookup"><span data-stu-id="ea6af-118">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="ea6af-119">\_prima operazione di attributo stampante \_ \_ completata \_</span><span class="sxs-lookup"><span data-stu-id="ea6af-119">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="ea6af-120">Se set e Printer sono impostati per lo spooling di stampa, tutti i processi che hanno completato lo spooling sono pianificati per la stampa prima dei processi che non hanno completato lo spooling.</span><span class="sxs-lookup"><span data-stu-id="ea6af-120">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="ea6af-121">\_attributo stampante \_ Abilita \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="ea6af-121">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="ea6af-122">Se impostato, viene chiamato **DevQueryPrint** .</span><span class="sxs-lookup"><span data-stu-id="ea6af-122">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="ea6af-123">**DevQueryPrint** può avere esito negativo se le configurazioni di documento e stampante non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="ea6af-123">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="ea6af-124">Impostando questo flag, i documenti non corrispondenti verranno mantenuti nella coda.</span><span class="sxs-lookup"><span data-stu-id="ea6af-124">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="ea6af-125">attributo della stampante \_ \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="ea6af-125">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="ea6af-126">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ea6af-126">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="ea6af-127">\_KEEPPRINTEDJOBS attributo \_ stampante</span><span class="sxs-lookup"><span data-stu-id="ea6af-127">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="ea6af-128">Se impostata, i processi vengono conservati dopo la stampa.</span><span class="sxs-lookup"><span data-stu-id="ea6af-128">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="ea6af-129">Se non impostata, i processi vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="ea6af-129">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="ea6af-130">\_attributo stampante \_ locale</span><span class="sxs-lookup"><span data-stu-id="ea6af-130">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="ea6af-131">La stampante è una stampante locale.</span><span class="sxs-lookup"><span data-stu-id="ea6af-131">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="ea6af-132">\_rete attributi \_ stampante</span><span class="sxs-lookup"><span data-stu-id="ea6af-132">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="ea6af-133">La stampante è una connessione alla stampante di rete.</span><span class="sxs-lookup"><span data-stu-id="ea6af-133">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="ea6af-134">\_attributo Printer \_ pubblicato</span><span class="sxs-lookup"><span data-stu-id="ea6af-134">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="ea6af-135">Indica se la stampante è pubblicata nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="ea6af-135">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="ea6af-136">attributo stampante in \_ \_ coda</span><span class="sxs-lookup"><span data-stu-id="ea6af-136">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="ea6af-137">Se impostato, lo spooler della stampante e la stampa viene avviata dopo lo spooling dell'ultima pagina.</span><span class="sxs-lookup"><span data-stu-id="ea6af-137">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="ea6af-138">Se non è impostato e \_ l'attributo della stampante \_ Direct non è impostato, la stampante esegue lo spooling e la stampa durante lo spooling.</span><span class="sxs-lookup"><span data-stu-id="ea6af-138">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="ea6af-139">\_attributo stampante \_ \_ solo RAW</span><span class="sxs-lookup"><span data-stu-id="ea6af-139">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="ea6af-140">Indica che è possibile spoolare solo i processi di stampa con tipi di dati non elaborati.</span><span class="sxs-lookup"><span data-stu-id="ea6af-140">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="ea6af-141">\_attributo stampante \_ condiviso</span><span class="sxs-lookup"><span data-stu-id="ea6af-141">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="ea6af-142">La stampante è condivisa.</span><span class="sxs-lookup"><span data-stu-id="ea6af-142">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="ea6af-143">In Windows XP e nelle versioni successive di Windows è possibile utilizzare anche il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="ea6af-143">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="ea6af-144">Valore</span><span class="sxs-lookup"><span data-stu-id="ea6af-144">Value</span></span>                   | <span data-ttu-id="ea6af-145">Significato</span><span class="sxs-lookup"><span data-stu-id="ea6af-145">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6af-146">\_Fax attributo \_ stampante</span><span class="sxs-lookup"><span data-stu-id="ea6af-146">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="ea6af-147">Se impostato, Printer è una stampante fax.</span><span class="sxs-lookup"><span data-stu-id="ea6af-147">If set, printer is a fax printer.</span></span> <span data-ttu-id="ea6af-148">Questo può essere impostato solo da [**AddPrinter**](addprinter.md), ma può essere recuperato da [**EnumPrinters**](enumprinters.md) e [**GetPrinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="ea6af-148">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="ea6af-149">In Windows Vista e nelle versioni successive di Windows è possibile utilizzare anche i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea6af-149">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="ea6af-150">Valore</span><span class="sxs-lookup"><span data-stu-id="ea6af-150">Value</span></span>                               | <span data-ttu-id="ea6af-151">Significato</span><span class="sxs-lookup"><span data-stu-id="ea6af-151">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ea6af-152">\_ \_ nome descrittivo dell'attributo Printer \_</span><span class="sxs-lookup"><span data-stu-id="ea6af-152">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="ea6af-153">Un computer si è connesso a questa stampante e ne è stato assegnato un nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="ea6af-153">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="ea6af-154">\_computer attributo \_ stampante</span><span class="sxs-lookup"><span data-stu-id="ea6af-154">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="ea6af-155">La stampante è una connessione per computer.</span><span class="sxs-lookup"><span data-stu-id="ea6af-155">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="ea6af-156">\_ \_ utente push attributo \_ stampante</span><span class="sxs-lookup"><span data-stu-id="ea6af-156">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="ea6af-157">La stampante è stata installata usando i criteri utente per le connessioni push Printer.</span><span class="sxs-lookup"><span data-stu-id="ea6af-157">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="ea6af-158">\_ \_ computer push degli attributi stampante \_</span><span class="sxs-lookup"><span data-stu-id="ea6af-158">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="ea6af-159">La stampante è stata installata usando i criteri del computer connessioni stampante push.</span><span class="sxs-lookup"><span data-stu-id="ea6af-159">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ea6af-160">**DeviceNotSelectedTimeout**</span><span class="sxs-lookup"><span data-stu-id="ea6af-160">**DeviceNotSelectedTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="ea6af-161">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ea6af-161">This value is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea6af-162">**TransmissionRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="ea6af-162">**TransmissionRetryTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="ea6af-163">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ea6af-163">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea6af-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea6af-164">Requirements</span></span>



| <span data-ttu-id="ea6af-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea6af-165">Requirement</span></span> | <span data-ttu-id="ea6af-166">Valore</span><span class="sxs-lookup"><span data-stu-id="ea6af-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6af-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea6af-167">Minimum supported client</span></span><br/> | <span data-ttu-id="ea6af-168">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea6af-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ea6af-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea6af-169">Minimum supported server</span></span><br/> | <span data-ttu-id="ea6af-170">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea6af-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ea6af-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea6af-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea6af-172"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea6af-172"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ea6af-173">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ea6af-173">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ea6af-174">**\_ \_ Info stampante \_ 5W** (Unicode) e **\_ \_ Info stampante \_ 5a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ea6af-174">**\_PRINTER\_INFO\_5W** (Unicode) and **\_PRINTER\_INFO\_5A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ea6af-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea6af-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea6af-176">Stampa</span><span class="sxs-lookup"><span data-stu-id="ea6af-176">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ea6af-177">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="ea6af-177">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ea6af-178">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="ea6af-178">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="ea6af-179">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ea6af-179">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="ea6af-180">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ea6af-180">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="ea6af-181">**\_Informazioni stampante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ea6af-181">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="ea6af-182">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ea6af-182">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="ea6af-183">**\_Informazioni stampante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ea6af-183">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="ea6af-184">**\_Informazioni stampante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="ea6af-184">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




