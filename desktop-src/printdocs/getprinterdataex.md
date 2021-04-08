---
description: La funzione GetPrinterDataEx recupera i dati di configurazione per la stampante o il server di stampa specificato.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: Funzione GetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bdadf2e1259445ca5285e5b12bc906140a137cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759662"
---
# <a name="getprinterdataex-function"></a><span data-ttu-id="5ab4a-103">GetPrinterDataEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="5ab4a-103">GetPrinterDataEx function</span></span>

<span data-ttu-id="5ab4a-104">La funzione **GetPrinterDataEx** recupera i dati di configurazione per la stampante o il server di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-104">The **GetPrinterDataEx** function retrieves configuration data for the specified printer or print server.</span></span> <span data-ttu-id="5ab4a-105">**GetPrinterDataEx** è in grado di recuperare i valori archiviati dalla funzione [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="5ab4a-105">**GetPrinterDataEx** can retrieve values that the [**SetPrinterData**](setprinterdata.md) function stored.</span></span> <span data-ttu-id="5ab4a-106">Inoltre, **GetPrinterDataEx** è in grado di recuperare i valori che la funzione [**SetPrinterDataEx**](setprinterdataex.md) archivia con una chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-106">In addition, **GetPrinterDataEx** can retrieve values that the [**SetPrinterDataEx**](setprinterdataex.md) function stored under a specified key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab4a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ab4a-107">Syntax</span></span>


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="5ab4a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ab4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ab4a-109">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ab4a-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab4a-110">Handle per la stampante o il server di stampa per il quale la funzione recupera i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-110">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="5ab4a-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="5ab4a-112">*pKeyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ab4a-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab4a-113">Puntatore a una stringa con terminazione null che specifica la chiave che contiene il valore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-113">A pointer to a null-terminated string that specifies the key containing the value to be retrieved.</span></span> <span data-ttu-id="5ab4a-114">Usare il carattere barra rovesciata ( \\ ) come delimitatore per specificare un percorso con una o più sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-114">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="5ab4a-115">Se *hPrinter* è un handle per una stampante e *pKeyName* è **null** o una stringa vuota, **GetPrinterDataEx** restituisce **l' \_ errore \_ parametro non valido**.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-115">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **GetPrinterDataEx** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

<span data-ttu-id="5ab4a-116">Se *hPrinter* è un handle per un server di stampa, *pKeyName* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-116">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5ab4a-117">*pValueName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ab4a-117">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab4a-118">Puntatore a una stringa con terminazione null che identifica i dati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-118">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="5ab4a-119">Per le stampanti, questa stringa specifica il nome di un valore nella chiave *pKeyName* .</span><span class="sxs-lookup"><span data-stu-id="5ab4a-119">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="5ab4a-120">Per i server di stampa, questa stringa è una delle stringhe predefinite elencate nella sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-120">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="5ab4a-121">*pType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ab4a-121">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab4a-122">Puntatore a una variabile che riceve il tipo di dati archiviati nel valore.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-122">A pointer to a variable that receives the type of data stored in the value.</span></span> <span data-ttu-id="5ab4a-123">La funzione restituisce il tipo specificato nella chiamata [**SetPrinterDataEx**](setprinterdataex.md) quando i dati sono stati archiviati.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-123">The function returns the type specified in the [**SetPrinterDataEx**](setprinterdataex.md) call when the data was stored.</span></span> <span data-ttu-id="5ab4a-124">Questo parametro può essere **null** se non sono necessarie le informazioni.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-124">This parameter can be **NULL** if you don't need the information.</span></span> <span data-ttu-id="5ab4a-125">**GetPrinterDataEx** passa *pType* come parametro *lpdwType* di una chiamata di funzione [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="5ab4a-125">**GetPrinterDataEx** passes *pType* on as the *lpdwType* parameter of a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function call.</span></span>

</dd> <dt>

<span data-ttu-id="5ab4a-126">*pData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ab4a-126">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab4a-127">Puntatore a un buffer che riceve i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-127">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="5ab4a-128">*nSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ab4a-128">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab4a-129">Dimensione, in byte, del buffer a cui punta *pData*.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-129">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

</dd> <dt>

<span data-ttu-id="5ab4a-130">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ab4a-130">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab4a-131">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-131">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="5ab4a-132">Se la dimensione del buffer specificata da *nSize* è troppo piccola, la funzione restituisce l' **errore \_ più \_ dati** e *pcbNeeded* indica le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-132">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ab4a-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ab4a-133">Return value</span></span>

<span data-ttu-id="5ab4a-134">Se la funzione ha esito positivo, il valore restituito è **Error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-134">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="5ab4a-135">Se la funzione ha esito negativo, il valore restituito è un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-135">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ab4a-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ab4a-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ab4a-137">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5ab4a-138">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5ab4a-139">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5ab4a-140">**GetPrinterDataEx** recupera i dati di configurazione della stampante impostati dalle funzioni [**SetPrinterDataEx**](setprinterdataex.md) e [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="5ab4a-140">**GetPrinterDataEx** retrieves printer-configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

<span data-ttu-id="5ab4a-141">La chiamata di **GetPrinterDataEx** con il parametro *pKeyName* impostato su "PrinterDriverData" equivale alla chiamata alla funzione [**GetPrinterData**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="5ab4a-141">Calling **GetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="5ab4a-142">Se *hPrinter* è un handle per un server di stampa, *pValueName* può specificare uno dei seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-142">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="5ab4a-143">valore</span><span class="sxs-lookup"><span data-stu-id="5ab4a-143">Value</span></span>                                                               | <span data-ttu-id="5ab4a-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ab4a-144">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab4a-145">**SPLREG \_ consentire all' \_ utente \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-145">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="5ab4a-146">Windows XP con Service Pack 2 (SP2) e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-146">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="5ab4a-147">Windows Server 2003 con Service Pack 1 (SP1) e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-147">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="5ab4a-148">**\_architettura SPLREG**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-148">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-149">**\_bip SPLREG \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-149">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-150">**SPLREG \_ directory predefinita dello \_ spooling \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-150">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-151">**\_nome del \_ computer \_ DNS SPLREG**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-151">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-152">**SPLREG \_ DS \_ presente**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-152">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="5ab4a-153">In caso di esito positivo, *pData* contiene 0x0001 se il computer si trova in un dominio DS; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-153">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="5ab4a-154">**SPLREG \_ DS \_ presente \_ per l' \_ utente**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-154">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="5ab4a-155">In caso di esito positivo, *pData* contiene 0x0001 se l'utente è connesso a un dominio DS; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-155">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="5ab4a-156">**\_registro eventi di SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-156">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-157">**\_versione principale di SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-157">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-158">**\_versione secondaria \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-158">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-159">**\_popup NET \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-159">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="5ab4a-160">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-160">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="5ab4a-161">**SPLREG \_ net \_ popup \_ al \_ computer**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-161">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="5ab4a-162">In caso di esito positivo, *pData* contiene 1 se le notifiche dei processi devono essere inviate al computer client oppure 0 se le notifiche dei processi devono essere inviate all'utente.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-162">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="5ab4a-163">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-163">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="5ab4a-164">**\_versione del sistema operativo SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-164">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="5ab4a-165">Windows XP e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-165">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-166">**\_VERSIONEX del sistema operativo SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-166">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-167">**\_ \_ \_ impostazione predefinita priorità thread porta SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-167">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-168">**\_ \_ priorità thread della porta SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-168">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-169">**\_gruppi di \_ isolamento del driver di stampa SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="5ab4a-170">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="5ab4a-171">**SPLREG \_ tempo di isolamento del driver di stampa \_ prima del \_ \_ \_ \_ riciclo**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="5ab4a-172">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="5ab4a-173">**\_numero massimo di oggetti di isolamento del driver di stampa SPLREG \_ \_ prima del \_ \_ \_ \_ riciclo**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="5ab4a-174">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="5ab4a-175">**\_timeout di \_ \_ \_ inattività isolamento driver di \_ stampa SPLREG**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-175">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="5ab4a-176">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="5ab4a-177">**\_criteri di \_ \_ esecuzione isolamento \_ driver \_ di stampa SPLREG**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-177">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="5ab4a-178">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="5ab4a-179">**\_criteri di \_ \_ sostituzione isolamento \_ driver \_ di stampa SPLREG**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-179">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="5ab4a-180">Windows 7 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="5ab4a-181">**\_fax remoto di SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-181">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="5ab4a-182">In caso di esito positivo, *pData* contiene 0x0001 se il servizio fax supporta client remoti. in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-182">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5ab4a-183">**\_popup nuovo tentativo SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-183">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="5ab4a-184">In caso di esito positivo, *pData* contiene 1 se il server è impostato per ritentare le finestre popup per tutti i processi oppure 0 se il server non ritenta le finestre popup per tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-184">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="5ab4a-185">Non supportato in Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-185">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="5ab4a-186">**\_priorità thread dell'utilità di pianificazione SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-186">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-187">**\_ \_ \_ impostazione predefinita priorità thread dell'utilità di pianificazione SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-187">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ab4a-188">**\_WEBSHAREMGMT SPLREG**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-188">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="5ab4a-189">Windows Server 2003 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="5ab4a-189">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="5ab4a-190">I valori seguenti di *pValueName* indicano il comportamento di stampa del pool quando si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-190">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="5ab4a-191">valore</span><span class="sxs-lookup"><span data-stu-id="5ab4a-191">Value</span></span>                                       | <span data-ttu-id="5ab4a-192">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ab4a-192">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab4a-193">**\_ \_ \_ errore di riavvio del processo di SPLREG nel \_ pool \_**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-193">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="5ab4a-194">Il valore di *pData* indica il tempo, in secondi, in cui un processo viene riavviato in un'altra porta dopo che si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-194">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="5ab4a-195">Questa impostazione viene usata con **\_ \_ il processo di riavvio del SPLREG \_ nel \_ pool \_ abilitato**.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-195">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="5ab4a-196">**SPLREG \_ riavvio \_ \_ del processo nel \_ pool \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-196">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="5ab4a-197">Un valore diverso da zero in *pData* indica che è abilitato il **processo di riavvio SPLREG \_ \_ \_ sull' \_ \_ errore del pool** .</span><span class="sxs-lookup"><span data-stu-id="5ab4a-197">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="5ab4a-198">Il tempo specificato nel **processo di riavvio del SPLREG \_ \_ per l' \_ \_ \_ errore del pool** è minimo.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-198">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="5ab4a-199">Il tempo effettivo può essere più lungo, a seconda delle impostazioni di monitoraggio porta seguenti, che sono valori del registro di sistema in questa chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="5ab4a-199">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="5ab4a-200">**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ porte**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-200">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="5ab4a-201">Chiamare la funzione [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) per eseguire una query su questi valori.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-201">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="5ab4a-202">Impostazione di monitoraggio porta</span><span class="sxs-lookup"><span data-stu-id="5ab4a-202">Port monitor setting</span></span>     | <span data-ttu-id="5ab4a-203">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5ab4a-203">Data type</span></span>      | <span data-ttu-id="5ab4a-204">Significato</span><span class="sxs-lookup"><span data-stu-id="5ab4a-204">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab4a-205">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-205">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="5ab4a-206">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-206">**REG\_DWORD**</span></span> | <span data-ttu-id="5ab4a-207">Se un valore diverso da zero, Abilita il monitoraggio della porta per aggiornare lo spooler con lo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-207">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="5ab4a-208">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-208">**StatusUpdateInterval**</span></span> | <span data-ttu-id="5ab4a-209">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-209">**REG\_DWORD**</span></span> | <span data-ttu-id="5ab4a-210">Specifica l'intervallo, in minuti, quando il monitoraggio porta aggiorna lo spooler con lo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-210">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="5ab4a-211">Se *pKeyName* è una delle chiavi di servizio directory (DS) predefinite (vedere [**seprinter**](setprinter.md)) e *pValueName* contiene una virgola (','), la parte di *pValueName* prima della virgola è il nome del valore e la parte di *pValueName* a destra della virgola è l'OID della proprietà DS.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-211">If *pKeyName* is one of the predefined Directory Service (DS) keys (see [**SetPrinter**](setprinter.md)) and *pValueName* contains a comma (','), then the portion of *pValueName* before the comma is the value name and the portion of *pValueName* to the right of the comma is the DS Property OID.</span></span> <span data-ttu-id="5ab4a-212">Viene creata una sottochiave denominata OID e viene immesso un nuovo valore costituito dal nome del valore e dall'OID sotto la chiave OID.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-212">A subkey called OID is created and a new value that consists of the value name and OID is entered under the OID key.</span></span> <span data-ttu-id="5ab4a-213">[**SetPrinterDataEx**](setprinterdataex.md) aggiunge anche il nome del valore e i dati sotto la chiave DS.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-213">[**SetPrinterDataEx**](setprinterdataex.md) also adds the value name and data under the DS key.</span></span>

<span data-ttu-id="5ab4a-214">In Windows 7 e versioni successive di Windows, per impostazione predefinita viene eseguito il rendering dei processi di stampa inviati a un server di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-214">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="5ab4a-215">La configurazione del rendering lato client per una stampante può essere letta impostando *pKeyName* su "PrinterDriverData" e *pValueName* sul valore dell'impostazione nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-215">The configuration of client-side rendering for a printer can be read by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="5ab4a-216">Impostazione</span><span class="sxs-lookup"><span data-stu-id="5ab4a-216">Setting</span></span>                      | <span data-ttu-id="5ab4a-217">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5ab4a-217">Data type</span></span>      | <span data-ttu-id="5ab4a-218">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ab4a-218">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab4a-219">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-219">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="5ab4a-220">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-220">**REG\_DWORD**</span></span> | <span data-ttu-id="5ab4a-221">Il valore 0, o se questo valore non è presente nel registro di sistema, Abilita il rendering predefinito lato client dei processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-221">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="5ab4a-222">Il valore 1 disabilita il rendering lato client dei processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-222">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="5ab4a-223">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-223">**ForceClientSideRendering**</span></span> | <span data-ttu-id="5ab4a-224">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-224">**REG\_DWORD**</span></span> | <span data-ttu-id="5ab4a-225">Il valore 0, o se questo valore non è presente nel registro di sistema, provocherà il rendering dei processi di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-225">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="5ab4a-226">Se non è possibile eseguire il rendering di un processo di stampa sul client, ne verrà eseguito il rendering nel server.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-226">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="5ab4a-227">Se non è possibile eseguire il rendering di un processo di stampa sul server, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-227">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="5ab4a-228">Il valore 1 eseguirà il rendering dei processi di stampa nel client.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-228">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="5ab4a-229">Se non è possibile eseguire il rendering di un processo di stampa sul client, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5ab4a-229">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5ab4a-230">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ab4a-230">Requirements</span></span>



| <span data-ttu-id="5ab4a-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ab4a-231">Requirement</span></span> | <span data-ttu-id="5ab4a-232">Valore</span><span class="sxs-lookup"><span data-stu-id="5ab4a-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab4a-233">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ab4a-233">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab4a-234">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5ab4a-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5ab4a-235">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ab4a-235">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab4a-236">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5ab4a-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ab4a-237">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ab4a-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ab4a-238"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ab4a-238"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5ab4a-239">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ab4a-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ab4a-240"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ab4a-240"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5ab4a-241">DLL</span><span class="sxs-lookup"><span data-stu-id="5ab4a-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ab4a-242"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5ab4a-242"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5ab4a-243">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5ab4a-243">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5ab4a-244">**GetPrinterDataExW** (Unicode) e **GetPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5ab4a-244">**GetPrinterDataExW** (Unicode) and **GetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="5ab4a-245">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ab4a-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab4a-246">Stampa</span><span class="sxs-lookup"><span data-stu-id="5ab4a-246">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5ab4a-247">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="5ab4a-247">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5ab4a-248">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-248">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="5ab4a-249">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="5ab4a-249">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

