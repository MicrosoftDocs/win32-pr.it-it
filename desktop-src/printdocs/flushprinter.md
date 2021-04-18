---
description: La funzione FlushPrinter Invia un buffer alla stampante per cancellarla da uno stato temporaneo.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Funzione FlushPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528998"
---
# <a name="flushprinter-function"></a><span data-ttu-id="91c81-103">FlushPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="91c81-103">FlushPrinter function</span></span>

<span data-ttu-id="91c81-104">La funzione **FlushPrinter** Invia un buffer alla stampante per cancellarla da uno stato temporaneo.</span><span class="sxs-lookup"><span data-stu-id="91c81-104">The **FlushPrinter** function sends a buffer to the printer in order to clear it from a transient state.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c81-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91c81-105">Syntax</span></span>


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a><span data-ttu-id="91c81-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="91c81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c81-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c81-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c81-108">Handle per l'oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="91c81-108">A handle to the printer object.</span></span> <span data-ttu-id="91c81-109">Deve corrispondere allo stesso handle utilizzato, in una chiamata [**WritePrinter**](writeprinter.md) precedente, dal driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="91c81-109">This should be the same handle that was used, in a prior [**WritePrinter**](writeprinter.md) call, by the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="91c81-110">*pbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c81-110">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c81-111">Puntatore a una matrice di byte che contiene i dati da scrivere sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="91c81-111">A pointer to an array of bytes that contains the data to be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="91c81-112">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c81-112">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c81-113">Dimensione, in byte, della matrice a cui punta *pbuf*.</span><span class="sxs-lookup"><span data-stu-id="91c81-113">The size, in bytes, of the array pointed to by *pBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="91c81-114">*pcWritten* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="91c81-114">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91c81-115">Puntatore a un valore che riceve il numero di byte di dati scritti nella stampante.</span><span class="sxs-lookup"><span data-stu-id="91c81-115">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="91c81-116">*cSleep* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c81-116">*cSleep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c81-117">Tempo, in millisecondi, per il quale la riga di I/O nella porta della stampante deve rimanere inattiva.</span><span class="sxs-lookup"><span data-stu-id="91c81-117">The time, in milliseconds, for which the I/O line to the printer port should be kept idle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c81-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91c81-118">Return value</span></span>

<span data-ttu-id="91c81-119">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="91c81-119">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="91c81-120">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="91c81-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c81-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="91c81-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91c81-122">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="91c81-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="91c81-123">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91c81-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="91c81-124">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="91c81-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="91c81-125">**FlushPrinter** deve essere chiamato solo se [**WritePrinter**](writeprinter.md) ha avuto esito negativo, lasciando la stampante in uno stato temporaneo.</span><span class="sxs-lookup"><span data-stu-id="91c81-125">**FlushPrinter** should be called only if [**WritePrinter**](writeprinter.md) failed, leaving the printer in a transient state.</span></span> <span data-ttu-id="91c81-126">Ad esempio, la stampante potrebbe entrare in uno stato temporaneo quando il processo viene interrotto e il driver della stampante ha inviato parzialmente dati non elaborati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="91c81-126">For example, the printer could get into a transient state when the job gets aborted and the printer driver has partially sent some raw data to the printer.</span></span>

<span data-ttu-id="91c81-127">**FlushPrinter** può inoltre specificare un periodo di inattività durante il quale lo spooler di stampa non pianifica alcun processo nella porta stampante corrispondente.</span><span class="sxs-lookup"><span data-stu-id="91c81-127">**FlushPrinter** also can specify an idle period during which the print spooler does not schedule any jobs to the corresponding printer port.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c81-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91c81-128">Requirements</span></span>



| <span data-ttu-id="91c81-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="91c81-129">Requirement</span></span> | <span data-ttu-id="91c81-130">Valore</span><span class="sxs-lookup"><span data-stu-id="91c81-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c81-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91c81-131">Minimum supported client</span></span><br/> | <span data-ttu-id="91c81-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91c81-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="91c81-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91c81-133">Minimum supported server</span></span><br/> | <span data-ttu-id="91c81-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91c81-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="91c81-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91c81-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="91c81-136"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91c81-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="91c81-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="91c81-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="91c81-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91c81-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="91c81-139">DLL</span><span class="sxs-lookup"><span data-stu-id="91c81-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91c81-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="91c81-140"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="91c81-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91c81-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c81-142">Stampa</span><span class="sxs-lookup"><span data-stu-id="91c81-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="91c81-143">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="91c81-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="91c81-144">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="91c81-144">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




