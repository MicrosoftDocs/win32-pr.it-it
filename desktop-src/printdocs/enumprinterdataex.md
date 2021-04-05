---
description: La funzione EnumPrinterDataEx enumera tutti i nomi e i dati dei valori per una stampante e una chiave specificate.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Funzione EnumPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757853"
---
# <a name="enumprinterdataex-function"></a><span data-ttu-id="fd7f4-103">EnumPrinterDataEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="fd7f4-103">EnumPrinterDataEx function</span></span>

<span data-ttu-id="fd7f4-104">La funzione **EnumPrinterDataEx** enumera tutti i nomi e i dati dei valori per una stampante e una chiave specificate.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-104">The **EnumPrinterDataEx** function enumerates all value names and data for a specified printer and key.</span></span>

<span data-ttu-id="fd7f4-105">I dati della stampante vengono archiviati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="fd7f4-106">Durante l'enumerazione dei dati della stampante, non chiamare le funzioni del registro di sistema che potrebbero modificare i dati.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7f4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd7f4-107">Syntax</span></span>


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a><span data-ttu-id="fd7f4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd7f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd7f4-109">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd7f4-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7f4-110">Handle per la stampante per il quale la funzione recupera i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-110">A handle to the printer for which the function retrieves configuration data.</span></span> <span data-ttu-id="fd7f4-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="fd7f4-112">*pKeyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd7f4-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7f4-113">Puntatore a una stringa con terminazione null che specifica la chiave che contiene i valori da enumerare.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-113">A pointer to a null-terminated string that specifies the key containing the values to enumerate.</span></span> <span data-ttu-id="fd7f4-114">Usare il carattere barra rovesciata ( \\ ) come delimitatore per specificare un percorso con una o più sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-114">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="fd7f4-115">**EnumPrinterDataEx** enumera tutti i valori della chiave, ma non enumera i valori delle sottochiavi della chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-115">**EnumPrinterDataEx** enumerates all values of the key, but does not enumerate values of subkeys of the specified key.</span></span> <span data-ttu-id="fd7f4-116">Utilizzare la funzione [**EnumPrinterKey**](enumprinterkey.md) per enumerare le sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-116">Use the [**EnumPrinterKey**](enumprinterkey.md) function to enumerate subkeys.</span></span>

<span data-ttu-id="fd7f4-117">Se *pKeyName* è **null** o una stringa vuota, **EnumPrinterDataEx** restituisce l' \_ errore \_ parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-117">If *pKeyName* is **NULL** or an empty string, **EnumPrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="fd7f4-118">*pEnumValues* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd7f4-118">*pEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7f4-119">Puntatore a un buffer che riceve una matrice di strutture [**di \_ \_ valori enum della stampante**](printer-enum-values.md) .</span><span class="sxs-lookup"><span data-stu-id="fd7f4-119">A pointer to a buffer that receives an array of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures.</span></span> <span data-ttu-id="fd7f4-120">Ogni struttura contiene il nome del valore, il tipo, i dati e le dimensioni di un valore sotto la chiave.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-120">Each structure contains the value name, type, data, and sizes of a value under the key.</span></span>

</dd> <dt>

<span data-ttu-id="fd7f4-121">*cbEnumValues* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd7f4-121">*cbEnumValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7f4-122">Dimensione, in byte, del buffer a cui punta *pcbEnumValues*.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-122">The size, in bytes, of the buffer pointed to by *pcbEnumValues*.</span></span> <span data-ttu-id="fd7f4-123">Se si imposta *cbEnumValues* su zero, il parametro *pcbEnumValues* restituisce le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-123">If you set *cbEnumValues* to zero, the *pcbEnumValues* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="fd7f4-124">*pcbEnumValues* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd7f4-124">*pcbEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7f4-125">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di configurazione recuperati.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-125">A pointer to a variable that receives the size, in bytes, of the retrieved configuration data.</span></span> <span data-ttu-id="fd7f4-126">Se la dimensione del buffer specificata da *cbEnumValues* è troppo piccola, la funzione restituisce l'errore di \_ altri \_ dati e *pcbEnumValues* indica le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-126">If the buffer size specified by *cbEnumValues* is too small, the function returns ERROR\_MORE\_DATA and *pcbEnumValues* indicates the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="fd7f4-127">*pnEnumValues* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd7f4-127">*pnEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7f4-128">Puntatore a una variabile che riceve il numero di strutture [**di \_ \_ valori enum della stampante**](printer-enum-values.md) restituite in *pEnumValues*.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-128">A pointer to a variable that receives the number of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures returned in *pEnumValues*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd7f4-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd7f4-129">Return value</span></span>

<span data-ttu-id="fd7f4-130">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-130">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="fd7f4-131">Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-131">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd7f4-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd7f4-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd7f4-133">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fd7f4-134">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fd7f4-135">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="fd7f4-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="fd7f4-136">**EnumPrinterDataEx** recupera i dati di configurazione della stampante impostati dalle funzioni [**SetPrinterDataEx**](setprinterdataex.md) e [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="fd7f4-136">**EnumPrinterDataEx** retrieves printer configuration data set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7f4-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd7f4-137">Requirements</span></span>



| <span data-ttu-id="fd7f4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd7f4-138">Requirement</span></span> | <span data-ttu-id="fd7f4-139">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7f4-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7f4-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd7f4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7f4-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fd7f4-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fd7f4-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd7f4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7f4-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fd7f4-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fd7f4-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd7f4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd7f4-145"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd7f4-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fd7f4-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd7f4-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd7f4-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd7f4-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fd7f4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fd7f4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd7f4-149"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fd7f4-149"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="fd7f4-150">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="fd7f4-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fd7f4-151">**EnumPrinterDataExW** (Unicode) e **EnumPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fd7f4-151">**EnumPrinterDataExW** (Unicode) and **EnumPrinterDataExA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="fd7f4-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd7f4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7f4-153">Stampa</span><span class="sxs-lookup"><span data-stu-id="fd7f4-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fd7f4-154">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="fd7f4-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fd7f4-155">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="fd7f4-155">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="fd7f4-156">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="fd7f4-156">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="fd7f4-157">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="fd7f4-157">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="fd7f4-158">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="fd7f4-158">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="fd7f4-159">**\_valori enum della stampante \_**</span><span class="sxs-lookup"><span data-stu-id="fd7f4-159">**PRINTER\_ENUM\_VALUES**</span></span>](printer-enum-values.md)
</dt> <dt>

[<span data-ttu-id="fd7f4-160">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="fd7f4-160">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="fd7f4-161">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="fd7f4-161">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




