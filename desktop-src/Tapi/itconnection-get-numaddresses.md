---
description: Il \_ metodo Get NumAddresses ottiene il numero di indirizzi da utilizzare per la sessione.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: 'Metodo ITConnection:: get_NumAddresses (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b121275c6af8f026e7321e4fd85327e970eb78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326508"
---
# <a name="itconnectionget_numaddresses-method"></a><span data-ttu-id="d2680-103">Metodo ITConnection:: Get \_ NumAddresses</span><span class="sxs-lookup"><span data-stu-id="d2680-103">ITConnection::get\_NumAddresses method</span></span>

<span data-ttu-id="d2680-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d2680-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d2680-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d2680-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d2680-106">Il metodo **get \_ NumAddresses** ottiene il numero di indirizzi da utilizzare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="d2680-106">The **get\_NumAddresses** method gets the number of addresses to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2680-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2680-107">Syntax</span></span>


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="d2680-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2680-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2680-109">*pNumAddresses* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d2680-109">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2680-110">Numero di indirizzi per la sessione.</span><span class="sxs-lookup"><span data-stu-id="d2680-110">Number of addresses for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2680-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2680-111">Return value</span></span>

<span data-ttu-id="d2680-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d2680-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d2680-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d2680-113">Return code</span></span>                                                                                   | <span data-ttu-id="d2680-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2680-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2680-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d2680-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d2680-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d2680-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d2680-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d2680-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d2680-118">Il parametro *pNumAddresse* s non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="d2680-118">The *pNumAddresse* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="d2680-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d2680-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d2680-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d2680-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="d2680-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="d2680-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d2680-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="d2680-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d2680-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d2680-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d2680-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="d2680-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="d2680-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2680-125">Requirements</span></span>



| <span data-ttu-id="d2680-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2680-126">Requirement</span></span> | <span data-ttu-id="d2680-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d2680-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2680-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d2680-128">TAPI version</span></span><br/> | <span data-ttu-id="d2680-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d2680-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d2680-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2680-130">Header</span></span><br/>       | <dl> <span data-ttu-id="d2680-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2680-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2680-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="d2680-132">Library</span></span><br/>      | <dl> <span data-ttu-id="d2680-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2680-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d2680-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d2680-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="d2680-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2680-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2680-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2680-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2680-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="d2680-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




