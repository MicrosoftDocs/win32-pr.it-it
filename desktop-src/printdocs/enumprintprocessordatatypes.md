---
description: La funzione EnumPrintProcessorDatatypes enumera i tipi di dati supportati da un processore di stampa specificato.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: Funzione EnumPrintProcessorDatatypes (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528999"
---
# <a name="enumprintprocessordatatypes-function"></a><span data-ttu-id="57cb6-103">EnumPrintProcessorDatatypes (funzione)</span><span class="sxs-lookup"><span data-stu-id="57cb6-103">EnumPrintProcessorDatatypes function</span></span>

<span data-ttu-id="57cb6-104">La funzione **EnumPrintProcessorDatatypes** enumera i tipi di dati supportati da un processore di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="57cb6-104">The **EnumPrintProcessorDatatypes** function enumerates the data types that a specified print processor supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="57cb6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57cb6-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="57cb6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="57cb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57cb6-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57cb6-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cb6-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui risiede il processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="57cb6-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor resides.</span></span> <span data-ttu-id="57cb6-109">Se questo parametro è **null**, vengono enumerati i tipi di dati per il processore di stampa locale.</span><span class="sxs-lookup"><span data-stu-id="57cb6-109">If this parameter is **NULL**, the data types for the local print processor are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="57cb6-110">*pPrintProcessorName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57cb6-110">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cb6-111">Puntatore a una stringa con terminazione null che specifica il nome del processore di stampa i cui tipi di dati sono enumerati.</span><span class="sxs-lookup"><span data-stu-id="57cb6-111">A pointer to a null-terminated string that specifies the name of the print processor whose data types are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="57cb6-112">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="57cb6-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cb6-113">Tipo di informazioni restituite nel buffer di *pDatatypes* .</span><span class="sxs-lookup"><span data-stu-id="57cb6-113">The type of information returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="57cb6-114">Questo parametro deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="57cb6-114">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="57cb6-115">*pDatatypes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57cb6-115">*pDatatypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57cb6-116">Puntatore a un buffer che riceve una matrice di strutture di [**tipo \_ info \_ 1**](datatypes-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="57cb6-116">A pointer to a buffer that receives an array of [**DATATYPES\_INFO\_1**](datatypes-info-1.md) structures.</span></span> <span data-ttu-id="57cb6-117">Ogni struttura descrive un tipo di dati disponibile.</span><span class="sxs-lookup"><span data-stu-id="57cb6-117">Each structure describes an available data type.</span></span> <span data-ttu-id="57cb6-118">Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture e qualsiasi stringa o altri dati a cui fanno riferimento i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="57cb6-118">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="57cb6-119">Per determinare le dimensioni del buffer richieste, chiamare **EnumPrintProcessorDatatypes** con *cbBuf* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="57cb6-119">To determine the required buffer size, call **EnumPrintProcessorDatatypes** with *cbBuf* set to zero.</span></span> <span data-ttu-id="57cb6-120">**EnumPrintProcessorDatatypes** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="57cb6-120">**EnumPrintProcessorDatatypes** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="57cb6-121">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57cb6-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cb6-122">Dimensione, in byte, del buffer a cui punta *pDatatypes*.</span><span class="sxs-lookup"><span data-stu-id="57cb6-122">The size, in bytes, of the buffer pointed to by *pDatatypes*.</span></span>

</dd> <dt>

<span data-ttu-id="57cb6-123">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57cb6-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57cb6-124">Puntatore a una variabile che riceve il numero di byte copiati nel buffer *pDatatypes* se la funzione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="57cb6-124">A pointer to a variable that receives the number of bytes copied to the *pDatatypes* buffer if the function succeeds.</span></span> <span data-ttu-id="57cb6-125">Se il buffer è troppo piccolo, la funzione ha esito negativo e la variabile riceve il numero di byte necessari.</span><span class="sxs-lookup"><span data-stu-id="57cb6-125">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="57cb6-126">*pcReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57cb6-126">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57cb6-127">Puntatore a una variabile che riceve il numero di strutture restituite nel buffer di *pDatatypes* .</span><span class="sxs-lookup"><span data-stu-id="57cb6-127">A pointer to a variable that receives the number of structures returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="57cb6-128">Il numero dei tipi di dati supportati.</span><span class="sxs-lookup"><span data-stu-id="57cb6-128">This is the number of supported data types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57cb6-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57cb6-129">Return value</span></span>

<span data-ttu-id="57cb6-130">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="57cb6-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="57cb6-131">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="57cb6-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="57cb6-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="57cb6-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="57cb6-133">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="57cb6-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="57cb6-134">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="57cb6-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="57cb6-135">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="57cb6-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="57cb6-136">v</span><span class="sxs-lookup"><span data-stu-id="57cb6-136">v</span></span>

<span data-ttu-id="57cb6-137">A partire da Windows Vista, le informazioni sul tipo di dati dei server di stampa remoti vengono recuperate da una cache locale.</span><span class="sxs-lookup"><span data-stu-id="57cb6-137">Starting with Windows Vista, the data type information from remote print servers is retrieved from a local cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="57cb6-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57cb6-138">Requirements</span></span>



| <span data-ttu-id="57cb6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="57cb6-139">Requirement</span></span> | <span data-ttu-id="57cb6-140">Valore</span><span class="sxs-lookup"><span data-stu-id="57cb6-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57cb6-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cb6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="57cb6-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57cb6-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="57cb6-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cb6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="57cb6-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57cb6-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="57cb6-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57cb6-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="57cb6-146"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57cb6-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="57cb6-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="57cb6-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="57cb6-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57cb6-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="57cb6-149">DLL</span><span class="sxs-lookup"><span data-stu-id="57cb6-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57cb6-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="57cb6-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="57cb6-151">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="57cb6-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="57cb6-152">**EnumPrintProcessorDatatypesW** (Unicode) e **EnumPrintProcessorDatatypesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="57cb6-152">**EnumPrintProcessorDatatypesW** (Unicode) and **EnumPrintProcessorDatatypesA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="57cb6-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57cb6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57cb6-154">Stampa</span><span class="sxs-lookup"><span data-stu-id="57cb6-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="57cb6-155">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="57cb6-155">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="57cb6-156">**TIPI di \_ dati \_ 1**</span><span class="sxs-lookup"><span data-stu-id="57cb6-156">**DATATYPES\_INFO\_1**</span></span>](datatypes-info-1.md)
</dt> <dt>

[<span data-ttu-id="57cb6-157">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="57cb6-157">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

