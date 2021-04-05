---
description: La funzione StartDocPrinter notifica allo spooler di stampa che è necessario eseguire lo spooling di un documento per la stampa.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: Funzione StartDocPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884669"
---
# <a name="startdocprinter-function"></a><span data-ttu-id="54a6b-103">StartDocPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="54a6b-103">StartDocPrinter function</span></span>

<span data-ttu-id="54a6b-104">La funzione **StartDocPrinter** notifica allo spooler di stampa che è necessario eseguire lo spooling di un documento per la stampa.</span><span class="sxs-lookup"><span data-stu-id="54a6b-104">The **StartDocPrinter** function notifies the print spooler that a document is to be spooled for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a6b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54a6b-105">Syntax</span></span>


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a><span data-ttu-id="54a6b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="54a6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54a6b-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54a6b-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a6b-108">Handle per la stampante.</span><span class="sxs-lookup"><span data-stu-id="54a6b-108">A handle to the printer.</span></span> <span data-ttu-id="54a6b-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="54a6b-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="54a6b-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="54a6b-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a6b-111">Versione della struttura a cui punta *pDocInfo* .</span><span class="sxs-lookup"><span data-stu-id="54a6b-111">The version of the structure to which *pDocInfo* points.</span></span> <span data-ttu-id="54a6b-112">Questo valore deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="54a6b-112">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="54a6b-113">*pDocInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54a6b-113">*pDocInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54a6b-114">Puntatore a una struttura [**doc \_ info \_ 1**](doc-info-1.md) che descrive il documento da stampare.</span><span class="sxs-lookup"><span data-stu-id="54a6b-114">A pointer to a [**DOC\_INFO\_1**](doc-info-1.md) structure that describes the document to print.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54a6b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54a6b-115">Return value</span></span>

<span data-ttu-id="54a6b-116">Se la funzione ha esito positivo, il valore restituito identifica il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="54a6b-116">If the function succeeds, the return value identifies the print job.</span></span>

<span data-ttu-id="54a6b-117">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="54a6b-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="54a6b-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="54a6b-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54a6b-119">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="54a6b-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="54a6b-120">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="54a6b-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="54a6b-121">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="54a6b-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="54a6b-122">La sequenza tipica per un processo di stampa è la seguente:</span><span class="sxs-lookup"><span data-stu-id="54a6b-122">The typical sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="54a6b-123">Per iniziare un processo di stampa, chiamare **StartDocPrinter**.</span><span class="sxs-lookup"><span data-stu-id="54a6b-123">To begin a print job, call **StartDocPrinter**.</span></span>
2.  <span data-ttu-id="54a6b-124">Per iniziare ogni pagina, chiamare [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="54a6b-124">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="54a6b-125">Per scrivere i dati in una pagina, chiamare [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="54a6b-125">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="54a6b-126">Per terminare ogni pagina, chiamare [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="54a6b-126">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="54a6b-127">Ripetere 2, 3 e 4 per il numero di pagine necessario.</span><span class="sxs-lookup"><span data-stu-id="54a6b-127">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="54a6b-128">Per terminare il processo di stampa, chiamare [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="54a6b-128">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="54a6b-129">Si noti che la chiamata a [**StartPagePrinter**](startpageprinter.md) e [**EndPagePrinter**](endpageprinter.md) potrebbe non essere necessaria, ad esempio se il tipo di dati di stampa include le informazioni sulla pagina.</span><span class="sxs-lookup"><span data-stu-id="54a6b-129">Note that calling [**StartPagePrinter**](startpageprinter.md) and [**EndPagePrinter**](endpageprinter.md) may not be necessary, such as if the print data type includes the page information.</span></span>

<span data-ttu-id="54a6b-130">Quando una pagina in un file con spooling supera circa 350 MB, potrebbe non essere possibile stampare e inviare un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="54a6b-130">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="54a6b-131">Questo può verificarsi, ad esempio, durante la stampa di file EMF di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="54a6b-131">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="54a6b-132">Il limite delle dimensioni della pagina dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamante e la quantità di frammentazione nell'heap dei processi.</span><span class="sxs-lookup"><span data-stu-id="54a6b-132">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="54a6b-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="54a6b-133">Examples</span></span>

<span data-ttu-id="54a6b-134">Per un programma di esempio che usa questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="54a6b-134">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54a6b-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54a6b-135">Requirements</span></span>



| <span data-ttu-id="54a6b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="54a6b-136">Requirement</span></span> | <span data-ttu-id="54a6b-137">Valore</span><span class="sxs-lookup"><span data-stu-id="54a6b-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a6b-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54a6b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="54a6b-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54a6b-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="54a6b-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54a6b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="54a6b-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54a6b-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="54a6b-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54a6b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="54a6b-143"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54a6b-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="54a6b-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="54a6b-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="54a6b-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54a6b-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="54a6b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="54a6b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54a6b-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="54a6b-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="54a6b-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="54a6b-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="54a6b-149">**StartDocPrinterW** (Unicode) e **StartDocPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="54a6b-149">**StartDocPrinterW** (Unicode) and **StartDocPrinterA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="54a6b-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54a6b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a6b-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="54a6b-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="54a6b-152">**\_Informazioni doc \_ 1**</span><span class="sxs-lookup"><span data-stu-id="54a6b-152">**DOC\_INFO\_1**</span></span>](doc-info-1.md)
</dt> <dt>

[<span data-ttu-id="54a6b-153">**Informazioni del documento \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="54a6b-153">**DOC\_INFO\_2**</span></span>](doc-info-2.md)
</dt> <dt>

[<span data-ttu-id="54a6b-154">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="54a6b-154">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="54a6b-155">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="54a6b-155">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="54a6b-156">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="54a6b-156">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="54a6b-157">Stampa</span><span class="sxs-lookup"><span data-stu-id="54a6b-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="54a6b-158">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="54a6b-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="54a6b-159">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="54a6b-159">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="54a6b-160">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="54a6b-160">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="54a6b-161">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="54a6b-161">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




