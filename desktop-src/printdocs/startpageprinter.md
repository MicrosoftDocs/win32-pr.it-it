---
description: La funzione StartPagePrinter notifica allo spooler che una pagina sta per essere stampata sulla stampante specificata.
ms.assetid: 8ac7c47b-b3a7-4642-bfb7-54e014139fbf
title: Funzione StartPagePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f8d1c5cc296fae1b166b891fc881a6abcdb6b2af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967375"
---
# <a name="startpageprinter-function"></a><span data-ttu-id="65cc4-103">StartPagePrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="65cc4-103">StartPagePrinter function</span></span>

<span data-ttu-id="65cc4-104">La funzione **StartPagePrinter** notifica allo spooler che una pagina sta per essere stampata sulla stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="65cc4-104">The **StartPagePrinter** function notifies the spooler that a page is about to be printed on the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="65cc4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65cc4-105">Syntax</span></span>


```C++
BOOL StartPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="65cc4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="65cc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65cc4-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65cc4-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65cc4-108">Handle per una stampante.</span><span class="sxs-lookup"><span data-stu-id="65cc4-108">Handle to a printer.</span></span> <span data-ttu-id="65cc4-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="65cc4-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65cc4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65cc4-110">Return value</span></span>

<span data-ttu-id="65cc4-111">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="65cc4-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="65cc4-112">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="65cc4-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="65cc4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="65cc4-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65cc4-114">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="65cc4-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="65cc4-115">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="65cc4-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="65cc4-116">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="65cc4-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="65cc4-117">La sequenza per un processo di stampa è la seguente:</span><span class="sxs-lookup"><span data-stu-id="65cc4-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="65cc4-118">Per iniziare un processo di stampa, chiamare [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="65cc4-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="65cc4-119">Per iniziare ogni pagina, chiamare **StartPagePrinter**.</span><span class="sxs-lookup"><span data-stu-id="65cc4-119">To begin each page, call **StartPagePrinter**.</span></span>
3.  <span data-ttu-id="65cc4-120">Per scrivere i dati in una pagina, chiamare [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="65cc4-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="65cc4-121">Per terminare ogni pagina, chiamare [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="65cc4-121">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="65cc4-122">Ripetere 2, 3 e 4 per il numero di pagine necessario.</span><span class="sxs-lookup"><span data-stu-id="65cc4-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="65cc4-123">Per terminare il processo di stampa, chiamare [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="65cc4-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="65cc4-124">Quando una pagina in un file con spooling supera circa 350 MB, potrebbe non essere possibile stampare e inviare un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="65cc4-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="65cc4-125">Questo può verificarsi, ad esempio, durante la stampa di file EMF di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="65cc4-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="65cc4-126">Il limite delle dimensioni della pagina dipende da molti fattori, tra cui la quantità di memoria virtuale disponibile, la quantità di memoria allocata dai processi chiamante e la quantità di frammentazione nell'heap dei processi.</span><span class="sxs-lookup"><span data-stu-id="65cc4-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="examples"></a><span data-ttu-id="65cc4-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="65cc4-127">Examples</span></span>

<span data-ttu-id="65cc4-128">Per un programma di esempio che usa questa funzione, vedere [procedura: stampare con l'API di stampa GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="65cc4-128">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65cc4-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65cc4-129">Requirements</span></span>



| <span data-ttu-id="65cc4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="65cc4-130">Requirement</span></span> | <span data-ttu-id="65cc4-131">Valore</span><span class="sxs-lookup"><span data-stu-id="65cc4-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65cc4-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65cc4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="65cc4-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65cc4-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="65cc4-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65cc4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="65cc4-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65cc4-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="65cc4-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65cc4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="65cc4-137"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65cc4-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="65cc4-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="65cc4-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="65cc4-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65cc4-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="65cc4-140">DLL</span><span class="sxs-lookup"><span data-stu-id="65cc4-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65cc4-141"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65cc4-141"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="65cc4-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65cc4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65cc4-143">Stampa</span><span class="sxs-lookup"><span data-stu-id="65cc4-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="65cc4-144">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="65cc4-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="65cc4-145">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="65cc4-145">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="65cc4-146">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="65cc4-146">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="65cc4-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="65cc4-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="65cc4-148">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="65cc4-148">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="65cc4-149">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="65cc4-149">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="65cc4-150">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="65cc4-150">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




