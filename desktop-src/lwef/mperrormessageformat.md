---
title: Funzione MpErrorMessageFormat (MpClient. h)
description: Restituisce un messaggio di errore formattato basato su un codice di errore.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpErrorMessageFormat
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964797"
---
# <a name="mperrormessageformat-function"></a><span data-ttu-id="a45a4-104">MpErrorMessageFormat (funzione)</span><span class="sxs-lookup"><span data-stu-id="a45a4-104">MpErrorMessageFormat function</span></span>

<span data-ttu-id="a45a4-105">Restituisce un messaggio di errore formattato basato su un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="a45a4-105">Returns a formatted error message based on an error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a45a4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a45a4-106">Syntax</span></span>


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a45a4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a45a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a45a4-108">*hMpHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a45a4-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a45a4-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="a45a4-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="a45a4-110">Handle per l'interfaccia di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="a45a4-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="a45a4-111">Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="a45a4-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a45a4-112">*hrError* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a45a4-112">*hrError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a45a4-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a45a4-113">Type: **HRESULT**</span></span>

<span data-ttu-id="a45a4-114">Codice di errore basato su **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a45a4-114">An **HRESULT**-based error code.</span></span>

</dd> <dt>

<span data-ttu-id="a45a4-115">*pwszErrorDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a45a4-115">*pwszErrorDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a45a4-116">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="a45a4-116">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="a45a4-117">Restituisce un messaggio di errore formattato basato su _hrError \*.</span><span class="sxs-lookup"><span data-stu-id="a45a4-117">Returns a formatted error message based on _hrError\*.</span></span> <span data-ttu-id="a45a4-118">Questa stringa deve essere liberata usando [**MpFreeMemory**](mpfreememory.md).</span><span class="sxs-lookup"><span data-stu-id="a45a4-118">This string must be freed using [**MpFreeMemory**](mpfreememory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a45a4-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a45a4-119">Return value</span></span>

<span data-ttu-id="a45a4-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a45a4-120">Type: **HRESULT**</span></span>

<span data-ttu-id="a45a4-121">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a45a4-121">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="a45a4-122">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="a45a4-122">If the function fails then the return value is a failed **HRESULT** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a45a4-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a45a4-123">Remarks</span></span>

<span data-ttu-id="a45a4-124">Questa funzione è in grado di formattare i codici di errore di sistema oltre a codici di errore specifici restituiti dalle funzioni di malware Protection.</span><span class="sxs-lookup"><span data-stu-id="a45a4-124">This function is capable of formatting system error codes in addition to specific error codes returned by malware protection functions.</span></span> <span data-ttu-id="a45a4-125">I codici di errore **HRESULT** specifici per le funzioni di malware Protection hanno una struttura di 0x50.</span><span class="sxs-lookup"><span data-stu-id="a45a4-125">The **HRESULT** error codes specific to malware protection functions have a facility of 0x50.</span></span> <span data-ttu-id="a45a4-126">Di seguito è riportato un elenco di un subset di codici di errore specifici di malware Protection che possono essere restituiti da varie funzioni di malware Protection.</span><span class="sxs-lookup"><span data-stu-id="a45a4-126">Below is a list of a subset of the malware protection-specific error codes that can be returned by various malware protection functions.</span></span> <span data-ttu-id="a45a4-127">Utilizzando la macro **HRESULT \_ dallo \_ \_ stato MP**, i codici di errore seguenti possono essere convertiti in **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a45a4-127">Using the macro **HRESULT\_FROM\_MP\_STATUS**, the following error codes can be converted to **HRESULT**.</span></span> <span data-ttu-id="a45a4-128">Vedere anche [codici di errore del motore anti-malware di Forefront Client Security](https://support.microsoft.com/kb/939359) per un elenco di altri possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="a45a4-128">See also [Forefront Client Security anti-malware engine error codes](https://support.microsoft.com/kb/939359) for a list of other possible error codes.</span></span>



| <span data-ttu-id="a45a4-129">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="a45a4-129">Error Code</span></span>                              | <span data-ttu-id="a45a4-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a45a4-130">Description</span></span>                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a45a4-131">ERRORE \_ MP \_ noengine</span><span class="sxs-lookup"><span data-stu-id="a45a4-131">ERROR\_MP\_NOENGINE</span></span>                     | <span data-ttu-id="a45a4-132">Nessun motore è caricato nel servizio antimalware per eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="a45a4-132">No engine is loaded in antimalware service to perform the requested operation.</span></span>                                              |
| <span data-ttu-id="a45a4-133">ERRORE \_ MP \_ Nessuna \_ memoria</span><span class="sxs-lookup"><span data-stu-id="a45a4-133">ERROR\_MP\_NO\_MEMORY</span></span>                   | <span data-ttu-id="a45a4-134">Il motore antimalware ha rilevato una situazione di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a45a4-134">The antimalware engine has encountered a no memory situation.</span></span>                                                               |
| <span data-ttu-id="a45a4-135">ERRORE \_ \_ rimozione MP \_ non riuscita</span><span class="sxs-lookup"><span data-stu-id="a45a4-135">ERROR\_MP\_REMOVE\_FAILED</span></span>               | <span data-ttu-id="a45a4-136">Operazione di rimozione non riuscita per una minaccia specifica.</span><span class="sxs-lookup"><span data-stu-id="a45a4-136">Remove operation failed for a specific threat.</span></span>                                                                              |
| <span data-ttu-id="a45a4-137">ERRORE \_ \_ quarantena MP \_ non riuscita</span><span class="sxs-lookup"><span data-stu-id="a45a4-137">ERROR\_MP\_QUARANTINE\_FAILED</span></span>           | <span data-ttu-id="a45a4-138">Operazione di quarantena non riuscita per una minaccia specifica.</span><span class="sxs-lookup"><span data-stu-id="a45a4-138">Quarantine operation failed for a specific threat.</span></span>                                                                          |
| <span data-ttu-id="a45a4-139">rischio di errore \_ MP \_ \_ non \_ trovato</span><span class="sxs-lookup"><span data-stu-id="a45a4-139">ERROR\_MP\_THREAT\_NOT\_FOUND</span></span>           | <span data-ttu-id="a45a4-140">La minaccia specifica non esiste più nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a45a4-140">The specific threat no longer exists in the system.</span></span>                                                                         |
| <span data-ttu-id="a45a4-141">ERRORE \_ di \_ rimozione MP \_ non \_ supportata</span><span class="sxs-lookup"><span data-stu-id="a45a4-141">ERROR\_MP\_REMOVE\_NOT\_SUPPORTED</span></span>       | <span data-ttu-id="a45a4-142">L'operazione di rimozione per una minaccia specifica all'interno del tipo di contenitore non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a45a4-142">Remove operation for a specific threat inside the container type is not supported.</span></span>                                          |
| <span data-ttu-id="a45a4-143">ERRORE \_ MP \_ rimozione del \_ contenitore non modificabile \_</span><span class="sxs-lookup"><span data-stu-id="a45a4-143">ERROR\_MP\_REMOVE\_IMMUTABLE\_CONTAINER</span></span> | <span data-ttu-id="a45a4-144">A causa dei criteri del motore, un'operazione di rimozione di una minaccia specifica all'interno di un contenitore bloccato non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a45a4-144">Due to engine policy, a remove operation of a specific threat inside a blocked container is not supported.</span></span> <span data-ttu-id="a45a4-145">(Archivi di posta elettronica).</span><span class="sxs-lookup"><span data-stu-id="a45a4-145">(Mail archives.)</span></span> |
| <span data-ttu-id="a45a4-146">ERRORE \_ MP \_ BADDB \_ OLDENGINE</span><span class="sxs-lookup"><span data-stu-id="a45a4-146">ERROR\_MP\_BADDB\_OLDENGINE</span></span>             | <span data-ttu-id="a45a4-147">La richiesta di aggiornamento della firma ha fornito un motore o uno o più file di firma meno recenti.</span><span class="sxs-lookup"><span data-stu-id="a45a4-147">Signature update request provided an older engine or signature files(s).</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="a45a4-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a45a4-148">Requirements</span></span>



| <span data-ttu-id="a45a4-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="a45a4-149">Requirement</span></span> | <span data-ttu-id="a45a4-150">Valore</span><span class="sxs-lookup"><span data-stu-id="a45a4-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a45a4-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a45a4-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a45a4-152">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a45a4-152">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a45a4-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a45a4-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a45a4-154">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a45a4-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a45a4-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a45a4-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="a45a4-156"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a45a4-156"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a45a4-157">DLL</span><span class="sxs-lookup"><span data-stu-id="a45a4-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a45a4-158"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a45a4-158"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a45a4-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a45a4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a45a4-160">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="a45a4-160">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="a45a4-161">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="a45a4-161">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="a45a4-162">Codici di errore del motore anti-malware di Forefront Client Security</span><span class="sxs-lookup"><span data-stu-id="a45a4-162">Forefront Client Security anti-malware engine error codes</span></span>](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





