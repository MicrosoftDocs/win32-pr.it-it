---
description: La funzione EnumPrinterDrivers enumera i driver della stampante installati in un server di stampa specificato.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Funzione EnumPrinterDrivers (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756395"
---
# <a name="enumprinterdrivers-function"></a><span data-ttu-id="c1d30-103">EnumPrinterDrivers (funzione)</span><span class="sxs-lookup"><span data-stu-id="c1d30-103">EnumPrinterDrivers function</span></span>

<span data-ttu-id="c1d30-104">La funzione **EnumPrinterDrivers** enumera i driver della stampante installati in un server di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="c1d30-104">The **EnumPrinterDrivers** function enumerates the printer drivers installed on a specified printer server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d30-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1d30-105">Syntax</span></span>


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="c1d30-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1d30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d30-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d30-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui vengono enumerati i driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="c1d30-108">A pointer to a null-terminated string that specifies the name of the server on which the printer drivers are enumerated.</span></span>

<span data-ttu-id="c1d30-109">Se *pname* è **null**, la funzione enumera i driver della stampante locale.</span><span class="sxs-lookup"><span data-stu-id="c1d30-109">If *pName* is **NULL**, the function enumerates the local printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="c1d30-110">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d30-111">Puntatore a una stringa con terminazione null che specifica l'ambiente, ad esempio Windows x86, Windows IA64, Windows x64 o Windows NT R4000.</span><span class="sxs-lookup"><span data-stu-id="c1d30-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, Windows x64, or Windows NT R4000).</span></span> <span data-ttu-id="c1d30-112">Se questo parametro è **null**, la funzione utilizza l'ambiente corrente del chiamante/client (non del server di destinazione).</span><span class="sxs-lookup"><span data-stu-id="c1d30-112">If this parameter is **NULL**, the function uses the current environment of the caller/client (not of the destination/server).</span></span>

<span data-ttu-id="c1d30-113">Se la stringa *pEnvironment* specifica "All", **EnumPrinterDrivers** enumera i driver della stampante per tutte le piattaforme installate nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="c1d30-113">If the *pEnvironment* string specifies "all", **EnumPrinterDrivers** enumerates printer drivers for all platforms installed on the specified server.</span></span>

</dd> <dt>

<span data-ttu-id="c1d30-114">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-114">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d30-115">Tipo di struttura di informazioni restituito nel buffer *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="c1d30-115">The type of information structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="c1d30-116">Può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="c1d30-116">It can be one of the following.</span></span>



| <span data-ttu-id="c1d30-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c1d30-117">Value</span></span>                                                                                                | <span data-ttu-id="c1d30-118">Significato</span><span class="sxs-lookup"><span data-stu-id="c1d30-118">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c1d30-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-119"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="c1d30-120">**\_Informazioni driver \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c1d30-120">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="c1d30-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="c1d30-122">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c1d30-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="c1d30-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="c1d30-124">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="c1d30-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="c1d30-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="c1d30-126">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="c1d30-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="c1d30-127"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-127"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="c1d30-128">**\_Informazioni driver \_ 5**</span><span class="sxs-lookup"><span data-stu-id="c1d30-128">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="c1d30-129"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-129"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="c1d30-130">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="c1d30-130">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="c1d30-131"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-131"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="c1d30-132">**\_Informazioni driver \_ 8**</span><span class="sxs-lookup"><span data-stu-id="c1d30-132">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="c1d30-133">*pDriverInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-133">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d30-134">Puntatore a un buffer che riceve una matrice di strutture di \_ informazioni del driver \_ \* , come specificato dal *livello*.</span><span class="sxs-lookup"><span data-stu-id="c1d30-134">A pointer to a buffer that receives an array of DRIVER\_INFO\_\* structures, as specified by *Level*.</span></span> <span data-ttu-id="c1d30-135">Ogni struttura contiene dati che descrivono un driver della stampante disponibile.</span><span class="sxs-lookup"><span data-stu-id="c1d30-135">Each structure contains data that describes an available printer driver.</span></span> <span data-ttu-id="c1d30-136">Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture e qualsiasi stringa o altri dati a cui fanno riferimento i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="c1d30-136">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="c1d30-137">Per determinare le dimensioni del buffer richieste, chiamare **EnumPrinterDrivers** con *cbBuf* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="c1d30-137">To determine the required buffer size, call **EnumPrinterDrivers** with *cbBuf* set to zero.</span></span> <span data-ttu-id="c1d30-138">**EnumPrinterDrivers** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="c1d30-138">**EnumPrinterDrivers** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="c1d30-139">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d30-140">Dimensione, in byte, del buffer a cui punta *pDriverInfo*</span><span class="sxs-lookup"><span data-stu-id="c1d30-140">The size, in bytes, of the buffer pointed to by *pDriverInfo*</span></span>

</dd> <dt>

<span data-ttu-id="c1d30-141">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d30-142">Puntatore a una variabile che riceve il numero di byte copiati nel buffer *pDriverInfo* se la funzione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c1d30-142">A pointer to a variable that receives the number of bytes copied to the *pDriverInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="c1d30-143">Se il buffer è troppo piccolo, la funzione ha esito negativo e la variabile riceve il numero di byte necessari.</span><span class="sxs-lookup"><span data-stu-id="c1d30-143">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="c1d30-144">*pcReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-144">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d30-145">Puntatore a una variabile che riceve il numero di strutture restituite nel buffer di *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="c1d30-145">A pointer to a variable that receives the number of structures returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="c1d30-146">Il numero di driver della stampante installati nel server di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="c1d30-146">This is the number of printer drivers installed on the specified print server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d30-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1d30-147">Return value</span></span>

<span data-ttu-id="c1d30-148">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c1d30-148">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c1d30-149">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="c1d30-149">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1d30-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1d30-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1d30-151">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="c1d30-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c1d30-152">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1d30-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c1d30-153">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="c1d30-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1d30-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1d30-154">Requirements</span></span>



| <span data-ttu-id="c1d30-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1d30-155">Requirement</span></span> | <span data-ttu-id="c1d30-156">Valore</span><span class="sxs-lookup"><span data-stu-id="c1d30-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d30-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d30-157">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d30-158">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c1d30-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d30-159">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d30-160">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1d30-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c1d30-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1d30-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1d30-162"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c1d30-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="c1d30-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1d30-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c1d30-165">DLL</span><span class="sxs-lookup"><span data-stu-id="c1d30-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1d30-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c1d30-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c1d30-167">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c1d30-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c1d30-168">**EnumPrinterDriversW** (Unicode) e **EnumPrinterDriversA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c1d30-168">**EnumPrinterDriversW** (Unicode) and **EnumPrinterDriversA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="c1d30-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1d30-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d30-170">Stampa</span><span class="sxs-lookup"><span data-stu-id="c1d30-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c1d30-171">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="c1d30-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c1d30-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="c1d30-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="c1d30-173">**\_Informazioni driver \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c1d30-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="c1d30-174">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c1d30-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="c1d30-175">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="c1d30-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="c1d30-176">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="c1d30-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="c1d30-177">**\_Informazioni driver \_ 5**</span><span class="sxs-lookup"><span data-stu-id="c1d30-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="c1d30-178">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="c1d30-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="c1d30-179">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="c1d30-179">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

