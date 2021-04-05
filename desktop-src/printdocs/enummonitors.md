---
description: La funzione EnumMonitors recupera informazioni sui monitoraggi di porta installati nel server specificato.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Funzione EnumMonitors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756401"
---
# <a name="enummonitors-function"></a><span data-ttu-id="18638-103">EnumMonitors (funzione)</span><span class="sxs-lookup"><span data-stu-id="18638-103">EnumMonitors function</span></span>

<span data-ttu-id="18638-104">La funzione **EnumMonitors** recupera informazioni sui monitoraggi di porta installati nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="18638-104">The **EnumMonitors** function retrieves information about the port monitors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="18638-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18638-105">Syntax</span></span>


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="18638-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18638-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18638-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18638-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18638-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui risiedono i monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="18638-108">A pointer to a null-terminated string that specifies the name of the server on which the monitors reside.</span></span> <span data-ttu-id="18638-109">Se questo parametro è **null**, vengono enumerati i monitoraggi locali.</span><span class="sxs-lookup"><span data-stu-id="18638-109">If this parameter is **NULL**, the local monitors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="18638-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="18638-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18638-111">Versione della struttura a cui punta *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="18638-111">The version of the structure pointed to by *pMonitors*.</span></span>

<span data-ttu-id="18638-112">Questo valore può essere 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="18638-112">This value can be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="18638-113">*pMonitors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="18638-113">*pMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18638-114">Puntatore a un buffer che riceve una matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="18638-114">A pointer to a buffer that receives an array of structures.</span></span> <span data-ttu-id="18638-115">Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui fanno riferimento i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="18638-115">The buffer must be large enough to store the strings referenced by the structure members.</span></span>

<span data-ttu-id="18638-116">Per determinare le dimensioni del buffer richieste, chiamare **EnumMonitors** con *cbBuf* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="18638-116">To determine the required buffer size, call **EnumMonitors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="18638-117">**EnumMonitors** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="18638-117">**EnumMonitors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

<span data-ttu-id="18638-118">Il buffer riceve una matrice di strutture di [**monitoraggio \_ info \_ 1**](monitor-info-1.md) se *Level* è 1 o [**monitora le strutture \_ info \_ 2**](monitor-info-2.md) se *Level* è 2.</span><span class="sxs-lookup"><span data-stu-id="18638-118">The buffer receives an array of [**MONITOR\_INFO\_1**](monitor-info-1.md) structures if *Level* is 1, or [**MONITOR\_INFO\_2**](monitor-info-2.md) structures if *Level* is 2.</span></span>

</dd> <dt>

<span data-ttu-id="18638-119">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18638-119">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18638-120">Dimensione, in byte, del buffer a cui punta *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="18638-120">The size, in bytes, of the buffer pointed to by *pMonitors*.</span></span>

</dd> <dt>

<span data-ttu-id="18638-121">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="18638-121">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18638-122">Puntatore a una variabile che riceve il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="18638-122">A pointer to a variable that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="18638-123">*pcReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="18638-123">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18638-124">Puntatore a una variabile che riceve il numero di strutture restituite nel buffer a cui punta *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="18638-124">A pointer to a variable that receives the number of structures that were returned in the buffer pointed to by *pMonitors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18638-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18638-125">Return value</span></span>

<span data-ttu-id="18638-126">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="18638-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="18638-127">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="18638-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="18638-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="18638-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="18638-129">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="18638-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="18638-130">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18638-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="18638-131">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="18638-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18638-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18638-132">Requirements</span></span>



| <span data-ttu-id="18638-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="18638-133">Requirement</span></span> | <span data-ttu-id="18638-134">Valore</span><span class="sxs-lookup"><span data-stu-id="18638-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18638-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18638-135">Minimum supported client</span></span><br/> | <span data-ttu-id="18638-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18638-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="18638-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18638-137">Minimum supported server</span></span><br/> | <span data-ttu-id="18638-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18638-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="18638-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18638-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="18638-140"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18638-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="18638-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="18638-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="18638-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18638-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="18638-143">DLL</span><span class="sxs-lookup"><span data-stu-id="18638-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18638-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="18638-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="18638-145">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="18638-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="18638-146">**EnumMonitorsW** (Unicode) e **EnumMonitorsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="18638-146">**EnumMonitorsW** (Unicode) and **EnumMonitorsA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="18638-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18638-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18638-148">Stampa</span><span class="sxs-lookup"><span data-stu-id="18638-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="18638-149">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="18638-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="18638-150">**Informazioni di monitoraggio \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="18638-150">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> <dt>

[<span data-ttu-id="18638-151">**Informazioni sul monitoraggio \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="18638-151">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

