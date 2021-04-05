---
description: La funzione DeletePrinterDataEx Elimina un valore specificato dai dati di configurazione di una stampante.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: Funzione DeletePrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757388"
---
# <a name="deleteprinterdataex-function"></a><span data-ttu-id="4c924-103">DeletePrinterDataEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="4c924-103">DeletePrinterDataEx function</span></span>

<span data-ttu-id="4c924-104">La funzione **DeletePrinterDataEx** Elimina un valore specificato dai dati di configurazione di una stampante.</span><span class="sxs-lookup"><span data-stu-id="4c924-104">The **DeletePrinterDataEx** function deletes a specified value from the configuration data for a printer.</span></span> <span data-ttu-id="4c924-105">I dati di configurazione di una stampante sono costituiti da un set di valori denominati e tipizzati archiviati in una gerarchia di chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4c924-105">A printer's configuration data consists of a set of named and typed values stored in a hierarchy of registry keys.</span></span> <span data-ttu-id="4c924-106">La funzione Elimina un valore specificato in una chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="4c924-106">The function deletes a specified value under a specified key.</span></span>

<span data-ttu-id="4c924-107">Come la funzione [**DeletePrinterData**](deleteprinterdata.md) , **DeletePrinterDataEx** può eliminare i valori archiviati dalla funzione [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="4c924-107">Like the [**DeletePrinterData**](deleteprinterdata.md) function, **DeletePrinterDataEx** can delete values stored by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="4c924-108">Inoltre, **DeletePrinterDataEx** può eliminare i valori archiviati con una chiave specificata dalla funzione [**SetPrinterDataEx**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="4c924-108">In addition, **DeletePrinterDataEx** can delete values stored under a specified key by the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c924-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c924-109">Syntax</span></span>


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="4c924-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c924-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c924-111">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c924-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c924-112">Handle per la stampante per il quale la funzione Elimina un valore.</span><span class="sxs-lookup"><span data-stu-id="4c924-112">A handle to the printer for which the function deletes a value.</span></span> <span data-ttu-id="4c924-113">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="4c924-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4c924-114">*pKeyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c924-114">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c924-115">Puntatore a una stringa con terminazione null che specifica la chiave contenente il valore da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4c924-115">A pointer to a null-terminated string that specifies the key containing the value to delete.</span></span> <span data-ttu-id="4c924-116">Usare il carattere barra rovesciata ( \\ ) come delimitatore per specificare un percorso con una o più sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="4c924-116">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="4c924-117">Se *pKeyName* è **null** o una stringa vuota, **DeletePrinterDataEx** restituisce l' \_ errore \_ parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="4c924-117">If *pKeyName* is **NULL** or an empty string, **DeletePrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="4c924-118">*pValueName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c924-118">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c924-119">Puntatore a una stringa con terminazione null che specifica il nome del valore da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4c924-119">A pointer to a null-terminated string that specifies the name of the value to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c924-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c924-120">Return value</span></span>

<span data-ttu-id="4c924-121">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4c924-121">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="4c924-122">Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="4c924-122">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c924-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c924-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c924-124">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4c924-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4c924-125">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c924-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4c924-126">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="4c924-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c924-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c924-127">Requirements</span></span>



| <span data-ttu-id="4c924-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c924-128">Requirement</span></span> | <span data-ttu-id="4c924-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4c924-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c924-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c924-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4c924-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4c924-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4c924-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c924-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4c924-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4c924-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4c924-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c924-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c924-135"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c924-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4c924-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c924-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c924-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c924-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4c924-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4c924-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c924-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4c924-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4c924-140">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4c924-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4c924-141">**DeletePrinterDataExW** (Unicode) e **DeletePrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4c924-141">**DeletePrinterDataExW** (Unicode) and **DeletePrinterDataExA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="4c924-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c924-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c924-143">Stampa</span><span class="sxs-lookup"><span data-stu-id="4c924-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4c924-144">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="4c924-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4c924-145">**DeletePrinterKey**</span><span class="sxs-lookup"><span data-stu-id="4c924-145">**DeletePrinterKey**</span></span>](deleteprinterkey.md)
</dt> <dt>

[<span data-ttu-id="4c924-146">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="4c924-146">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="4c924-147">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="4c924-147">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="4c924-148">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="4c924-148">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="4c924-149">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4c924-149">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="4c924-150">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="4c924-150">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




