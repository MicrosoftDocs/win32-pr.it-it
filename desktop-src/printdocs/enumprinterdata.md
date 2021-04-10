---
description: La funzione EnumPrinterData enumera i dati di configurazione per una stampante specificata.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Funzione EnumPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227349"
---
# <a name="enumprinterdata-function"></a><span data-ttu-id="97b0c-103">EnumPrinterData (funzione)</span><span class="sxs-lookup"><span data-stu-id="97b0c-103">EnumPrinterData function</span></span>

<span data-ttu-id="97b0c-104">La funzione **EnumPrinterData** enumera i dati di configurazione per una stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="97b0c-104">The **EnumPrinterData** function enumerates configuration data for a specified printer.</span></span>

<span data-ttu-id="97b0c-105">Per recuperare i dati di configurazione in una singola chiamata, utilizzare la funzione [**EnumPrinterDataEx**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="97b0c-105">To retrieve the configuration data in a single call, use the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b0c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97b0c-106">Syntax</span></span>


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="97b0c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="97b0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97b0c-108">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b0c-109">Handle per la stampante i cui dati di configurazione devono essere ottenuti.</span><span class="sxs-lookup"><span data-stu-id="97b0c-109">A handle to the printer whose configuration data is to be obtained.</span></span> <span data-ttu-id="97b0c-110">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="97b0c-110">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="97b0c-111">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b0c-112">Valore di indice che specifica il valore dei dati di configurazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="97b0c-112">An index value that specifies the configuration data value to retrieve.</span></span>

<span data-ttu-id="97b0c-113">Impostare questo parametro su zero per la prima chiamata a **EnumPrinterData** per un handle di stampante specificato.</span><span class="sxs-lookup"><span data-stu-id="97b0c-113">Set this parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="97b0c-114">Quindi incrementare di uno il parametro per le chiamate successive che interessano la stessa stampante, finché la funzione non restituisce un errore di \_ \_ altri \_ elementi.</span><span class="sxs-lookup"><span data-stu-id="97b0c-114">Then increment the parameter by one for subsequent calls involving the same printer, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="97b0c-115">Per ulteriori informazioni, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="97b0c-115">See the following Remarks section for further information.</span></span>

<span data-ttu-id="97b0c-116">Se si usa la tecnica descritta nelle descrizioni dei parametri *cbValueName* e *cbData* per ottenere valori di dimensioni del buffer adeguati, impostando entrambi i parametri su zero in una prima chiamata a **EnumPrinterData** per un handle di stampante specificato, il valore di *dwIndex* non è rilevante per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="97b0c-116">If you use the technique mentioned in the descriptions of the *cbValueName* and *cbData* parameters to obtain adequate buffer size values, setting both those parameters to zero in a first call to **EnumPrinterData** for a specified printer handle, the value of *dwIndex* does not matter for that call.</span></span> <span data-ttu-id="97b0c-117">Impostare *dwIndex* su zero nella chiamata successiva a **EnumPrinterData** per avviare il processo di enumerazione effettivo.</span><span class="sxs-lookup"><span data-stu-id="97b0c-117">Set *dwIndex* to zero in the next call to **EnumPrinterData** to start the actual enumeration process.</span></span>

<span data-ttu-id="97b0c-118">I valori dei dati di configurazione non sono ordinati.</span><span class="sxs-lookup"><span data-stu-id="97b0c-118">Configuration data values are not ordered.</span></span> <span data-ttu-id="97b0c-119">I nuovi valori avranno un indice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="97b0c-119">New values will have an arbitrary index.</span></span> <span data-ttu-id="97b0c-120">Ciò significa che la funzione **EnumPrinterData** può restituire valori in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="97b0c-120">This means that the **EnumPrinterData** function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="97b0c-121">*pValueName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-121">*pValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97b0c-122">Puntatore a un buffer che riceve il nome del valore dei dati di configurazione, incluso un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="97b0c-122">A pointer to a buffer that receives the name of the configuration data value, including a terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="97b0c-123">*cbValueName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-123">*cbValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b0c-124">Dimensione, in byte, del buffer a cui punta *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="97b0c-124">The size, in bytes, of the buffer pointed to by *pValueName*.</span></span>

<span data-ttu-id="97b0c-125">Se si desidera che il sistema operativo fornisca una dimensione del buffer adeguata, impostare questo parametro e il parametro *cbData* su zero per la prima chiamata a **EnumPrinterData** per un handle di stampante specificato.</span><span class="sxs-lookup"><span data-stu-id="97b0c-125">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbData* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="97b0c-126">Quando la funzione restituisce, la variabile a cui punta *pcbValueName* conterrà una dimensione del buffer sufficientemente grande da poter enumerare correttamente tutti i nomi dei valori dei dati di configurazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="97b0c-126">When the function returns, the variable pointed to by *pcbValueName* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="97b0c-127">*pcbValueName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-127">*pcbValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97b0c-128">Puntatore a una variabile che riceve il numero di byte archiviati nel buffer a cui punta *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="97b0c-128">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pValueName*.</span></span>

</dd> <dt>

<span data-ttu-id="97b0c-129">*pType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-129">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97b0c-130">Puntatore a una variabile che riceve un codice che indica il tipo di dati archiviati nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="97b0c-130">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="97b0c-131">Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="97b0c-131">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span> <span data-ttu-id="97b0c-132">Il parametro *pType* può essere **null** se il codice di tipo non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="97b0c-132">The *pType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="97b0c-133">*pData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-133">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97b0c-134">Puntatore a un buffer che riceve il valore dei dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="97b0c-134">A pointer to a buffer that receives the configuration data value.</span></span>

<span data-ttu-id="97b0c-135">Questo parametro può essere **null** se il valore dei dati di configurazione non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="97b0c-135">This parameter can be **NULL** if the configuration data value is not required.</span></span>

</dd> <dt>

<span data-ttu-id="97b0c-136">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-136">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b0c-137">Dimensione, in byte, del buffer a cui punta *pData*.</span><span class="sxs-lookup"><span data-stu-id="97b0c-137">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="97b0c-138">Se si desidera che il sistema operativo fornisca una dimensione del buffer adeguata, impostare questo parametro e il parametro *cbValueName* su zero per la prima chiamata a **EnumPrinterData** per un handle di stampante specificato.</span><span class="sxs-lookup"><span data-stu-id="97b0c-138">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbValueName* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="97b0c-139">Quando la funzione restituisce, la variabile a cui punta *pcbData* conterrà una dimensione del buffer sufficientemente grande da poter enumerare correttamente tutti i nomi dei valori dei dati di configurazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="97b0c-139">When the function returns, the variable pointed to by *pcbData* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="97b0c-140">*pcbData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-140">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97b0c-141">Puntatore a una variabile che riceve il numero di byte archiviati nel buffer a cui punta *pData*.</span><span class="sxs-lookup"><span data-stu-id="97b0c-141">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="97b0c-142">Questo parametro può essere **null** se *pData* è **null**.</span><span class="sxs-lookup"><span data-stu-id="97b0c-142">This parameter can be **NULL** if *pData* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97b0c-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97b0c-143">Return value</span></span>

<span data-ttu-id="97b0c-144">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="97b0c-144">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="97b0c-145">Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="97b0c-145">If the function fails, the return value is a system error code.</span></span>

<span data-ttu-id="97b0c-146">La funzione restituisce un errore se non sono presenti altri \_ \_ \_ valori dei dati di configurazione da recuperare per un handle di stampante specificato.</span><span class="sxs-lookup"><span data-stu-id="97b0c-146">The function returns ERROR\_NO\_MORE\_ITEMS when there are no more configuration data values to retrieve for a specified printer handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="97b0c-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="97b0c-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="97b0c-148">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="97b0c-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="97b0c-149">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97b0c-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="97b0c-150">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="97b0c-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="97b0c-151">**EnumPrinterData** recupera i dati di configurazione della stampante impostati dalla funzione [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="97b0c-151">**EnumPrinterData** retrieves printer configuration data set by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="97b0c-152">I dati di configurazione di una stampante sono costituiti da un set di valori denominati e tipizzati.</span><span class="sxs-lookup"><span data-stu-id="97b0c-152">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="97b0c-153">La funzione **EnumPrinterData** ottiene uno di questi valori, il nome e il codice del tipo, ogni volta che viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="97b0c-153">The **EnumPrinterData** function obtains one of these values, and its name and a type code, each time you call it.</span></span> <span data-ttu-id="97b0c-154">Chiamare la funzione **EnumPrinterData** più volte in successione per ottenere tutti i valori dei dati di configurazione di una stampante.</span><span class="sxs-lookup"><span data-stu-id="97b0c-154">Call the **EnumPrinterData** function several times in succession to obtain all of a printer's configuration data values.</span></span>

<span data-ttu-id="97b0c-155">I dati di configurazione della stampante vengono archiviati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="97b0c-155">Printer configuration data is stored in the registry.</span></span> <span data-ttu-id="97b0c-156">Durante l'enumerazione dei dati di configurazione della stampante, è consigliabile evitare di chiamare le funzioni del registro di sistema che potrebbero modificare i dati.</span><span class="sxs-lookup"><span data-stu-id="97b0c-156">While enumerating printer configuration data, you should avoid calling registry functions that might change that data.</span></span>

<span data-ttu-id="97b0c-157">Se si vuole che il sistema operativo fornisca una dimensione del buffer adeguata, chiamare prima **EnumPrinterData** con i parametri *cbValueName* e *cbData* impostati su zero, come indicato in precedenza nella sezione Parameters.</span><span class="sxs-lookup"><span data-stu-id="97b0c-157">If you want to have the operating system supply an adequate buffer size, first call **EnumPrinterData** with both the *cbValueName* and *cbData* parameters set to zero, as noted earlier in the Parameters section.</span></span> <span data-ttu-id="97b0c-158">Il valore di *dwIndex* non è rilevante per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="97b0c-158">The value of *dwIndex* does not matter for this call.</span></span> <span data-ttu-id="97b0c-159">Quando la funzione restituisce, \* *pcbValueName* e \* *pcbData* conterranno dimensioni del buffer sufficientemente grandi da poter enumerare tutti i valori e i nomi dei valori dei dati di configurazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="97b0c-159">When the function returns, \**pcbValueName* and \**pcbData* will contain buffer sizes that are large enough to enumerate all of the printer's configuration data value names and values.</span></span> <span data-ttu-id="97b0c-160">Alla chiamata successiva, allocare il nome del valore e i buffer di dati, impostare *cbValueName* e *cbData* sulle dimensioni in byte dei buffer allocati e impostare *dwIndex* su zero.</span><span class="sxs-lookup"><span data-stu-id="97b0c-160">On the next call, allocate value name and data buffers, set *cbValueName* and *cbData* to the sizes in bytes of the allocated buffers, and set *dwIndex* to zero.</span></span> <span data-ttu-id="97b0c-161">Successivamente, continuare a chiamare la funzione **EnumPrinterData** , incrementando di uno ogni volta *dwIndex* , fino a quando la funzione non restituisce un errore di \_ \_ altri \_ elementi.</span><span class="sxs-lookup"><span data-stu-id="97b0c-161">Thereafter, continue to call the **EnumPrinterData** function, incrementing *dwIndex* by one each time, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="requirements"></a><span data-ttu-id="97b0c-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97b0c-162">Requirements</span></span>



| <span data-ttu-id="97b0c-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="97b0c-163">Requirement</span></span> | <span data-ttu-id="97b0c-164">Valore</span><span class="sxs-lookup"><span data-stu-id="97b0c-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97b0c-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97b0c-165">Minimum supported client</span></span><br/> | <span data-ttu-id="97b0c-166">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="97b0c-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97b0c-167">Minimum supported server</span></span><br/> | <span data-ttu-id="97b0c-168">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97b0c-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="97b0c-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97b0c-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="97b0c-170"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97b0c-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="97b0c-171">Libreria</span><span class="sxs-lookup"><span data-stu-id="97b0c-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="97b0c-172"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97b0c-172"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="97b0c-173">DLL</span><span class="sxs-lookup"><span data-stu-id="97b0c-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97b0c-174"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="97b0c-174"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="97b0c-175">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="97b0c-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="97b0c-176">**EnumPrinterDataW** (Unicode) e **EnumPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="97b0c-176">**EnumPrinterDataW** (Unicode) and **EnumPrinterDataA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="97b0c-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97b0c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b0c-178">Stampa</span><span class="sxs-lookup"><span data-stu-id="97b0c-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="97b0c-179">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="97b0c-179">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="97b0c-180">**DeletePrinterData**</span><span class="sxs-lookup"><span data-stu-id="97b0c-180">**DeletePrinterData**</span></span>](deleteprinterdata.md)
</dt> <dt>

[<span data-ttu-id="97b0c-181">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="97b0c-181">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="97b0c-182">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="97b0c-182">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="97b0c-183">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="97b0c-183">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="97b0c-184">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="97b0c-184">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="97b0c-185">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="97b0c-185">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

