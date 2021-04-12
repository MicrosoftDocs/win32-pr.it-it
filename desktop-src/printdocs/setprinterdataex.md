---
description: La funzione SetPrinterDataEx imposta i dati di configurazione per una stampante o un server di stampa. La funzione archivia i dati di configurazione nella chiave del registro di sistema Printers.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Funzione SetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233343"
---
# <a name="setprinterdataex-function"></a><span data-ttu-id="b0ed8-104">SetPrinterDataEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="b0ed8-104">SetPrinterDataEx function</span></span>

<span data-ttu-id="b0ed8-105">La funzione **SetPrinterDataEx** imposta i dati di configurazione per una stampante o un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-105">The **SetPrinterDataEx** function sets the configuration data for a printer or print server.</span></span> <span data-ttu-id="b0ed8-106">La funzione archivia i dati di configurazione sotto la chiave del registro di sistema della stampante.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-106">The function stores the configuration data under the printer's registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0ed8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0ed8-107">Syntax</span></span>


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a><span data-ttu-id="b0ed8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0ed8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0ed8-109">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0ed8-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ed8-110">Handle per la stampante o il server di stampa per il quale la funzione imposta i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="b0ed8-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="b0ed8-112">*pKeyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0ed8-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ed8-113">Puntatore a una stringa con terminazione null che specifica la chiave contenente il valore da impostare.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-113">A pointer to a null-terminated string that specifies the key containing the value to set.</span></span> <span data-ttu-id="b0ed8-114">Se la chiave o le sottochiavi specificate non esistono, la funzione le crea.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-114">If the specified key or subkeys do not exist, the function creates them.</span></span>

<span data-ttu-id="b0ed8-115">Per archiviare i dati di configurazione che possono essere pubblicati nel servizio directory (DS), specificare una delle seguenti chiavi del registro di sistema predefinite.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-115">To store configuration data that can be published in the directory service (DS), specify one of the following predefined registry keys.</span></span>



| <span data-ttu-id="b0ed8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b0ed8-116">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="b0ed8-117">Significato</span><span class="sxs-lookup"><span data-stu-id="b0ed8-117">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <span data-ttu-id="b0ed8-118"><dt>**SPLDS_DRIVER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="b0ed8-118"><dt>**SPLDS_DRIVER_KEY**</dt></span></span> </dl>    | <span data-ttu-id="b0ed8-119">I driver della stampante utilizzano questa chiave per archiviare le proprietà del driver.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-119">Printer drivers use this key to store driver properties.</span></span><br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <span data-ttu-id="b0ed8-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="b0ed8-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span></span> </dl> | <span data-ttu-id="b0ed8-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-121">Reserved.</span></span> <span data-ttu-id="b0ed8-122">Utilizzato solo dallo spooler di stampa per archiviare le proprietà dello spooler interno.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-122">Used only by the print spooler to store internal spooler properties.</span></span><br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <span data-ttu-id="b0ed8-123"><dt>**SPLDS_USER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="b0ed8-123"><dt>**SPLDS_USER_KEY**</dt></span></span> </dl>          | <span data-ttu-id="b0ed8-124">Le applicazioni utilizzano questa chiave per archiviare le proprietà della stampante, ad esempio i numeri degli asset della stampante.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-124">Applications use this key to store printer properties such as printer asset numbers.</span></span><br/> |



 

<span data-ttu-id="b0ed8-125">I valori archiviati con la chiave di SPLDS_USER_KEY vengono pubblicati nel servizio directory solo se nello schema è presente una proprietà corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-125">Values that are stored under the SPLDS_USER_KEY key are published in the directory service only if there is a corresponding property in the schema.</span></span> <span data-ttu-id="b0ed8-126">Un amministratore di dominio deve creare la proprietà, se non esiste già.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-126">A domain administrator must create the property if it doesn't already exist.</span></span> <span data-ttu-id="b0ed8-127">Per pubblicare una proprietà definita dall'utente dopo aver usato **SetPrinterDataEx** per aggiungere o modificare un valore, chiamare [**seprinter**](setprinter.md) con *Level* = 7 e con il membro **dwAction** di [**PRINTER_INFO_7**](printer-info-7.md) impostato su **DSPRINT_UPDATE**.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-127">To publish a user-defined property after you use **SetPrinterDataEx** to add or change a value, call [**SetPrinter**](setprinter.md) with *Level* = 7 and with the **dwAction** member of [**PRINTER_INFO_7**](printer-info-7.md) set to **DSPRINT_UPDATE**.</span></span>

<span data-ttu-id="b0ed8-128">È possibile specificare altre chiavi per archiviare i dati di configurazione non DS.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-128">You can specify other keys to store non-DS configuration data.</span></span> <span data-ttu-id="b0ed8-129">Usare il carattere barra rovesciata ( \\ ) come delimitatore per specificare un percorso con una o più sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-129">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="b0ed8-130">Se *hPrinter* è un handle per una stampante e *pKeyName* è **null** o una stringa vuota, **SetPrinterDataEx** restituisce **ERROR_INVALID_PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-130">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **SetPrinterDataEx** returns **ERROR_INVALID_PARAMETER**.</span></span>

<span data-ttu-id="b0ed8-131">Se *hPrinter* è un handle per un server di stampa, *pKeyName* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-131">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

<span data-ttu-id="b0ed8-132">Non utilizzare **SPLDS_SPOOLER_KEY**.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-132">Do not use **SPLDS_SPOOLER_KEY**.</span></span> <span data-ttu-id="b0ed8-133">Per modificare le proprietà della stampante dello spooler, usare [**Seprinter**](setprinter.md) con *Level* = 2.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-133">To change the spooler printer properties, use [**SetPrinter**](setprinter.md) with *Level* = 2.</span></span>

</dd> <dt>

<span data-ttu-id="b0ed8-134">*pValueName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0ed8-134">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ed8-135">Puntatore a una stringa con terminazione null che identifica i dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-135">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="b0ed8-136">Per le stampanti, questa stringa specifica il nome di un valore nella chiave *pKeyName* .</span><span class="sxs-lookup"><span data-stu-id="b0ed8-136">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="b0ed8-137">Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-137">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b0ed8-138">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b0ed8-138">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ed8-139">Codice che indica il tipo di dati a cui punta il parametro *pData* .</span><span class="sxs-lookup"><span data-stu-id="b0ed8-139">A code indicating the type of data pointed to by the *pData* parameter.</span></span> <span data-ttu-id="b0ed8-140">Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="b0ed8-140">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

<span data-ttu-id="b0ed8-141">Se *pKeyName* specifica una delle chiavi del servizio directory predefinite, il *tipo* deve essere **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** o **REG_BINARY**.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-141">If *pKeyName* specifies one of the predefined directory service keys, *Type* must be **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD**, or **REG_BINARY**.</span></span> <span data-ttu-id="b0ed8-142">Se si utilizza **REG_BINARY** , *cbData* deve essere uguale a 1 e il servizio directory considera i dati come un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-142">If **REG_BINARY** is used, *cbData* must be equal to 1, and the directory service treats the data as a Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="b0ed8-143">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0ed8-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ed8-144">Puntatore a un buffer che contiene i dati di configurazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-144">A pointer to a buffer that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="b0ed8-145">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0ed8-145">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ed8-146">Dimensione, in byte, della matrice.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-146">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0ed8-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0ed8-147">Return value</span></span>

<span data-ttu-id="b0ed8-148">Se la funzione ha esito positivo, il valore restituito viene **ERROR_SUCCESS**.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-148">If the function succeeds, the return value is **ERROR_SUCCESS**.</span></span>

<span data-ttu-id="b0ed8-149">Se la funzione ha esito negativo, il valore restituito è un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-149">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0ed8-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0ed8-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b0ed8-151">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b0ed8-152">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b0ed8-153">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b0ed8-154">Per recuperare i dati di configurazione esistenti per una stampante o uno spooler di stampa, chiamare la funzione [**GetPrinterDataEx**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="b0ed8-154">To retrieve existing configuration data for a printer or print spooler, call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

<span data-ttu-id="b0ed8-155">La chiamata di **SetPrinterDataEx** con il parametro *pKeyName* impostato su "PrinterDriverData" equivale alla chiamata alla funzione [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="b0ed8-155">Calling **SetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="b0ed8-156">Se *hPrinter* è un handle per un server di stampa, *pValueName* può specificare uno dei seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-156">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="b0ed8-157">valore</span><span class="sxs-lookup"><span data-stu-id="b0ed8-157">Value</span></span>                                                               | <span data-ttu-id="b0ed8-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0ed8-158">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ed8-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span></span>                                | <span data-ttu-id="b0ed8-160">Windows XP con Service Pack 2 (SP2) e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-160">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="b0ed8-161">Windows Server 2003 con Service Pack 1 (SP1) e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-161">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="b0ed8-162">**SPLREG_BEEP_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-162">**SPLREG_BEEP_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="b0ed8-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="b0ed8-164">**SPLREG_EVENT_LOG**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-164">**SPLREG_EVENT_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="b0ed8-165">**SPLREG_NET_POPUP**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-165">**SPLREG_NET_POPUP**</span></span>                                              | <span data-ttu-id="b0ed8-166">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-166">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="b0ed8-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="b0ed8-168">**SPLREG_PORT_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-168">**SPLREG_PORT_THREAD_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="b0ed8-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span></span>                        | <span data-ttu-id="b0ed8-170">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="b0ed8-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span></span>         | <span data-ttu-id="b0ed8-172">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="b0ed8-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span></span> | <span data-ttu-id="b0ed8-174">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="b0ed8-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span></span>                 | <span data-ttu-id="b0ed8-176">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="b0ed8-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span></span>             | <span data-ttu-id="b0ed8-178">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="b0ed8-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span></span>              | <span data-ttu-id="b0ed8-180">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="b0ed8-181">**SPLREG_RETRY_POPUP**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-181">**SPLREG_RETRY_POPUP**</span></span>                                            | <span data-ttu-id="b0ed8-182">In caso di esito positivo, *pData* contiene 1 se il server è impostato per ritentare le finestre popup per tutti i processi oppure 0 se il server non ritenta le finestre popup per tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-182">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="b0ed8-183">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-183">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="b0ed8-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="b0ed8-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="b0ed8-186">**SPLREG_WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-186">**SPLREG_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="b0ed8-187">Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="b0ed8-187">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="b0ed8-188">Se si passa uno dei seguenti valori predefiniti come *pValueName* , viene impostato il comportamento di stampa del pool quando si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-188">Passing one of the following predefined values as *pValueName* sets the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="b0ed8-189">valore</span><span class="sxs-lookup"><span data-stu-id="b0ed8-189">Value</span></span>                                       | <span data-ttu-id="b0ed8-190">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0ed8-190">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ed8-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span></span>   | <span data-ttu-id="b0ed8-192">Il valore di *pData* indica il tempo, in secondi, in cui un processo viene riavviato in un'altra porta dopo che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-192">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="b0ed8-193">Questa impostazione viene utilizzata con **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-193">This setting is used with **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span></span><br/> |
| <span data-ttu-id="b0ed8-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span></span> | <span data-ttu-id="b0ed8-195">Un valore diverso da zero in *pData* indica che **SPLREG_RESTART_JOB_ON_POOL_ERROR** è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-195">A nonzero value in *pData* indicates that **SPLREG_RESTART_JOB_ON_POOL_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="b0ed8-196">Il tempo specificato in **SPLREG_RESTART_JOB_ON_POOL_ERROR** è il tempo minimo.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-196">The time specified in **SPLREG_RESTART_JOB_ON_POOL_ERROR** is a minimum time.</span></span> <span data-ttu-id="b0ed8-197">Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio porta seguenti, che sono valori del registro di sistema in questa chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="b0ed8-197">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="b0ed8-198">**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ porte**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-198">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="b0ed8-199">Chiamare la funzione [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) per impostare questi valori.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-199">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="b0ed8-200">Impostazione di monitoraggio porta</span><span class="sxs-lookup"><span data-stu-id="b0ed8-200">Port monitor setting</span></span>     | <span data-ttu-id="b0ed8-201">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b0ed8-201">Data type</span></span>      | <span data-ttu-id="b0ed8-202">Significato</span><span class="sxs-lookup"><span data-stu-id="b0ed8-202">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ed8-203">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-203">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="b0ed8-204">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-204">**REG_DWORD**</span></span> | <span data-ttu-id="b0ed8-205">Se un valore diverso da zero, Abilita il monitoraggio della porta per aggiornare lo spooler con lo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-205">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="b0ed8-206">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-206">**StatusUpdateInterval**</span></span> | <span data-ttu-id="b0ed8-207">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-207">**REG_DWORD**</span></span> | <span data-ttu-id="b0ed8-208">Specifica l'intervallo, in minuti, quando il monitoraggio porta aggiorna lo spooler con lo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-208">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="b0ed8-209">Per assicurarsi che lo spooler reindirizza i processi alla successiva stampante disponibile nel pool (quando il processo di stampa non viene stampato entro l'intervallo di tempo impostato), il monitor porta deve supportare SNMP e le porte di rete nel pool devono essere configurate come "stato SNMP abilitato".</span><span class="sxs-lookup"><span data-stu-id="b0ed8-209">To ensure that the spooler redirects jobs to the next available printer in the pool (when the print job is not printed within the set time), the port monitor must support SNMP and the network ports in the pool must be configured as "SNMP status enabled."</span></span> <span data-ttu-id="b0ed8-210">Il monitoraggio porta che supporta SNMP è il monitor porta TCP/IP standard.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-210">The port monitor that supports SNMP is Standard TCP/IP port monitor.</span></span>

<span data-ttu-id="b0ed8-211">In Windows 7 e versioni successive di Windows, per impostazione predefinita viene eseguito il rendering dei processi di stampa inviati a un server di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-211">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="b0ed8-212">Il rendering lato client dei processi di stampa può essere configurato impostando *pKeyName* su "PrinterDriverData" e *pValueName* sul valore dell'impostazione nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-212">Client-side rendering of print jobs can be configured by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="b0ed8-213">Impostazione</span><span class="sxs-lookup"><span data-stu-id="b0ed8-213">Setting</span></span>                      | <span data-ttu-id="b0ed8-214">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b0ed8-214">Data type</span></span>      | <span data-ttu-id="b0ed8-215">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0ed8-215">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ed8-216">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-216">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="b0ed8-217">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-217">**REG_DWORD**</span></span> | <span data-ttu-id="b0ed8-218">Il valore 0, o se questo valore non è presente nel registro di sistema, Abilita il rendering predefinito lato client dei processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-218">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="b0ed8-219">Il valore 1 disabilita il rendering lato client dei processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-219">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="b0ed8-220">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-220">**ForceClientSideRendering**</span></span> | <span data-ttu-id="b0ed8-221">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-221">**REG_DWORD**</span></span> | <span data-ttu-id="b0ed8-222">Il valore 0, o se questo valore non è presente nel registro di sistema, provocherà il rendering dei processi di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-222">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="b0ed8-223">Se non è possibile eseguire il rendering di un processo di stampa sul client, ne verrà eseguito il rendering nel server.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-223">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="b0ed8-224">Se non è possibile eseguire il rendering di un processo di stampa sul server, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-224">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="b0ed8-225">Il valore 1 eseguirà il rendering dei processi di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-225">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="b0ed8-226">Se non è possibile eseguire il rendering di un processo di stampa sul client, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b0ed8-226">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0ed8-227">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0ed8-227">Requirements</span></span>



| <span data-ttu-id="b0ed8-228">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0ed8-228">Requirement</span></span> | <span data-ttu-id="b0ed8-229">Valore</span><span class="sxs-lookup"><span data-stu-id="b0ed8-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ed8-230">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0ed8-230">Minimum supported client</span></span><br/> | <span data-ttu-id="b0ed8-231">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b0ed8-231">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b0ed8-232">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0ed8-232">Minimum supported server</span></span><br/> | <span data-ttu-id="b0ed8-233">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b0ed8-233">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b0ed8-234">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0ed8-234">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0ed8-235"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0ed8-235"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b0ed8-236">Libreria</span><span class="sxs-lookup"><span data-stu-id="b0ed8-236">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0ed8-237"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0ed8-237"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b0ed8-238">DLL</span><span class="sxs-lookup"><span data-stu-id="b0ed8-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0ed8-239"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b0ed8-239"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b0ed8-240">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b0ed8-240">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b0ed8-241">**SetPrinterDataExW** (Unicode) e **SetPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b0ed8-241">**SetPrinterDataExW** (Unicode) and **SetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="b0ed8-242">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0ed8-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0ed8-243">Stampa</span><span class="sxs-lookup"><span data-stu-id="b0ed8-243">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b0ed8-244">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="b0ed8-244">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b0ed8-245">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-245">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="b0ed8-246">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-246">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="b0ed8-247">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-247">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="b0ed8-248">**PRINTER_INFO_7**</span><span class="sxs-lookup"><span data-stu-id="b0ed8-248">**PRINTER_INFO_7**</span></span>](printer-info-7.md)
</dt> </dl>

 

