---
description: Il \_ metodo Get NumPorts ottiene il numero di porte necessarie per la sessione. La sessione usa il numero di porte specificato a partire dal valore restituito da Get \_ presenta.
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'Metodo ITMedia:: get_NumPorts (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc223ddd5d210d2c1d440c52ca4201ccd6334b08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333555"
---
# <a name="itmediaget_numports-method"></a><span data-ttu-id="862cc-104">Metodo ITMedia:: Get \_ NumPorts</span><span class="sxs-lookup"><span data-stu-id="862cc-104">ITMedia::get\_NumPorts method</span></span>

<span data-ttu-id="862cc-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="862cc-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="862cc-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="862cc-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="862cc-107">Il metodo **get \_ NumPorts** ottiene il numero di porte necessarie per la sessione.</span><span class="sxs-lookup"><span data-stu-id="862cc-107">The **get\_NumPorts** method gets the number of ports needed for the session.</span></span> <span data-ttu-id="862cc-108">La sessione usa il numero di porte specificato a partire dal valore restituito da [**get \_ presenta**](itmedia-get-startport.md).</span><span class="sxs-lookup"><span data-stu-id="862cc-108">The session uses the specified number of ports starting from the value returned by [**get\_StartPort**](itmedia-get-startport.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="862cc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="862cc-109">Syntax</span></span>


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="862cc-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="862cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="862cc-111">*pNumPorts* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="862cc-111">*pNumPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="862cc-112">Puntatore al numero di porte.</span><span class="sxs-lookup"><span data-stu-id="862cc-112">Pointer to the number of ports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="862cc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="862cc-113">Return value</span></span>

<span data-ttu-id="862cc-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="862cc-114">This method can return one of these values.</span></span>



| <span data-ttu-id="862cc-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="862cc-115">Return code</span></span>                                                                                   | <span data-ttu-id="862cc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="862cc-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="862cc-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="862cc-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="862cc-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="862cc-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="862cc-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="862cc-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="862cc-120">Il parametro *pNumPorts* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="862cc-120">The *pNumPorts* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="862cc-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="862cc-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="862cc-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="862cc-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="862cc-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="862cc-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="862cc-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="862cc-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="862cc-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="862cc-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="862cc-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="862cc-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="862cc-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="862cc-127">Requirements</span></span>



| <span data-ttu-id="862cc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="862cc-128">Requirement</span></span> | <span data-ttu-id="862cc-129">Valore</span><span class="sxs-lookup"><span data-stu-id="862cc-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="862cc-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="862cc-130">TAPI version</span></span><br/> | <span data-ttu-id="862cc-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="862cc-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="862cc-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="862cc-132">Header</span></span><br/>       | <dl> <span data-ttu-id="862cc-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="862cc-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="862cc-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="862cc-134">Library</span></span><br/>      | <dl> <span data-ttu-id="862cc-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="862cc-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="862cc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="862cc-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="862cc-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="862cc-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="862cc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="862cc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862cc-139">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="862cc-139">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




