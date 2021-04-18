---
description: Il \_ metodo get Name ottiene il nome della sessione.
ms.assetid: 97b44a01-585b-434c-ad59-51c35e8a1ceb
title: 'Metodo ITSdp:: get_Name (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b41d431a76f3d0bb2122847e8ee5c3a4dde3c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325593"
---
# <a name="itsdpget_name-method"></a><span data-ttu-id="e47c7-103">Metodo ITSdp:: Get \_ Name</span><span class="sxs-lookup"><span data-stu-id="e47c7-103">ITSdp::get\_Name method</span></span>

<span data-ttu-id="e47c7-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e47c7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e47c7-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e47c7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e47c7-106">Il metodo **get \_ Name** ottiene il nome della sessione.</span><span class="sxs-lookup"><span data-stu-id="e47c7-106">The **get\_Name** method gets the session name.</span></span> <span data-ttu-id="e47c7-107">Deve essere una stringa convertibile ASCII se il set di caratteri è ASCII.</span><span class="sxs-lookup"><span data-stu-id="e47c7-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="e47c7-108">In caso contrario, può essere qualsiasi stringa **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="e47c7-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="e47c7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e47c7-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="e47c7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e47c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e47c7-111">*ppName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e47c7-111">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e47c7-112">Puntatore a un **BSTR** che contiene il nome della sessione.</span><span class="sxs-lookup"><span data-stu-id="e47c7-112">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e47c7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e47c7-113">Return value</span></span>

<span data-ttu-id="e47c7-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="e47c7-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e47c7-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e47c7-115">Return code</span></span>                                                                                   | <span data-ttu-id="e47c7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e47c7-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e47c7-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e47c7-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e47c7-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e47c7-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e47c7-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e47c7-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e47c7-120">Il parametro *ppName* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="e47c7-120">The *ppName* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="e47c7-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="e47c7-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e47c7-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e47c7-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e47c7-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="e47c7-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e47c7-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="e47c7-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e47c7-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e47c7-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e47c7-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="e47c7-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e47c7-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="e47c7-127">Remarks</span></span>

<span data-ttu-id="e47c7-128">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppName* .</span><span class="sxs-lookup"><span data-stu-id="e47c7-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e47c7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e47c7-129">Requirements</span></span>



| <span data-ttu-id="e47c7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e47c7-130">Requirement</span></span> | <span data-ttu-id="e47c7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e47c7-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e47c7-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e47c7-132">TAPI version</span></span><br/> | <span data-ttu-id="e47c7-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e47c7-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e47c7-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e47c7-134">Header</span></span><br/>       | <dl> <span data-ttu-id="e47c7-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e47c7-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e47c7-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="e47c7-136">Library</span></span><br/>      | <dl> <span data-ttu-id="e47c7-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e47c7-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e47c7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e47c7-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="e47c7-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e47c7-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e47c7-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e47c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e47c7-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="e47c7-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="e47c7-142">**ITSdp: nome ut:p \_**</span><span class="sxs-lookup"><span data-stu-id="e47c7-142">**ITSdp::put\_Name**</span></span>](itsdp-put-name.md)
</dt> </dl>

 

