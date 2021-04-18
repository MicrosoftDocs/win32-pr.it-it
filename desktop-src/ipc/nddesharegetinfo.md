---
description: Recupera le informazioni sulla condivisione DDE. Questa operazione viene in genere eseguita per la modifica.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Funzione NDdeShareGetInfo (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305710"
---
# <a name="nddesharegetinfo-function"></a><span data-ttu-id="6a31e-104">NDdeShareGetInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="6a31e-104">NDdeShareGetInfo function</span></span>

<span data-ttu-id="6a31e-105">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="6a31e-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="6a31e-106">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="6a31e-107">Recupera le informazioni sulla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="6a31e-107">Retrieves DDE share information.</span></span> <span data-ttu-id="6a31e-108">Questa operazione viene in genere eseguita per la modifica.</span><span class="sxs-lookup"><span data-stu-id="6a31e-108">This is usually done for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a31e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a31e-109">Syntax</span></span>


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a><span data-ttu-id="6a31e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a31e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a31e-111">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a31e-112">Nome del server in cui risiede l'DSDM.</span><span class="sxs-lookup"><span data-stu-id="6a31e-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="6a31e-113">*lpszShareName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a31e-114">Nome della condivisione le cui informazioni devono essere recuperate da DSDM.</span><span class="sxs-lookup"><span data-stu-id="6a31e-114">The share name whose information is to be retrieved from the DSDM.</span></span> <span data-ttu-id="6a31e-115">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6a31e-115">This parameter must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a31e-116">*nLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a31e-117">Livello di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6a31e-117">The information level.</span></span> <span data-ttu-id="6a31e-118">Questo parametro deve essere 2.</span><span class="sxs-lookup"><span data-stu-id="6a31e-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="6a31e-119">*lpBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-119">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a31e-120">Puntatore a un buffer che riceve la struttura [**NDDESHAREINFO**](nddeshareinfo-str.md) e i dati associati a cui puntano i relativi membri.</span><span class="sxs-lookup"><span data-stu-id="6a31e-120">A pointer to a buffer that receives the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure and associated data pointed to by its members.</span></span> <span data-ttu-id="6a31e-121">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6a31e-121">This parameter can be **NULL**.</span></span> <span data-ttu-id="6a31e-122">Se *lpBuffer* è **null**, DSDM calcola il numero di byte necessari per archiviare le informazioni di condivisione richieste e restituisce tale valore nel campo *lpnTotalAvailable* insieme all' \_ errore NDDE BUF \_ troppo \_ piccolo.</span><span class="sxs-lookup"><span data-stu-id="6a31e-122">If *lpBuffer* is **NULL**, then the DSDM calculates the number of bytes required to store the requested share information and returns that value in the *lpnTotalAvailable* field along with the NDDE\_BUF\_TOO\_SMALL error.</span></span>

</dd> <dt>

<span data-ttu-id="6a31e-123">*cBufSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a31e-124">Dimensioni in byte del buffer *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="6a31e-124">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="6a31e-125">Se *lpBuffer* è **null**, *cBufSize* deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6a31e-125">If *lpBuffer* is **NULL**, then *cBufSize* should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6a31e-126">*lpnTotalAvailable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-126">*lpnTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a31e-127">Puntatore a una variabile che riceve il numero totale di byte necessari per archiviare le informazioni di condivisione richieste.</span><span class="sxs-lookup"><span data-stu-id="6a31e-127">A pointer to a variable that receives the total number of bytes needed to store the requested share information.</span></span> <span data-ttu-id="6a31e-128">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6a31e-128">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a31e-129">*lpnItems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-129">*lpnItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a31e-130">Puntatore a una maschera di selezione dell'elemento per il recupero parziale delle informazioni sulla condivisione.</span><span class="sxs-lookup"><span data-stu-id="6a31e-130">A pointer to an item selection mask for partial share information retrieval.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a31e-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a31e-131">Return value</span></span>

<span data-ttu-id="6a31e-132">Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="6a31e-132">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="6a31e-133">Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="6a31e-133">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="6a31e-134">Se il parametro *lpBuffer* è **null**, restituisce NDDE \_ BUF \_ troppo \_ piccolo.</span><span class="sxs-lookup"><span data-stu-id="6a31e-134">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a31e-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a31e-135">Requirements</span></span>



| <span data-ttu-id="6a31e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a31e-136">Requirement</span></span> | <span data-ttu-id="6a31e-137">Valore</span><span class="sxs-lookup"><span data-stu-id="6a31e-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a31e-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a31e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6a31e-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6a31e-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a31e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6a31e-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a31e-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6a31e-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a31e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a31e-143"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a31e-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a31e-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a31e-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a31e-145"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a31e-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6a31e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6a31e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a31e-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a31e-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="6a31e-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6a31e-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6a31e-149">**NDdeShareGetInfoW** (Unicode) e **NDdeShareGetInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6a31e-149">**NDdeShareGetInfoW** (Unicode) and **NDdeShareGetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6a31e-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a31e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a31e-151">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="6a31e-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="6a31e-152">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="6a31e-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="6a31e-153">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="6a31e-153">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="6a31e-154">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="6a31e-154">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> </dl>

 

 




