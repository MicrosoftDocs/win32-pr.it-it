---
description: Il \_ metodo get Count ottiene il numero di supporti nella sessione.
ms.assetid: 9d085a34-9a49-4447-8d11-56d71a2a3592
title: 'Metodo ITMediaCollection:: get_Count (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f5a4fb6d7f1b942f37aae1356c7b49e0e60f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330469"
---
# <a name="itmediacollectionget_count-method"></a><span data-ttu-id="8fbfa-103">Metodo ITMediaCollection:: Get \_ Count</span><span class="sxs-lookup"><span data-stu-id="8fbfa-103">ITMediaCollection::get\_Count method</span></span>

<span data-ttu-id="8fbfa-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8fbfa-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8fbfa-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8fbfa-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8fbfa-106">Il metodo **get \_ count** ottiene il numero di supporti nella sessione.</span><span class="sxs-lookup"><span data-stu-id="8fbfa-106">The **get\_Count** method gets the number of media in the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbfa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fbfa-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8fbfa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fbfa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fbfa-109">*pval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8fbfa-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbfa-110">Numero di supporti nella sessione.</span><span class="sxs-lookup"><span data-stu-id="8fbfa-110">Count of media in the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fbfa-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fbfa-111">Return value</span></span>

<span data-ttu-id="8fbfa-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="8fbfa-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8fbfa-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8fbfa-113">Return code</span></span>                                                                                   | <span data-ttu-id="8fbfa-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fbfa-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8fbfa-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8fbfa-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8fbfa-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8fbfa-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8fbfa-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="8fbfa-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8fbfa-118">Il parametro *pval* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="8fbfa-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="8fbfa-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8fbfa-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8fbfa-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8fbfa-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8fbfa-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="8fbfa-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8fbfa-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="8fbfa-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8fbfa-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8fbfa-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8fbfa-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="8fbfa-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="8fbfa-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fbfa-125">Requirements</span></span>



| <span data-ttu-id="8fbfa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fbfa-126">Requirement</span></span> | <span data-ttu-id="8fbfa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8fbfa-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbfa-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="8fbfa-128">TAPI version</span></span><br/> | <span data-ttu-id="8fbfa-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8fbfa-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8fbfa-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fbfa-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8fbfa-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fbfa-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8fbfa-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="8fbfa-132">Library</span></span><br/>      | <dl> <span data-ttu-id="8fbfa-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fbfa-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8fbfa-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8fbfa-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="8fbfa-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fbfa-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fbfa-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fbfa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbfa-137">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="8fbfa-137">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




