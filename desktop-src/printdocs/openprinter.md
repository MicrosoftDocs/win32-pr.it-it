---
description: La funzione OpenPrinter recupera un handle per la stampante o il server di stampa specificato o per altri tipi di handle nel sottosistema di stampa.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: Funzione OpenPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313023"
---
# <a name="openprinter-function"></a><span data-ttu-id="85439-103">OpenPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="85439-103">OpenPrinter function</span></span>

<span data-ttu-id="85439-104">La funzione **OpenPrinter** recupera un handle per la stampante o il server di stampa specificato o per altri tipi di handle nel sottosistema di stampa.</span><span class="sxs-lookup"><span data-stu-id="85439-104">The **OpenPrinter** function retrieves a handle to the specified printer or print server or other types of handles in the print subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="85439-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85439-105">Syntax</span></span>


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="85439-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85439-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85439-107">*pPrinterName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85439-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85439-108">Puntatore a una stringa con terminazione null che specifica il nome della stampante o del server di stampa, l'oggetto Printer, XcvMonitor o XcvPort.</span><span class="sxs-lookup"><span data-stu-id="85439-108">A pointer to a null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="85439-109">Per un oggetto Printer, utilizzare: PrinterName, job xxxx.</span><span class="sxs-lookup"><span data-stu-id="85439-109">For a printer object use: PrinterName, Job xxxx.</span></span> <span data-ttu-id="85439-110">Per un XcvMonitor, usare: ServerName, XcvMonitor MonitorName.</span><span class="sxs-lookup"><span data-stu-id="85439-110">For an XcvMonitor, use: ServerName, XcvMonitor MonitorName.</span></span> <span data-ttu-id="85439-111">Per un XcvPort, usare: ServerName, XcvPort Portaname.</span><span class="sxs-lookup"><span data-stu-id="85439-111">For an XcvPort, use: ServerName, XcvPort PortName.</span></span>

<span data-ttu-id="85439-112">Se è **null**, indica il server di stampa locale.</span><span class="sxs-lookup"><span data-stu-id="85439-112">If **NULL**, it indicates the local printer server.</span></span>

</dd> <dt>

<span data-ttu-id="85439-113">*phPrinter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85439-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85439-114">Puntatore a una variabile che riceve un handle (non thread-safe) per l'oggetto della stampante o del server di stampa aperto.</span><span class="sxs-lookup"><span data-stu-id="85439-114">A pointer to a variable that receives a handle (not thread safe) to the open printer or print server object.</span></span>

<span data-ttu-id="85439-115">Il parametro *phPrinter* può restituire un handle XCV per l'utilizzo con la funzione XcvData.</span><span class="sxs-lookup"><span data-stu-id="85439-115">The *phPrinter* parameter can return an Xcv handle for use with the XcvData function.</span></span> <span data-ttu-id="85439-116">Per ulteriori informazioni su XcvData, vedere DDK.</span><span class="sxs-lookup"><span data-stu-id="85439-116">For more information about XcvData, see the DDK.</span></span>

</dd> <dt>

<span data-ttu-id="85439-117">*pDefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85439-117">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85439-118">Un puntatore a una struttura di [**\_ impostazioni predefinite della stampante**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="85439-118">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="85439-119">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="85439-119">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85439-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85439-120">Return value</span></span>

<span data-ttu-id="85439-121">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="85439-121">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="85439-122">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="85439-122">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="85439-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="85439-123">Remarks</span></span>

<span data-ttu-id="85439-124">Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="85439-124">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="85439-125">Un handle ottenuto per una stampante remota mediante una chiamata a **OpenPrinter** per una stampante remota accede alla stampante tramite una cache locale nel servizio spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="85439-125">A handle obtained for a remote printer by a call to **OpenPrinter** for a remote printer accesses the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="85439-126">Questa cache non è precisa in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="85439-126">This cache isn't real-time accurate.</span></span> <span data-ttu-id="85439-127">Per ottenere dati accurati, sostituire la chiamata OpenPrinter con [**OpenPrinter2**](openprinter2.md) con POptions. dwFlags impostato sull' \_ opzione Printer \_ No \_ cache.</span><span class="sxs-lookup"><span data-stu-id="85439-127">To obtain accurate data, replace the OpenPrinter call with [**OpenPrinter2**](openprinter2.md) with pOptions.dwFlags set to PRINTER\_OPTION\_NO\_CACHE.</span></span> <span data-ttu-id="85439-128">Si noti che solo OpenPrinter2W è funzionante.</span><span class="sxs-lookup"><span data-stu-id="85439-128">Note that only OpenPrinter2W is functional.</span></span> <span data-ttu-id="85439-129">La funzione restituisce un handle della stampante che usa altre chiamate API di stampa e ignora la cache locale.</span><span class="sxs-lookup"><span data-stu-id="85439-129">The function returns a printer handle that uses other Printing API calls and bypasses the local cache.</span></span> <span data-ttu-id="85439-130">Questo metodo si blocca durante l'attesa della comunicazione di rete con la stampante remota, quindi potrebbe non essere restituito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="85439-130">This method blocks while waiting for network communication with the remote printer, so it might not return immediately.</span></span> <span data-ttu-id="85439-131">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="85439-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="85439-132">La chiamata di questa funzione da un thread che gestisce l'interazione dell'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="85439-132">Calling this function from a thread that manages user interface interaction might make the application appear unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="85439-133">Un handle ottenuto da una chiamata a **OpenPrinter** per una stampante remota effettuerà l'accesso alla stampante tramite una cache locale nel servizio spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="85439-133">A handle obtained by a call to **OpenPrinter** for a remote printer will access the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="85439-134">Questa cache è, in base alla progettazione, non accurata in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="85439-134">This cache is, by design, not real time accurate.</span></span> <span data-ttu-id="85439-135">Se è necessario ottenere dati accurati, sostituire la chiamata **OpenPrinter** con [**OpenPrinter2**](openprinter2.md) con *pOptions. dwFlags* impostato sull' [**\_ opzione Printer \_ No \_ cache**](printer-options.md).</span><span class="sxs-lookup"><span data-stu-id="85439-135">If you need to obtain accurate data, replace the **OpenPrinter** call with [**OpenPrinter2**](openprinter2.md) with *pOptions.dwFlags* set to [**PRINTER\_OPTION\_NO\_CACHE**](printer-options.md).</span></span> <span data-ttu-id="85439-136">Si noti che solo **OpenPrinter2W** è funzionante.</span><span class="sxs-lookup"><span data-stu-id="85439-136">Note that only **OpenPrinter2W** is functional.</span></span> <span data-ttu-id="85439-137">In questo modo la funzione restituisce un handle della stampante che esegue altre chiamate API di stampa per ignorare la cache locale.</span><span class="sxs-lookup"><span data-stu-id="85439-137">Doing so the function returns a printer handle that makes other Printing API calls to bypass the local cache.</span></span> <span data-ttu-id="85439-138">Si noti che questo approccio si bloccherà durante l'attesa della comunicazione di rete di andata e ritorno alla stampante remota, quindi potrebbe non essere immediatamente reimpostata.</span><span class="sxs-lookup"><span data-stu-id="85439-138">Note that this approach will block while waiting for the round-trip network communication to the remote printer, so it may not return immediately.</span></span> <span data-ttu-id="85439-139">La velocità con cui questa funzione restituisce dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e l'implementazione di driver della stampante, difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="85439-139">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation - factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="85439-140">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe quindi far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="85439-140">Therefore calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="85439-141">L'handle a cui fa riferimento *phPrinter* non è thread-safe.</span><span class="sxs-lookup"><span data-stu-id="85439-141">The handle pointed to by *phPrinter* is not thread safe.</span></span> <span data-ttu-id="85439-142">Se i chiamanti devono utilizzarlo contemporaneamente su più thread, devono fornire l'accesso di sincronizzazione personalizzato all'handle della stampante utilizzando le [funzioni di sincronizzazione](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="85439-142">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="85439-143">Per evitare di scrivere codice personalizzato, l'applicazione può aprire un handle della stampante in ogni thread, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="85439-143">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="85439-144">Il parametro *pDefault* consente di specificare il tipo di dati e i valori della modalità dispositivo usati per la stampa dei documenti inviati dalla funzione [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="85439-144">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="85439-145">È tuttavia possibile eseguire l'override di questi valori utilizzando la funzione [**SetJob**](setjob.md) dopo l'avvio di un documento.</span><span class="sxs-lookup"><span data-stu-id="85439-145">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="85439-146">Le [**Impostazioni DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definite nella struttura delle impostazioni [**\_ predefinite della stampante**](printer-defaults.md) del parametro *pDefault* non vengono utilizzate quando il valore del membro *pDatatype* della struttura [**doc \_ info \_ 1**](doc-info-1.md) passato nel parametro *pDocInfo* della chiamata [**StartDocPrinter**](startdocprinter.md) è "Raw".</span><span class="sxs-lookup"><span data-stu-id="85439-146">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) settings defined in the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure of the *pDefault* parameter are not used when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW".</span></span> <span data-ttu-id="85439-147">Quando un documento di alto livello (ad esempio un file Adobe PDF o Microsoft Word) o altri dati della stampante (ad esempio, PCL, PS o HPGL) vengono inviati direttamente a una stampante con *pDatatype* impostato su "Raw", il documento deve descrivere completamente le impostazioni del processo di stampa in stile **DEVMODE** nella lingua compresa nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="85439-147">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer with *pDatatype* set to "RAW", the document must fully describe the **DEVMODE**-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="85439-148">È possibile chiamare la funzione **OpenPrinter** per aprire un handle per un server di stampa o per determinare i diritti di accesso di un client a un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="85439-148">You can call the **OpenPrinter** function to open a handle to a print server or to determine the access rights that a client has to a print server.</span></span> <span data-ttu-id="85439-149">A tale scopo, specificare il nome del server di stampa nel parametro *pPrinterName* , impostare i membri **pDatatype** e **pDevMode** della struttura [**Printer \_ defaults**](printer-defaults.md) su **null** e impostare il membro **desiredAccess** per specificare un valore della maschera di accesso al server, ad esempio server \_ All \_ Access.</span><span class="sxs-lookup"><span data-stu-id="85439-149">To do so, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="85439-150">Al termine dell'handle, passarlo alla funzione [**ClosePrinter**](closeprinter.md) per chiuderla.</span><span class="sxs-lookup"><span data-stu-id="85439-150">When you finish with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="85439-151">Utilizzare il membro **desiredAccess** della struttura [**Printer \_ defaults**](printer-defaults.md) per specificare i diritti di accesso necessari per la stampante.</span><span class="sxs-lookup"><span data-stu-id="85439-151">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the access rights that you need to the printer.</span></span> <span data-ttu-id="85439-152">I diritti di accesso possono essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="85439-152">The access rights can be one of the following.</span></span> <span data-ttu-id="85439-153">Se *pDefault* è **null**, i diritti di accesso sono Printer \_ usare l'accesso \_ .)</span><span class="sxs-lookup"><span data-stu-id="85439-153">(If *pDefault* is **NULL**, then the access rights are PRINTER\_ACCESS\_USE.)</span></span>



| <span data-ttu-id="85439-154">Valore di accesso desiderato</span><span class="sxs-lookup"><span data-stu-id="85439-154">Desired Access value</span></span>                        | <span data-ttu-id="85439-155">Significato</span><span class="sxs-lookup"><span data-stu-id="85439-155">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85439-156">\_amministrazione dell'accesso alla stampante \_</span><span class="sxs-lookup"><span data-stu-id="85439-156">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="85439-157">Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="85439-157">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="85439-158">\_uso dell'accesso alla stampante \_</span><span class="sxs-lookup"><span data-stu-id="85439-158">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="85439-159">Per eseguire operazioni di stampa di base.</span><span class="sxs-lookup"><span data-stu-id="85439-159">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="85439-160">\_tutti gli \_ accessi alla stampante</span><span class="sxs-lookup"><span data-stu-id="85439-160">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="85439-161">Per eseguire tutte le attività amministrative e le operazioni di stampa di base, ad eccezione della sincronizzazione (vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="85439-161">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                     |
| <span data-ttu-id="85439-162">\_gestione dell'accesso alla stampante \_ \_ limitata</span><span class="sxs-lookup"><span data-stu-id="85439-162">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="85439-163">Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="85439-163">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="85439-164">Questo valore è disponibile a partire da Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="85439-164">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="85439-165">valori di sicurezza generici, ad esempio WRITE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="85439-165">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="85439-166">Per consentire diritti di accesso di controllo specifici.</span><span class="sxs-lookup"><span data-stu-id="85439-166">To allow specific control access rights.</span></span> <span data-ttu-id="85439-167">Vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="85439-167">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="85439-168">Se un utente non dispone dell'autorizzazione per aprire una stampante o un server di stampa specificato con l'accesso desiderato, la chiamata a **OpenPrinter** avrà esito negativo con un valore restituito pari a zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il valore Error \_ Access \_ negato.</span><span class="sxs-lookup"><span data-stu-id="85439-168">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter** call will fail with a return value of zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

## <a name="examples"></a><span data-ttu-id="85439-169">Esempio</span><span class="sxs-lookup"><span data-stu-id="85439-169">Examples</span></span>

<span data-ttu-id="85439-170">Per un programma di esempio che usa questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="85439-170">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85439-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85439-171">Requirements</span></span>



| <span data-ttu-id="85439-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="85439-172">Requirement</span></span> | <span data-ttu-id="85439-173">Valore</span><span class="sxs-lookup"><span data-stu-id="85439-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85439-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85439-174">Minimum supported client</span></span><br/> | <span data-ttu-id="85439-175">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="85439-175">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="85439-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85439-176">Minimum supported server</span></span><br/> | <span data-ttu-id="85439-177">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="85439-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="85439-178">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85439-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="85439-179"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85439-179"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="85439-180">Libreria</span><span class="sxs-lookup"><span data-stu-id="85439-180">Library</span></span><br/>                  | <dl> <span data-ttu-id="85439-181"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85439-181"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="85439-182">DLL</span><span class="sxs-lookup"><span data-stu-id="85439-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85439-183"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="85439-183"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="85439-184">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="85439-184">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="85439-185">**OpenPrinterW** (Unicode) e **OpenPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="85439-185">**OpenPrinterW** (Unicode) and **OpenPrinterA** (ANSI)</span></span><br/>                                         |



## <a name="see-also"></a><span data-ttu-id="85439-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85439-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85439-187">Stampa</span><span class="sxs-lookup"><span data-stu-id="85439-187">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="85439-188">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="85439-188">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="85439-189">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="85439-189">**WritePrinter**</span></span>](writeprinter.md)
</dt> <dt>

[<span data-ttu-id="85439-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="85439-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="85439-191">**\_impostazioni predefinite stampanti**</span><span class="sxs-lookup"><span data-stu-id="85439-191">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="85439-192">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="85439-192">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="85439-193">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="85439-193">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="85439-194">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="85439-194">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

