---
description: Il \_ metodo Get NetworkType ottiene il tipo di rete.
ms.assetid: 5597284a-9cc6-422b-a064-cda25aa5964b
title: 'Metodo ITConnection:: get_NetworkType (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31189ec0e3b42e3ed249cd0c62365b1f8c793908
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326511"
---
# <a name="itconnectionget_networktype-method"></a><span data-ttu-id="bbe15-103">Metodo ITConnection:: Get \_ NetworkType</span><span class="sxs-lookup"><span data-stu-id="bbe15-103">ITConnection::get\_NetworkType method</span></span>

<span data-ttu-id="bbe15-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bbe15-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bbe15-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bbe15-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bbe15-106">Il metodo **get \_ NetworkType** ottiene il tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="bbe15-106">The **get\_NetworkType** method gets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe15-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbe15-107">Syntax</span></span>


```C++
HRESULT get_NetworkType(
  [out] BSTR *ppNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="bbe15-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbe15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbe15-109">*ppNetworkType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bbe15-109">*ppNetworkType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe15-110">Puntatore a un **BSTR** che contiene il tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="bbe15-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbe15-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbe15-111">Return value</span></span>

<span data-ttu-id="bbe15-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="bbe15-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bbe15-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bbe15-113">Return code</span></span>                                                                                   | <span data-ttu-id="bbe15-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbe15-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbe15-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe15-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bbe15-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bbe15-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="bbe15-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe15-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bbe15-118">Il parametro *ppNetworkType* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="bbe15-118">The *ppNetworkType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="bbe15-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe15-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bbe15-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bbe15-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="bbe15-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe15-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="bbe15-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="bbe15-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bbe15-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="bbe15-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="bbe15-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="bbe15-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="bbe15-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbe15-125">Remarks</span></span>

<span data-ttu-id="bbe15-126">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppNetworkType* .</span><span class="sxs-lookup"><span data-stu-id="bbe15-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppNetworkType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe15-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbe15-127">Requirements</span></span>



| <span data-ttu-id="bbe15-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe15-128">Requirement</span></span> | <span data-ttu-id="bbe15-129">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe15-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe15-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="bbe15-130">TAPI version</span></span><br/> | <span data-ttu-id="bbe15-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bbe15-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bbe15-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbe15-132">Header</span></span><br/>       | <dl> <span data-ttu-id="bbe15-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe15-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbe15-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="bbe15-134">Library</span></span><br/>      | <dl> <span data-ttu-id="bbe15-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbe15-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bbe15-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bbe15-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="bbe15-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbe15-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbe15-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbe15-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe15-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="bbe15-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="bbe15-140">**ITConnection::p UT \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="bbe15-140">**ITConnection::put\_NetworkType**</span></span>](itconnection-put-networktype.md)
</dt> </dl>

 

