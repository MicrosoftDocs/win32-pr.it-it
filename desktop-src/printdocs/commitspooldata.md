---
description: La funzione CommitSpoolData notifica allo spooler di stampa che una quantità specificata di dati è stata scritta in un file di spool specificato ed è pronta per essere sottoposta a rendering.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Funzione CommitSpoolData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881405"
---
# <a name="commitspooldata-function"></a><span data-ttu-id="ffebd-103">CommitSpoolData (funzione)</span><span class="sxs-lookup"><span data-stu-id="ffebd-103">CommitSpoolData function</span></span>

<span data-ttu-id="ffebd-104">La funzione **CommitSpoolData** notifica allo spooler di stampa che una quantità specificata di dati è stata scritta in un file di spool specificato ed è pronta per essere sottoposta a rendering.</span><span class="sxs-lookup"><span data-stu-id="ffebd-104">The **CommitSpoolData** function notifies the print spooler that a specified amount of data has been written to a specified spool file and is ready to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffebd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffebd-105">Syntax</span></span>


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a><span data-ttu-id="ffebd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffebd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffebd-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffebd-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffebd-108">Handle per la stampante a cui è stato inviato il processo.</span><span class="sxs-lookup"><span data-stu-id="ffebd-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="ffebd-109">Deve corrispondere allo stesso handle usato per ottenere *hSpoolFile* con [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="ffebd-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffebd-110">*hSpoolFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffebd-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffebd-111">Handle per il file di spooling modificato.</span><span class="sxs-lookup"><span data-stu-id="ffebd-111">A handle to the spool file being changed.</span></span> <span data-ttu-id="ffebd-112">Alla prima chiamata di **CommitSpoolData**, deve essere lo stesso handle restituito da [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="ffebd-112">On the first call of **CommitSpoolData**, this should be the same handle that was returned by [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span> <span data-ttu-id="ffebd-113">Le chiamate successive a **CommitSpoolData** devono passare l'handle restituito dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="ffebd-113">Subsequent calls to **CommitSpoolData** should pass the handle returned by the preceding call.</span></span> <span data-ttu-id="ffebd-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ffebd-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ffebd-115">*cbCommit*</span><span class="sxs-lookup"><span data-stu-id="ffebd-115">*cbCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="ffebd-116">Numero di byte di cui è stato eseguito il commit nello spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="ffebd-116">The number of bytes committed to the print spooler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffebd-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffebd-117">Return value</span></span>

<span data-ttu-id="ffebd-118">Se la funzione ha esito positivo, restituisce un handle per il file di spooling.</span><span class="sxs-lookup"><span data-stu-id="ffebd-118">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="ffebd-119">Se la funzione ha esito negativo, restituisce un valore di handle non valido \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ffebd-119">If the function fails, it returns INVALID\_HANDLE\_VALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffebd-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffebd-120">Remarks</span></span>

<span data-ttu-id="ffebd-121">Le applicazioni che inviano un processo di stampa spooler possono chiamare [**GetSpoolFileHandle**](getspoolfilehandle.md) e quindi scrivere direttamente i dati nell'handle di file spool chiamando [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span><span class="sxs-lookup"><span data-stu-id="ffebd-121">Applications submitting a spooler print job can call [**GetSpoolFileHandle**](getspoolfilehandle.md) and then directly write data to the spool file handle by calling [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span></span> <span data-ttu-id="ffebd-122">Per notificare allo spooler di stampa che il file contiene dati di cui è possibile eseguire il rendering, l'applicazione deve chiamare **CommitSpoolData** e specificare il numero di byte disponibili.</span><span class="sxs-lookup"><span data-stu-id="ffebd-122">To notify the print spooler that the file contains data which is ready to be rendered, the application must call **CommitSpoolData** and provide the number of available bytes.</span></span>

<span data-ttu-id="ffebd-123">Se **CommitSpoolData** viene chiamato più volte, ogni chiamata deve usare l'handle di file di spool restituito dalla chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="ffebd-123">If **CommitSpoolData** is called multiple times, each call must use the spool file handle returned by the previous call.</span></span> <span data-ttu-id="ffebd-124">Quando non vengono scritti più dati nel file di spooling, è necessario chiamare [**CloseSpoolFileHandle**](closespoolfilehandle.md) per l'handle di file restituito dall'ultima chiamata a **CommitSpoolData**.</span><span class="sxs-lookup"><span data-stu-id="ffebd-124">When no more data will be written to the spool file, [**CloseSpoolFileHandle**](closespoolfilehandle.md) should be called for the file handle returned by the last call to **CommitSpoolData**.</span></span>

<span data-ttu-id="ffebd-125">Prima di chiamare **CommitSpoolData**, le applicazioni devono impostare il puntatore del file sulla posizione in cui si trovava prima di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="ffebd-125">Before calling **CommitSpoolData**, applications must set the file pointer to the position it had before it wrote data to the file.</span></span> <span data-ttu-id="ffebd-126">Nel processo di rendering dei dati nel file dello spooler, lo spooler di stampa sposterà il puntatore del file di spool *cbCommit* byte dal valore corrente del puntatore del file.</span><span class="sxs-lookup"><span data-stu-id="ffebd-126">In the process of rendering the data in the spooler file, the print spooler will move the spool file pointer *cbCommit* bytes from the current value of file pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffebd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffebd-127">Requirements</span></span>



| <span data-ttu-id="ffebd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffebd-128">Requirement</span></span> | <span data-ttu-id="ffebd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ffebd-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffebd-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffebd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ffebd-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ffebd-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ffebd-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffebd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ffebd-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ffebd-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ffebd-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ffebd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffebd-135"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffebd-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ffebd-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="ffebd-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ffebd-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffebd-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ffebd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ffebd-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffebd-139"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ffebd-139"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="ffebd-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffebd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffebd-141">Stampa</span><span class="sxs-lookup"><span data-stu-id="ffebd-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ffebd-142">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="ffebd-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ffebd-143">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="ffebd-143">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="ffebd-144">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="ffebd-144">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> </dl>

 

