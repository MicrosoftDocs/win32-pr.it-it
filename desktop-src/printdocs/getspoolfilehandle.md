---
description: La funzione GetSpoolFileHandle recupera un handle per il file di spooling associato al processo attualmente inviato dall'applicazione.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Funzione GetSpoolFileHandle (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058244"
---
# <a name="getspoolfilehandle-function"></a><span data-ttu-id="9c7e4-103">GetSpoolFileHandle (funzione)</span><span class="sxs-lookup"><span data-stu-id="9c7e4-103">GetSpoolFileHandle function</span></span>

<span data-ttu-id="9c7e4-104">La funzione **GetSpoolFileHandle** recupera un handle per il file di spooling associato al processo attualmente inviato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-104">The **GetSpoolFileHandle** function retrieves a handle for the spool file associated with the job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c7e4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c7e4-105">Syntax</span></span>


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="9c7e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c7e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c7e4-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c7e4-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c7e4-108">Handle per la stampante a cui è stato inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="9c7e4-109">Deve corrispondere allo stesso handle utilizzato per inviare il processo.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-109">This should be the same handle that was used to submit the job.</span></span> <span data-ttu-id="9c7e4-110">Usare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-110">(Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c7e4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c7e4-111">Return value</span></span>

<span data-ttu-id="9c7e4-112">Se la funzione ha esito positivo, restituisce un handle per il file di spooling.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-112">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="9c7e4-113">Se la funzione ha esito negativo, restituisce un **\_ \_ valore di handle non valido**.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-113">If the function fails, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c7e4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c7e4-114">Remarks</span></span>

<span data-ttu-id="9c7e4-115">Con l'handle per il file di spooling, l'applicazione può scrivere nel file spool con le chiamate a [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) seguito da [**CommitSpoolData**](commitspooldata.md).</span><span class="sxs-lookup"><span data-stu-id="9c7e4-115">With the handle to the spool file, your application can write to the spool file with calls to [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) followed by [**CommitSpoolData**](commitspooldata.md).</span></span>

<span data-ttu-id="9c7e4-116">L'applicazione non deve chiamare [**ClosePrinter**](closeprinter.md) su *hPrinter* fino a quando non ha eseguito l'accesso al file di spooling per l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-116">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="9c7e4-117">Deve quindi chiamare [**CloseSpoolFileHandle**](closespoolfilehandle.md) seguito da **ClosePrinter**.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-117">Then it should call [**CloseSpoolFileHandle**](closespoolfilehandle.md) followed by **ClosePrinter**.</span></span> <span data-ttu-id="9c7e4-118">I tentativi di accesso all'handle di file di spooling dopo la chiusura del *hPrinter* originale avranno esito negativo anche se l'handle di file non è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-118">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="9c7e4-119">Se **ClosePrinter** viene chiamato per primo, **CloseSpoolFileHandle** avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-119">**CloseSpoolFileHandle** will itself fail if **ClosePrinter** is called first.</span></span>

<span data-ttu-id="9c7e4-120">Questa funzione avrà esito negativo se viene chiamata prima del completamento dello spooling del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="9c7e4-120">This function will fail if it is called before the print job has finished spooling.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c7e4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c7e4-121">Requirements</span></span>



| <span data-ttu-id="9c7e4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c7e4-122">Requirement</span></span> | <span data-ttu-id="9c7e4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9c7e4-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c7e4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c7e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9c7e4-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c7e4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9c7e4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c7e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9c7e4-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c7e4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9c7e4-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c7e4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c7e4-129"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c7e4-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9c7e4-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="9c7e4-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c7e4-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c7e4-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9c7e4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9c7e4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c7e4-133"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9c7e4-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9c7e4-134">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9c7e4-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9c7e4-135">**GetSpoolFileHandleW** (Unicode) e **GetSpoolFileHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9c7e4-135">**GetSpoolFileHandleW** (Unicode) and **GetSpoolFileHandleA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="9c7e4-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c7e4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c7e4-137">Stampa</span><span class="sxs-lookup"><span data-stu-id="9c7e4-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9c7e4-138">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="9c7e4-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9c7e4-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9c7e4-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="9c7e4-140">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="9c7e4-140">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="9c7e4-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="9c7e4-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="9c7e4-142">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="9c7e4-142">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="9c7e4-143">**CommitSpoolData**</span><span class="sxs-lookup"><span data-stu-id="9c7e4-143">**CommitSpoolData**</span></span>](commitspooldata.md)
</dt> </dl>

 

