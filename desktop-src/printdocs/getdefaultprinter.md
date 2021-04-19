---
description: La funzione GetDefaultPrinter Recupera il nome della stampante predefinita per l'utente corrente nel computer locale.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: Funzione GetDefaultPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311823"
---
# <a name="getdefaultprinter-function"></a><span data-ttu-id="24954-103">GetDefaultPrinter (funzione)</span><span class="sxs-lookup"><span data-stu-id="24954-103">GetDefaultPrinter function</span></span>

<span data-ttu-id="24954-104">La funzione **GetDefaultPrinter** Recupera il nome della stampante predefinita per l'utente corrente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="24954-104">The **GetDefaultPrinter** function retrieves the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="24954-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24954-105">Syntax</span></span>


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="24954-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24954-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24954-107">*pszBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24954-107">*pszBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24954-108">Puntatore a un buffer che riceve una stringa di caratteri con terminazione null contenente il nome predefinito della stampante.</span><span class="sxs-lookup"><span data-stu-id="24954-108">A pointer to a buffer that receives a null-terminated character string containing the default printer name.</span></span> <span data-ttu-id="24954-109">Se questo parametro è **null**, la funzione ha esito negativo e la variabile a cui punta *pcchBuffer* restituisce le dimensioni del buffer richieste in caratteri.</span><span class="sxs-lookup"><span data-stu-id="24954-109">If this parameter is **NULL**, the function fails and the variable pointed to by *pcchBuffer* returns the required buffer size, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="24954-110">*pcchBuffer* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="24954-110">*pcchBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="24954-111">In input, specifica la dimensione, in caratteri, del buffer *pszBuffer* .</span><span class="sxs-lookup"><span data-stu-id="24954-111">On input, specifies the size, in characters, of the *pszBuffer* buffer.</span></span> <span data-ttu-id="24954-112">Nell'output, riceve la dimensione, in caratteri, della stringa del nome della stampante, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="24954-112">On output, receives the size, in characters, of the printer name string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24954-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24954-113">Return value</span></span>

<span data-ttu-id="24954-114">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero e la variabile a cui punta *pcchBuffer* contiene il numero di caratteri copiati nel buffer *pszBuffer* , incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="24954-114">If the function succeeds, the return value is a nonzero value and the variable pointed to by *pcchBuffer* contains the number of characters copied to the *pszBuffer* buffer, including the terminating null character.</span></span>

<span data-ttu-id="24954-115">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="24954-115">If the function fails, the return value is zero.</span></span>



| <span data-ttu-id="24954-116">Valore</span><span class="sxs-lookup"><span data-stu-id="24954-116">Value</span></span>                       | <span data-ttu-id="24954-117">Significato</span><span class="sxs-lookup"><span data-stu-id="24954-117">Meaning</span></span>                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24954-118">ERRORE \_ buffer insufficiente \_</span><span class="sxs-lookup"><span data-stu-id="24954-118">ERROR\_INSUFFICIENT\_BUFFER</span></span> | <span data-ttu-id="24954-119">Il buffer *pszBuffer* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="24954-119">The *pszBuffer* buffer is too small.</span></span> <span data-ttu-id="24954-120">La variabile a cui punta *pcchBuffer* contiene le dimensioni del buffer richieste, in caratteri.</span><span class="sxs-lookup"><span data-stu-id="24954-120">The variable pointed to by *pcchBuffer* contains the required buffer size, in characters.</span></span> |
| <span data-ttu-id="24954-121">FILE di errore \_ \_ non \_ trovato</span><span class="sxs-lookup"><span data-stu-id="24954-121">ERROR\_FILE\_NOT\_FOUND</span></span>     | <span data-ttu-id="24954-122">Non è presente alcuna stampante predefinita.</span><span class="sxs-lookup"><span data-stu-id="24954-122">There is no default printer.</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="24954-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="24954-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="24954-124">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="24954-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="24954-125">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24954-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="24954-126">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="24954-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24954-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24954-127">Requirements</span></span>



| <span data-ttu-id="24954-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="24954-128">Requirement</span></span> | <span data-ttu-id="24954-129">Valore</span><span class="sxs-lookup"><span data-stu-id="24954-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24954-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24954-130">Minimum supported client</span></span><br/> | <span data-ttu-id="24954-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24954-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="24954-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24954-132">Minimum supported server</span></span><br/> | <span data-ttu-id="24954-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24954-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="24954-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24954-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="24954-135"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24954-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="24954-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="24954-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="24954-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24954-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="24954-138">DLL</span><span class="sxs-lookup"><span data-stu-id="24954-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24954-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="24954-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="24954-140">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="24954-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="24954-141">**GetDefaultPrinterW** (Unicode) e **GetDefaultPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="24954-141">**GetDefaultPrinterW** (Unicode) and **GetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="24954-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24954-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24954-143">Stampa</span><span class="sxs-lookup"><span data-stu-id="24954-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="24954-144">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="24954-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="24954-145">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="24954-145">**SetDefaultPrinter**</span></span>](setdefaultprinter.md)
</dt> </dl>

 

 




