---
description: La funzione DeletePrinterKey Elimina una chiave specificata e tutte le relative sottochiavi per una stampante specificata.
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: Funzione DeletePrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757748"
---
# <a name="deleteprinterkey-function"></a><span data-ttu-id="e90de-103">DeletePrinterKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="e90de-103">DeletePrinterKey function</span></span>

<span data-ttu-id="e90de-104">La funzione **DeletePrinterKey** Elimina una chiave specificata e tutte le relative sottochiavi per una stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="e90de-104">The **DeletePrinterKey** function deletes a specified key and all its subkeys for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90de-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e90de-105">Syntax</span></span>


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a><span data-ttu-id="e90de-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e90de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90de-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e90de-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90de-108">Handle per la stampante per il quale la funzione Elimina una chiave.</span><span class="sxs-lookup"><span data-stu-id="e90de-108">A handle to the printer for which the function deletes a key.</span></span> <span data-ttu-id="e90de-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="e90de-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e90de-110">*pKeyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e90de-110">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90de-111">Puntatore a una stringa con terminazione null che specifica la chiave da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e90de-111">A pointer to a null-terminated string that specifies the key to delete.</span></span> <span data-ttu-id="e90de-112">Usare il carattere barra rovesciata ( \\ ) come delimitatore per specificare un percorso con una o più sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="e90de-112">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span>

<span data-ttu-id="e90de-113">Se *pKeyName* è una stringa vuota (""), **DeletePrinterKey** Elimina tutte le chiavi sotto la chiave di primo livello per la stampante.</span><span class="sxs-lookup"><span data-stu-id="e90de-113">If *pKeyName* is an empty string (""), **DeletePrinterKey** deletes all keys below the top-level key for the printer.</span></span> <span data-ttu-id="e90de-114">Se *pKeyName* è **null**, **DeletePrinterKey** restituisce l' \_ errore \_ parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="e90de-114">If *pKeyName* is **NULL**, **DeletePrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90de-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e90de-115">Return value</span></span>

<span data-ttu-id="e90de-116">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e90de-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e90de-117">Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="e90de-117">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e90de-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e90de-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e90de-119">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e90de-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e90de-120">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e90de-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e90de-121">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="e90de-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e90de-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e90de-122">Requirements</span></span>



| <span data-ttu-id="e90de-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90de-123">Requirement</span></span> | <span data-ttu-id="e90de-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e90de-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90de-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90de-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e90de-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e90de-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e90de-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90de-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e90de-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e90de-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e90de-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e90de-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e90de-130"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e90de-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e90de-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="e90de-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e90de-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e90de-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e90de-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e90de-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90de-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e90de-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e90de-135">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e90de-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e90de-136">**DeletePrinterKeyW** (Unicode) e **DeletePrinterKeyA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e90de-136">**DeletePrinterKeyW** (Unicode) and **DeletePrinterKeyA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="e90de-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e90de-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90de-138">Stampa</span><span class="sxs-lookup"><span data-stu-id="e90de-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e90de-139">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="e90de-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e90de-140">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="e90de-140">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="e90de-141">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="e90de-141">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="e90de-142">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="e90de-142">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="e90de-143">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="e90de-143">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="e90de-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e90de-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e90de-145">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="e90de-145">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




