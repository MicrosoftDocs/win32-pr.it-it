---
description: La funzione GetPrinterDriver recupera i dati del driver per la stampante specificata. Se il driver non è installato nel computer locale, GetPrinterDriver lo installa.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: Funzione GetPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a67a77a8167bf207231d2f3f6f063ed7636e201f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318384"
---
# <a name="getprinterdriver-function"></a><span data-ttu-id="4f5c4-104">GetPrinterDriver (funzione)</span><span class="sxs-lookup"><span data-stu-id="4f5c4-104">GetPrinterDriver function</span></span>

<span data-ttu-id="4f5c4-105">La funzione **GetPrinterDriver** recupera i dati del driver per la stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-105">The **GetPrinterDriver** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="4f5c4-106">Se il driver non è installato nel computer locale, **GetPrinterDriver** lo installa.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-106">If the driver is not installed on the local computer, **GetPrinterDriver** installs it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f5c4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f5c4-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="4f5c4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f5c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f5c4-109">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f5c4-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f5c4-110">Handle per la stampante per il quale devono essere recuperati i dati del driver.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-110">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="4f5c4-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4f5c4-112">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f5c4-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f5c4-113">Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="4f5c4-113">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="4f5c4-114">Se questo parametro è **null**, viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-114">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="4f5c4-115">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4f5c4-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f5c4-116">Struttura del driver della stampante restituita nel buffer di *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="4f5c4-116">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="4f5c4-117">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4f5c4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4f5c4-118">Value</span></span>                                                                                                | <span data-ttu-id="4f5c4-119">Significato</span><span class="sxs-lookup"><span data-stu-id="4f5c4-119">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4f5c4-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-120"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="4f5c4-121">**\_Informazioni driver \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-121">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="4f5c4-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-122"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="4f5c4-123">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-123">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="4f5c4-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-124"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="4f5c4-125">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-125">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="4f5c4-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-126"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="4f5c4-127">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-127">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="4f5c4-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-128"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="4f5c4-129">**\_Informazioni driver \_ 5**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-129">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="4f5c4-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-130"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="4f5c4-131">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-131">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="4f5c4-132"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-132"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="4f5c4-133">**\_Informazioni driver \_ 8**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-133">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="4f5c4-134">*pDriverInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f5c4-134">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f5c4-135">Puntatore a un buffer che riceve una struttura contenente informazioni sul driver, come specificato dal livello.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-135">A pointer to a buffer that receives a structure containing information about the driver, as specified by Level.</span></span> <span data-ttu-id="4f5c4-136">Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui puntano i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-136">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="4f5c4-137">Per determinare le dimensioni del buffer richieste, chiamare **GetPrinterDriver** con *cbBuf* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-137">To determine the required buffer size, call **GetPrinterDriver** with *cbBuf* set to zero.</span></span> <span data-ttu-id="4f5c4-138">**GetPrinterDriver** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-138">**GetPrinterDriver** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="4f5c4-139">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f5c4-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f5c4-140">Dimensione, in byte, della matrice in corrispondenza della quale punta *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="4f5c4-140">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="4f5c4-141">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f5c4-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f5c4-142">Puntatore a un valore che riceve il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-142">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f5c4-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f5c4-143">Return value</span></span>

<span data-ttu-id="4f5c4-144">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-144">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4f5c4-145">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-145">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="4f5c4-146">Per un driver inesistente, la funzione restituisce l' \_ errore \_ driver della stampante sconosciuto \_ .</span><span class="sxs-lookup"><span data-stu-id="4f5c4-146">For a non-existent driver, the function returns ERROR\_UNKNOWN\_PRINTER\_DRIVER.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f5c4-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f5c4-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f5c4-148">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4f5c4-149">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4f5c4-150">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4f5c4-151">Il driver info [**\_ \_ 2**](driver-info-2.md), [**driver \_ info \_ 3**](driver-info-3.md), [**driver \_ info \_ 4**](driver-info-4.md), [**driver \_ info \_ 5**](driver-info-5.md)e [**driver \_ info \_ 6**](driver-info-6.md) strutture contengono il nome file o il percorso completo e il nome file del driver della stampante nel membro **pDriverPath** .</span><span class="sxs-lookup"><span data-stu-id="4f5c4-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), and [**DRIVER\_INFO\_6**](driver-info-6.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="4f5c4-152">Un'applicazione può utilizzare il percorso e il nome file per caricare un driver della stampante chiamando la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e specificando il percorso e il nome del file come argomento singolo.</span><span class="sxs-lookup"><span data-stu-id="4f5c4-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f5c4-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f5c4-153">Requirements</span></span>



| <span data-ttu-id="4f5c4-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f5c4-154">Requirement</span></span> | <span data-ttu-id="4f5c4-155">Valore</span><span class="sxs-lookup"><span data-stu-id="4f5c4-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f5c4-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f5c4-156">Minimum supported client</span></span><br/> | <span data-ttu-id="4f5c4-157">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f5c4-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4f5c4-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f5c4-158">Minimum supported server</span></span><br/> | <span data-ttu-id="4f5c4-159">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4f5c4-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4f5c4-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f5c4-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f5c4-161"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-161"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4f5c4-162">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f5c4-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f5c4-163"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-163"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4f5c4-164">DLL</span><span class="sxs-lookup"><span data-stu-id="4f5c4-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f5c4-165"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4f5c4-165"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4f5c4-166">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4f5c4-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4f5c4-167">**GetPrinterDriverW** (Unicode) e **GetPrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4f5c4-167">**GetPrinterDriverW** (Unicode) and **GetPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="4f5c4-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f5c4-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5c4-169">Stampa</span><span class="sxs-lookup"><span data-stu-id="4f5c4-169">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-170">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="4f5c4-170">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-171">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-171">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-172">**\_Informazioni driver \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-172">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-173">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-173">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-174">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-174">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-175">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-175">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-176">**\_Informazioni driver \_ 5**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-176">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-177">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-177">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-178">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-178">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="4f5c4-179">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4f5c4-179">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

