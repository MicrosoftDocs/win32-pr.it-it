---
description: La funzione AddJob aggiunge un processo di stampa all'elenco dei processi di stampa che possono essere pianificati dallo spooler di stampa. La funzione recupera il nome del file che è possibile usare per archiviare il processo.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: Funzione AddJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756410"
---
# <a name="addjob-function"></a><span data-ttu-id="2494a-104">AddJob (funzione)</span><span class="sxs-lookup"><span data-stu-id="2494a-104">AddJob function</span></span>

<span data-ttu-id="2494a-105">La funzione **AddJob** aggiunge un processo di stampa all'elenco dei processi di stampa che possono essere pianificati dallo spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="2494a-105">The **AddJob** function adds a print job to the list of print jobs that can be scheduled by the print spooler.</span></span> <span data-ttu-id="2494a-106">La funzione recupera il nome del file che è possibile usare per archiviare il processo.</span><span class="sxs-lookup"><span data-stu-id="2494a-106">The function retrieves the name of the file you can use to store the job.</span></span>

> [!NOTE]
> <span data-ttu-id="2494a-107">Nei sistemi operativi Windows 8 e versioni successive, non è consigliabile usare direttamente **AddJob** perché esistono casi, ad esempio la stampa in una coda con file: o PORTPROMPT:) dove **AddJob** avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2494a-107">In Windows 8 and later operating systems, we do not recommended using **AddJob** directly because there are cases (such as printing to a queue using File: or PORTPROMPT:) where **AddJob** will fail.</span></span> <span data-ttu-id="2494a-108">Si consiglia invece di utilizzare l' [API di stampa GDI](gdi-printing.md), l' [API di stampa XPS](xps-printing.md), [**StartDocPrinter**](startdocprinter.md)o il metodo appropriato dallo spazio dei nomi [**Windows. graphics. Printing**](/uwp/api/Windows.Graphics.Printing) , a seconda dello scenario di stampa.</span><span class="sxs-lookup"><span data-stu-id="2494a-108">Instead, you are advised to use [GDI Print API](gdi-printing.md), [XPS Print API](xps-printing.md), [**StartDocPrinter**](startdocprinter.md), or the appropriate method from the [**Windows.Graphics.Printing**](/uwp/api/Windows.Graphics.Printing) namespace, depending on the print scenario.</span></span>
>
> <span data-ttu-id="2494a-109">Se si tenta di stampare in una coda usando **file:** o **PORTPROMPT:**, **ADDJOB** restituirà l' \_ errore non supportato.</span><span class="sxs-lookup"><span data-stu-id="2494a-109">If you try to print to a queue using **File:** or **PORTPROMPT:**, **AddJob** will Return the NOT\_SUPPORTED error.</span></span>

## <a name="syntax"></a><span data-ttu-id="2494a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2494a-110">Syntax</span></span>

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a><span data-ttu-id="2494a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="2494a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2494a-112">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2494a-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2494a-113">Handle che specifica la stampante per il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="2494a-113">A handle that specifies the printer for the print job.</span></span> <span data-ttu-id="2494a-114">Deve trattarsi di una stampante locale configurata come stampante con spooling.</span><span class="sxs-lookup"><span data-stu-id="2494a-114">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="2494a-115">Se *hPrinter* è un handle per una connessione stampante remota o se la stampante è configurata per la stampa diretta, la funzione **AddJob** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2494a-115">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **AddJob** function fails.</span></span> <span data-ttu-id="2494a-116">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="2494a-116">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="2494a-117">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2494a-117">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2494a-118">Versione della struttura di dati del processo di stampa che la funzione archivia nel buffer a cui punta *pData*.</span><span class="sxs-lookup"><span data-stu-id="2494a-118">The version of the print job information data structure that the function stores into the buffer pointed to by *pData*.</span></span> <span data-ttu-id="2494a-119">Impostare questo parametro su uno.</span><span class="sxs-lookup"><span data-stu-id="2494a-119">Set this parameter to one.</span></span>

</dd> <dt>

<span data-ttu-id="2494a-120">*pData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2494a-120">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2494a-121">Puntatore a un buffer che riceve una struttura di dati [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e una stringa di percorso.</span><span class="sxs-lookup"><span data-stu-id="2494a-121">A pointer to a buffer that receives an [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="2494a-122">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2494a-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2494a-123">Dimensione, in byte, del buffer a cui punta *pData*.</span><span class="sxs-lookup"><span data-stu-id="2494a-123">The size, in bytes, of the buffer pointed to by *pData*.</span></span> <span data-ttu-id="2494a-124">Il buffer deve essere sufficientemente grande da contenere una struttura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e una stringa di percorso.</span><span class="sxs-lookup"><span data-stu-id="2494a-124">The buffer needs to be large enough to contain an [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="2494a-125">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2494a-125">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2494a-126">Puntatore a una variabile che riceve le dimensioni totali, in byte, della struttura di dati [**ADDJOB \_ info \_ 1**](addjob-info-1.md) più la stringa di percorso.</span><span class="sxs-lookup"><span data-stu-id="2494a-126">A pointer to a variable that receives the total size, in bytes, of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure plus the path string.</span></span> <span data-ttu-id="2494a-127">Se questo valore è minore o uguale a *cbBuf* e la funzione ha esito positivo, si tratta del numero effettivo di byte scritti nel buffer a cui punta *pData*.</span><span class="sxs-lookup"><span data-stu-id="2494a-127">If this value is less than or equal to *cbBuf* and the function succeeds, this is the actual number of bytes written to the buffer pointed to by *pData*.</span></span> <span data-ttu-id="2494a-128">Se questo numero è maggiore di *cbBuf*, il buffer è troppo piccolo ed è necessario chiamare nuovamente la funzione con una dimensione del buffer almeno pari a \* *pcbNeeded*.</span><span class="sxs-lookup"><span data-stu-id="2494a-128">If this number is greater than *cbBuf*, the buffer is too small, and you must call the function again with a buffer size at least as large as \**pcbNeeded*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2494a-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2494a-129">Return value</span></span>

<span data-ttu-id="2494a-130">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="2494a-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2494a-131">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="2494a-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2494a-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="2494a-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2494a-133">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="2494a-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2494a-134">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2494a-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2494a-135">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="2494a-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="2494a-136">È possibile chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire il file dello spooler specificato dal membro **path** della struttura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) , quindi chiamare la funzione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per scrivere i dati del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="2494a-136">You can call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the spool file specified by the **Path** member of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure, and then call the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to write print job data to it.</span></span> <span data-ttu-id="2494a-137">Al termine di questa operazione, chiamare la funzione [**ScheduleJob**](schedulejob.md) per notificare allo spooler di stampa che il processo di stampa può essere pianificato dallo spooler per la stampa.</span><span class="sxs-lookup"><span data-stu-id="2494a-137">After that is done, call the [**ScheduleJob**](schedulejob.md) function to notify the print spooler that the print job can now be scheduled by the spooler for printing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2494a-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2494a-138">Requirements</span></span>



| <span data-ttu-id="2494a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2494a-139">Requirement</span></span> | <span data-ttu-id="2494a-140">Valore</span><span class="sxs-lookup"><span data-stu-id="2494a-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2494a-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2494a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2494a-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2494a-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2494a-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2494a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2494a-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2494a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2494a-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2494a-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2494a-146"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2494a-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2494a-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="2494a-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="2494a-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2494a-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2494a-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2494a-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2494a-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="2494a-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="2494a-151">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2494a-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2494a-152">**AddJobW** (Unicode) e **AddJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2494a-152">**AddJobW** (Unicode) and **AddJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="2494a-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2494a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2494a-154">**ADDJOB \_ info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2494a-154">**ADDJOB\_INFO\_1**</span></span>](addjob-info-1.md)
</dt> <dt>

[<span data-ttu-id="2494a-155">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="2494a-155">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="2494a-156">API di stampa GDI</span><span class="sxs-lookup"><span data-stu-id="2494a-156">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="2494a-157">Stampa</span><span class="sxs-lookup"><span data-stu-id="2494a-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2494a-158">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="2494a-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2494a-159">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="2494a-159">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="2494a-160">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="2494a-160">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="2494a-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="2494a-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="2494a-162">**Windows. graphics. Printing**</span><span class="sxs-lookup"><span data-stu-id="2494a-162">**Windows.Graphics.Printing**</span></span>](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[<span data-ttu-id="2494a-163">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="2494a-163">**WriteFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="2494a-164">API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="2494a-164">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

