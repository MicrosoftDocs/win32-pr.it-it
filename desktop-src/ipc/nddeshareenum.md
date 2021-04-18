---
description: Recupera l'elenco delle condivisioni DDE disponibili.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Funzione NDdeShareEnum (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315598"
---
# <a name="nddeshareenum-function"></a><span data-ttu-id="57cdd-103">NDdeShareEnum (funzione)</span><span class="sxs-lookup"><span data-stu-id="57cdd-103">NDdeShareEnum function</span></span>

<span data-ttu-id="57cdd-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="57cdd-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="57cdd-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="57cdd-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="57cdd-106">Recupera l'elenco delle condivisioni DDE disponibili.</span><span class="sxs-lookup"><span data-stu-id="57cdd-106">Retrieves the list of available DDE shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="57cdd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57cdd-107">Syntax</span></span>


```C++
UINT NDdeShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="57cdd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="57cdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57cdd-109">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57cdd-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cdd-110">Nome del server in cui risiede l'DSDM.</span><span class="sxs-lookup"><span data-stu-id="57cdd-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="57cdd-111">*nLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57cdd-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cdd-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="57cdd-112">Reserved.</span></span> <span data-ttu-id="57cdd-113">Questo parametro deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="57cdd-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="57cdd-114">*lpBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57cdd-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57cdd-115">Puntatore a un buffer che riceve l'elenco di condivisioni DDE.</span><span class="sxs-lookup"><span data-stu-id="57cdd-115">A pointer to a buffer that receives the list of DDE shares.</span></span> <span data-ttu-id="57cdd-116">L'elenco delle condivisioni DDE viene archiviato come sequenza di stringhe separate da null che terminano con un carattere null doppio alla fine.</span><span class="sxs-lookup"><span data-stu-id="57cdd-116">The list of DDE shares is stored as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="57cdd-117">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="57cdd-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="57cdd-118">Se *lpBuffer* è **null**, DSDM restituisce la dimensione del buffer necessaria per memorizzare l'elenco di condivisioni nel parametro *lpcbTotalAvailable* .</span><span class="sxs-lookup"><span data-stu-id="57cdd-118">If *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="57cdd-119">*cBufSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57cdd-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cdd-120">Dimensioni in byte del buffer *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="57cdd-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="57cdd-121">Questo parametro deve essere zero se *lpBuffer* è **null**.</span><span class="sxs-lookup"><span data-stu-id="57cdd-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="57cdd-122">*lpnEntriesRead* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57cdd-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57cdd-123">Puntatore a una variabile che riceve il numero totale di condivisioni enumerate.</span><span class="sxs-lookup"><span data-stu-id="57cdd-123">A pointer to a variable that receives the total number of shares being enumerated.</span></span> <span data-ttu-id="57cdd-124">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="57cdd-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="57cdd-125">*lpcbTotalAvailable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57cdd-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57cdd-126">Puntatore a una variabile che riceve il numero totale di byte necessari nel buffer per archiviare l'elenco di condivisioni DDE.</span><span class="sxs-lookup"><span data-stu-id="57cdd-126">A pointer to a variable that receives the total number of bytes needed in the buffer to store the list of DDE shares.</span></span> <span data-ttu-id="57cdd-127">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="57cdd-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57cdd-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57cdd-128">Return value</span></span>

<span data-ttu-id="57cdd-129">Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="57cdd-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="57cdd-130">Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="57cdd-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="57cdd-131">Se il parametro *lpBuffer* è **null**, restituisce NDDE \_ BUF \_ troppo \_ piccolo.</span><span class="sxs-lookup"><span data-stu-id="57cdd-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="57cdd-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57cdd-132">Requirements</span></span>



| <span data-ttu-id="57cdd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="57cdd-133">Requirement</span></span> | <span data-ttu-id="57cdd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="57cdd-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57cdd-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cdd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="57cdd-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57cdd-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="57cdd-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cdd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="57cdd-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57cdd-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="57cdd-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57cdd-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="57cdd-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="57cdd-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="57cdd-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="57cdd-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="57cdd-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57cdd-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="57cdd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="57cdd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57cdd-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57cdd-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="57cdd-145">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="57cdd-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="57cdd-146">**NDdeShareEnumW** (Unicode) e **NDdeShareEnumA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="57cdd-146">**NDdeShareEnumW** (Unicode) and **NDdeShareEnumA** (ANSI)</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="57cdd-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57cdd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57cdd-148">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="57cdd-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="57cdd-149">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="57cdd-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




