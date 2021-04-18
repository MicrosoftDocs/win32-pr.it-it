---
description: La funzione GetPrinterData recupera i dati di configurazione per la stampante o il server di stampa specificato.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Funzione GetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314995"
---
# <a name="getprinterdata-function"></a><span data-ttu-id="4f68e-103">GetPrinterData (funzione)</span><span class="sxs-lookup"><span data-stu-id="4f68e-103">GetPrinterData function</span></span>

<span data-ttu-id="4f68e-104">La funzione **GetPrinterData** recupera i dati di configurazione per la stampante o il server di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="4f68e-104">The **GetPrinterData** function retrieves configuration data for the specified printer or print server.</span></span>

<span data-ttu-id="4f68e-105">In Windows 2000 e versioni successive di Windows, la chiamata di **GetPrinterData** equivale alla chiamata di [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) con il parametro *pKeyName* impostato su "PrinterDriverData".</span><span class="sxs-lookup"><span data-stu-id="4f68e-105">In Windows 2000 and later versions of Windows, calling **GetPrinterData** is equivalent to calling [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="4f68e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f68e-106">Syntax</span></span>


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="4f68e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f68e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f68e-108">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f68e-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f68e-109">Handle per la stampante o il server di stampa per il quale la funzione recupera i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="4f68e-109">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="4f68e-110">Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="4f68e-110">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4f68e-111">*pValueName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f68e-111">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f68e-112">Puntatore a una stringa con terminazione null che identifica i dati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="4f68e-112">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="4f68e-113">Per le stampanti, questa stringa è il nome di un valore del registro di sistema nella chiave "PrinterDriverData" della stampante nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4f68e-113">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="4f68e-114">Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="4f68e-114">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="4f68e-115">*pType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f68e-115">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f68e-116">Puntatore a una variabile che riceve un valore che indica il tipo di dati recuperati in *pData*.</span><span class="sxs-lookup"><span data-stu-id="4f68e-116">A pointer to a variable that receives a value that indicates the type of data retrieved in *pData*.</span></span> <span data-ttu-id="4f68e-117">La funzione restituisce il tipo specificato nella chiamata a [**SetPrinterData**](setprinterdata.md) o [**SetPrinterDataEx**](setprinterdataex.md) in cui sono archiviati i dati.</span><span class="sxs-lookup"><span data-stu-id="4f68e-117">The function returns the type specified in the [**SetPrinterData**](setprinterdata.md) or [**SetPrinterDataEx**](setprinterdataex.md) call that stored the data.</span></span> <span data-ttu-id="4f68e-118">Se non è necessario il tipo di dati, impostare questo parametro su **null** .</span><span class="sxs-lookup"><span data-stu-id="4f68e-118">Set this parameter to **NULL** if you don't need the data type.</span></span>

</dd> <dt>

<span data-ttu-id="4f68e-119">*pData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f68e-119">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f68e-120">Puntatore a un buffer che riceve i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="4f68e-120">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="4f68e-121">*nSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f68e-121">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f68e-122">Dimensione, in byte, del buffer a cui punta *pData* .</span><span class="sxs-lookup"><span data-stu-id="4f68e-122">The size, in bytes, of the buffer that *pData* points to.</span></span>

</dd> <dt>

<span data-ttu-id="4f68e-123">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f68e-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f68e-124">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="4f68e-124">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="4f68e-125">Se la dimensione del buffer specificata da *nSize* è troppo piccola, la funzione restituisce l' **errore \_ più \_ dati** e *pcbNeeded* indica le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="4f68e-125">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f68e-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f68e-126">Return value</span></span>

<span data-ttu-id="4f68e-127">Se la funzione ha esito positivo, il valore restituito è **Error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="4f68e-127">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="4f68e-128">Se la funzione ha esito negativo, il valore restituito è un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="4f68e-128">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f68e-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f68e-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f68e-130">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4f68e-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4f68e-131">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4f68e-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4f68e-132">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="4f68e-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4f68e-133">**GetPrinterData** recupera i dati di configurazione della stampante impostati dalla funzione [**SetPrinterDataEx**](setprinterdataex.md) o [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="4f68e-133">**GetPrinterData** retrieves printer configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) or [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="4f68e-134">**GetPrinterData** potrebbe attivare una chiamata di Windows a [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), che potrebbe scrivere nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4f68e-134">**GetPrinterData** might trigger a Windows call to [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), which might write to the registry.</span></span> <span data-ttu-id="4f68e-135">In tal caso, è possibile che si verifichino effetti collaterali, ad esempio l'attivazione di un evento di aggiornamento o di aggiornamento della stampante con ID 20 nel client, se la stampante è condivisa in una rete.</span><span class="sxs-lookup"><span data-stu-id="4f68e-135">If it does, side effects can occur, such as triggering an update or upgrade printer event ID 20 in the client, if the printer is shared in a network.</span></span>

<span data-ttu-id="4f68e-136">Se *hPrinter* è un handle per un server di stampa, *pValueName* può specificare uno dei seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4f68e-136">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="4f68e-137">valore</span><span class="sxs-lookup"><span data-stu-id="4f68e-137">Value</span></span>                                                               | <span data-ttu-id="4f68e-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f68e-138">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f68e-139">**SPLREG \_ consentire all' \_ utente \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="4f68e-139">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="4f68e-140">Windows XP con Service Pack 2 (SP2) e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-140">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="4f68e-141">Windows Server 2003 con Service Pack 1 (SP1) e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-141">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="4f68e-142">**\_architettura SPLREG**</span><span class="sxs-lookup"><span data-stu-id="4f68e-142">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-143">**\_bip SPLREG \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="4f68e-143">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-144">**SPLREG \_ directory predefinita dello \_ spooling \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-144">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-145">**\_nome del \_ computer \_ DNS SPLREG**</span><span class="sxs-lookup"><span data-stu-id="4f68e-145">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-146">**SPLREG \_ DS \_ presente**</span><span class="sxs-lookup"><span data-stu-id="4f68e-146">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="4f68e-147">In caso di esito positivo, *pData* contiene 0x0001 se il computer si trova in un dominio DS; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="4f68e-147">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="4f68e-148">**SPLREG \_ DS \_ presente \_ per l' \_ utente**</span><span class="sxs-lookup"><span data-stu-id="4f68e-148">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="4f68e-149">In caso di esito positivo, *pData* contiene 0x0001 se l'utente è connesso a un dominio DS; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="4f68e-149">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="4f68e-150">**\_registro eventi di SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-150">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-151">**\_versione principale di SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-151">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-152">**\_versione secondaria \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="4f68e-152">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-153">**\_popup NET \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="4f68e-153">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="4f68e-154">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-154">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="4f68e-155">**SPLREG \_ net \_ popup \_ al \_ computer**</span><span class="sxs-lookup"><span data-stu-id="4f68e-155">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="4f68e-156">In caso di esito positivo, *pData* contiene 1 se le notifiche dei processi devono essere inviate al computer client oppure 0 se le notifiche dei processi devono essere inviate all'utente.</span><span class="sxs-lookup"><span data-stu-id="4f68e-156">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="4f68e-157">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-157">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="4f68e-158">**\_versione del sistema operativo SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-158">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="4f68e-159">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-159">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-160">**\_VERSIONEX del sistema operativo SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-160">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-161">**\_ \_ \_ impostazione predefinita priorità thread porta SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-161">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-162">**\_ \_ priorità thread della porta SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-162">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-163">**\_gruppi di \_ isolamento del driver di stampa SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-163">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="4f68e-164">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-164">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4f68e-165">**SPLREG \_ tempo di isolamento del driver di stampa \_ prima del \_ \_ \_ \_ riciclo**</span><span class="sxs-lookup"><span data-stu-id="4f68e-165">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="4f68e-166">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-166">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4f68e-167">**\_numero massimo di oggetti di isolamento del driver di stampa SPLREG \_ \_ prima del \_ \_ \_ \_ riciclo**</span><span class="sxs-lookup"><span data-stu-id="4f68e-167">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="4f68e-168">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-168">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4f68e-169">**\_timeout di \_ \_ \_ inattività isolamento driver di \_ stampa SPLREG**</span><span class="sxs-lookup"><span data-stu-id="4f68e-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="4f68e-170">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4f68e-171">**\_criteri di \_ \_ esecuzione isolamento \_ driver \_ di stampa SPLREG**</span><span class="sxs-lookup"><span data-stu-id="4f68e-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="4f68e-172">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4f68e-173">**\_criteri di \_ \_ sostituzione isolamento \_ driver \_ di stampa SPLREG**</span><span class="sxs-lookup"><span data-stu-id="4f68e-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="4f68e-174">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="4f68e-175">**\_fax remoto di SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-175">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="4f68e-176">In caso di esito positivo, *pData* contiene 0x0001 se il servizio fax supporta client remoti. in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="4f68e-176">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="4f68e-177">**\_popup nuovo tentativo SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-177">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="4f68e-178">In caso di esito positivo, *pData* contiene 1 se il server è impostato per ritentare le finestre popup per tutti i processi oppure 0 se il server non ritenta le finestre popup per tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="4f68e-178">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="4f68e-179">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-179">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="4f68e-180">**\_priorità thread dell'utilità di pianificazione SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-180">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-181">**\_ \_ \_ impostazione predefinita priorità thread dell'utilità di pianificazione SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-181">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="4f68e-182">**\_WEBSHAREMGMT SPLREG**</span><span class="sxs-lookup"><span data-stu-id="4f68e-182">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="4f68e-183">Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="4f68e-183">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="4f68e-184">I valori seguenti di *pValueName* indicano il comportamento di stampa del pool quando si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="4f68e-184">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="4f68e-185">valore</span><span class="sxs-lookup"><span data-stu-id="4f68e-185">Value</span></span>                                       | <span data-ttu-id="4f68e-186">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f68e-186">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f68e-187">**\_ \_ \_ errore di riavvio del processo di SPLREG nel \_ pool \_**</span><span class="sxs-lookup"><span data-stu-id="4f68e-187">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="4f68e-188">Il valore di *pData* indica il tempo, in secondi, in cui un processo viene riavviato in un'altra porta dopo che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="4f68e-188">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="4f68e-189">Questa impostazione viene usata con **\_ \_ il processo di riavvio del SPLREG \_ nel \_ pool \_ abilitato**.</span><span class="sxs-lookup"><span data-stu-id="4f68e-189">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="4f68e-190">**SPLREG \_ riavvio \_ \_ del processo nel \_ pool \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="4f68e-190">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="4f68e-191">Un valore diverso da zero in *pData* indica che è abilitato il **processo di riavvio SPLREG \_ \_ \_ sull' \_ \_ errore del pool** .</span><span class="sxs-lookup"><span data-stu-id="4f68e-191">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="4f68e-192">Il tempo specificato nel **processo di riavvio del SPLREG \_ \_ per l' \_ \_ \_ errore del pool** è minimo.</span><span class="sxs-lookup"><span data-stu-id="4f68e-192">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="4f68e-193">Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio porta seguenti, che sono valori del registro di sistema in questa chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="4f68e-193">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="4f68e-194">**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ porte**</span><span class="sxs-lookup"><span data-stu-id="4f68e-194">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="4f68e-195">Chiamare la funzione [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) per eseguire una query su questi valori.</span><span class="sxs-lookup"><span data-stu-id="4f68e-195">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="4f68e-196">Impostazione di monitoraggio porta</span><span class="sxs-lookup"><span data-stu-id="4f68e-196">Port monitor setting</span></span>     | <span data-ttu-id="4f68e-197">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4f68e-197">Data type</span></span>      | <span data-ttu-id="4f68e-198">Significato</span><span class="sxs-lookup"><span data-stu-id="4f68e-198">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f68e-199">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="4f68e-199">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="4f68e-200">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4f68e-200">**REG\_DWORD**</span></span> | <span data-ttu-id="4f68e-201">Se un valore diverso da zero, Abilita il monitoraggio della porta per aggiornare lo spooler con lo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="4f68e-201">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="4f68e-202">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="4f68e-202">**StatusUpdateInterval**</span></span> | <span data-ttu-id="4f68e-203">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4f68e-203">**REG\_DWORD**</span></span> | <span data-ttu-id="4f68e-204">Specifica l'intervallo, in minuti, quando il monitoraggio porta aggiorna lo spooler con lo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="4f68e-204">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="4f68e-205">In Windows 7 e versioni successive di Windows, per impostazione predefinita viene eseguito il rendering dei processi di stampa inviati a un server di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="4f68e-205">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="4f68e-206">I valori seguenti configurano il rendering lato client di un processo di stampa e possono essere letti se si impostano i valori seguenti in *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="4f68e-206">The following values configure client-side rendering of a print jobs and can be read if you set the following values in *pValueName*.</span></span>



| <span data-ttu-id="4f68e-207">Impostazione</span><span class="sxs-lookup"><span data-stu-id="4f68e-207">Setting</span></span>                      | <span data-ttu-id="4f68e-208">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4f68e-208">Data type</span></span>      | <span data-ttu-id="4f68e-209">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f68e-209">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f68e-210">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="4f68e-210">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="4f68e-211">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4f68e-211">**REG\_DWORD**</span></span> | <span data-ttu-id="4f68e-212">Il valore 0, o se questo valore non è presente nel registro di sistema, Abilita il rendering predefinito lato client dei processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="4f68e-212">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="4f68e-213">Il valore 1 disabilita il rendering lato client dei processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="4f68e-213">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="4f68e-214">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="4f68e-214">**ForceClientSideRendering**</span></span> | <span data-ttu-id="4f68e-215">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4f68e-215">**REG\_DWORD**</span></span> | <span data-ttu-id="4f68e-216">Il valore 0, o se questo valore non è presente nel registro di sistema, provocherà il rendering dei processi di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="4f68e-216">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="4f68e-217">Se non è possibile eseguire il rendering di un processo di stampa sul client, ne verrà eseguito il rendering nel server.</span><span class="sxs-lookup"><span data-stu-id="4f68e-217">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="4f68e-218">Se non è possibile eseguire il rendering di un processo di stampa sul server, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4f68e-218">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="4f68e-219">Il valore 1 eseguirà il rendering dei processi di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="4f68e-219">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="4f68e-220">Se non è possibile eseguire il rendering di un processo di stampa sul client, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4f68e-220">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4f68e-221">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f68e-221">Requirements</span></span>



| <span data-ttu-id="4f68e-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f68e-222">Requirement</span></span> | <span data-ttu-id="4f68e-223">Valore</span><span class="sxs-lookup"><span data-stu-id="4f68e-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f68e-224">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f68e-224">Minimum supported client</span></span><br/> | <span data-ttu-id="4f68e-225">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f68e-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4f68e-226">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f68e-226">Minimum supported server</span></span><br/> | <span data-ttu-id="4f68e-227">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f68e-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4f68e-228">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f68e-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f68e-229"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f68e-229"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4f68e-230">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f68e-230">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f68e-231"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f68e-231"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4f68e-232">DLL</span><span class="sxs-lookup"><span data-stu-id="4f68e-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f68e-233"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4f68e-233"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4f68e-234">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4f68e-234">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4f68e-235">**GetPrinterDataW** (Unicode) e **GetPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4f68e-235">**GetPrinterDataW** (Unicode) and **GetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="4f68e-236">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f68e-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f68e-237">Stampa</span><span class="sxs-lookup"><span data-stu-id="4f68e-237">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4f68e-238">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="4f68e-238">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4f68e-239">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="4f68e-239">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="4f68e-240">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4f68e-240">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="4f68e-241">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="4f68e-241">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="4f68e-242">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="4f68e-242">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="4f68e-243">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="4f68e-243">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="4f68e-244">**PRINTPROCESSOR \_ Caps \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4f68e-244">**PRINTPROCESSOR\_CAPS\_1**</span></span>](printprocessor-caps-1.md)
</dt> </dl>

 

