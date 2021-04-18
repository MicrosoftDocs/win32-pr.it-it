---
description: La funzione ReadPrinter recupera i dati dalla stampante specificata.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: Funzione ReadPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ddbdfc03b80557583c60f461f0c7e3a6fe2473fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314000"
---
# <a name="readprinter-function"></a><span data-ttu-id="e5cbd-103">ReadPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="e5cbd-103">ReadPrinter function</span></span>

<span data-ttu-id="e5cbd-104">La funzione **ReadPrinter** recupera i dati dalla stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-104">The **ReadPrinter** function retrieves data from the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5cbd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5cbd-105">Syntax</span></span>


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a><span data-ttu-id="e5cbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5cbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5cbd-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5cbd-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5cbd-108">Handle per l'oggetto stampante per il quale recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-108">A handle to the printer object for which to retrieve data.</span></span> <span data-ttu-id="e5cbd-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) per recuperare un handle di oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-109">Use the [**OpenPrinter**](openprinter.md) function to retrieve a printer object handle.</span></span> <span data-ttu-id="e5cbd-110">Usare il formato: PrinterName, job xxxx.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-110">Use the format: Printername, Job xxxx.</span></span>

</dd> <dt>

<span data-ttu-id="e5cbd-111">*pbuf* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e5cbd-111">*pBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5cbd-112">Puntatore a un buffer che riceve i dati della stampante.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-112">A pointer to a buffer that receives the printer data.</span></span>

</dd> <dt>

<span data-ttu-id="e5cbd-113">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5cbd-113">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5cbd-114">Dimensione, in byte, del buffer a cui punta *pbuf* .</span><span class="sxs-lookup"><span data-stu-id="e5cbd-114">The size, in bytes, of the buffer to which *pBuf* points.</span></span>

</dd> <dt>

<span data-ttu-id="e5cbd-115">*pNoBytesRead* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e5cbd-115">*pNoBytesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5cbd-116">Puntatore a una variabile che riceve il numero di byte di dati copiati nella matrice a cui punta *pbuf* .</span><span class="sxs-lookup"><span data-stu-id="e5cbd-116">A pointer to a variable that receives the number of bytes of data copied into the array to which *pBuf* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5cbd-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5cbd-117">Return value</span></span>

<span data-ttu-id="e5cbd-118">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e5cbd-119">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5cbd-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5cbd-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e5cbd-121">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e5cbd-122">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e5cbd-123">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e5cbd-124">**ReadPrinter** restituisce un errore se il dispositivo o la stampante non è bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="e5cbd-124">**ReadPrinter** returns an error if the device or the printer is not bidirectional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5cbd-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5cbd-125">Requirements</span></span>



| <span data-ttu-id="e5cbd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5cbd-126">Requirement</span></span> | <span data-ttu-id="e5cbd-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e5cbd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5cbd-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5cbd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e5cbd-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e5cbd-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e5cbd-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5cbd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e5cbd-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e5cbd-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e5cbd-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5cbd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5cbd-133"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5cbd-133"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e5cbd-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5cbd-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5cbd-135"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5cbd-135"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e5cbd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e5cbd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5cbd-137"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5cbd-137"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e5cbd-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5cbd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5cbd-139">Stampa</span><span class="sxs-lookup"><span data-stu-id="e5cbd-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e5cbd-140">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="e5cbd-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e5cbd-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e5cbd-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




