---
description: La funzione WritePrinter notifica allo spooler di stampa che i dati devono essere scritti nella stampante specificata.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Funzione WritePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312568"
---
# <a name="writeprinter-function"></a><span data-ttu-id="75b49-103">WritePrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="75b49-103">WritePrinter function</span></span>

<span data-ttu-id="75b49-104">La funzione **WritePrinter** notifica allo spooler di stampa che i dati devono essere scritti nella stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="75b49-104">The **WritePrinter** function notifies the print spooler that data should be written to the specified printer.</span></span>

> [!Note]  
> <span data-ttu-id="75b49-105">**WritePrinter** supporta solo la stampa GDI e non deve essere utilizzato per la stampa XPS.</span><span class="sxs-lookup"><span data-stu-id="75b49-105">**WritePrinter** only supports GDI printing and must not be used for XPS printing.</span></span> <span data-ttu-id="75b49-106">Se il processo di stampa usa il percorso di stampa XPS o OpenXPS, usare l' [API di stampa XPS](/windows/desktop/printdocs/xps-printing).</span><span class="sxs-lookup"><span data-stu-id="75b49-106">If your print job uses the XPS or the OpenXPS print path, then use the [XPS Print API](/windows/desktop/printdocs/xps-printing).</span></span> <span data-ttu-id="75b49-107">L'invio di processi di stampa XPS o OpenXPS allo spooler mediante **WritePrinter** non è supportato e può causare risultati indeterminati.</span><span class="sxs-lookup"><span data-stu-id="75b49-107">Sending XPS or OpenXPS print jobs to the spooler using **WritePrinter** is not supported and can result in undetermined results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="75b49-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75b49-108">Syntax</span></span>


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a><span data-ttu-id="75b49-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="75b49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b49-110">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b49-110">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b49-111">Handle per la stampante.</span><span class="sxs-lookup"><span data-stu-id="75b49-111">A handle to the printer.</span></span> <span data-ttu-id="75b49-112">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="75b49-112">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="75b49-113">*pbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b49-113">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b49-114">Puntatore a una matrice di byte che contiene i dati che devono essere scritti sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="75b49-114">A pointer to an array of bytes that contains the data that should be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="75b49-115">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b49-115">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b49-116">Dimensione, in byte, della matrice.</span><span class="sxs-lookup"><span data-stu-id="75b49-116">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="75b49-117">*pcWritten* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="75b49-117">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75b49-118">Puntatore a un valore che riceve il numero di byte di dati scritti nella stampante.</span><span class="sxs-lookup"><span data-stu-id="75b49-118">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b49-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75b49-119">Return value</span></span>

<span data-ttu-id="75b49-120">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="75b49-120">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="75b49-121">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="75b49-121">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b49-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="75b49-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="75b49-123">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="75b49-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="75b49-124">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="75b49-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="75b49-125">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="75b49-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="75b49-126">La sequenza per un processo di stampa è la seguente:</span><span class="sxs-lookup"><span data-stu-id="75b49-126">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="75b49-127">Per iniziare un processo di stampa, chiamare [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="75b49-127">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="75b49-128">Per iniziare ogni pagina, chiamare [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="75b49-128">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="75b49-129">Per scrivere i dati in una pagina, chiamare **WritePrinter**.</span><span class="sxs-lookup"><span data-stu-id="75b49-129">To write data to a page, call **WritePrinter**.</span></span>
4.  <span data-ttu-id="75b49-130">Per terminare ogni pagina, chiamare [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="75b49-130">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="75b49-131">Ripetere 2, 3 e 4 per il numero di pagine necessario.</span><span class="sxs-lookup"><span data-stu-id="75b49-131">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="75b49-132">Per terminare il processo di stampa, chiamare [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="75b49-132">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="75b49-133">Quando un documento di alto livello (ad esempio un file Adobe PDF o Microsoft Word) o altri dati della stampante (ad esempio, PCL, PS o HPGL) vengono inviati direttamente a una stampante, le impostazioni di stampa definite nel documento prendono le precedenti rispetto alle impostazioni di stampa di Windows.</span><span class="sxs-lookup"><span data-stu-id="75b49-133">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer, the print settings defined in the document take precedent over Windows print settings.</span></span> <span data-ttu-id="75b49-134">Documents output quando il valore del membro *pDatatype* della struttura [**doc \_ info \_ 1**](doc-info-1.md) passato nel parametro *pDocInfo* della chiamata [**StartDocPrinter**](startdocprinter.md) è "Raw" deve descrivere completamente le impostazioni del processo di stampa di tipo [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)nella lingua compresa nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="75b49-134">Documents output when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW" must fully describe the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="75b49-135">Nelle versioni di Windows precedenti a Windows XP, quando una pagina in un file con spooling supera circa 350 MB, potrebbe non essere possibile stampare e inviare un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="75b49-135">In versions of Windows prior to Windows XP, when a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="75b49-136">Questo può verificarsi, ad esempio, durante la stampa di file EMF di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="75b49-136">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="75b49-137">Il limite delle dimensioni della pagina nelle versioni di Windows precedenti a Windows XP dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamante e la quantità di frammentazione nell'heap dei processi.</span><span class="sxs-lookup"><span data-stu-id="75b49-137">The page size limit in versions of Windows prior to Windows XP depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span> <span data-ttu-id="75b49-138">In Windows XP e versioni successive di Windows, i file EMF devono avere una dimensione di 2 GB o minore.</span><span class="sxs-lookup"><span data-stu-id="75b49-138">In Windows XP and later versions of Windows, EMF files must be 2GB or less in size.</span></span> <span data-ttu-id="75b49-139">Se **WritePrinter** viene usato per scrivere dati non EMF, ad esempio il PDL pronto per la stampa, le dimensioni del file sono limitate solo dallo spazio disponibile su disco.</span><span class="sxs-lookup"><span data-stu-id="75b49-139">If **WritePrinter** is used to write non EMF data, such as printer-ready PDL, the size of the file is limited only by the available disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="75b49-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="75b49-140">Examples</span></span>

<span data-ttu-id="75b49-141">Per un programma di esempio che usa questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="75b49-141">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75b49-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75b49-142">Requirements</span></span>



| <span data-ttu-id="75b49-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b49-143">Requirement</span></span> | <span data-ttu-id="75b49-144">Valore</span><span class="sxs-lookup"><span data-stu-id="75b49-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b49-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75b49-145">Minimum supported client</span></span><br/> | <span data-ttu-id="75b49-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75b49-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="75b49-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75b49-147">Minimum supported server</span></span><br/> | <span data-ttu-id="75b49-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75b49-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="75b49-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75b49-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b49-150"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75b49-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="75b49-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="75b49-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="75b49-152"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75b49-152"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="75b49-153">DLL</span><span class="sxs-lookup"><span data-stu-id="75b49-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75b49-154"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75b49-154"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="75b49-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75b49-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b49-156">Stampa</span><span class="sxs-lookup"><span data-stu-id="75b49-156">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="75b49-157">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="75b49-157">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="75b49-158">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="75b49-158">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="75b49-159">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="75b49-159">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="75b49-160">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="75b49-160">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="75b49-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="75b49-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="75b49-162">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="75b49-162">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="75b49-163">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="75b49-163">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

