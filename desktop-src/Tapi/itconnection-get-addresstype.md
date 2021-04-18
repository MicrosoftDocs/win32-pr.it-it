---
description: Il \_ metodo Get AddressType ottiene il tipo di indirizzo.
ms.assetid: b2ff6303-6beb-429c-ad1a-2f729749e5db
title: 'Metodo ITConnection:: get_AddressType (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d015b0b395f0219fa9a7af2ca7002f242cfaa1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328225"
---
# <a name="itconnectionget_addresstype-method"></a><span data-ttu-id="73e2b-103">Metodo ITConnection:: Get \_ AddressType</span><span class="sxs-lookup"><span data-stu-id="73e2b-103">ITConnection::get\_AddressType method</span></span>

<span data-ttu-id="73e2b-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="73e2b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="73e2b-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="73e2b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="73e2b-106">Il metodo **get \_ addressType** ottiene il tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="73e2b-106">The **get\_AddressType** method gets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e2b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73e2b-107">Syntax</span></span>


```C++
HRESULT get_AddressType(
  [out] BSTR *ppAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="73e2b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="73e2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e2b-109">*ppAddressType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="73e2b-109">*ppAddressType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73e2b-110">Puntatore a un **BSTR** che contiene il tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="73e2b-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e2b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73e2b-111">Return value</span></span>

<span data-ttu-id="73e2b-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="73e2b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="73e2b-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="73e2b-113">Return code</span></span>                                                                                   | <span data-ttu-id="73e2b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73e2b-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="73e2b-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="73e2b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="73e2b-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="73e2b-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="73e2b-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="73e2b-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="73e2b-118">Il parametro *ppAddressType* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="73e2b-118">The *ppAddressType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="73e2b-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="73e2b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="73e2b-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="73e2b-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="73e2b-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="73e2b-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="73e2b-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="73e2b-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="73e2b-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="73e2b-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="73e2b-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="73e2b-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="73e2b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="73e2b-125">Remarks</span></span>

<span data-ttu-id="73e2b-126">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppAddressType* .</span><span class="sxs-lookup"><span data-stu-id="73e2b-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppAddressType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="73e2b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73e2b-127">Requirements</span></span>



| <span data-ttu-id="73e2b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="73e2b-128">Requirement</span></span> | <span data-ttu-id="73e2b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="73e2b-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73e2b-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="73e2b-130">TAPI version</span></span><br/> | <span data-ttu-id="73e2b-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="73e2b-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="73e2b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73e2b-132">Header</span></span><br/>       | <dl> <span data-ttu-id="73e2b-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="73e2b-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="73e2b-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="73e2b-134">Library</span></span><br/>      | <dl> <span data-ttu-id="73e2b-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73e2b-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="73e2b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="73e2b-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="73e2b-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73e2b-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e2b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73e2b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e2b-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="73e2b-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="73e2b-140">**ITConnection::p UT \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="73e2b-140">**ITConnection::put\_AddressType**</span></span>](itconnection-put-addresstype.md)
</dt> </dl>

 

