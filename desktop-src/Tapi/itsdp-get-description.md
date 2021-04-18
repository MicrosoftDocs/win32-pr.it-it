---
description: Il \_ metodo get Description ottiene la descrizione della sessione (BSTR).
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: 'Metodo ITSdp:: get_Description (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f60f7aefcfac852a1665f54a59ff0541b1d82a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333657"
---
# <a name="itsdpget_description-method"></a><span data-ttu-id="f9983-103">Metodo ITSdp:: Get \_ Description</span><span class="sxs-lookup"><span data-stu-id="f9983-103">ITSdp::get\_Description method</span></span>

<span data-ttu-id="f9983-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f9983-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f9983-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f9983-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f9983-106">Il metodo **get \_ Description** ottiene la descrizione della sessione (**BSTR**).</span><span class="sxs-lookup"><span data-stu-id="f9983-106">The **get\_Description** method gets the session description (**BSTR**).</span></span> <span data-ttu-id="f9983-107">Deve essere una stringa convertibile ASCII se il set di caratteri è ASCII.</span><span class="sxs-lookup"><span data-stu-id="f9983-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="f9983-108">In caso contrario, può essere qualsiasi stringa **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="f9983-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="f9983-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9983-109">Syntax</span></span>


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a><span data-ttu-id="f9983-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9983-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9983-111">*ppDescription* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f9983-111">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9983-112">Puntatore a un **BSTR** che contiene la descrizione della sessione.</span><span class="sxs-lookup"><span data-stu-id="f9983-112">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9983-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9983-113">Return value</span></span>

<span data-ttu-id="f9983-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f9983-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f9983-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f9983-115">Return code</span></span>                                                                                   | <span data-ttu-id="f9983-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9983-116">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9983-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9983-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f9983-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f9983-118">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f9983-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="f9983-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f9983-120">Il parametro *ppDescription* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="f9983-120">The *ppDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="f9983-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f9983-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f9983-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f9983-122">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="f9983-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="f9983-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f9983-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f9983-124">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f9983-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f9983-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f9983-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="f9983-126">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="f9983-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9983-127">Remarks</span></span>

<span data-ttu-id="f9983-128">Per liberare il parametro *ppDescription* , l'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="f9983-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the *ppDescription* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9983-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9983-129">Requirements</span></span>



| <span data-ttu-id="f9983-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9983-130">Requirement</span></span> | <span data-ttu-id="f9983-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f9983-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9983-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f9983-132">TAPI version</span></span><br/> | <span data-ttu-id="f9983-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f9983-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f9983-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9983-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f9983-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9983-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9983-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="f9983-136">Library</span></span><br/>      | <dl> <span data-ttu-id="f9983-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9983-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f9983-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f9983-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="f9983-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9983-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9983-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9983-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9983-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="f9983-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="f9983-142">**ITSdp: Descrizione UT:p \_**</span><span class="sxs-lookup"><span data-stu-id="f9983-142">**ITSdp::put\_Description**</span></span>](itsdp-put-description.md)
</dt> </dl>

 

