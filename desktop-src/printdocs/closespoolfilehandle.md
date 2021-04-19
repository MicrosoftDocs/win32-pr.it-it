---
description: La funzione CloseSpoolFileHandle chiude un handle a un file di spooling associato al processo di stampa attualmente inviato dall'applicazione.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Funzione CloseSpoolFileHandle (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311560"
---
# <a name="closespoolfilehandle-function"></a><span data-ttu-id="ee461-103">CloseSpoolFileHandle (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee461-103">CloseSpoolFileHandle function</span></span>

<span data-ttu-id="ee461-104">La funzione **CloseSpoolFileHandle** chiude un handle a un file di spooling associato al processo di stampa attualmente inviato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee461-104">The **CloseSpoolFileHandle** function closes a handle to a spool file associated with the print job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee461-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee461-105">Syntax</span></span>


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a><span data-ttu-id="ee461-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee461-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee461-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee461-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee461-108">Handle per la stampante a cui è stato inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="ee461-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="ee461-109">Deve corrispondere allo stesso handle usato per ottenere *hSpoolFile* con [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="ee461-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee461-110">*hSpoolFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee461-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee461-111">Handle per il file di spooling da chiudere.</span><span class="sxs-lookup"><span data-stu-id="ee461-111">A handle to the spool file being closed.</span></span> <span data-ttu-id="ee461-112">Se [**CommitSpoolData**](commitspooldata.md) non è stato chiamato dopo la chiamata di [**GetSpoolFileHandle**](getspoolfilehandle.md) , deve essere lo stesso handle restituito da **GetSpoolFileHandle**.</span><span class="sxs-lookup"><span data-stu-id="ee461-112">If [**CommitSpoolData**](commitspooldata.md) has not been called since [**GetSpoolFileHandle**](getspoolfilehandle.md) was called, then this should be the same handle that was returned by **GetSpoolFileHandle**.</span></span> <span data-ttu-id="ee461-113">In caso contrario, deve essere l'handle restituito dalla chiamata più recente a **CommitSpoolData**.</span><span class="sxs-lookup"><span data-stu-id="ee461-113">Otherwise, it should be the handle that was returned by the most recent call to **CommitSpoolData**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee461-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee461-114">Return value</span></span>

<span data-ttu-id="ee461-115">**True** se ha esito positivo, **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ee461-115">**TRUE**, if it succeeds, **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee461-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee461-116">Remarks</span></span>

<span data-ttu-id="ee461-117">L'applicazione non deve chiamare [**ClosePrinter**](closeprinter.md) su *hPrinter* fino a quando non ha eseguito l'accesso al file di spooling per l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="ee461-117">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="ee461-118">Deve quindi chiamare **CloseSpoolFileHandle** seguito da **ClosePrinter**.</span><span class="sxs-lookup"><span data-stu-id="ee461-118">Then it should call **CloseSpoolFileHandle** followed by **ClosePrinter**.</span></span> <span data-ttu-id="ee461-119">I tentativi di accesso all'handle di file di spooling dopo la chiusura del *hPrinter* originale avranno esito negativo anche se l'handle di file non è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="ee461-119">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="ee461-120">**CloseSpoolFileHandle** avrà esito negativo se **ClosePrinter** viene chiamato per primo.</span><span class="sxs-lookup"><span data-stu-id="ee461-120">**CloseSpoolFileHandle** will fail if **ClosePrinter** is called first.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee461-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee461-121">Requirements</span></span>



| <span data-ttu-id="ee461-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee461-122">Requirement</span></span> | <span data-ttu-id="ee461-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ee461-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee461-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee461-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ee461-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee461-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ee461-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee461-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ee461-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee461-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ee461-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee461-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee461-129"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee461-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ee461-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="ee461-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee461-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee461-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ee461-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ee461-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee461-133"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ee461-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="ee461-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee461-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee461-135">Stampa</span><span class="sxs-lookup"><span data-stu-id="ee461-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ee461-136">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="ee461-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ee461-137">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="ee461-137">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="ee461-138">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="ee461-138">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> </dl>

 

 




