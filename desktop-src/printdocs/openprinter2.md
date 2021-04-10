---
description: Recupera un handle per la stampante, il server di stampa o altri tipi di handle specificati nel sottosistema di stampa, durante l'impostazione di alcune opzioni della stampante.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: Funzione OpenPrinter2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882513"
---
# <a name="openprinter2-function"></a><span data-ttu-id="838d9-103">OpenPrinter2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="838d9-103">OpenPrinter2 function</span></span>

<span data-ttu-id="838d9-104">Recupera un handle per la stampante, il server di stampa o altri tipi di handle specificati nel sottosistema di stampa, durante l'impostazione di alcune opzioni della stampante.</span><span class="sxs-lookup"><span data-stu-id="838d9-104">Retrieves a handle to the specified printer, print server, or other types of handles in the print subsystem, while setting some of the printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="838d9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="838d9-105">Syntax</span></span>


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a><span data-ttu-id="838d9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="838d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838d9-107">*pPrinterName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="838d9-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838d9-108">Puntatore a una stringa costante con terminazione null che specifica il nome della stampante o del server di stampa, l'oggetto Printer, XcvMonitor o XcvPort.</span><span class="sxs-lookup"><span data-stu-id="838d9-108">A pointer to a constant null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="838d9-109">Per un oggetto Printer, utilizzare: PrinterName, job xxxx.</span><span class="sxs-lookup"><span data-stu-id="838d9-109">For a printer object, use: PrinterName,Job xxxx.</span></span> <span data-ttu-id="838d9-110">Per un XcvMonitor, usare: ServerName, XcvMonitor MonitorName.</span><span class="sxs-lookup"><span data-stu-id="838d9-110">For an XcvMonitor, use: ServerName,XcvMonitor MonitorName.</span></span> <span data-ttu-id="838d9-111">Per un XcvPort, usare: ServerName, XcvPort Portaname.</span><span class="sxs-lookup"><span data-stu-id="838d9-111">For an XcvPort, use: ServerName,XcvPort PortName.</span></span>

<span data-ttu-id="838d9-112">**Windows Vista:** Se è **null**, indica il server di stampa locale.</span><span class="sxs-lookup"><span data-stu-id="838d9-112">**Windows Vista:** If **NULL**, it indicates the local print server.</span></span>

</dd> <dt>

<span data-ttu-id="838d9-113">*phPrinter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="838d9-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="838d9-114">Puntatore a una variabile che riceve un handle per l'oggetto Open Printer o Print Server.</span><span class="sxs-lookup"><span data-stu-id="838d9-114">A pointer to a variable that receives a handle to the open printer or print server object.</span></span>

</dd> <dt>

<span data-ttu-id="838d9-115">*pDefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="838d9-115">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838d9-116">Un puntatore a una struttura di [**\_ impostazioni predefinite della stampante**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="838d9-116">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="838d9-117">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="838d9-117">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="838d9-118">*pOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="838d9-118">*pOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838d9-119">Puntatore a una struttura [**di \_ Opzioni della stampante**](printer-options.md) .</span><span class="sxs-lookup"><span data-stu-id="838d9-119">A pointer to a [**PRINTER\_OPTIONS**](printer-options.md) structure.</span></span> <span data-ttu-id="838d9-120">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="838d9-120">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="838d9-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="838d9-121">Return value</span></span>

<span data-ttu-id="838d9-122">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="838d9-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="838d9-123">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="838d9-123">If the function fails, the return value is zero.</span></span> <span data-ttu-id="838d9-124">Per informazioni estese sugli errori, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="838d9-124">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="838d9-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="838d9-125">Remarks</span></span>

<span data-ttu-id="838d9-126">Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="838d9-126">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="838d9-127">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="838d9-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="838d9-128">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="838d9-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="838d9-129">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="838d9-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="838d9-130">La versione ANSI di questa funzione non è implementata e restituisce l'errore \_ non \_ supportato.</span><span class="sxs-lookup"><span data-stu-id="838d9-130">The ANSI version of this function is not implemented and returns ERROR\_NOT\_SUPPORTED.</span></span>

<span data-ttu-id="838d9-131">Il parametro *pDefault* consente di specificare il tipo di dati e i valori della modalità dispositivo usati per la stampa dei documenti inviati dalla funzione [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="838d9-131">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="838d9-132">È tuttavia possibile eseguire l'override di questi valori utilizzando la funzione [**SetJob**](setjob.md) dopo l'avvio di un documento.</span><span class="sxs-lookup"><span data-stu-id="838d9-132">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="838d9-133">È possibile chiamare la funzione **OpenPrinter2** per aprire un handle per un server di stampa o per determinare i diritti di accesso client a un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="838d9-133">You can call the **OpenPrinter2** function to open a handle to a print server or to determine client access rights to a print server.</span></span> <span data-ttu-id="838d9-134">A tale scopo, specificare il nome del server di stampa nel parametro *pPrinterName* , impostare i membri **pDatatype** e **pDevMode** della struttura [**Printer \_ defaults**](printer-defaults.md) su **null** e impostare il membro **desiredAccess** per specificare un valore della maschera di accesso al server, ad esempio server \_ All \_ Access.</span><span class="sxs-lookup"><span data-stu-id="838d9-134">To do this, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="838d9-135">Al termine dell'handle, passarlo alla funzione [**ClosePrinter**](closeprinter.md) per chiuderlo.</span><span class="sxs-lookup"><span data-stu-id="838d9-135">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="838d9-136">Utilizzare il membro **desiredAccess** della struttura [**Printer \_ defaults**](printer-defaults.md) per specificare i diritti di accesso necessari.</span><span class="sxs-lookup"><span data-stu-id="838d9-136">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the necessary access rights.</span></span> <span data-ttu-id="838d9-137">I diritti di accesso possono essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="838d9-137">The access rights can be one of the following.</span></span>



| <span data-ttu-id="838d9-138">Valore di accesso desiderato</span><span class="sxs-lookup"><span data-stu-id="838d9-138">Desired Access value</span></span>                        | <span data-ttu-id="838d9-139">Significato</span><span class="sxs-lookup"><span data-stu-id="838d9-139">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838d9-140">\_amministrazione dell'accesso alla stampante \_</span><span class="sxs-lookup"><span data-stu-id="838d9-140">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="838d9-141">Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="838d9-141">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="838d9-142">\_uso dell'accesso alla stampante \_</span><span class="sxs-lookup"><span data-stu-id="838d9-142">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="838d9-143">Per eseguire operazioni di stampa di base.</span><span class="sxs-lookup"><span data-stu-id="838d9-143">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="838d9-144">\_tutti gli \_ accessi alla stampante</span><span class="sxs-lookup"><span data-stu-id="838d9-144">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="838d9-145">Per eseguire tutte le attività amministrative e le operazioni di stampa di base, ad eccezione della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="838d9-145">To perform all administrative tasks and basic printing operations except SYNCHRONIZE.</span></span> <span data-ttu-id="838d9-146">Vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="838d9-146">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                         |
| <span data-ttu-id="838d9-147">\_gestione dell'accesso alla stampante \_ \_ limitata</span><span class="sxs-lookup"><span data-stu-id="838d9-147">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="838d9-148">Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="838d9-148">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="838d9-149">Questo valore è disponibile a partire da Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="838d9-149">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="838d9-150">valori di sicurezza generici, ad esempio WRITE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="838d9-150">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="838d9-151">Per consentire diritti di accesso di controllo specifici.</span><span class="sxs-lookup"><span data-stu-id="838d9-151">To allow specific control access rights.</span></span> <span data-ttu-id="838d9-152">Vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="838d9-152">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="838d9-153">Se un utente non dispone dell'autorizzazione per aprire una stampante o un server di stampa specificato con l'accesso desiderato, la chiamata a **OpenPrinter2** avrà esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il valore Error \_ Access \_ denied.</span><span class="sxs-lookup"><span data-stu-id="838d9-153">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter2** call will fail, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="838d9-154">Quando *pPrinterName* è una stampante locale, **OpenPrinter2** ignora tutti i valori di **dwFlags** a cui la struttura [**delle \_ Opzioni della stampante**](printer-options.md) ha puntato usando *pOptions*, ad eccezione del client dell' \_ opzione Printer \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="838d9-154">When *pPrinterName* is a local printer, then **OpenPrinter2** ignores all values of the **dwFlags** that the [**PRINTER\_OPTIONS**](printer-options.md) structure pointed to using *pOptions*, except PRINTER\_OPTION\_CLIENT\_CHANGE.</span></span> <span data-ttu-id="838d9-155">Se quest'ultimo viene passato, **OpenPrinter2** restituirà un errore di \_ accesso \_ negato.</span><span class="sxs-lookup"><span data-stu-id="838d9-155">If the latter is passed, then **OpenPrinter2** will return ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="838d9-156">Di conseguenza, quando si apre una stampante locale, **OpenPrinter2** non offre alcun vantaggio rispetto a [**OpenPrinter**](openprinter.md).</span><span class="sxs-lookup"><span data-stu-id="838d9-156">Accordingly, when opening a local printer, **OpenPrinter2** provides no advantage over [**OpenPrinter**](openprinter.md).</span></span>

<span data-ttu-id="838d9-157">**Windows Vista:** I dati della stampante restituiti da **OpenPrinter2** vengono recuperati da una cache locale, a meno che non sia stata impostata l' **\_ opzione stampante nessun flag \_ \_ della cache** nel campo **dwFlags** della struttura delle [**\_ Opzioni stampante**](printer-options.md) a cui fa riferimento *pOptions*.</span><span class="sxs-lookup"><span data-stu-id="838d9-157">**Windows Vista:** The printer data returned by **OpenPrinter2** is retrieved from a local cache unless the **PRINTER\_OPTION\_NO\_CACHE** flag is set in the **dwFlags** field of the [**PRINTER\_OPTIONS**](printer-options.md) structure referenced by *pOptions*.</span></span>

## <a name="examples"></a><span data-ttu-id="838d9-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="838d9-158">Examples</span></span>

<span data-ttu-id="838d9-159">In questo esempio, **OpenPrinter2** ha esito negativo quando \_ \_ la gestione dell'accesso alla stampante \_ limitata viene passata alla struttura delle [**\_ impostazioni predefinite della stampante**](printer-defaults.md) e l'utente non dispone dell'autorizzazione appropriata.</span><span class="sxs-lookup"><span data-stu-id="838d9-159">In this example, **OpenPrinter2** fails when PRINTER\_ACCESS\_MANAGE\_LIMITED is passed to the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure, and the user does not have the appropriate permission.</span></span>


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



<span data-ttu-id="838d9-160">Per un programma di esempio che illustra come usare questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="838d9-160">For a sample program that shows how to use this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="838d9-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="838d9-161">Requirements</span></span>



| <span data-ttu-id="838d9-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="838d9-162">Requirement</span></span> | <span data-ttu-id="838d9-163">Valore</span><span class="sxs-lookup"><span data-stu-id="838d9-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838d9-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="838d9-164">Minimum supported client</span></span><br/> | <span data-ttu-id="838d9-165">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="838d9-165">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="838d9-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="838d9-166">Minimum supported server</span></span><br/> | <span data-ttu-id="838d9-167">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="838d9-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="838d9-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="838d9-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="838d9-169"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="838d9-169"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="838d9-170">Libreria</span><span class="sxs-lookup"><span data-stu-id="838d9-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="838d9-171"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="838d9-171"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="838d9-172">DLL</span><span class="sxs-lookup"><span data-stu-id="838d9-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="838d9-173"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="838d9-173"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="838d9-174">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="838d9-174">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="838d9-175">**OpenPrinter2W** (Unicode) e **OpenPrinter2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="838d9-175">**OpenPrinter2W** (Unicode) and **OpenPrinter2A** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="838d9-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="838d9-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838d9-177">Stampa</span><span class="sxs-lookup"><span data-stu-id="838d9-177">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="838d9-178">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="838d9-178">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="838d9-179">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="838d9-179">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="838d9-180">**\_impostazioni predefinite stampanti**</span><span class="sxs-lookup"><span data-stu-id="838d9-180">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="838d9-181">**\_Opzioni stampante**</span><span class="sxs-lookup"><span data-stu-id="838d9-181">**PRINTER\_OPTIONS**</span></span>](printer-options.md)
</dt> <dt>

[<span data-ttu-id="838d9-182">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="838d9-182">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="838d9-183">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="838d9-183">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="838d9-184">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="838d9-184">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="838d9-185">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="838d9-185">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

