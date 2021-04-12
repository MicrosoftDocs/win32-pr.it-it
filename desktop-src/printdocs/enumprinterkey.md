---
description: La funzione EnumPrinterKey enumera le sottochiavi di una chiave specificata per una stampante specificata.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Funzione EnumPrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347496"
---
# <a name="enumprinterkey-function"></a><span data-ttu-id="bdc4a-103">EnumPrinterKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="bdc4a-103">EnumPrinterKey function</span></span>

<span data-ttu-id="bdc4a-104">La funzione **EnumPrinterKey** enumera le sottochiavi di una chiave specificata per una stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-104">The **EnumPrinterKey** function enumerates the subkeys of a specified key for a specified printer.</span></span>

<span data-ttu-id="bdc4a-105">I dati della stampante vengono archiviati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="bdc4a-106">Durante l'enumerazione dei dati della stampante, non chiamare le funzioni del registro di sistema che potrebbero modificare i dati.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdc4a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdc4a-107">Syntax</span></span>


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a><span data-ttu-id="bdc4a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdc4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc4a-109">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdc4a-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdc4a-110">Handle per la stampante per il quale la funzione enumera le sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-110">A handle to the printer for which the function enumerates subkeys.</span></span> <span data-ttu-id="bdc4a-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="bdc4a-112">*pKeyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdc4a-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdc4a-113">Puntatore a una stringa con terminazione null che specifica la chiave contenente le sottochiavi da enumerare.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-113">A pointer to a null-terminated string that specifies the key containing the subkeys to enumerate.</span></span> <span data-ttu-id="bdc4a-114">Usare il carattere barra rovesciata ' \\ ' come delimitatore per specificare un percorso con una o più sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-114">Use the backslash '\\' character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="bdc4a-115">**EnumPrinterKey** enumera tutte le sottochiavi della chiave, ma non enumera le sottochiavi di tali sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-115">**EnumPrinterKey** enumerates all subkeys of the key, but does not enumerate the subkeys of those subkeys.</span></span>

<span data-ttu-id="bdc4a-116">Se *pKeyName* è una stringa vuota (""), **EnumPrinterKey** enumera la chiave di primo livello per la stampante.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-116">If *pKeyName* is an empty string (""), **EnumPrinterKey** enumerates the top-level key for the printer.</span></span> <span data-ttu-id="bdc4a-117">Se *pKeyName* è **null**, **EnumPrinterKey** restituisce l' \_ errore \_ parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-117">If *pKeyName* is **NULL**, **EnumPrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="bdc4a-118">*pSubkey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bdc4a-118">*pSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdc4a-119">Puntatore a un buffer che riceve una matrice di nomi di sottochiavi con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-119">A pointer to a buffer that receives an array of null-terminated subkey names.</span></span> <span data-ttu-id="bdc4a-120">La matrice viene terminata da due caratteri null.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-120">The array is terminated by two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="bdc4a-121">*cbSubkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdc4a-121">*cbSubkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdc4a-122">Dimensione, in byte, del buffer a cui punta *pSubkey*.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-122">The size, in bytes, of the buffer pointed to by *pSubkey*.</span></span> <span data-ttu-id="bdc4a-123">Se si imposta *cbSubkey* su zero, il parametro *pcbSubkey* restituisce le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-123">If you set *cbSubkey* to zero, the *pcbSubkey* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="bdc4a-124">*pcbSubkey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bdc4a-124">*pcbSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdc4a-125">Puntatore a una variabile che riceve il numero di byte recuperati nel buffer di *pSubkey* .</span><span class="sxs-lookup"><span data-stu-id="bdc4a-125">A pointer to a variable that receives the number of bytes retrieved in the *pSubkey* buffer.</span></span> <span data-ttu-id="bdc4a-126">Se la dimensione del buffer specificata da *cbSubkey* è troppo piccola, la funzione restituisce l'errore di \_ altri \_ dati e *pcbSubkey* indica le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-126">If the buffer size specified by *cbSubkey* is too small, the function returns ERROR\_MORE\_DATA and *pcbSubkey* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc4a-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdc4a-127">Return value</span></span>

<span data-ttu-id="bdc4a-128">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-128">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="bdc4a-129">Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-129">If the function fails, the return value is a system error code.</span></span> <span data-ttu-id="bdc4a-130">Se *pKeyName* non esiste, il valore restituito è errore \_ file \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-130">If *pKeyName* does not exist, the return value is ERROR\_FILE\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc4a-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdc4a-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bdc4a-132">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bdc4a-133">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bdc4a-134">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bdc4a-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdc4a-135">Requirements</span></span>



| <span data-ttu-id="bdc4a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdc4a-136">Requirement</span></span> | <span data-ttu-id="bdc4a-137">Valore</span><span class="sxs-lookup"><span data-stu-id="bdc4a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc4a-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdc4a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc4a-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bdc4a-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bdc4a-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdc4a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc4a-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bdc4a-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bdc4a-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdc4a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc4a-143"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdc4a-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bdc4a-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="bdc4a-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdc4a-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdc4a-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bdc4a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="bdc4a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdc4a-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bdc4a-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bdc4a-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bdc4a-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bdc4a-149">**EnumPrinterKeyW** (Unicode) e **EnumPrinterKeyA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bdc4a-149">**EnumPrinterKeyW** (Unicode) and **EnumPrinterKeyA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="bdc4a-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdc4a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc4a-151">Stampa</span><span class="sxs-lookup"><span data-stu-id="bdc4a-151">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bdc4a-152">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="bdc4a-152">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bdc4a-153">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="bdc4a-153">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="bdc4a-154">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="bdc4a-154">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="bdc4a-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="bdc4a-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="bdc4a-156">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="bdc4a-156">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




