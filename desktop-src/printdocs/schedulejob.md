---
description: La funzione ScheduleJob richiede che lo spooler di stampa pianifichi un processo di stampa specificato per la stampa.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Funzione ScheduleJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 1ef938cc2a9b1893a4825255325457d5c210842a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314989"
---
# <a name="schedulejob-function"></a><span data-ttu-id="02a6d-103">ScheduleJob (funzione)</span><span class="sxs-lookup"><span data-stu-id="02a6d-103">ScheduleJob function</span></span>

<span data-ttu-id="02a6d-104">La funzione **ScheduleJob** richiede che lo spooler di stampa pianifichi un processo di stampa specificato per la stampa.</span><span class="sxs-lookup"><span data-stu-id="02a6d-104">The **ScheduleJob** function requests that the print spooler schedule a specified print job for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a6d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02a6d-105">Syntax</span></span>


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a><span data-ttu-id="02a6d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02a6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a6d-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02a6d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a6d-108">Handle per la stampante per il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="02a6d-108">A handle to the printer for the print job.</span></span> <span data-ttu-id="02a6d-109">Deve trattarsi di una stampante locale configurata come stampante con spooling.</span><span class="sxs-lookup"><span data-stu-id="02a6d-109">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="02a6d-110">Se *hPrinter* è un handle per una connessione stampante remota o se la stampante è configurata per la stampa diretta, la funzione **ScheduleJob** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="02a6d-110">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **ScheduleJob** function fails.</span></span> <span data-ttu-id="02a6d-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="02a6d-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

<span data-ttu-id="02a6d-112">*hPrinter* deve essere lo stesso handle della stampante specificato nella chiamata a [**AddJob**](addjob.md) che ha ottenuto l'identificatore del processo di stampa *dwJobID* .</span><span class="sxs-lookup"><span data-stu-id="02a6d-112">*hPrinter* must be the same printer handle specified in the call to [**AddJob**](addjob.md) that obtained the *dwJobID* print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="02a6d-113">*dwJobID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02a6d-113">*dwJobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02a6d-114">Processo di stampa da pianificare.</span><span class="sxs-lookup"><span data-stu-id="02a6d-114">The print job to be scheduled.</span></span> <span data-ttu-id="02a6d-115">È possibile ottenere questo identificatore del processo di stampa chiamando la funzione [**AddJob**](addjob.md) .</span><span class="sxs-lookup"><span data-stu-id="02a6d-115">You obtain this print job identifier by calling the [**AddJob**](addjob.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a6d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02a6d-116">Return value</span></span>

<span data-ttu-id="02a6d-117">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="02a6d-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="02a6d-118">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="02a6d-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="02a6d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="02a6d-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02a6d-120">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="02a6d-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="02a6d-121">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="02a6d-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="02a6d-122">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="02a6d-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="02a6d-123">Prima di chiamare la funzione **ScheduleJob** è necessario chiamare correttamente la funzione [**AddJob**](addjob.md) .</span><span class="sxs-lookup"><span data-stu-id="02a6d-123">You must successfully call the [**AddJob**](addjob.md) function before calling the **ScheduleJob** function.</span></span> <span data-ttu-id="02a6d-124">**AddJob** Ottiene l'identificatore del processo di stampa passato a **ScheduleJob** come *dwJobID*.</span><span class="sxs-lookup"><span data-stu-id="02a6d-124">**AddJob** obtains the print job identifier that you pass to **ScheduleJob** as *dwJobID*.</span></span> <span data-ttu-id="02a6d-125">Entrambe le chiamate devono usare lo stesso valore per *hPrinter*.</span><span class="sxs-lookup"><span data-stu-id="02a6d-125">Both calls must use the same value for *hPrinter*.</span></span>

<span data-ttu-id="02a6d-126">La funzione **ScheduleJob** verifica la presenza di un file di spooling valido.</span><span class="sxs-lookup"><span data-stu-id="02a6d-126">The **ScheduleJob** function checks for a valid spool file.</span></span> <span data-ttu-id="02a6d-127">Se è presente un file di spooling non valido o se è vuoto, **ScheduleJob** Elimina sia il file di spooling che la voce del processo di stampa corrispondente nello spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="02a6d-127">If there is an invalid spool file, or if it is empty, **ScheduleJob** deletes both the spool file and the corresponding print job entry in the print spooler.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a6d-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02a6d-128">Requirements</span></span>



| <span data-ttu-id="02a6d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="02a6d-129">Requirement</span></span> | <span data-ttu-id="02a6d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="02a6d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02a6d-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02a6d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="02a6d-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="02a6d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="02a6d-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02a6d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="02a6d-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="02a6d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="02a6d-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02a6d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="02a6d-136"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02a6d-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="02a6d-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="02a6d-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="02a6d-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02a6d-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="02a6d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="02a6d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02a6d-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02a6d-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="02a6d-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02a6d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a6d-142">Stampa</span><span class="sxs-lookup"><span data-stu-id="02a6d-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="02a6d-143">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="02a6d-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="02a6d-144">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="02a6d-144">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="02a6d-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="02a6d-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




