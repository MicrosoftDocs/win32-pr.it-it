---
description: La funzione EnumPorts enumera le porte disponibili per la stampa in un server specificato.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Funzione EnumPorts (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314996"
---
# <a name="enumports-function"></a><span data-ttu-id="9557a-103">EnumPorts (funzione)</span><span class="sxs-lookup"><span data-stu-id="9557a-103">EnumPorts function</span></span>

<span data-ttu-id="9557a-104">La funzione **EnumPorts** enumera le porte disponibili per la stampa in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="9557a-104">The **EnumPorts** function enumerates the ports that are available for printing on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9557a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9557a-105">Syntax</span></span>


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="9557a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9557a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9557a-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9557a-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9557a-108">Puntatore a una stringa con terminazione null che specifica il nome del server di cui si desidera enumerare le porte di stampa.</span><span class="sxs-lookup"><span data-stu-id="9557a-108">A pointer to a null-terminated string that specifies the name of the server whose printer ports you want to enumerate.</span></span>

<span data-ttu-id="9557a-109">Se *pname* è **null**, la funzione enumera le porte della stampante del computer locale.</span><span class="sxs-lookup"><span data-stu-id="9557a-109">If *pName* is **NULL**, the function enumerates the local machine's printer ports.</span></span>

</dd> <dt>

<span data-ttu-id="9557a-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9557a-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9557a-111">Tipo di informazioni restituite nel buffer di *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="9557a-111">The type of information returned in the *pPorts* buffer.</span></span> <span data-ttu-id="9557a-112">Se *Level* è 1, *pPorts* riceve una matrice di strutture di [**Port \_ info \_ 1**](port-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="9557a-112">If *Level* is 1, *pPorts* receives an array of [**PORT\_INFO\_1**](port-info-1.md) structures.</span></span> <span data-ttu-id="9557a-113">Se *Level* è 2, *pPorts* riceve una matrice di strutture [**Port \_ info \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="9557a-113">If *Level* is 2, *pPorts* receives an array of [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="9557a-114">*pPorts* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9557a-114">*pPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9557a-115">Puntatore a un buffer che riceve una matrice di strutture delle informazioni di porta [**\_ \_ 1**](port-info-1.md) o della [**porta \_ \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="9557a-115">A pointer to a buffer that receives an array of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span> <span data-ttu-id="9557a-116">Ogni struttura contiene dati che descrivono una porta stampante disponibile.</span><span class="sxs-lookup"><span data-stu-id="9557a-116">Each structure contains data that describes an available printer port.</span></span> <span data-ttu-id="9557a-117">Il buffer deve essere sufficientemente grande da archiviare le stringhe a cui puntano i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="9557a-117">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="9557a-118">Per determinare le dimensioni del buffer richieste, chiamare **EnumPorts** con *cbBuf* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="9557a-118">To determine the required buffer size, call **EnumPorts** with *cbBuf* set to zero.</span></span> <span data-ttu-id="9557a-119">**EnumPorts** ha esito negativo, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ buffer insufficiente \_ e il parametro *pcbNeeded* restituisce la dimensione, in byte, del buffer necessario per memorizzare la matrice di strutture e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="9557a-119">**EnumPorts** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="9557a-120">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9557a-120">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9557a-121">Dimensione, in byte, del buffer a cui punta *pPorts*.</span><span class="sxs-lookup"><span data-stu-id="9557a-121">The size, in bytes, of the buffer pointed to by *pPorts*.</span></span>

</dd> <dt>

<span data-ttu-id="9557a-122">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9557a-122">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9557a-123">Puntatore a una variabile che riceve il numero di byte copiati nel buffer di *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="9557a-123">A pointer to a variable that receives the number of bytes copied to the *pPorts* buffer.</span></span> <span data-ttu-id="9557a-124">Se il buffer è troppo piccolo, la funzione ha esito negativo e la variabile riceve il numero di byte necessari.</span><span class="sxs-lookup"><span data-stu-id="9557a-124">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="9557a-125">*pcReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9557a-125">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9557a-126">Puntatore a una variabile che riceve il numero di strutture [**Port \_ info \_ 1**](port-info-1.md) o [**Port \_ info \_ 2**](port-info-2.md) restituite nel buffer *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="9557a-126">A pointer to a variable that receives the number of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures returned in the *pPorts* buffer.</span></span> <span data-ttu-id="9557a-127">Il numero di porte della stampante disponibili sul server specificato.</span><span class="sxs-lookup"><span data-stu-id="9557a-127">This is the number of printer ports that are available on the specified server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9557a-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9557a-128">Return value</span></span>

<span data-ttu-id="9557a-129">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="9557a-129">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9557a-130">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="9557a-130">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9557a-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="9557a-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9557a-132">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="9557a-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9557a-133">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9557a-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9557a-134">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="9557a-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9557a-135">La funzione **EnumPorts** può avere esito positivo anche se per il server specificato da *pname* non è stata definita una stampante.</span><span class="sxs-lookup"><span data-stu-id="9557a-135">The **EnumPorts** function can succeed even if the server specified by *pName* does not have a printer defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="9557a-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9557a-136">Requirements</span></span>



| <span data-ttu-id="9557a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9557a-137">Requirement</span></span> | <span data-ttu-id="9557a-138">Valore</span><span class="sxs-lookup"><span data-stu-id="9557a-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9557a-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9557a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9557a-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9557a-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9557a-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9557a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9557a-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9557a-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9557a-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9557a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9557a-144"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9557a-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9557a-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="9557a-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="9557a-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9557a-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9557a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9557a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9557a-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9557a-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9557a-149">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9557a-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9557a-150">**EnumPortsW** (Unicode) e **EnumPortsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9557a-150">**EnumPortsW** (Unicode) and **EnumPortsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="9557a-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9557a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9557a-152">Stampa</span><span class="sxs-lookup"><span data-stu-id="9557a-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9557a-153">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="9557a-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9557a-154">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="9557a-154">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="9557a-155">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="9557a-155">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="9557a-156">**\_Informazioni porta \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9557a-156">**PORT\_INFO\_1**</span></span>](port-info-1.md)
</dt> <dt>

[<span data-ttu-id="9557a-157">**Informazioni sulla porta \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9557a-157">**PORT\_INFO\_2**</span></span>](port-info-2.md)
</dt> </dl>

 

