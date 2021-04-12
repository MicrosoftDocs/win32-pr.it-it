---
description: La funzione GetPrinterDriver2 recupera i dati del driver per la stampante specificata. Se il driver non è installato nel computer locale, GetPrinterDriver2 lo installa e visualizza qualsiasi interfaccia utente per la finestra specificata.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: Funzione GetPrinterDriver2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233730"
---
# <a name="getprinterdriver2-function"></a><span data-ttu-id="02b3c-104">GetPrinterDriver2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="02b3c-104">GetPrinterDriver2 function</span></span>

<span data-ttu-id="02b3c-105">La funzione **GetPrinterDriver2** recupera i dati del driver per la stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="02b3c-105">The **GetPrinterDriver2** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="02b3c-106">Se il driver non è installato nel computer locale, **GetPrinterDriver2** lo installa e visualizza qualsiasi interfaccia utente per la finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="02b3c-106">If the driver is not installed on the local computer, **GetPrinterDriver2** installs it and displays any user interface to the specified window.</span></span>

## <a name="syntax"></a><span data-ttu-id="02b3c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02b3c-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="02b3c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="02b3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02b3c-109">*HWND* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="02b3c-109">*hWnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="02b3c-110">Handle della finestra che verrà utilizzata come finestra padre di qualsiasi interfaccia utente, ad esempio una finestra di dialogo, visualizzata dal driver durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="02b3c-110">A handle of the window that will be used as the parent window of any user interface, such as a dialog box, that the driver displays during installation.</span></span> <span data-ttu-id="02b3c-111">Se il valore di questo parametro è **null**, l'interfaccia utente del driver verrà comunque visualizzata all'utente durante l'installazione, ma non avrà una finestra padre.</span><span class="sxs-lookup"><span data-stu-id="02b3c-111">If the value of this parameter is **NULL**, the driver's user interface will still be displayed to the user during installation, but it will not have a parent window.</span></span>

</dd> <dt>

<span data-ttu-id="02b3c-112">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02b3c-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02b3c-113">Handle per la stampante per il quale devono essere recuperati i dati del driver.</span><span class="sxs-lookup"><span data-stu-id="02b3c-113">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="02b3c-114">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="02b3c-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="02b3c-115">*pEnvironment* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="02b3c-115">*pEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="02b3c-116">Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="02b3c-116">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="02b3c-117">Se questo parametro è **null**, viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="02b3c-117">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="02b3c-118">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="02b3c-118">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02b3c-119">Struttura del driver della stampante restituita nel buffer di *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="02b3c-119">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="02b3c-120">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="02b3c-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="02b3c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="02b3c-121">Value</span></span>                                                                                                | <span data-ttu-id="02b3c-122">Significato</span><span class="sxs-lookup"><span data-stu-id="02b3c-122">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="02b3c-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-123"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="02b3c-124">**\_Informazioni driver \_ 1**</span><span class="sxs-lookup"><span data-stu-id="02b3c-124">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="02b3c-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-125"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="02b3c-126">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="02b3c-126">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="02b3c-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-127"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="02b3c-128">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="02b3c-128">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="02b3c-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-129"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="02b3c-130">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="02b3c-130">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="02b3c-131"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-131"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="02b3c-132">**\_Informazioni driver \_ 5**</span><span class="sxs-lookup"><span data-stu-id="02b3c-132">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="02b3c-133"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-133"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="02b3c-134">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="02b3c-134">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="02b3c-135"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-135"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="02b3c-136">**\_Informazioni driver \_ 8**</span><span class="sxs-lookup"><span data-stu-id="02b3c-136">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="02b3c-137">*pDriverInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="02b3c-137">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02b3c-138">Puntatore a un buffer che riceve una struttura contenente informazioni sul driver, come specificato dal *livello*.</span><span class="sxs-lookup"><span data-stu-id="02b3c-138">A pointer to a buffer that receives a structure containing information about the driver, as specified by *Level*.</span></span> <span data-ttu-id="02b3c-139">Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui puntano i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="02b3c-139">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="02b3c-140">Per determinare le dimensioni del buffer richieste, chiamare **GetPrinterDriver2** con *cbBuf* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="02b3c-140">To determine the required buffer size, call **GetPrinterDriver2** with *cbBuf* set to zero.</span></span> <span data-ttu-id="02b3c-141">**GetPrinterDriver2** ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore \_ \_ buffer insufficiente** e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="02b3c-141">**GetPrinterDriver2** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="02b3c-142">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02b3c-142">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02b3c-143">Dimensione, in byte, della matrice in corrispondenza della quale punta *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="02b3c-143">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="02b3c-144">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="02b3c-144">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02b3c-145">Puntatore a un valore che riceve il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="02b3c-145">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02b3c-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02b3c-146">Return value</span></span>

<span data-ttu-id="02b3c-147">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="02b3c-147">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="02b3c-148">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="02b3c-148">If the function fails, the return value is zero.</span></span> <span data-ttu-id="02b3c-149">Per ottenere lo stato restituito, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="02b3c-149">To get the return status, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="02b3c-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="02b3c-150">Remarks</span></span>

<span data-ttu-id="02b3c-151">Il driver info [**\_ \_ 2**](driver-info-2.md), [**driver \_ info \_ 3**](driver-info-3.md), [**driver \_ info \_ 4**](driver-info-4.md), [**driver \_ info \_ 5**](driver-info-5.md), [**driver \_ info \_ 6**](driver-info-6.md)e [**driver \_ info \_ 8**](driver-info-8.md) Structures contengono il nome file o il percorso completo e il nome file del driver della stampante nel membro **pDriverPath** .</span><span class="sxs-lookup"><span data-stu-id="02b3c-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), [**DRIVER\_INFO\_6**](driver-info-6.md), and [**DRIVER\_INFO\_8**](driver-info-8.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="02b3c-152">Un'applicazione può utilizzare il percorso e il nome file per caricare un driver della stampante chiamando la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e specificando il percorso e il nome del file come argomento singolo.</span><span class="sxs-lookup"><span data-stu-id="02b3c-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

<span data-ttu-id="02b3c-153">La versione ANSI di questa funzione, **GetPrinterDriver2A** , non è supportata e restituisce l' **errore \_ non \_ supportato**.</span><span class="sxs-lookup"><span data-stu-id="02b3c-153">The ANSI version of this function, **GetPrinterDriver2A** is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="02b3c-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02b3c-154">Requirements</span></span>



| <span data-ttu-id="02b3c-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="02b3c-155">Requirement</span></span> | <span data-ttu-id="02b3c-156">Valore</span><span class="sxs-lookup"><span data-stu-id="02b3c-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b3c-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02b3c-157">Minimum supported client</span></span><br/> | <span data-ttu-id="02b3c-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02b3c-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="02b3c-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02b3c-159">Minimum supported server</span></span><br/> | <span data-ttu-id="02b3c-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02b3c-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="02b3c-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02b3c-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="02b3c-162"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="02b3c-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="02b3c-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="02b3c-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="02b3c-165">DLL</span><span class="sxs-lookup"><span data-stu-id="02b3c-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02b3c-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="02b3c-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="02b3c-167">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="02b3c-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="02b3c-168">**GetPrinterDriver2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="02b3c-168">**GetPrinterDriver2W** (Unicode)</span></span><br/>                                                               |



## <a name="see-also"></a><span data-ttu-id="02b3c-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02b3c-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b3c-170">Stampa</span><span class="sxs-lookup"><span data-stu-id="02b3c-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="02b3c-171">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="02b3c-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="02b3c-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="02b3c-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="02b3c-173">**\_Informazioni driver \_ 1**</span><span class="sxs-lookup"><span data-stu-id="02b3c-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="02b3c-174">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="02b3c-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="02b3c-175">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="02b3c-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="02b3c-176">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="02b3c-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="02b3c-177">**\_Informazioni driver \_ 5**</span><span class="sxs-lookup"><span data-stu-id="02b3c-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="02b3c-178">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="02b3c-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="02b3c-179">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="02b3c-179">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="02b3c-180">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="02b3c-180">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="02b3c-181">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="02b3c-181">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

