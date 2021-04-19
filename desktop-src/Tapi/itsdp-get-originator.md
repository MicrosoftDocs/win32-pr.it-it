---
description: Il \_ metodo Get originator ottiene il mittente della conferenza.
ms.assetid: a324098d-ae22-42e9-901e-b277433af199
title: 'Metodo ITSdp:: get_Originator (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f751dd5a9dffe2d3bbc7883b8a0f8f18f8e6381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326485"
---
# <a name="itsdpget_originator-method"></a><span data-ttu-id="7b357-103">Metodo ITSdp:: Get \_ originator</span><span class="sxs-lookup"><span data-stu-id="7b357-103">ITSdp::get\_Originator method</span></span>

<span data-ttu-id="7b357-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7b357-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7b357-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="7b357-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7b357-106">Il metodo **get \_ originator** ottiene il mittente della conferenza.</span><span class="sxs-lookup"><span data-stu-id="7b357-106">The **get\_Originator** method gets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b357-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b357-107">Syntax</span></span>


```C++
HRESULT get_Originator(
  [out] BSTR *ppOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="7b357-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b357-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b357-109">*ppOriginator* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7b357-109">*ppOriginator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b357-110">Puntatore a una rappresentazione **BSTR** del creatore della conferenza.</span><span class="sxs-lookup"><span data-stu-id="7b357-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b357-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b357-111">Return value</span></span>

<span data-ttu-id="7b357-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7b357-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7b357-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7b357-113">Return code</span></span>                                                                                   | <span data-ttu-id="7b357-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b357-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7b357-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7b357-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7b357-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7b357-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7b357-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="7b357-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7b357-118">Il parametro *ppOriginator* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="7b357-118">The *ppOriginator* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="7b357-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="7b357-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7b357-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7b357-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7b357-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="7b357-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7b357-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7b357-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7b357-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b357-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7b357-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="7b357-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="7b357-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b357-125">Remarks</span></span>

<span data-ttu-id="7b357-126">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppOriginator* .</span><span class="sxs-lookup"><span data-stu-id="7b357-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppOriginator* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b357-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b357-127">Requirements</span></span>



| <span data-ttu-id="7b357-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b357-128">Requirement</span></span> | <span data-ttu-id="7b357-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7b357-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b357-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7b357-130">TAPI version</span></span><br/> | <span data-ttu-id="7b357-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7b357-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7b357-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b357-132">Header</span></span><br/>       | <dl> <span data-ttu-id="7b357-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b357-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b357-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="7b357-134">Library</span></span><br/>      | <dl> <span data-ttu-id="7b357-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b357-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7b357-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7b357-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="7b357-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b357-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b357-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b357-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b357-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="7b357-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="7b357-140">**ITSdp: origine UT:p \_**</span><span class="sxs-lookup"><span data-stu-id="7b357-140">**ITSdp::put\_Originator**</span></span>](itsdp-put-originator.md)
</dt> </dl>

 

