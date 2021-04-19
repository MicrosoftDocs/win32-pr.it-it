---
description: Il \_ metodo get Count ottiene il numero di elementi nella raccolta.
ms.assetid: 9fe96af3-bb7b-4f6c-8df2-85bf7850c527
title: 'Metodo ITTimeCollection:: get_Count (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a385c8fa3120cbeaa4b876a8af4f60e0df5cb48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326751"
---
# <a name="ittimecollectionget_count-method"></a><span data-ttu-id="d1269-103">Metodo ITTimeCollection:: Get \_ Count</span><span class="sxs-lookup"><span data-stu-id="d1269-103">ITTimeCollection::get\_Count method</span></span>

<span data-ttu-id="d1269-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d1269-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d1269-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d1269-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d1269-106">Il metodo **get \_ count** ottiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="d1269-106">The **get\_Count** method gets the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1269-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1269-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d1269-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1269-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1269-109">*pval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d1269-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1269-110">Puntatore al numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="d1269-110">Pointer to the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1269-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1269-111">Return value</span></span>

<span data-ttu-id="d1269-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d1269-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d1269-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d1269-113">Return code</span></span>                                                                                   | <span data-ttu-id="d1269-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1269-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d1269-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1269-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d1269-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d1269-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d1269-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d1269-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d1269-118">Il parametro *pval* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="d1269-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="d1269-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d1269-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d1269-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d1269-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d1269-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="d1269-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d1269-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="d1269-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d1269-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d1269-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d1269-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="d1269-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="d1269-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1269-125">Requirements</span></span>



| <span data-ttu-id="d1269-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1269-126">Requirement</span></span> | <span data-ttu-id="d1269-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d1269-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1269-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d1269-128">TAPI version</span></span><br/> | <span data-ttu-id="d1269-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d1269-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d1269-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1269-130">Header</span></span><br/>       | <dl> <span data-ttu-id="d1269-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1269-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1269-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="d1269-132">Library</span></span><br/>      | <dl> <span data-ttu-id="d1269-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1269-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d1269-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d1269-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="d1269-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1269-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1269-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1269-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1269-137">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="d1269-137">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="d1269-138">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="d1269-138">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




