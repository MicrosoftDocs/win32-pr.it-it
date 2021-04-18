---
description: Il \_ metodo Get IsValid convalida il BLOB di Session Descriptor Protocol (SDP; vedere RFC 2327) per i valori di struttura e di campo.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: 'Metodo ITSdp:: get_IsValid (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ca3cfdc1061e0a2830010ec39b2e6667c9341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333654"
---
# <a name="itsdpget_isvalid-method"></a><span data-ttu-id="ccdc5-103">Metodo ITSdp:: Get \_ IsValid</span><span class="sxs-lookup"><span data-stu-id="ccdc5-103">ITSdp::get\_IsValid method</span></span>

<span data-ttu-id="ccdc5-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ccdc5-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ccdc5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ccdc5-106">Il metodo **get \_ IsValid** convalida il BLOB di Session Descriptor Protocol (SDP; vedere RFC 2327) per i valori di struttura e di campo.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-106">The **get\_IsValid** method validates the Session Descriptor Protocol (SDP; see RFC 2327) blob for structure and field values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccdc5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccdc5-107">Syntax</span></span>


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a><span data-ttu-id="ccdc5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccdc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccdc5-109">*pfIsValid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ccdc5-109">*pfIsValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccdc5-110">Indica se la struttura del BLOB è valida.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-110">Indicates whether the blob structure is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccdc5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccdc5-111">Return value</span></span>

<span data-ttu-id="ccdc5-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ccdc5-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ccdc5-113">Return code</span></span>                                                                                   | <span data-ttu-id="ccdc5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccdc5-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ccdc5-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ccdc5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ccdc5-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ccdc5-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ccdc5-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ccdc5-118">Il parametro *pfIsValid* non è valido.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-118">The *pfIsValid* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="ccdc5-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ccdc5-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ccdc5-120">Il parametro *pfIsValid* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-120">The *pfIsValid* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="ccdc5-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ccdc5-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ccdc5-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ccdc5-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="ccdc5-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ccdc5-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ccdc5-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ccdc5-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ccdc5-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="ccdc5-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="ccdc5-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccdc5-127">Requirements</span></span>



| <span data-ttu-id="ccdc5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccdc5-128">Requirement</span></span> | <span data-ttu-id="ccdc5-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ccdc5-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccdc5-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="ccdc5-130">TAPI version</span></span><br/> | <span data-ttu-id="ccdc5-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ccdc5-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ccdc5-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccdc5-132">Header</span></span><br/>       | <dl> <span data-ttu-id="ccdc5-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccdc5-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccdc5-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="ccdc5-134">Library</span></span><br/>      | <dl> <span data-ttu-id="ccdc5-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccdc5-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ccdc5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ccdc5-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="ccdc5-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccdc5-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccdc5-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccdc5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccdc5-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="ccdc5-139">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




