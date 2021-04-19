---
description: La funzione AbortPrinter Elimina un file di spooling delle stampanti se la stampante è configurata per lo spooling.
ms.assetid: b361fba5-e4e7-4c9e-ab32-b8ab88dcb1dc
title: Funzione AbortPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbortPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f28e0c921db8fd075b6cad0e1df07401faaaffb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311573"
---
# <a name="abortprinter-function"></a><span data-ttu-id="68365-103">AbortPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="68365-103">AbortPrinter function</span></span>

<span data-ttu-id="68365-104">La funzione **AbortPrinter** Elimina il file di spool della stampante se la stampante è configurata per lo spooling.</span><span class="sxs-lookup"><span data-stu-id="68365-104">The **AbortPrinter** function deletes a printer's spool file if the printer is configured for spooling.</span></span>

## <a name="syntax"></a><span data-ttu-id="68365-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68365-105">Syntax</span></span>


```C++
BOOL AbortPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="68365-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="68365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68365-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68365-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68365-108">Handle per la stampante da cui viene eliminato il file di spooling.</span><span class="sxs-lookup"><span data-stu-id="68365-108">Handle to the printer from which the spool file is deleted.</span></span> <span data-ttu-id="68365-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="68365-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68365-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68365-110">Return value</span></span>

<span data-ttu-id="68365-111">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="68365-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="68365-112">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="68365-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="68365-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="68365-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="68365-114">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="68365-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="68365-115">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68365-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="68365-116">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="68365-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="68365-117">Se la stampante non è configurata per lo spooling, la funzione **AbortPrinter** non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="68365-117">If the printer is not configured for spooling, the **AbortPrinter** function has no effect.</span></span>

<span data-ttu-id="68365-118">La sequenza per un processo di stampa è la seguente:</span><span class="sxs-lookup"><span data-stu-id="68365-118">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="68365-119">Per iniziare un processo di stampa, chiamare [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="68365-119">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="68365-120">Per iniziare ogni pagina, chiamare [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="68365-120">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="68365-121">Per scrivere i dati in una pagina, chiamare [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="68365-121">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="68365-122">Per terminare ogni pagina, chiamare [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="68365-122">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="68365-123">Ripetere 2, 3 e 4 per il numero di pagine necessario.</span><span class="sxs-lookup"><span data-stu-id="68365-123">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="68365-124">Per terminare il processo di stampa, chiamare [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="68365-124">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="68365-125">Quando una pagina in un file con spooling supera circa 350 MB, potrebbe non essere possibile stampare e inviare un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="68365-125">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="68365-126">Questo può verificarsi, ad esempio, durante la stampa di file EMF di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="68365-126">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="68365-127">Il limite delle dimensioni della pagina dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamante e la quantità di frammentazione nell'heap dei processi.</span><span class="sxs-lookup"><span data-stu-id="68365-127">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="68365-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68365-128">Requirements</span></span>



| <span data-ttu-id="68365-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="68365-129">Requirement</span></span> | <span data-ttu-id="68365-130">Valore</span><span class="sxs-lookup"><span data-stu-id="68365-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68365-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68365-131">Minimum supported client</span></span><br/> | <span data-ttu-id="68365-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="68365-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="68365-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68365-133">Minimum supported server</span></span><br/> | <span data-ttu-id="68365-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="68365-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="68365-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68365-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="68365-136"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68365-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="68365-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="68365-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="68365-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68365-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="68365-139">DLL</span><span class="sxs-lookup"><span data-stu-id="68365-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68365-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68365-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="68365-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68365-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68365-142">Stampa</span><span class="sxs-lookup"><span data-stu-id="68365-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="68365-143">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="68365-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="68365-144">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="68365-144">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="68365-145">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="68365-145">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="68365-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="68365-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="68365-147">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="68365-147">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="68365-148">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="68365-148">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="68365-149">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="68365-149">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




