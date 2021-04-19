---
description: Il \_ metodo GET STARTADDRESS ottiene il primo indirizzo da usare per la sessione.
ms.assetid: 3c4fec19-1b7d-4052-afd8-7aaf095907d0
title: 'Metodo ITConnection:: get_StartAddress (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84266d1874e7d04acb594bcfb9d99b440b0390b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326505"
---
# <a name="itconnectionget_startaddress-method"></a><span data-ttu-id="9bc77-103">Metodo ITConnection:: Get \_ STARTADDRESS</span><span class="sxs-lookup"><span data-stu-id="9bc77-103">ITConnection::get\_StartAddress method</span></span>

<span data-ttu-id="9bc77-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9bc77-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9bc77-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="9bc77-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9bc77-106">Il metodo **get \_ STARTADDRESS** ottiene il primo indirizzo da usare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="9bc77-106">The **get\_StartAddress** method gets the first address to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc77-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bc77-107">Syntax</span></span>


```C++
HRESULT get_StartAddress(
  [out] BSTR *ppStartAddress
);
```



## <a name="parameters"></a><span data-ttu-id="9bc77-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bc77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bc77-109">*ppStartAddress* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9bc77-109">*ppStartAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc77-110">Puntatore a un **BSTR** che contiene l'indirizzo iniziale della sessione.</span><span class="sxs-lookup"><span data-stu-id="9bc77-110">Pointer to a **BSTR** containing the starting address for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bc77-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bc77-111">Return value</span></span>

<span data-ttu-id="9bc77-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="9bc77-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9bc77-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9bc77-113">Return code</span></span>                                                                                   | <span data-ttu-id="9bc77-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bc77-114">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="9bc77-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc77-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9bc77-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="9bc77-116">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="9bc77-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc77-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9bc77-118">Il parametro *ppStartAddress* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="9bc77-118">The *ppStartAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="9bc77-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc77-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9bc77-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9bc77-120">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="9bc77-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc77-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9bc77-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="9bc77-122">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="9bc77-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc77-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9bc77-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="9bc77-124">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9bc77-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bc77-125">Remarks</span></span>

<span data-ttu-id="9bc77-126">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppStartAddress* .</span><span class="sxs-lookup"><span data-stu-id="9bc77-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppStartAddress* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bc77-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bc77-127">Requirements</span></span>



| <span data-ttu-id="9bc77-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bc77-128">Requirement</span></span> | <span data-ttu-id="9bc77-129">Valore</span><span class="sxs-lookup"><span data-stu-id="9bc77-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc77-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="9bc77-130">TAPI version</span></span><br/> | <span data-ttu-id="9bc77-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9bc77-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9bc77-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bc77-132">Header</span></span><br/>       | <dl> <span data-ttu-id="9bc77-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bc77-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9bc77-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="9bc77-134">Library</span></span><br/>      | <dl> <span data-ttu-id="9bc77-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bc77-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9bc77-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9bc77-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="9bc77-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bc77-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bc77-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bc77-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc77-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="9bc77-139">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

