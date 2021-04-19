---
description: Il \_ metodo Get Item ottiene un elemento dalla raccolta usando un indice.
ms.assetid: 7401ae21-190d-479c-aebc-51bf8a953b94
title: 'Metodo ITTimeCollection:: get_Item (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b9dec40070ff3abddce0e425300f6d805c1cc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326748"
---
# <a name="ittimecollectionget_item-method"></a><span data-ttu-id="71a19-103">Metodo ITTimeCollection:: Get \_ Item</span><span class="sxs-lookup"><span data-stu-id="71a19-103">ITTimeCollection::get\_Item method</span></span>

<span data-ttu-id="71a19-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="71a19-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="71a19-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="71a19-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="71a19-106">Il metodo **get \_ Item** ottiene un elemento dalla raccolta usando un indice.</span><span class="sxs-lookup"><span data-stu-id="71a19-106">The **get\_Item** method gets an item from the collection using an index.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a19-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71a19-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG   Index,
  [out] ITTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="71a19-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="71a19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71a19-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="71a19-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a19-110">Indice dell'elemento da ottenere.</span><span class="sxs-lookup"><span data-stu-id="71a19-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="71a19-111">*pval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="71a19-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71a19-112">Puntatore a [**ITTime**](ittime.md) interfaccia desiderata.</span><span class="sxs-lookup"><span data-stu-id="71a19-112">Pointer to [**ITTime**](ittime.md) desired interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71a19-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71a19-113">Return value</span></span>

<span data-ttu-id="71a19-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="71a19-114">This method can return one of these values.</span></span>



| <span data-ttu-id="71a19-115">Valore</span><span class="sxs-lookup"><span data-stu-id="71a19-115">Value</span></span>                                                                                         | <span data-ttu-id="71a19-116">Significato</span><span class="sxs-lookup"><span data-stu-id="71a19-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="71a19-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71a19-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="71a19-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="71a19-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="71a19-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="71a19-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="71a19-120">Il parametro *pval* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="71a19-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="71a19-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="71a19-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="71a19-122">Il parametro di *Indice* non è valido.</span><span class="sxs-lookup"><span data-stu-id="71a19-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="71a19-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="71a19-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="71a19-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="71a19-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="71a19-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="71a19-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="71a19-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="71a19-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="71a19-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="71a19-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="71a19-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="71a19-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="71a19-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="71a19-129">Remarks</span></span>

<span data-ttu-id="71a19-130">TAPI chiama il metodo **AddRef** sull'interfaccia [**ITTime**](ittime.md) restituita dall'**\_ elemento i TTimeCollection:: Get**.</span><span class="sxs-lookup"><span data-stu-id="71a19-130">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by I **TTimeCollection::get\_Item**.</span></span> <span data-ttu-id="71a19-131">L'applicazione deve chiamare **Release** sull'interfaccia **ITTime** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="71a19-131">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="71a19-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71a19-132">Requirements</span></span>



| <span data-ttu-id="71a19-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="71a19-133">Requirement</span></span> | <span data-ttu-id="71a19-134">Valore</span><span class="sxs-lookup"><span data-stu-id="71a19-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71a19-135">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="71a19-135">TAPI version</span></span><br/> | <span data-ttu-id="71a19-136">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="71a19-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="71a19-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71a19-137">Header</span></span><br/>       | <dl> <span data-ttu-id="71a19-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="71a19-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="71a19-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="71a19-139">Library</span></span><br/>      | <dl> <span data-ttu-id="71a19-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71a19-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="71a19-141">DLL</span><span class="sxs-lookup"><span data-stu-id="71a19-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="71a19-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71a19-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a19-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71a19-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a19-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="71a19-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="71a19-145">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="71a19-145">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




