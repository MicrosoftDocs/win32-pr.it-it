---
description: La funzione DeletePrinter Elimina l'oggetto stampante specificato.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Funzione DeletePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311552"
---
# <a name="deleteprinter-function"></a><span data-ttu-id="9db32-103">DeletePrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="9db32-103">DeletePrinter function</span></span>

<span data-ttu-id="9db32-104">La funzione **DeletePrinter** Elimina l'oggetto stampante specificato.</span><span class="sxs-lookup"><span data-stu-id="9db32-104">The **DeletePrinter** function deletes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9db32-105">Syntax</span></span>


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="9db32-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9db32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db32-107">*hPrinter* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="9db32-107">*hPrinter* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9db32-108">Handle per un oggetto Printer che verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="9db32-108">Handle to a printer object that will be deleted.</span></span> <span data-ttu-id="9db32-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="9db32-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db32-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9db32-110">Return value</span></span>

<span data-ttu-id="9db32-111">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="9db32-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9db32-112">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="9db32-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db32-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9db32-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9db32-114">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="9db32-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9db32-115">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9db32-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9db32-116">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="9db32-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9db32-117">Se sono presenti processi di stampa rimanenti da elaborare per la stampante specificata, **DeletePrinter** contrassegna la stampante per l'eliminazione in sospeso e quindi la Elimina al termine della stampa di tutti i processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="9db32-117">If there are print jobs remaining to be processed for the specified printer, **DeletePrinter** marks the printer for pending deletion, and then deletes it when all the print jobs have been printed.</span></span> <span data-ttu-id="9db32-118">Non è possibile aggiungere processi di stampa a una stampante contrassegnata per l'eliminazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="9db32-118">No print jobs can be added to a printer that is marked for pending deletion.</span></span>

<span data-ttu-id="9db32-119">Una stampante contrassegnata per l'eliminazione in sospeso non può essere mantenuta, ma i processi di stampa possono essere conservati, ripresi e riavviati.</span><span class="sxs-lookup"><span data-stu-id="9db32-119">A printer marked for pending deletion cannot be held, but its print jobs can be held, resumed, and restarted.</span></span> <span data-ttu-id="9db32-120">Se la stampante viene mantenuta e sono presenti processi per la stampante, **DeletePrinter** ha esito negativo e viene \_ negato l'accesso agli errori \_ .</span><span class="sxs-lookup"><span data-stu-id="9db32-120">If the printer is held and there are jobs for the printer, **DeletePrinter** fails with ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="9db32-121">Si noti che **DeletePrinter** non chiude l'handle che lo viene passato.</span><span class="sxs-lookup"><span data-stu-id="9db32-121">Note that **DeletePrinter** does not close the handle that is passed to it.</span></span> <span data-ttu-id="9db32-122">Pertanto, l'applicazione deve comunque chiamare [**ClosePrinter**](closeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="9db32-122">Thus, the application must still call [**ClosePrinter**](closeprinter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9db32-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9db32-123">Requirements</span></span>



| <span data-ttu-id="9db32-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9db32-124">Requirement</span></span> | <span data-ttu-id="9db32-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9db32-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db32-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9db32-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9db32-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9db32-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9db32-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9db32-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9db32-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9db32-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9db32-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9db32-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db32-131"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9db32-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9db32-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="9db32-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9db32-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9db32-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9db32-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9db32-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db32-135"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db32-135"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="9db32-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9db32-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db32-137">Stampa</span><span class="sxs-lookup"><span data-stu-id="9db32-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9db32-138">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="9db32-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9db32-139">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="9db32-139">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="9db32-140">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="9db32-140">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="9db32-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9db32-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




