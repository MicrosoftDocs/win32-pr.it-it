---
description: La funzione ResetPrinter specifica il tipo di dati e i valori della modalità dispositivo da usare per la stampa dei documenti inviati dalla funzione StartDocPrinter. È possibile eseguire l'override di questi valori utilizzando la funzione SetJob dopo l'avvio della stampa del documento.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: Funzione ResetPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8bdfef0229a646e802878a96370d27d49a6bfc2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312569"
---
# <a name="resetprinter-function"></a><span data-ttu-id="480db-104">ResetPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="480db-104">ResetPrinter function</span></span>

<span data-ttu-id="480db-105">La funzione **ResetPrinter** specifica il tipo di dati e i valori della modalità dispositivo da usare per la stampa dei documenti inviati dalla funzione [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="480db-105">The **ResetPrinter** function specifies the data type and device mode values to be used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="480db-106">È possibile eseguire l'override di questi valori utilizzando la funzione [**SetJob**](setjob.md) dopo l'avvio della stampa del documento.</span><span class="sxs-lookup"><span data-stu-id="480db-106">These values can be overridden by using the [**SetJob**](setjob.md) function after document printing has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="480db-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="480db-107">Syntax</span></span>


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="480db-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="480db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="480db-109">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="480db-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="480db-110">Handle per la stampante.</span><span class="sxs-lookup"><span data-stu-id="480db-110">Handle to the printer.</span></span> <span data-ttu-id="480db-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="480db-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="480db-112">*pDefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="480db-112">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="480db-113">Puntatore a una struttura di [**\_ impostazioni predefinite della stampante**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="480db-113">Pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span>

<span data-ttu-id="480db-114">La funzione **ResetPrinter** ignora il membro **desiredAccess** della struttura [**Printer \_ defaults**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="480db-114">The **ResetPrinter** function ignores the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="480db-115">Impostare il membro su zero.</span><span class="sxs-lookup"><span data-stu-id="480db-115">Set that member to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="480db-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="480db-116">Return value</span></span>

<span data-ttu-id="480db-117">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="480db-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="480db-118">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="480db-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="480db-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="480db-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="480db-120">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="480db-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="480db-121">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="480db-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="480db-122">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="480db-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="480db-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="480db-123">Requirements</span></span>



| <span data-ttu-id="480db-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="480db-124">Requirement</span></span> | <span data-ttu-id="480db-125">Valore</span><span class="sxs-lookup"><span data-stu-id="480db-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="480db-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="480db-126">Minimum supported client</span></span><br/> | <span data-ttu-id="480db-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="480db-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="480db-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="480db-128">Minimum supported server</span></span><br/> | <span data-ttu-id="480db-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="480db-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="480db-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="480db-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="480db-131"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="480db-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="480db-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="480db-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="480db-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="480db-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="480db-134">DLL</span><span class="sxs-lookup"><span data-stu-id="480db-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="480db-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="480db-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="480db-136">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="480db-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="480db-137">**ResetPrinterW** (Unicode) e **ResetPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="480db-137">**ResetPrinterW** (Unicode) and **ResetPrinterA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="480db-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="480db-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="480db-139">Stampa</span><span class="sxs-lookup"><span data-stu-id="480db-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="480db-140">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="480db-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="480db-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="480db-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="480db-142">**\_impostazioni predefinite stampanti**</span><span class="sxs-lookup"><span data-stu-id="480db-142">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="480db-143">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="480db-143">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="480db-144">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="480db-144">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




