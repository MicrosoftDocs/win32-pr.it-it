---
description: La funzione GetPrinter recupera le informazioni su una stampante specificata.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: Funzione GetPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318035"
---
# <a name="getprinter-function"></a><span data-ttu-id="bc5b3-103">GetPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="bc5b3-103">GetPrinter function</span></span>

<span data-ttu-id="bc5b3-104">La funzione **GetPrinter** recupera le informazioni su una stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-104">The **GetPrinter** function retrieves information about a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc5b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc5b3-105">Syntax</span></span>


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="bc5b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc5b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc5b3-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc5b3-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc5b3-108">Handle per la stampante per il quale la funzione recupera le informazioni.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-108">A handle to the printer for which the function retrieves information.</span></span> <span data-ttu-id="bc5b3-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="bc5b3-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="bc5b3-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc5b3-111">Il livello o il tipo di struttura archiviato dalla funzione nel buffer a cui punta *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-111">The level or type of structure that the function stores into the buffer pointed to by *pPrinter*.</span></span>

<span data-ttu-id="bc5b3-112">Questo valore può essere 1, 2, 3, 4, 5, 6, 7, 8 o 9.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-112">This value can be 1, 2, 3, 4, 5, 6, 7, 8 or 9.</span></span>

</dd> <dt>

<span data-ttu-id="bc5b3-113">*pPrinter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bc5b3-113">*pPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc5b3-114">Puntatore a un buffer che riceve una struttura contenente informazioni sulla stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-114">A pointer to a buffer that receives a structure containing information about the specified printer.</span></span> <span data-ttu-id="bc5b3-115">Il buffer deve essere sufficientemente grande da ricevere la struttura e tutte le stringhe o altri dati a cui puntano i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-115">The buffer must be large enough to receive the structure and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="bc5b3-116">Se il buffer è troppo piccolo, il parametro *pcbNeeded* restituisce le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-116">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

<span data-ttu-id="bc5b3-117">Il tipo di struttura è determinato dal valore di *Level*.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-117">The type of structure is determined by the value of *Level*.</span></span>



| <span data-ttu-id="bc5b3-118">Level</span><span class="sxs-lookup"><span data-stu-id="bc5b3-118">Level</span></span>                                                                                                | <span data-ttu-id="bc5b3-119">Struttura</span><span class="sxs-lookup"><span data-stu-id="bc5b3-119">Structure</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="bc5b3-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-120"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="bc5b3-121">Una [**struttura \_ con \_ informazioni generali sulla stampante.**](printer-info-1.md)</span><span class="sxs-lookup"><span data-stu-id="bc5b3-121">A [**PRINTER\_INFO\_1**](printer-info-1.md) structure containing general printer information.</span></span><br/>                                                                                                        |
| <span id="2"></span><dl> <span data-ttu-id="bc5b3-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-122"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="bc5b3-123">Struttura [**di \_ info \_ 2 della stampante**](printer-info-2.md) che contiene informazioni dettagliate sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-123">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                             |
| <span id="3"></span><dl> <span data-ttu-id="bc5b3-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="bc5b3-125">Struttura [**di \_ informazioni \_ sulla stampante 3**](printer-info-3.md) contenente le informazioni di sicurezza della stampante.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-125">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                 |
| <span id="4"></span><dl> <span data-ttu-id="bc5b3-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="bc5b3-127">Struttura [**di \_ informazioni \_ di stampa 4**](printer-info-4.md) contenente informazioni minime sulla stampante, tra cui il nome della stampante, il nome del server e l'eventuale presenza di una stampante remota o locale.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-127">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="bc5b3-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-128"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="bc5b3-129">Struttura [**di \_ informazioni \_ sulla stampante 5**](printer-info-5.md) che contiene informazioni sulla stampante, ad esempio attributi della stampante e impostazioni di timeout.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-129">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                               |
| <span id="6"></span><dl> <span data-ttu-id="bc5b3-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-130"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="bc5b3-131">Struttura della [**stampante \_ info \_ 6**](printer-info-6.md) che specifica il valore di stato di una stampante.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-131">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                      |
| <span id="7"></span><dl> <span data-ttu-id="bc5b3-132"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-132"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="bc5b3-133">Struttura [**di \_ info \_ 7 della stampante**](printer-info-7.md) che indica se la stampante è pubblicata nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-133">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure that indicates whether the printer is published in the directory service.</span></span><br/>                                                                      |
| <span id="8"></span><dl> <span data-ttu-id="bc5b3-134"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-134"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="bc5b3-135">Una struttura di [**\_ Info stampa \_ 8**](printer-info-8.md) che specifica le impostazioni della stampante predefinite globali.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-135">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                |
| <span id="9"></span><dl> <span data-ttu-id="bc5b3-136"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-136"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="bc5b3-137">Struttura [**Printer \_ info \_ 9**](printer-info-9.md) che specifica le impostazioni della stampante predefinite per utente.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-137">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="bc5b3-138">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc5b3-138">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc5b3-139">Dimensione, in byte, del buffer a cui punta *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-139">The size, in bytes, of the buffer pointed to by *pPrinter*.</span></span>

</dd> <dt>

<span data-ttu-id="bc5b3-140">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bc5b3-140">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc5b3-141">Puntatore a una variabile che la funzione imposta sulle dimensioni, in byte, delle informazioni sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-141">A pointer to a variable that the function sets to the size, in bytes, of the printer information.</span></span> <span data-ttu-id="bc5b3-142">Se *cbBuf* è minore di questo valore, **GetPrinter** ha esito negativo e il valore rappresenta le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-142">If *cbBuf* is smaller than this value, **GetPrinter** fails, and the value represents the required buffer size.</span></span> <span data-ttu-id="bc5b3-143">Se *cbBuf* è maggiore o uguale a questo valore, **GetPrinter** ha esito positivo e il valore rappresenta il numero di byte archiviati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-143">If *cbBuf* is equal to or greater than this value, **GetPrinter** succeeds, and the value represents the number of bytes stored in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc5b3-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc5b3-144">Return value</span></span>

<span data-ttu-id="bc5b3-145">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-145">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bc5b3-146">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-146">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc5b3-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc5b3-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bc5b3-148">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bc5b3-149">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bc5b3-150">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="bc5b3-151">Il membro **pDevMode** nelle strutture Printer Info [**\_ \_ 2**](printer-info-2.md), [**Printer \_ info \_ 8**](printer-info-8.md)e [**Printer \_ info \_ 9**](printer-info-9.md) può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-151">The **pDevMode** member in the [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_8**](printer-info-8.md), and [**PRINTER\_INFO\_9**](printer-info-9.md) structures can be **NULL**.</span></span> <span data-ttu-id="bc5b3-152">In tal caso, la stampante è inutilizzabile fino a quando il driver non viene reinstallato correttamente.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-152">When this happens, the printer is unusable until the driver is reinstalled successfully.</span></span>

<span data-ttu-id="bc5b3-153">Per le strutture [**Printer \_ info \_ 2**](printer-info-2.md) e [**Printer \_ info \_ 3**](printer-info-3.md) contenenti un puntatore a un descrittore di sicurezza, la funzione recupera solo i componenti del descrittore di sicurezza che il chiamante dispone delle autorizzazioni per la lettura.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-153">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function retrieves only those components of the security descriptor that the caller has permission to read.</span></span> <span data-ttu-id="bc5b3-154">Per recuperare particolari componenti del descrittore di sicurezza, è necessario specificare i diritti di accesso necessari quando si chiama la funzione [**OpenPrinter**](openprinter.md) per recuperare un handle per la stampante.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-154">To retrieve particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="bc5b3-155">La tabella seguente illustra i diritti di accesso necessari per leggere i diversi componenti del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-155">The following table shows the access rights required to read the various security descriptor components.</span></span>



| <span data-ttu-id="bc5b3-156">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="bc5b3-156">Access Right</span></span>                        | <span data-ttu-id="bc5b3-157">Componente del descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="bc5b3-157">Security Descriptor Component</span></span>                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc5b3-158">controllo di lettura \_</span><span class="sxs-lookup"><span data-stu-id="bc5b3-158">READ\_CONTROL</span></span><br/>            | <span data-ttu-id="bc5b3-159">Proprietario</span><span class="sxs-lookup"><span data-stu-id="bc5b3-159">Owner</span></span><br/> <span data-ttu-id="bc5b3-160">Gruppo primario</span><span class="sxs-lookup"><span data-stu-id="bc5b3-160">Primary group</span></span><br/> <span data-ttu-id="bc5b3-161">Elenco di controllo di accesso discrezionale (DACL)</span><span class="sxs-lookup"><span data-stu-id="bc5b3-161">Discretionary access-control list (DACL)</span></span><br/> |
| <span data-ttu-id="bc5b3-162">ACCESSO \_ alla \_ sicurezza del sistema</span><span class="sxs-lookup"><span data-stu-id="bc5b3-162">ACCESS\_SYSTEM\_SECURITY</span></span><br/> | <span data-ttu-id="bc5b3-163">Elenco di controllo di accesso di sistema (SACL)</span><span class="sxs-lookup"><span data-stu-id="bc5b3-163">System access-control list (SACL)</span></span><br/>                                                  |



 

<span data-ttu-id="bc5b3-164">Se si specifica Level 7, il membro **dwAction** di [**Printer \_ info \_ 7**](printer-info-7.md) restituisce uno dei valori seguenti per indicare se la stampante è pubblicata nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-164">If you specify level 7, the **dwAction** member of [**PRINTER\_INFO\_7**](printer-info-7.md) returns one of the following values to indicate whether the printer is published in the directory service.</span></span>



| <span data-ttu-id="bc5b3-165">valore dwAction</span><span class="sxs-lookup"><span data-stu-id="bc5b3-165">dwAction value</span></span>     | <span data-ttu-id="bc5b3-166">Significato</span><span class="sxs-lookup"><span data-stu-id="bc5b3-166">Meaning</span></span>                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc5b3-167">\_pubblicazione DSPRINT</span><span class="sxs-lookup"><span data-stu-id="bc5b3-167">DSPRINT\_PUBLISH</span></span>   | <span data-ttu-id="bc5b3-168">La stampante è pubblicata.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-168">The printer is published.</span></span> <span data-ttu-id="bc5b3-169">Il membro **pszObjectGUID** contiene il GUID dell'oggetto coda di stampa dei servizi directory associato alla stampante.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-169">The **pszObjectGUID** member contains the GUID of the directory services print queue object associated with the printer.</span></span>                                                                                                       |
| <span data-ttu-id="bc5b3-170">DSPRINT \_ annullare la pubblicazione</span><span class="sxs-lookup"><span data-stu-id="bc5b3-170">DSPRINT\_UNPUBLISH</span></span> | <span data-ttu-id="bc5b3-171">La stampante non è pubblicata.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-171">The printer is not published.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="bc5b3-172">DSPRINT \_ in sospeso</span><span class="sxs-lookup"><span data-stu-id="bc5b3-172">DSPRINT\_PENDING</span></span>   | <span data-ttu-id="bc5b3-173">Indica che il sistema sta tentando di completare un'operazione di pubblicazione o di Annulla pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-173">Indicates that the system is attempting to complete a publish or unpublish operation.</span></span> <span data-ttu-id="bc5b3-174">Se una chiamata del [**Seprinter**](setprinter.md) non riesce a pubblicare o annullare la pubblicazione di una stampante, il sistema tenta ulteriori tentativi di completare l'operazione in background.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-174">If a [**SetPrinter**](setprinter.md) call fails to publish or unpublish a printer, the system makes further attempts to complete the operation in the background.</span></span> |



 

<span data-ttu-id="bc5b3-175">A partire da Windows Vista, i dati della stampante restituiti da **getprintable** viene recuperato da una cache locale quando *hPrinter* fa riferimento a una stampante ospitata da un server di stampa ed è presente almeno una connessione aperta al server di stampa.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-175">Starting with Windows Vista, the printer data returned by **GetPrinter** is retrieved from a local cache when *hPrinter* refers to a printer hosted by a print server and there is at least one open connection to the print server.</span></span> <span data-ttu-id="bc5b3-176">In tutte le altre configurazioni, viene eseguita una query sui dati della stampante dal server di stampa.</span><span class="sxs-lookup"><span data-stu-id="bc5b3-176">In all other configurations, the printer data is queried from the print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc5b3-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc5b3-177">Requirements</span></span>



| <span data-ttu-id="bc5b3-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc5b3-178">Requirement</span></span> | <span data-ttu-id="bc5b3-179">Valore</span><span class="sxs-lookup"><span data-stu-id="bc5b3-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc5b3-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc5b3-180">Minimum supported client</span></span><br/> | <span data-ttu-id="bc5b3-181">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc5b3-181">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bc5b3-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc5b3-182">Minimum supported server</span></span><br/> | <span data-ttu-id="bc5b3-183">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc5b3-183">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bc5b3-184">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc5b3-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc5b3-185"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-185"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bc5b3-186">Libreria</span><span class="sxs-lookup"><span data-stu-id="bc5b3-186">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc5b3-187"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-187"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bc5b3-188">DLL</span><span class="sxs-lookup"><span data-stu-id="bc5b3-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc5b3-189"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bc5b3-189"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bc5b3-190">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bc5b3-190">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bc5b3-191">**GetPrinterW** (Unicode) e **getprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bc5b3-191">**GetPrinterW** (Unicode) and **GetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="bc5b3-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc5b3-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc5b3-193">Stampa</span><span class="sxs-lookup"><span data-stu-id="bc5b3-193">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-194">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="bc5b3-194">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-195">**AbortPrinter**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-195">**AbortPrinter**</span></span>](abortprinter.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-196">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-196">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-197">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-197">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-198">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-198">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-199">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-199">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-200">**\_Informazioni stampante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-200">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-201">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-201">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-202">**\_Informazioni stampante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-202">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-203">**\_Informazioni stampante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-203">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-204">**\_Informazioni stampante \_ 5**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-204">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-205">**Informazioni sulla stampante \_ \_ 7**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-205">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-206">**\_Informazioni stampante \_ 8**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-206">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-207">**Informazioni sulla stampante \_ \_ 9**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-207">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-208">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-208">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="bc5b3-209">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="bc5b3-209">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




