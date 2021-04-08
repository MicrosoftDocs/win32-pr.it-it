---
description: Segnala al servizio spooler di stampa se un processo di stampa XPS si trova nella fase di spooling o di rendering e quale parte dell'elaborazione è attualmente in corso.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Funzione ReportJobProcessingProgress (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967941"
---
# <a name="reportjobprocessingprogress-function"></a><span data-ttu-id="f4446-103">ReportJobProcessingProgress (funzione)</span><span class="sxs-lookup"><span data-stu-id="f4446-103">ReportJobProcessingProgress function</span></span>

<span data-ttu-id="f4446-104">Segnala al servizio spooler di stampa se un processo di stampa XPS si trova nella fase di spooling o di rendering e quale parte dell'elaborazione è attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="f4446-104">Reports to the Print Spooler service whether an XPS print job is in the spooling or the rendering phase and what part of the processing is currently underway.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4446-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4446-105">Syntax</span></span>


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a><span data-ttu-id="f4446-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4446-107">*printerHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4446-107">*printerHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4446-108">Handle della stampante per il quale la funzione deve recuperare informazioni.</span><span class="sxs-lookup"><span data-stu-id="f4446-108">A printer handle for which the function is to retrieve information.</span></span> <span data-ttu-id="f4446-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="f4446-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f4446-110">*jobId* \[in\]</span><span class="sxs-lookup"><span data-stu-id="f4446-110">*jobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4446-111">Identifica il processo di stampa per il quale recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="f4446-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="f4446-112">Usare la funzione [**AddJob**](addjob.md) o la funzione [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) per ottenere un identificatore del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f4446-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f4446-113">*jobOperation*</span><span class="sxs-lookup"><span data-stu-id="f4446-113">*jobOperation*</span></span> 
</dt> <dd>

<span data-ttu-id="f4446-114">Specifica se il processo si trova nella fase di spooling o nella fase di rendering.</span><span class="sxs-lookup"><span data-stu-id="f4446-114">Specifies whether the job is in the spooling phase or the rendering phase.</span></span>

</dd> <dt>

<span data-ttu-id="f4446-115">*jobProgress*</span><span class="sxs-lookup"><span data-stu-id="f4446-115">*jobProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="f4446-116">Specifica la parte dell'elaborazione attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="f4446-116">Specifies what part of the processing is currently underway.</span></span> <span data-ttu-id="f4446-117">Questo valore si riferisce agli eventi in fase di spooling o di rendering, a seconda del valore di *jobOperation*.</span><span class="sxs-lookup"><span data-stu-id="f4446-117">This value refers to events in either the spooling or rendering phase depending on the value of *jobOperation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4446-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4446-118">Return value</span></span>

<span data-ttu-id="f4446-119">Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="f4446-119">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="f4446-120">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f4446-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4446-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4446-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4446-122">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="f4446-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f4446-123">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4446-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f4446-124">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="f4446-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="f4446-125">**ReportJobProcessingProgress** segnala lo stato di avanzamento del processo di stampa XPS solo se il processo di stampa si trova nella fase di spooling o di rendering.</span><span class="sxs-lookup"><span data-stu-id="f4446-125">**ReportJobProcessingProgress** will only report the progress of the XPS print job if the print job is in the spooling or rendering phase.</span></span> <span data-ttu-id="f4446-126">**ReportJobProcessingProgress** avrà esito negativo se viene chiamato quando il processo di stampa XPS non si trova nella fase di spooling o di rendering.</span><span class="sxs-lookup"><span data-stu-id="f4446-126">**ReportJobProcessingProgress** will fail if it is called when the XPS print job is not in the spooling or rendering phase.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4446-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4446-127">Requirements</span></span>



| <span data-ttu-id="f4446-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4446-128">Requirement</span></span> | <span data-ttu-id="f4446-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f4446-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4446-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4446-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f4446-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4446-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f4446-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4446-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f4446-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4446-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f4446-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4446-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4446-135"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4446-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f4446-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4446-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4446-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4446-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f4446-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f4446-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4446-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4446-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f4446-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4446-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4446-141">Stampa</span><span class="sxs-lookup"><span data-stu-id="f4446-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f4446-142">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="f4446-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f4446-143">**EPrintXPSJobOperation**</span><span class="sxs-lookup"><span data-stu-id="f4446-143">**EPrintXPSJobOperation**</span></span>](eprintxpsjoboperation.md)
</dt> <dt>

[<span data-ttu-id="f4446-144">**EPrintXPSJobProgress**</span><span class="sxs-lookup"><span data-stu-id="f4446-144">**EPrintXPSJobProgress**</span></span>](eprintxpsjobprogress.md)
</dt> </dl>

 

