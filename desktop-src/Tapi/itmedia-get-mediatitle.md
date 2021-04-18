---
description: Il \_ metodo Get MediaTitle recupera un titolo testuale per i supporti che l'applicazione può usare a scopo informativo o di visualizzazione. Se il set di caratteri è ASCII, deve essere una stringa convertibile ASCII. In caso contrario, può essere qualsiasi stringa BSTR.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'Metodo ITMedia:: get_MediaTitle (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327993"
---
# <a name="itmediaget_mediatitle-method"></a><span data-ttu-id="920c1-105">Metodo ITMedia:: Get \_ MediaTitle</span><span class="sxs-lookup"><span data-stu-id="920c1-105">ITMedia::get\_MediaTitle method</span></span>

<span data-ttu-id="920c1-106">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="920c1-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="920c1-107">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="920c1-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="920c1-108">Il metodo **get \_ MediaTitle** recupera un titolo testuale per i supporti che l'applicazione può usare a scopo informativo o di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="920c1-108">The **get\_MediaTitle** method retrieves a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="920c1-109">Se il set di caratteri è ASCII, deve essere una stringa convertibile ASCII.</span><span class="sxs-lookup"><span data-stu-id="920c1-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="920c1-110">In caso contrario, può essere qualsiasi stringa **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="920c1-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="920c1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="920c1-111">Syntax</span></span>


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="920c1-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="920c1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="920c1-113">*ppMediaTitle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="920c1-113">*ppMediaTitle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="920c1-114">Puntatore a un **BSTR** che contiene il titolo del supporto.</span><span class="sxs-lookup"><span data-stu-id="920c1-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="920c1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="920c1-115">Return value</span></span>

<span data-ttu-id="920c1-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="920c1-116">This method can return one of these values.</span></span>



| <span data-ttu-id="920c1-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="920c1-117">Return code</span></span>                                                                                   | <span data-ttu-id="920c1-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="920c1-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="920c1-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="920c1-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="920c1-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="920c1-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="920c1-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="920c1-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="920c1-122">Il parametro *ppMediaTitle* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="920c1-122">The *ppMediaTitle* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="920c1-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="920c1-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="920c1-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="920c1-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="920c1-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="920c1-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="920c1-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="920c1-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="920c1-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="920c1-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="920c1-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="920c1-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="920c1-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="920c1-129">Remarks</span></span>

<span data-ttu-id="920c1-130">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppMediaTitle* .</span><span class="sxs-lookup"><span data-stu-id="920c1-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaTitle* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="920c1-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="920c1-131">Requirements</span></span>



| <span data-ttu-id="920c1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="920c1-132">Requirement</span></span> | <span data-ttu-id="920c1-133">Valore</span><span class="sxs-lookup"><span data-stu-id="920c1-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="920c1-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="920c1-134">TAPI version</span></span><br/> | <span data-ttu-id="920c1-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="920c1-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="920c1-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="920c1-136">Header</span></span><br/>       | <dl> <span data-ttu-id="920c1-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="920c1-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="920c1-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="920c1-138">Library</span></span><br/>      | <dl> <span data-ttu-id="920c1-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="920c1-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="920c1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="920c1-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="920c1-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="920c1-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="920c1-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="920c1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="920c1-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="920c1-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="920c1-144">**ITMedia::P UT \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="920c1-144">**ITMedia::Put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)
</dt> </dl>

 

