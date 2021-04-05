---
description: La funzione SetPrinterData imposta i dati di configurazione per una stampante o un server di stampa.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Funzione SetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881394"
---
# <a name="setprinterdata-function"></a><span data-ttu-id="74d14-103">SetPrinterData (funzione)</span><span class="sxs-lookup"><span data-stu-id="74d14-103">SetPrinterData function</span></span>

<span data-ttu-id="74d14-104">La funzione **SetPrinterData** imposta i dati di configurazione per una stampante o un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="74d14-104">The **SetPrinterData** function sets the configuration data for a printer or print server.</span></span>

<span data-ttu-id="74d14-105">Per specificare la chiave del registro di sistema in cui archiviare i dati, chiamare la funzione [**SetPrinterDataEx**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="74d14-105">To specify the registry key under which to store the data, call the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span> <span data-ttu-id="74d14-106">La chiamata a **SetPrinterData** equivale alla chiamata della funzione **SetPrinterDataEx** con il parametro *pKeyName* impostato su "PrinterDriverData".</span><span class="sxs-lookup"><span data-stu-id="74d14-106">Calling **SetPrinterData** is equivalent to calling the **SetPrinterDataEx** function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="74d14-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74d14-107">Syntax</span></span>


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="74d14-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="74d14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74d14-109">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74d14-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d14-110">Handle per la stampante o il server di stampa per il quale la funzione imposta i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="74d14-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="74d14-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="74d14-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="74d14-112">*pValueName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74d14-112">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d14-113">Puntatore a una stringa con terminazione null che identifica i dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="74d14-113">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="74d14-114">Per le stampanti, questa stringa è il nome di un valore del registro di sistema nella chiave "PrinterDriverData" della stampante nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="74d14-114">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="74d14-115">Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="74d14-115">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="74d14-116">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="74d14-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d14-117">Codice che indica il tipo di dati a cui punta il parametro *pData* .</span><span class="sxs-lookup"><span data-stu-id="74d14-117">A code that indicates the type of data that the *pData* parameter points to.</span></span> <span data-ttu-id="74d14-118">Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="74d14-118">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="74d14-119">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74d14-119">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d14-120">Puntatore a una matrice di byte che contiene i dati di configurazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="74d14-120">A pointer to an array of bytes that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="74d14-121">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74d14-121">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d14-122">Dimensione, in byte, della matrice.</span><span class="sxs-lookup"><span data-stu-id="74d14-122">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74d14-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74d14-123">Return value</span></span>

<span data-ttu-id="74d14-124">Se la funzione ha esito positivo, il valore restituito è **Error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="74d14-124">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="74d14-125">Se la funzione ha esito negativo, il valore restituito è un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="74d14-125">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74d14-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="74d14-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="74d14-127">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="74d14-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="74d14-128">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74d14-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="74d14-129">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="74d14-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="74d14-130">Per recuperare i dati di configurazione esistenti per una stampante, chiamare la funzione [**GetPrinterDataEx**](getprinterdataex.md) o [**GetPrinterData**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="74d14-130">To retrieve existing configuration data for a printer, call the [**GetPrinterDataEx**](getprinterdataex.md) or [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="74d14-131">Se *hPrinter* è un handle per un server di stampa, *pValueName* può specificare uno dei seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="74d14-131">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="74d14-132">valore</span><span class="sxs-lookup"><span data-stu-id="74d14-132">Value</span></span>                                                               | <span data-ttu-id="74d14-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="74d14-133">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d14-134">**SPLREG \_ consentire all' \_ utente \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="74d14-134">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="74d14-135">Windows XP con Service Pack 2 (SP2) e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-135">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="74d14-136">Windows Server 2003 con Service Pack 1 (SP1) e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-136">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="74d14-137">**\_bip SPLREG \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="74d14-137">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74d14-138">**SPLREG \_ directory predefinita dello \_ spooling \_**</span><span class="sxs-lookup"><span data-stu-id="74d14-138">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74d14-139">**\_registro eventi di SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="74d14-139">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74d14-140">**\_popup NET \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="74d14-140">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="74d14-141">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-141">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="74d14-142">**\_ \_ \_ impostazione predefinita priorità thread porta SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="74d14-142">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74d14-143">**\_ \_ priorità thread della porta SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="74d14-143">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74d14-144">**\_gruppi di \_ isolamento del driver di stampa SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="74d14-144">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="74d14-145">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-145">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74d14-146">**SPLREG \_ tempo di isolamento del driver di stampa \_ prima del \_ \_ \_ \_ riciclo**</span><span class="sxs-lookup"><span data-stu-id="74d14-146">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="74d14-147">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-147">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74d14-148">**\_numero massimo di oggetti di isolamento del driver di stampa SPLREG \_ \_ prima del \_ \_ \_ \_ riciclo**</span><span class="sxs-lookup"><span data-stu-id="74d14-148">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="74d14-149">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-149">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74d14-150">**\_timeout di \_ \_ \_ inattività isolamento driver di \_ stampa SPLREG**</span><span class="sxs-lookup"><span data-stu-id="74d14-150">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="74d14-151">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-151">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74d14-152">**\_criteri di \_ \_ esecuzione isolamento \_ driver \_ di stampa SPLREG**</span><span class="sxs-lookup"><span data-stu-id="74d14-152">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="74d14-153">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-153">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74d14-154">**\_criteri di \_ \_ sostituzione isolamento \_ driver \_ di stampa SPLREG**</span><span class="sxs-lookup"><span data-stu-id="74d14-154">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="74d14-155">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-155">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74d14-156">**\_popup nuovo tentativo SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="74d14-156">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="74d14-157">In caso di esito positivo, *pData* contiene 1 se il server è impostato per ritentare le finestre popup per tutti i processi oppure 0 se il server non ritenta le finestre popup per tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="74d14-157">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="74d14-158">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-158">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="74d14-159">**\_priorità thread dell'utilità di pianificazione SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="74d14-159">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74d14-160">**\_ \_ \_ impostazione predefinita priorità thread dell'utilità di pianificazione SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="74d14-160">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74d14-161">**\_WEBSHAREMGMT SPLREG**</span><span class="sxs-lookup"><span data-stu-id="74d14-161">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="74d14-162">Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="74d14-162">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="74d14-163">I valori seguenti di *pValueName* determinano il comportamento di stampa del pool quando si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="74d14-163">The following values of *pValueName* determine the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="74d14-164">valore</span><span class="sxs-lookup"><span data-stu-id="74d14-164">Value</span></span>                                       | <span data-ttu-id="74d14-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="74d14-165">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d14-166">**\_ \_ \_ errore di riavvio del processo di SPLREG nel \_ pool \_**</span><span class="sxs-lookup"><span data-stu-id="74d14-166">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="74d14-167">Il valore di *pData* indica il tempo, in secondi, in cui un processo viene riavviato in un'altra porta dopo che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="74d14-167">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="74d14-168">Questa impostazione viene usata con **\_ \_ il processo di riavvio del SPLREG \_ nel \_ pool \_ abilitato**.</span><span class="sxs-lookup"><span data-stu-id="74d14-168">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="74d14-169">**SPLREG \_ riavvio \_ \_ del processo nel \_ pool \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="74d14-169">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="74d14-170">Un valore diverso da zero in *pData* indica che è abilitato il **processo di riavvio SPLREG \_ \_ \_ sull' \_ \_ errore del pool** .</span><span class="sxs-lookup"><span data-stu-id="74d14-170">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="74d14-171">Il tempo specificato nel **processo di riavvio del SPLREG \_ \_ per l' \_ \_ \_ errore del pool** è minimo.</span><span class="sxs-lookup"><span data-stu-id="74d14-171">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="74d14-172">Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio porta seguenti, che sono valori del registro di sistema in questa chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="74d14-172">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="74d14-173">**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ porte**</span><span class="sxs-lookup"><span data-stu-id="74d14-173">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="74d14-174">Chiamare la funzione [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) per impostare questi valori.</span><span class="sxs-lookup"><span data-stu-id="74d14-174">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="74d14-175">Impostazione di monitoraggio porta</span><span class="sxs-lookup"><span data-stu-id="74d14-175">Port monitor setting</span></span>     | <span data-ttu-id="74d14-176">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="74d14-176">Data type</span></span>      | <span data-ttu-id="74d14-177">Significato</span><span class="sxs-lookup"><span data-stu-id="74d14-177">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d14-178">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="74d14-178">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="74d14-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="74d14-179">**REG\_DWORD**</span></span> | <span data-ttu-id="74d14-180">Se un valore diverso da zero, Abilita il monitoraggio della porta per aggiornare lo spooler con lo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="74d14-180">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="74d14-181">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="74d14-181">**StatusUpdateInterval**</span></span> | <span data-ttu-id="74d14-182">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="74d14-182">**REG\_DWORD**</span></span> | <span data-ttu-id="74d14-183">Specifica l'intervallo, in minuti, quando il monitoraggio porta aggiorna lo spooler con lo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="74d14-183">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="74d14-184">In Windows 7 e versioni successive di Windows, per impostazione predefinita viene eseguito il rendering dei processi di stampa inviati a un server di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="74d14-184">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="74d14-185">Il rendering lato client di un processo di stampa può essere configurato per ogni stampante impostando i valori seguenti in *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="74d14-185">Client-side rendering of a print jobs can be configured for each printer by setting the following values in *pValueName*.</span></span>



| <span data-ttu-id="74d14-186">Impostazione</span><span class="sxs-lookup"><span data-stu-id="74d14-186">Setting</span></span>                      | <span data-ttu-id="74d14-187">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="74d14-187">Data type</span></span>      | <span data-ttu-id="74d14-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74d14-188">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d14-189">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="74d14-189">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="74d14-190">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="74d14-190">**REG\_DWORD**</span></span> | <span data-ttu-id="74d14-191">Il valore 0, o se questo valore non è presente nel registro di sistema, Abilita il rendering predefinito lato client dei processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="74d14-191">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="74d14-192">Il valore 1 disabilita il rendering lato client dei processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="74d14-192">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="74d14-193">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="74d14-193">**ForceClientSideRendering**</span></span> | <span data-ttu-id="74d14-194">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="74d14-194">**REG\_DWORD**</span></span> | <span data-ttu-id="74d14-195">Il valore 0, o se questo valore non è presente nel registro di sistema, causa il rendering dei processi di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="74d14-195">A value of 0, or if this value is not present in the registry, causes the print jobs to be rendered on the client.</span></span> <span data-ttu-id="74d14-196">Se non è possibile eseguire il rendering di un processo di stampa sul client, ne verrà eseguito il rendering nel server.</span><span class="sxs-lookup"><span data-stu-id="74d14-196">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="74d14-197">Se non è possibile eseguire il rendering di un processo di stampa sul server, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="74d14-197">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="74d14-198">Il valore 1 eseguirà il rendering dei processi di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="74d14-198">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="74d14-199">Se non è possibile eseguire il rendering di un processo di stampa sul client, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="74d14-199">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="74d14-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74d14-200">Requirements</span></span>



| <span data-ttu-id="74d14-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="74d14-201">Requirement</span></span> | <span data-ttu-id="74d14-202">Valore</span><span class="sxs-lookup"><span data-stu-id="74d14-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d14-203">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d14-203">Minimum supported client</span></span><br/> | <span data-ttu-id="74d14-204">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74d14-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="74d14-205">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d14-205">Minimum supported server</span></span><br/> | <span data-ttu-id="74d14-206">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74d14-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="74d14-207">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74d14-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="74d14-208"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74d14-208"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="74d14-209">Libreria</span><span class="sxs-lookup"><span data-stu-id="74d14-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="74d14-210"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74d14-210"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="74d14-211">DLL</span><span class="sxs-lookup"><span data-stu-id="74d14-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74d14-212"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="74d14-212"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="74d14-213">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="74d14-213">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74d14-214">**SetPrinterDataW** (Unicode) e **SetPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="74d14-214">**SetPrinterDataW** (Unicode) and **SetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="74d14-215">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74d14-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74d14-216">Stampa</span><span class="sxs-lookup"><span data-stu-id="74d14-216">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="74d14-217">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="74d14-217">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="74d14-218">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="74d14-218">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="74d14-219">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="74d14-219">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="74d14-220">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="74d14-220">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="74d14-221">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="74d14-221">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="74d14-222">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="74d14-222">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

