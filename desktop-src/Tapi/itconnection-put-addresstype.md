---
description: Il \_ metodo Put AddressType imposta il tipo di indirizzo.
ms.assetid: 73c64904-925c-4a35-a8f9-88b196b59b1e
title: 'ITConnection: metodo:p ut_AddressType (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb9bc9b83a71f78a68b6efc2fa73c259c4afe9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326499"
---
# <a name="itconnectionput_addresstype-method"></a><span data-ttu-id="a1852-103">ITConnection::p UT \_ addressType metodo</span><span class="sxs-lookup"><span data-stu-id="a1852-103">ITConnection::put\_AddressType method</span></span>

<span data-ttu-id="a1852-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a1852-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a1852-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a1852-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a1852-106">Il metodo **put \_ addressType** imposta il tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="a1852-106">The **put\_AddressType** method sets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1852-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1852-107">Syntax</span></span>


```C++
HRESULT put_AddressType(
  [in] BSTR pAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="a1852-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1852-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1852-109">*pAddressType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1852-109">*pAddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1852-110">Puntatore a un **BSTR** che contiene il tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="a1852-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1852-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1852-111">Return value</span></span>

<span data-ttu-id="a1852-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a1852-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a1852-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a1852-113">Return code</span></span>                                                                                   | <span data-ttu-id="a1852-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1852-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a1852-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a1852-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a1852-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a1852-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a1852-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a1852-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a1852-118">Il parametro *pAddressType* non è valido.</span><span class="sxs-lookup"><span data-stu-id="a1852-118">The *pAddressType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="a1852-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a1852-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a1852-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a1852-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a1852-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="a1852-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a1852-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a1852-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a1852-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a1852-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a1852-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="a1852-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a1852-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1852-125">Remarks</span></span>

<span data-ttu-id="a1852-126">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PAddressType* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="a1852-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAddressType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1852-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1852-127">Requirements</span></span>



| <span data-ttu-id="a1852-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1852-128">Requirement</span></span> | <span data-ttu-id="a1852-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a1852-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1852-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a1852-130">TAPI version</span></span><br/> | <span data-ttu-id="a1852-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a1852-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a1852-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1852-132">Header</span></span><br/>       | <dl> <span data-ttu-id="a1852-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1852-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1852-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1852-134">Library</span></span><br/>      | <dl> <span data-ttu-id="a1852-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1852-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a1852-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a1852-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="a1852-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1852-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1852-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1852-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1852-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="a1852-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="a1852-140">**ITConnection:: Get \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="a1852-140">**ITConnection::get\_AddressType**</span></span>](itconnection-get-addresstype.md)
</dt> </dl>

 

