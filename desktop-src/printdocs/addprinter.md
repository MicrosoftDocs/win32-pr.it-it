---
description: La funzione AddPrinter aggiunge una stampante all'elenco delle stampanti supportate per un server specificato.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Funzione AddPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227360"
---
# <a name="addprinter-function"></a><span data-ttu-id="13f51-103">AddPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="13f51-103">AddPrinter function</span></span>

<span data-ttu-id="13f51-104">La funzione **AddPrinter** aggiunge una stampante all'elenco delle stampanti supportate per un server specificato.</span><span class="sxs-lookup"><span data-stu-id="13f51-104">The **AddPrinter** function adds a printer to the list of supported printers for a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f51-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13f51-105">Syntax</span></span>


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="13f51-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="13f51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f51-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13f51-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13f51-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installata la stampante.</span><span class="sxs-lookup"><span data-stu-id="13f51-108">A pointer to a null-terminated string that specifies the name of the server on which the printer should be installed.</span></span> <span data-ttu-id="13f51-109">Se la stringa è **null**, la stampante viene installata localmente.</span><span class="sxs-lookup"><span data-stu-id="13f51-109">If this string is **NULL**, the printer is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="13f51-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="13f51-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13f51-111">Versione della struttura a cui punta *pPrinter* .</span><span class="sxs-lookup"><span data-stu-id="13f51-111">The version of the structure to which *pPrinter* points.</span></span> <span data-ttu-id="13f51-112">Questo valore deve essere 2.</span><span class="sxs-lookup"><span data-stu-id="13f51-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="13f51-113">*pPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13f51-113">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13f51-114">Puntatore a una struttura [**di \_ informazioni \_ sulla stampante 2**](printer-info-2.md) che contiene informazioni sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="13f51-114">A pointer to a [**PRINTER\_INFO\_2**](printer-info-2.md) structure that contains information about the printer.</span></span> <span data-ttu-id="13f51-115">È necessario specificare valori non **null** per i membri **pPrinterName**, **pPortName**, **pDriverName** e **pPrintProcessor** di questa struttura prima di chiamare **AddPrinter**.</span><span class="sxs-lookup"><span data-stu-id="13f51-115">You must specify non-**NULL** values for the **pPrinterName**, **pPortName**, **pDriverName**, and **pPrintProcessor** members of this structure before calling **AddPrinter**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f51-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13f51-116">Return value</span></span>

<span data-ttu-id="13f51-117">Se la funzione ha esito positivo, il valore restituito è un handle (non thread-safe) a un nuovo oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="13f51-117">If the function succeeds, the return value is a handle (not thread safe) to a new printer object.</span></span> <span data-ttu-id="13f51-118">Al termine dell'handle, passarlo alla funzione [**ClosePrinter**](closeprinter.md) per chiuderlo.</span><span class="sxs-lookup"><span data-stu-id="13f51-118">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="13f51-119">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="13f51-119">If the function fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="13f51-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="13f51-120">Remarks</span></span>

<span data-ttu-id="13f51-121">Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="13f51-121">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="13f51-122">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="13f51-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="13f51-123">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13f51-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="13f51-124">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="13f51-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="13f51-125">Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="13f51-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="13f51-126">L'handle restituito non è thread-safe.</span><span class="sxs-lookup"><span data-stu-id="13f51-126">The returned handle is not thread safe.</span></span> <span data-ttu-id="13f51-127">Se i chiamanti devono utilizzarlo contemporaneamente su più thread, devono fornire l'accesso di sincronizzazione personalizzato all'handle della stampante utilizzando le [funzioni di sincronizzazione](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="13f51-127">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="13f51-128">Per evitare di scrivere codice personalizzato, l'applicazione può aprire un handle della stampante in ogni thread, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="13f51-128">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="13f51-129">Di seguito sono riportati i membri della [**struttura \_ info \_ 2 della stampante**](printer-info-2.md) che è possibile impostare prima della chiamata della funzione **AddPrinter** :</span><span class="sxs-lookup"><span data-stu-id="13f51-129">The following are the members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure that can be set before the **AddPrinter** function is called:</span></span>

-   <span data-ttu-id="13f51-130">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="13f51-130">**Attributes**</span></span>
-   <span data-ttu-id="13f51-131">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="13f51-131">**pPrintProcessor**</span></span>
-   <span data-ttu-id="13f51-132">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="13f51-132">**DefaultPriority**</span></span>
-   <span data-ttu-id="13f51-133">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="13f51-133">**Priority**</span></span>
-   <span data-ttu-id="13f51-134">**pComment**</span><span class="sxs-lookup"><span data-stu-id="13f51-134">**pComment**</span></span>
-   <span data-ttu-id="13f51-135">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="13f51-135">**pSecurityDescriptor**</span></span>
-   <span data-ttu-id="13f51-136">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="13f51-136">**pDatatype**</span></span>
-   <span data-ttu-id="13f51-137">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="13f51-137">**pSepFile**</span></span>
-   <span data-ttu-id="13f51-138">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="13f51-138">**pDevMode**</span></span>
-   <span data-ttu-id="13f51-139">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="13f51-139">**pShareName**</span></span>
-   <span data-ttu-id="13f51-140">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="13f51-140">**pLocation**</span></span>
-   <span data-ttu-id="13f51-141">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="13f51-141">**StartTime**</span></span>
-   <span data-ttu-id="13f51-142">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="13f51-142">**pParameters**</span></span>
-   <span data-ttu-id="13f51-143">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="13f51-143">**UntilTime**</span></span>

<span data-ttu-id="13f51-144">I membri **status**, **cJobs** e **AveragePPM** della struttura [**Printer \_ info \_ 2**](printer-info-2.md) sono riservati per l'uso da parte della funzione [**GetPrinter**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="13f51-144">The **Status**, **cJobs**, and **AveragePPM** members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure are reserved for use by the [**GetPrinter**](getprinter.md) function.</span></span> <span data-ttu-id="13f51-145">Non devono essere impostate prima di chiamare **AddPrinter**.</span><span class="sxs-lookup"><span data-stu-id="13f51-145">They must not be set before calling **AddPrinter**.</span></span>

<span data-ttu-id="13f51-146">Se **pSecurityDescriptor** è **null**, il sistema assegna un descrittore di sicurezza predefinito alla stampante.</span><span class="sxs-lookup"><span data-stu-id="13f51-146">If **pSecurityDescriptor** is **NULL**, the system assigns a default security descriptor to the printer.</span></span> <span data-ttu-id="13f51-147">Il descrittore di sicurezza predefinito dispone delle autorizzazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="13f51-147">The default security descriptor has the following permissions.</span></span>



| <span data-ttu-id="13f51-148">Valore</span><span class="sxs-lookup"><span data-stu-id="13f51-148">Value</span></span>                          | <span data-ttu-id="13f51-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13f51-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f51-150">Amministratori e utenti esperti</span><span class="sxs-lookup"><span data-stu-id="13f51-150">Administrators and Power Users</span></span> | <span data-ttu-id="13f51-151">Controllo completo della coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="13f51-151">Full control on the print queue.</span></span> <span data-ttu-id="13f51-152">Ciò significa che i membri di questi gruppi possono stampare, gestire la coda (può eliminare la coda, modificare qualsiasi impostazione della coda, incluso il descrittore di sicurezza) e gestire i processi di stampa di tutti gli utenti (eliminazione, sospensione, ripresa, riavvio dei processi). Si noti che gli utenti avanzati non esistono prima di Windows XP Professional.</span><span class="sxs-lookup"><span data-stu-id="13f51-152">This means members of these groups can print, manage the queue (can delete the queue, change any setting of the queue, including the security descriptor), and manage the print jobs of all users (delete, pause, resume, restart jobs).Note that Power Users do not exist before Windows XP Professional.</span></span><br/> |
| <span data-ttu-id="13f51-153">Autore/proprietario</span><span class="sxs-lookup"><span data-stu-id="13f51-153">Creator/Owner</span></span>                  | <span data-ttu-id="13f51-154">Consente di gestire i processi personali.</span><span class="sxs-lookup"><span data-stu-id="13f51-154">Can manage own jobs.</span></span> <span data-ttu-id="13f51-155">Ciò significa che l'utente che invia processi può gestire (eliminare, sospendere, riprendere, riavviare) i propri processi.</span><span class="sxs-lookup"><span data-stu-id="13f51-155">This means that user who submit jobs can manage (delete, pause, resume, restart) their own jobs.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="13f51-156">Tutti</span><span class="sxs-lookup"><span data-stu-id="13f51-156">Everyone</span></span>                       | <span data-ttu-id="13f51-157">Esecuzione e controllo di lettura standard.</span><span class="sxs-lookup"><span data-stu-id="13f51-157">Execute and standard read control.</span></span> <span data-ttu-id="13f51-158">Ciò significa che i membri del gruppo Everyone possono stampare e leggere le proprietà della coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="13f51-158">This means that members of the everyone group can print and read properties of the print queue.</span></span>                                                                                                                                                                                                                     |



 

<span data-ttu-id="13f51-159">Dopo che un'applicazione ha creato un oggetto Printer con la funzione **AddPrinter** , è necessario utilizzare la funzione [**PrinterProperties**](printerproperties.md) per specificare le impostazioni corrette per il driver della stampante associato all'oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="13f51-159">After an application creates a printer object with the **AddPrinter** function, it must use the [**PrinterProperties**](printerproperties.md) function to specify the correct settings for the printer driver associated with the printer object.</span></span>

<span data-ttu-id="13f51-160">La funzione **AddPrinter** restituisce un errore se esiste già un oggetto Printer con lo stesso nome, a meno che l'oggetto non sia contrassegnato come eliminazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="13f51-160">The **AddPrinter** function returns an error if a printer object with the same name already exists, unless that object is marked as pending deletion.</span></span> <span data-ttu-id="13f51-161">In tal caso, la stampante esistente non viene eliminata e i parametri per la creazione di **AddPrinter** vengono usati per modificare le impostazioni della stampante esistente (come se l'applicazione avesse usato la funzione [**seprinter**](setprinter.md) ).</span><span class="sxs-lookup"><span data-stu-id="13f51-161">In that case, the existing printer is not deleted, and the **AddPrinter** creation parameters are used to change the existing printer settings (as if the application had used the [**SetPrinter**](setprinter.md) function).</span></span>

<span data-ttu-id="13f51-162">Utilizzare la funzione [**EnumPrintProcessors**](enumprintprocessors.md) per enumerare il set di processori di stampa installati in un server.</span><span class="sxs-lookup"><span data-stu-id="13f51-162">Use the [**EnumPrintProcessors**](enumprintprocessors.md) function to enumerate the set of print processors installed on a server.</span></span> <span data-ttu-id="13f51-163">Utilizzare la funzione [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) per enumerare il set di tipi di dati supportati da un processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="13f51-163">Use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to enumerate the set of data types that a print processor supports.</span></span> <span data-ttu-id="13f51-164">Utilizzare la funzione [**EnumPorts**](enumports.md) per enumerare il set di porte disponibili.</span><span class="sxs-lookup"><span data-stu-id="13f51-164">Use the [**EnumPorts**](enumports.md) function to enumerate the set of available ports.</span></span> <span data-ttu-id="13f51-165">Utilizzare la funzione [**EnumPrinterDrivers**](enumprinterdrivers.md) per enumerare i driver della stampante installati.</span><span class="sxs-lookup"><span data-stu-id="13f51-165">Use the [**EnumPrinterDrivers**](enumprinterdrivers.md) function to enumerate the installed printer drivers.</span></span>

<span data-ttu-id="13f51-166">Il chiamante della funzione **AddPrinter** deve avere \_ accesso al server \_ per amministrare l'accesso al server in cui deve essere creata la stampante.</span><span class="sxs-lookup"><span data-stu-id="13f51-166">The caller of the **AddPrinter** function must have SERVER\_ACCESS\_ADMINISTER access to the server on which the printer is to be created.</span></span> <span data-ttu-id="13f51-167">L'handle restituito dalla funzione avrà \_ le \_ autorizzazioni di accesso a tutte le stampanti e potrà essere utilizzato per eseguire operazioni amministrative sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="13f51-167">The handle returned by the function will have PRINTER\_ALL\_ACCESS permission, and can be used to perform administrative operations on the printer.</span></span>

<span data-ttu-id="13f51-168">Se la funzione **DrvPrinterEvent** viene passata al flag di evento della stampante \_ \_ \_ senza \_ flag dell'interfaccia utente, il driver non deve usare una chiamata dell'interfaccia utente durante **DrvPrinterEvent**.</span><span class="sxs-lookup"><span data-stu-id="13f51-168">If the **DrvPrinterEvent** function is passed the PRINTER\_EVENT\_FLAG\_NO\_UI flag, the driver should not use a UI call during **DrvPrinterEvent**.</span></span> <span data-ttu-id="13f51-169">Per eseguire processi correlati all'interfaccia utente, il programma di installazione deve usare la voce **VendorSetup** nel file con estensione inf della stampante o, per plug and Play dispositivi, il programma di installazione può usare un programma di coinstallazione specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13f51-169">To do UI-related jobs, the installer should either use the **VendorSetup** entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="13f51-170">Per ulteriori informazioni su **VendorSetup**, vedere Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="13f51-170">For more information about **VendorSetup**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="13f51-171">Per impostazione predefinita, il firewall connessione Internet (ICF) blocca le porte della stampante, ma viene abilitata un'eccezione per la condivisione di file e stampanti quando si esegue **AddPrinter**.</span><span class="sxs-lookup"><span data-stu-id="13f51-171">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing is enabled when you run **AddPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="13f51-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13f51-172">Requirements</span></span>



| <span data-ttu-id="13f51-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="13f51-173">Requirement</span></span> | <span data-ttu-id="13f51-174">Valore</span><span class="sxs-lookup"><span data-stu-id="13f51-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f51-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13f51-175">Minimum supported client</span></span><br/> | <span data-ttu-id="13f51-176">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13f51-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13f51-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13f51-177">Minimum supported server</span></span><br/> | <span data-ttu-id="13f51-178">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13f51-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13f51-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13f51-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="13f51-180"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13f51-180"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="13f51-181">Libreria</span><span class="sxs-lookup"><span data-stu-id="13f51-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="13f51-182"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13f51-182"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="13f51-183">DLL</span><span class="sxs-lookup"><span data-stu-id="13f51-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13f51-184"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="13f51-184"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="13f51-185">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="13f51-185">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="13f51-186">**AddPrinterW** (Unicode) e **AddPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="13f51-186">**AddPrinterW** (Unicode) and **AddPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="13f51-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13f51-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f51-188">Stampa</span><span class="sxs-lookup"><span data-stu-id="13f51-188">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="13f51-189">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="13f51-189">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="13f51-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="13f51-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="13f51-191">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="13f51-191">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="13f51-192">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="13f51-192">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="13f51-193">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="13f51-193">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="13f51-194">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="13f51-194">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="13f51-195">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="13f51-195">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="13f51-196">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="13f51-196">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="13f51-197">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="13f51-197">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="13f51-198">**PrinterProperties**</span><span class="sxs-lookup"><span data-stu-id="13f51-198">**PrinterProperties**</span></span>](printerproperties.md)
</dt> <dt>

[<span data-ttu-id="13f51-199">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="13f51-199">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

