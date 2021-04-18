---
description: Il \_ metodo GET ProtocolVersion ottiene la versione del protocollo SDP; vedere RFC 2327).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'Metodo ITSdp:: get_ProtocolVersion (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327503"
---
# <a name="itsdpget_protocolversion-method"></a><span data-ttu-id="f6d52-103">Metodo ITSdp:: Get \_ ProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="f6d52-103">ITSdp::get\_ProtocolVersion method</span></span>

<span data-ttu-id="f6d52-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f6d52-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f6d52-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f6d52-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f6d52-106">Il metodo **get \_ ProtocolVersion** ottiene la versione del protocollo SDP; vedere RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="f6d52-106">The **get\_ProtocolVersion** method gets the Session Descriptor Protocol (SDP; see RFC 2327) protocol version.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d52-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6d52-107">Syntax</span></span>


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="f6d52-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6d52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6d52-109">*pProtocolVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f6d52-109">*pProtocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d52-110">Puntatore alla versione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="f6d52-110">Pointer to the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6d52-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6d52-111">Return value</span></span>

<span data-ttu-id="f6d52-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f6d52-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f6d52-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f6d52-113">Return code</span></span>                                                                                   | <span data-ttu-id="f6d52-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6d52-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6d52-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f6d52-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f6d52-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f6d52-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="f6d52-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="f6d52-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f6d52-118">Il parametro *pProtocolVersion* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="f6d52-118">The *pProtocolVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="f6d52-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f6d52-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f6d52-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f6d52-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="f6d52-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="f6d52-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f6d52-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f6d52-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="f6d52-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f6d52-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f6d52-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="f6d52-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="f6d52-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6d52-125">Requirements</span></span>



| <span data-ttu-id="f6d52-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6d52-126">Requirement</span></span> | <span data-ttu-id="f6d52-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f6d52-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d52-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f6d52-128">TAPI version</span></span><br/> | <span data-ttu-id="f6d52-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f6d52-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f6d52-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6d52-130">Header</span></span><br/>       | <dl> <span data-ttu-id="f6d52-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6d52-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6d52-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="f6d52-132">Library</span></span><br/>      | <dl> <span data-ttu-id="f6d52-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6d52-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f6d52-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f6d52-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="f6d52-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6d52-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6d52-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6d52-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d52-137">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="f6d52-137">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




