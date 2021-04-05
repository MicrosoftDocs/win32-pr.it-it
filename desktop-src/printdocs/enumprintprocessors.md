---
description: La funzione EnumPrintProcessors enumera i processori di stampa installati nel server specificato.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: Funzione EnumPrintProcessors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967841"
---
# <a name="enumprintprocessors-function"></a><span data-ttu-id="41c10-103">EnumPrintProcessors (funzione)</span><span class="sxs-lookup"><span data-stu-id="41c10-103">EnumPrintProcessors function</span></span>

<span data-ttu-id="41c10-104">La funzione **EnumPrintProcessors** enumera i processori di stampa installati nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="41c10-104">The **EnumPrintProcessors** function enumerates the print processors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c10-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41c10-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="41c10-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41c10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41c10-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41c10-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c10-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui risiedono i processori di stampa.</span><span class="sxs-lookup"><span data-stu-id="41c10-108">A pointer to a null-terminated string that specifies the name of the server on which the print processors reside.</span></span> <span data-ttu-id="41c10-109">Se questo parametro è **null**, vengono enumerati i processori di stampa locali.</span><span class="sxs-lookup"><span data-stu-id="41c10-109">If this parameter is **NULL**, the local print processors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="41c10-110">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41c10-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c10-111">Puntatore a una stringa con terminazione null che specifica l'ambiente (ad esempio, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="41c10-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="41c10-112">Se questo parametro è **null**, viene utilizzato l'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="41c10-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="41c10-113">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="41c10-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c10-114">Tipo di informazioni restituite nel buffer di *pPrintProcessorInfo* .</span><span class="sxs-lookup"><span data-stu-id="41c10-114">The type of information returned in the *pPrintProcessorInfo* buffer.</span></span> <span data-ttu-id="41c10-115">Questo parametro deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="41c10-115">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="41c10-116">*pPrintProcessorInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41c10-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41c10-117">Puntatore a un buffer che riceve una matrice di strutture [**PRINTPROCESSOR \_ info \_ 1**](printprocessor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="41c10-117">A pointer to a buffer that receives an array of [**PRINTPROCESSOR\_INFO\_1**](printprocessor-info-1.md) structures.</span></span> <span data-ttu-id="41c10-118">Ogni struttura descrive un processore di stampa disponibile.</span><span class="sxs-lookup"><span data-stu-id="41c10-118">Each structure describes an available print processor.</span></span> <span data-ttu-id="41c10-119">Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture e qualsiasi stringa a cui puntano i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="41c10-119">The buffer must be large enough to receive the array of structures and any strings to which the structure members point.</span></span>

<span data-ttu-id="41c10-120">Per determinare le dimensioni del buffer richieste, chiamare **EnumPrintProcessors** con *cbBuf* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="41c10-120">To determine the required buffer size, call **EnumPrintProcessors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="41c10-121">**EnumPrintProcessors** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="41c10-121">**EnumPrintProcessors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="41c10-122">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41c10-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c10-123">Dimensione, in byte, del buffer a cui punta *pPrintProcessorInfo*.</span><span class="sxs-lookup"><span data-stu-id="41c10-123">The size, in bytes, of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="41c10-124">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41c10-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41c10-125">Puntatore a una variabile che riceve il numero di byte copiati nel buffer *pPrintProcessorInfo* se la funzione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="41c10-125">A pointer to a variable that receives the number of bytes copied to the *pPrintProcessorInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="41c10-126">Se il buffer è troppo piccolo, la funzione ha esito negativo e la variabile riceve il numero di byte necessari.</span><span class="sxs-lookup"><span data-stu-id="41c10-126">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="41c10-127">*pcReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41c10-127">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41c10-128">Puntatore a una variabile che riceve il numero di strutture restituite nel buffer di *pPrintProcessorInfo* .</span><span class="sxs-lookup"><span data-stu-id="41c10-128">A pointer to a variable that receives the number of structures returned in the *pPrintProcessorInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41c10-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41c10-129">Return value</span></span>

<span data-ttu-id="41c10-130">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="41c10-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="41c10-131">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="41c10-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="41c10-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="41c10-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="41c10-133">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="41c10-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="41c10-134">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="41c10-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="41c10-135">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="41c10-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41c10-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41c10-136">Requirements</span></span>



| <span data-ttu-id="41c10-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c10-137">Requirement</span></span> | <span data-ttu-id="41c10-138">Valore</span><span class="sxs-lookup"><span data-stu-id="41c10-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c10-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c10-139">Minimum supported client</span></span><br/> | <span data-ttu-id="41c10-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41c10-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="41c10-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c10-141">Minimum supported server</span></span><br/> | <span data-ttu-id="41c10-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41c10-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="41c10-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41c10-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c10-144"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41c10-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="41c10-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="41c10-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="41c10-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41c10-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="41c10-147">DLL</span><span class="sxs-lookup"><span data-stu-id="41c10-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c10-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="41c10-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="41c10-149">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="41c10-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="41c10-150">**EnumPrintProcessorsW** (Unicode) e **EnumPrintProcessorsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="41c10-150">**EnumPrintProcessorsW** (Unicode) and **EnumPrintProcessorsA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="41c10-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41c10-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c10-152">Stampa</span><span class="sxs-lookup"><span data-stu-id="41c10-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="41c10-153">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="41c10-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="41c10-154">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="41c10-154">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> <dt>

[<span data-ttu-id="41c10-155">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="41c10-155">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="41c10-156">**PRINTPROCESSOR \_ info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="41c10-156">**PRINTPROCESSOR\_INFO\_1**</span></span>](printprocessor-info-1.md)
</dt> </dl>

 

