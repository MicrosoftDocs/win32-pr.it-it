---
description: La funzione DeletePrinterData Elimina i dati di configurazione specificati per una stampante. I dati di configurazione di una stampante sono costituiti da un set di valori denominati e tipizzati. La funzione DeletePrinterData Elimina uno di questi valori, specificato in base al nome del relativo valore.
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: Funzione DeletePrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterData
- DeletePrinterDataA
- DeletePrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a88df8484d367ae2cc50f4a465b5db1dcd53c355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345311"
---
# <a name="deleteprinterdata-function"></a><span data-ttu-id="bbbab-105">DeletePrinterData (funzione)</span><span class="sxs-lookup"><span data-stu-id="bbbab-105">DeletePrinterData function</span></span>

<span data-ttu-id="bbbab-106">La funzione **DeletePrinterData** Elimina i dati di configurazione specificati per una stampante.</span><span class="sxs-lookup"><span data-stu-id="bbbab-106">The **DeletePrinterData** function deletes specified configuration data for a printer.</span></span> <span data-ttu-id="bbbab-107">I dati di configurazione di una stampante sono costituiti da un set di valori denominati e tipizzati.</span><span class="sxs-lookup"><span data-stu-id="bbbab-107">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="bbbab-108">La funzione **DeletePrinterData** Elimina uno di questi valori, specificato in base al nome del relativo valore.</span><span class="sxs-lookup"><span data-stu-id="bbbab-108">The **DeletePrinterData** function deletes one of these values, specified by its value name.</span></span>

<span data-ttu-id="bbbab-109">La chiamata a **DeletePrinterData** equivale alla chiamata della funzione [**DeletePrinterDataEx**](deleteprinterdataex.md) con il parametro *pKeyName* impostato su "PrinterDriverData".</span><span class="sxs-lookup"><span data-stu-id="bbbab-109">Calling **DeletePrinterData** is equivalent to calling the [**DeletePrinterDataEx**](deleteprinterdataex.md) function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="bbbab-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbbab-110">Syntax</span></span>


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="bbbab-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbbab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbbab-112">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bbbab-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbbab-113">Handle per la stampante i cui dati di configurazione devono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="bbbab-113">A handle to the printer whose configuration data is to be deleted.</span></span> <span data-ttu-id="bbbab-114">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="bbbab-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="bbbab-115">*pValueName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bbbab-115">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbbab-116">Puntatore al nome con terminazione null del valore dei dati di configurazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="bbbab-116">A pointer to the null-terminated name of the configuration data value to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbbab-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbbab-117">Return value</span></span>

<span data-ttu-id="bbbab-118">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bbbab-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="bbbab-119">Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="bbbab-119">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbbab-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbbab-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bbbab-121">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="bbbab-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bbbab-122">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bbbab-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bbbab-123">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="bbbab-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bbbab-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbbab-124">Requirements</span></span>



| <span data-ttu-id="bbbab-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbbab-125">Requirement</span></span> | <span data-ttu-id="bbbab-126">Valore</span><span class="sxs-lookup"><span data-stu-id="bbbab-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbbab-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbbab-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bbbab-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bbbab-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bbbab-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbbab-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bbbab-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bbbab-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bbbab-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbbab-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbbab-132"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbbab-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bbbab-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="bbbab-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="bbbab-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbbab-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bbbab-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bbbab-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbbab-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bbbab-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bbbab-137">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bbbab-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bbbab-138">**DeletePrinterDataW** (Unicode) e **DeletePrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bbbab-138">**DeletePrinterDataW** (Unicode) and **DeletePrinterDataA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="bbbab-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbbab-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbbab-140">Stampa</span><span class="sxs-lookup"><span data-stu-id="bbbab-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bbbab-141">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="bbbab-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bbbab-142">**EnumPrinterData**</span><span class="sxs-lookup"><span data-stu-id="bbbab-142">**EnumPrinterData**</span></span>](enumprinterdata.md)
</dt> <dt>

[<span data-ttu-id="bbbab-143">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="bbbab-143">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="bbbab-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="bbbab-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="bbbab-145">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="bbbab-145">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="bbbab-146">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="bbbab-146">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

 




