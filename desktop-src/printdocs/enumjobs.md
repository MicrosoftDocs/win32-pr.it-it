---
description: La funzione EnumJobs recupera le informazioni su un set specificato di processi di stampa per una stampante specificata.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Funzione EnumJobs (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232523"
---
# <a name="enumjobs-function"></a><span data-ttu-id="da03d-103">EnumJobs (funzione)</span><span class="sxs-lookup"><span data-stu-id="da03d-103">EnumJobs function</span></span>

<span data-ttu-id="da03d-104">La funzione **EnumJobs** recupera le informazioni su un set specificato di processi di stampa per una stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="da03d-104">The **EnumJobs** function retrieves information about a specified set of print jobs for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="da03d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da03d-105">Syntax</span></span>


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="da03d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da03d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da03d-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da03d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da03d-108">Handle per l'oggetto stampante i cui processi di stampa vengono enumerati dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="da03d-108">A handle to the printer object whose print jobs the function enumerates.</span></span> <span data-ttu-id="da03d-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="da03d-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="da03d-110">*FirstJob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da03d-110">*FirstJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da03d-111">Posizione in base zero all'interno della coda di stampa del primo processo di stampa da enumerare.</span><span class="sxs-lookup"><span data-stu-id="da03d-111">The zero-based position within the print queue of the first print job to enumerate.</span></span> <span data-ttu-id="da03d-112">Ad esempio, un valore pari a 0 indica che l'enumerazione deve iniziare dal primo processo di stampa nella coda di stampa. il valore 9 indica che l'enumerazione deve iniziare al decimo processo di stampa nella coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="da03d-112">For example, a value of 0 specifies that enumeration should begin at the first print job in the print queue; a value of 9 specifies that enumeration should begin at the tenth print job in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="da03d-113">*Nojobs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da03d-113">*NoJobs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da03d-114">Numero totale di processi di stampa da enumerare.</span><span class="sxs-lookup"><span data-stu-id="da03d-114">The total number of print jobs to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="da03d-115">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="da03d-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da03d-116">Tipo di informazioni restituite nel buffer di *pJob* .</span><span class="sxs-lookup"><span data-stu-id="da03d-116">The type of information returned in the *pJob* buffer.</span></span>



| <span data-ttu-id="da03d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="da03d-117">Value</span></span>                                                                                                | <span data-ttu-id="da03d-118">Significato</span><span class="sxs-lookup"><span data-stu-id="da03d-118">Meaning</span></span>                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="da03d-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="da03d-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="da03d-120">*pJob* riceve una matrice di strutture di [**informazioni sul processo \_ \_ 1**](job-info-1.md)</span><span class="sxs-lookup"><span data-stu-id="da03d-120">*pJob* receives an array of [**JOB\_INFO\_1**](job-info-1.md) structures</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="da03d-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="da03d-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="da03d-122">*pJob* riceve una matrice di strutture di [**informazioni sul processo \_ \_ 2**](job-info-2.md)</span><span class="sxs-lookup"><span data-stu-id="da03d-122">*pJob* receives an array of [**JOB\_INFO\_2**](job-info-2.md) structures</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="da03d-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="da03d-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="da03d-124">*pJob* riceve una matrice di strutture di [**informazioni sul processo \_ \_ 3**](job-info-3.md)</span><span class="sxs-lookup"><span data-stu-id="da03d-124">*pJob* receives an array of [**JOB\_INFO\_3**](job-info-3.md) structures</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="da03d-125">*pJob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="da03d-125">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da03d-126">Puntatore a un buffer che riceve una matrice di strutture di informazioni sul processo [**\_ \_ 1**](job-info-1.md), [**informazioni sul processo \_ \_ 2**](job-info-2.md)o [**informazioni sul processo \_ \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="da03d-126">A pointer to a buffer that receives an array of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures.</span></span> <span data-ttu-id="da03d-127">Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture e qualsiasi stringa o altri dati a cui fanno riferimento i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="da03d-127">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="da03d-128">Per determinare le dimensioni del buffer richieste, chiamare **EnumJobs** con *cbBuf* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="da03d-128">To determine the required buffer size, call **EnumJobs** with *cbBuf* set to zero.</span></span> <span data-ttu-id="da03d-129">**EnumJobs** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="da03d-129">**EnumJobs** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="da03d-130">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da03d-130">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da03d-131">Dimensione, in byte, del buffer *pJob* .</span><span class="sxs-lookup"><span data-stu-id="da03d-131">The size, in bytes, of the *pJob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="da03d-132">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="da03d-132">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da03d-133">Puntatore a una variabile che riceve il numero di byte copiati se la funzione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="da03d-133">A pointer to a variable that receives the number of bytes copied if the function succeeds.</span></span> <span data-ttu-id="da03d-134">Se la funzione ha esito negativo, la variabile riceve il numero di byte necessari.</span><span class="sxs-lookup"><span data-stu-id="da03d-134">If the function fails, the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="da03d-135">*pcReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="da03d-135">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da03d-136">Puntatore a una variabile che riceve il numero di strutture di informazioni di processo [**\_ \_ 1**](job-info-1.md), [**informazioni sul processo \_ \_ 2**](job-info-2.md)o [**informazioni sul processo \_ \_ 3**](job-info-3.md) restituite nel buffer *pJob* .</span><span class="sxs-lookup"><span data-stu-id="da03d-136">A pointer to a variable that receives the number of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures returned in the *pJob* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da03d-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da03d-137">Return value</span></span>

<span data-ttu-id="da03d-138">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="da03d-138">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="da03d-139">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="da03d-139">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="da03d-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="da03d-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="da03d-141">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="da03d-141">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="da03d-142">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="da03d-142">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="da03d-143">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="da03d-143">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="da03d-144">La [**struttura \_ info processo \_ 1**](job-info-1.md) contiene informazioni generali sul processo di stampa. la struttura di informazioni sul [**processo \_ \_ 2**](job-info-2.md) contiene informazioni molto più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="da03d-144">The [**JOB\_INFO\_1**](job-info-1.md) structure contains general print-job information; the [**JOB\_INFO\_2**](job-info-2.md) structure has much more detailed information.</span></span> <span data-ttu-id="da03d-145">La [**struttura \_ informazioni \_ sul processo 3**](job-info-3.md) contiene informazioni sulla modalità di collegamento dei processi.</span><span class="sxs-lookup"><span data-stu-id="da03d-145">The [**JOB\_INFO\_3**](job-info-3.md) structure contains information about how jobs are linked.</span></span>

<span data-ttu-id="da03d-146">Per determinare il numero di processi di stampa nella coda della stampante, chiamare la funzione [**GetPrinter**](getprinter.md) con il parametro *Level* impostato su 2.</span><span class="sxs-lookup"><span data-stu-id="da03d-146">To determine the number of print jobs in the printer queue, call the [**GetPrinter**](getprinter.md) function with the *Level* parameter set to 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="da03d-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da03d-147">Requirements</span></span>



| <span data-ttu-id="da03d-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="da03d-148">Requirement</span></span> | <span data-ttu-id="da03d-149">Valore</span><span class="sxs-lookup"><span data-stu-id="da03d-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da03d-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da03d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="da03d-151">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da03d-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="da03d-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da03d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="da03d-153">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da03d-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="da03d-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da03d-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="da03d-155"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da03d-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="da03d-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="da03d-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="da03d-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da03d-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="da03d-158">DLL</span><span class="sxs-lookup"><span data-stu-id="da03d-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da03d-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="da03d-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="da03d-160">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="da03d-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="da03d-161">**EnumJobsW** (Unicode) e **EnumJobsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="da03d-161">**EnumJobsW** (Unicode) and **EnumJobsA** (ANSI)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="da03d-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da03d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da03d-163">Stampa</span><span class="sxs-lookup"><span data-stu-id="da03d-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="da03d-164">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="da03d-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="da03d-165">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="da03d-165">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="da03d-166">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="da03d-166">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="da03d-167">**\_Informazioni processo \_ 1**</span><span class="sxs-lookup"><span data-stu-id="da03d-167">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="da03d-168">**Informazioni sul processo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="da03d-168">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="da03d-169">**Informazioni sul processo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="da03d-169">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="da03d-170">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="da03d-170">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="da03d-171">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="da03d-171">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

