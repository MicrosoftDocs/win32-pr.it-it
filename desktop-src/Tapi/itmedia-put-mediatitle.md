---
description: Il \_ metodo Put MediaTitle imposta un titolo testuale per i supporti che l'applicazione può usare a scopo informativo o di visualizzazione. Se il set di caratteri è ASCII, deve essere una stringa convertibile ASCII. In caso contrario, può essere qualsiasi stringa BSTR.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: 'ITMedia: metodo:p ut_MediaTitle (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326238"
---
# <a name="itmediaput_mediatitle-method"></a><span data-ttu-id="d066f-105">ITMedia::p UT \_ MediaTitle metodo</span><span class="sxs-lookup"><span data-stu-id="d066f-105">ITMedia::put\_MediaTitle method</span></span>

<span data-ttu-id="d066f-106">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d066f-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d066f-107">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d066f-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d066f-108">Il metodo **put \_ MediaTitle** imposta un titolo testuale per i supporti che l'applicazione può usare a scopo informativo o di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d066f-108">The **put\_MediaTitle** method sets a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="d066f-109">Se il set di caratteri è ASCII, deve essere una stringa convertibile ASCII.</span><span class="sxs-lookup"><span data-stu-id="d066f-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="d066f-110">In caso contrario, può essere qualsiasi stringa **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="d066f-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d066f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d066f-111">Syntax</span></span>


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="d066f-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="d066f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d066f-113">*pMediaTitle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d066f-113">*pMediaTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d066f-114">Puntatore a un **BSTR** che contiene il titolo del supporto.</span><span class="sxs-lookup"><span data-stu-id="d066f-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d066f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d066f-115">Return value</span></span>

<span data-ttu-id="d066f-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d066f-116">This method can return one of these values.</span></span>



| <span data-ttu-id="d066f-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d066f-117">Return code</span></span>                                                                                   | <span data-ttu-id="d066f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d066f-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d066f-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d066f-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d066f-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d066f-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d066f-122">Il parametro *pMediaTitle* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="d066f-122">The *pMediaTitle* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="d066f-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d066f-124">Il parametro *pMediaTitle* non è valido.</span><span class="sxs-lookup"><span data-stu-id="d066f-124">The *pMediaTitle* parameter is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="d066f-125"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d066f-126">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d066f-126">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d066f-127"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-127"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d066f-128">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="d066f-128">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d066f-129"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-129"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d066f-130">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="d066f-130">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="d066f-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="d066f-131">Remarks</span></span>

<span data-ttu-id="d066f-132">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PMediaTitle* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="d066f-132">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaTitle* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="d066f-133">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="d066f-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="d066f-134">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d066f-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d066f-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d066f-135">Requirements</span></span>



| <span data-ttu-id="d066f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d066f-136">Requirement</span></span> | <span data-ttu-id="d066f-137">Valore</span><span class="sxs-lookup"><span data-stu-id="d066f-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d066f-138">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d066f-138">TAPI version</span></span><br/> | <span data-ttu-id="d066f-139">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d066f-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d066f-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d066f-140">Header</span></span><br/>       | <dl> <span data-ttu-id="d066f-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d066f-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="d066f-142">Library</span></span><br/>      | <dl> <span data-ttu-id="d066f-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d066f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d066f-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="d066f-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d066f-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d066f-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d066f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d066f-147">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="d066f-147">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="d066f-148">**ITMedia:: Get \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="d066f-148">**ITMedia::get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)
</dt> </dl>

 

