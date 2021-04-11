---
description: La funzione GetJob recupera le informazioni su un processo di stampa specificato.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: Funzione GetJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227467"
---
# <a name="getjob-function"></a><span data-ttu-id="5f854-103">GetJob (funzione)</span><span class="sxs-lookup"><span data-stu-id="5f854-103">GetJob function</span></span>

<span data-ttu-id="5f854-104">La funzione **GetJob** recupera le informazioni su un processo di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="5f854-104">The **GetJob** function retrieves information about a specified print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f854-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f854-105">Syntax</span></span>


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="5f854-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f854-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f854-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f854-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f854-108">Handle per la stampante per il quale vengono recuperati i dati del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="5f854-108">A handle to the printer for which the print-job data is retrieved.</span></span> <span data-ttu-id="5f854-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="5f854-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="5f854-110">*JobID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f854-110">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f854-111">Identifica il processo di stampa per il quale recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="5f854-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="5f854-112">Usare la funzione [**AddJob**](addjob.md) o la funzione [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) per ottenere un identificatore del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="5f854-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5f854-113">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5f854-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f854-114">Tipo di informazioni restituite nel buffer di *pJob* .</span><span class="sxs-lookup"><span data-stu-id="5f854-114">The type of information returned in the *pJob* buffer.</span></span> <span data-ttu-id="5f854-115">Se *Level* è 1, *pJob* riceve una struttura di [**informazioni sul processo \_ \_ 1**](job-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="5f854-115">If *Level* is 1, *pJob* receives a [**JOB\_INFO\_1**](job-info-1.md) structure.</span></span> <span data-ttu-id="5f854-116">Se *Level* è 2, *pJob* riceve una struttura di [**informazioni sul processo \_ \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="5f854-116">If *Level* is 2, *pJob* receives a [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5f854-117">*pJob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5f854-117">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f854-118">Puntatore a un buffer che riceve una struttura di informazioni sul processo [**\_ \_ 1**](job-info-1.md) o [**\_ \_ 2**](job-info-2.md) che contiene informazioni sul processo.</span><span class="sxs-lookup"><span data-stu-id="5f854-118">A pointer to a buffer that receives a [**JOB\_INFO\_1**](job-info-1.md) or a [**JOB\_INFO\_2**](job-info-2.md) structure containing information about the job.</span></span> <span data-ttu-id="5f854-119">Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui puntano i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="5f854-119">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="5f854-120">Per determinare le dimensioni del buffer richieste, chiamare **GetJob** con *cbBuf* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="5f854-120">To determine the required buffer size, call **GetJob** with *cbBuf* set to zero.</span></span> <span data-ttu-id="5f854-121">**GetJob** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="5f854-121">**GetJob** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="5f854-122">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f854-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f854-123">Dimensione, in byte, della matrice.</span><span class="sxs-lookup"><span data-stu-id="5f854-123">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="5f854-124">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5f854-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f854-125">Puntatore a un valore che specifica il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="5f854-125">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f854-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f854-126">Return value</span></span>

<span data-ttu-id="5f854-127">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="5f854-127">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5f854-128">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="5f854-128">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f854-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f854-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5f854-130">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="5f854-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5f854-131">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f854-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5f854-132">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="5f854-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f854-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f854-133">Requirements</span></span>



| <span data-ttu-id="5f854-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f854-134">Requirement</span></span> | <span data-ttu-id="5f854-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5f854-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f854-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f854-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5f854-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f854-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5f854-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f854-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5f854-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f854-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5f854-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f854-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f854-141"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f854-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5f854-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="5f854-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f854-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f854-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5f854-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5f854-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f854-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5f854-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5f854-146">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5f854-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5f854-147">**GetJobW** (Unicode) e **GetJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5f854-147">**GetJobW** (Unicode) and **GetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="5f854-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f854-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f854-149">Stampa</span><span class="sxs-lookup"><span data-stu-id="5f854-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5f854-150">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="5f854-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5f854-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="5f854-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="5f854-152">**\_Informazioni processo \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5f854-152">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="5f854-153">**Informazioni sul processo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5f854-153">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="5f854-154">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="5f854-154">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="5f854-155">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="5f854-155">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

