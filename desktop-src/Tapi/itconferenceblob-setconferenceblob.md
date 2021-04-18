---
description: Il metodo SetConferenceBlob consente di eseguire il commit delle modifiche apportate al BLOB della conferenza. Per inizializzare il BLOB della conferenza per la prima volta, usare invece il metodo init.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'Metodo ITConferenceBlob:: SetConferenceBlob (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328230"
---
# <a name="itconferenceblobsetconferenceblob-method"></a><span data-ttu-id="d4472-104">Metodo ITConferenceBlob:: SetConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="d4472-104">ITConferenceBlob::SetConferenceBlob method</span></span>

<span data-ttu-id="d4472-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d4472-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d4472-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d4472-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d4472-107">Il metodo **SetConferenceBlob** consente di eseguire il commit delle modifiche apportate al BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="d4472-107">The **SetConferenceBlob** method commits changes to the conference blob.</span></span> <span data-ttu-id="d4472-108">Per inizializzare il BLOB della conferenza per la prima volta, usare invece il metodo [**init**](itconferenceblob-init.md) .</span><span class="sxs-lookup"><span data-stu-id="d4472-108">To initialize the conference blob for the first time, use the [**Init**](itconferenceblob-init.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4472-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4472-109">Syntax</span></span>


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="d4472-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4472-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4472-111">*Carattere* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4472-111">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4472-112">[**BLOB \_ \_**](blob-character-set.md) Descrittore del set di caratteri del set di caratteri del BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="d4472-112">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the conference blob's character set.</span></span>

</dd> <dt>

<span data-ttu-id="d4472-113">*pBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4472-113">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4472-114">Puntatore a un **BSTR** che contiene il BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="d4472-114">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4472-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4472-115">Return value</span></span>

<span data-ttu-id="d4472-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d4472-116">This method can return one of these values.</span></span>



| <span data-ttu-id="d4472-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d4472-117">Return code</span></span>                                                                                   | <span data-ttu-id="d4472-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4472-118">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4472-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d4472-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d4472-120">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d4472-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d4472-122">Il parametro *charactert* o *pBlob* non è valido.</span><span class="sxs-lookup"><span data-stu-id="d4472-122">The *CharacterSet* or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="d4472-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d4472-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d4472-124">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="d4472-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d4472-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="d4472-126">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d4472-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d4472-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="d4472-128">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="d4472-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4472-129">Remarks</span></span>

<span data-ttu-id="d4472-130">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PBlob* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="d4472-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pBlob* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4472-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4472-131">Requirements</span></span>



| <span data-ttu-id="d4472-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4472-132">Requirement</span></span> | <span data-ttu-id="d4472-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d4472-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4472-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d4472-134">TAPI version</span></span><br/> | <span data-ttu-id="d4472-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d4472-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d4472-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4472-136">Header</span></span><br/>       | <dl> <span data-ttu-id="d4472-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4472-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4472-138">Library</span></span><br/>      | <dl> <span data-ttu-id="d4472-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d4472-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d4472-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="d4472-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4472-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4472-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4472-143">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="d4472-143">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="d4472-144">**\_set di caratteri BLOB \_**</span><span class="sxs-lookup"><span data-stu-id="d4472-144">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

