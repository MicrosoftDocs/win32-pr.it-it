---
description: Il \_ metodo Get EnumerationIf restituisce l'interfaccia di enumerazione IEnumTime che enumera ITTime.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'Metodo ITTimeCollection:: get_EnumerationIf (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326747"
---
# <a name="ittimecollectionget_enumerationif-method"></a><span data-ttu-id="30485-103">Metodo ITTimeCollection:: Get \_ EnumerationIf</span><span class="sxs-lookup"><span data-stu-id="30485-103">ITTimeCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="30485-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="30485-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="30485-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="30485-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="30485-106">Il metodo **get \_ EnumerationIf** restituisce l'interfaccia di enumerazione [**IEnumTime**](ienumtime.md) che enumera [**ITTime**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="30485-106">The **get\_EnumerationIf** method returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30485-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30485-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="30485-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="30485-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30485-109">*pval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30485-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30485-110">Puntatore all'interfaccia [**IEnumTime**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="30485-110">Pointer to the [**IEnumTime**](ienumtime.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30485-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30485-111">Return value</span></span>

<span data-ttu-id="30485-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="30485-112">This method can return one of these values.</span></span>



| <span data-ttu-id="30485-113">Valore</span><span class="sxs-lookup"><span data-stu-id="30485-113">Value</span></span>                                                                                         | <span data-ttu-id="30485-114">Significato</span><span class="sxs-lookup"><span data-stu-id="30485-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="30485-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30485-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="30485-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="30485-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="30485-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="30485-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="30485-118">Il parametro *pval* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="30485-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="30485-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="30485-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="30485-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="30485-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="30485-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="30485-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="30485-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="30485-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="30485-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="30485-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="30485-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="30485-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="30485-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="30485-125">Remarks</span></span>

<span data-ttu-id="30485-126">Questo metodo è interscambiabile con [**get \_ \_ NewEnum**](ittimecollection-get--newenum.md) , ad eccezione del fatto che restituisce [**IEnumTime**](ienumtime.md) anziché **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="30485-126">This method is interchangeable with [**get\_\_NewEnum**](ittimecollection-get--newenum.md) except that it returns [**IEnumTime**](ienumtime.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="30485-127">TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumTime**](ienumtime.md) restituita da **ITTimeCollection:: Get \_ EnumerationIf**.</span><span class="sxs-lookup"><span data-stu-id="30485-127">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **ITTimeCollection::get\_EnumerationIf**.</span></span> <span data-ttu-id="30485-128">L'applicazione deve chiamare **Release** sull'interfaccia [**IEnumTime**](ienumtime.md) per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="30485-128">The application must call **Release** on the [**IEnumTime**](ienumtime.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="30485-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30485-129">Requirements</span></span>



| <span data-ttu-id="30485-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="30485-130">Requirement</span></span> | <span data-ttu-id="30485-131">Valore</span><span class="sxs-lookup"><span data-stu-id="30485-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30485-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="30485-132">TAPI version</span></span><br/> | <span data-ttu-id="30485-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="30485-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="30485-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30485-134">Header</span></span><br/>       | <dl> <span data-ttu-id="30485-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="30485-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="30485-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="30485-136">Library</span></span><br/>      | <dl> <span data-ttu-id="30485-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30485-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="30485-138">DLL</span><span class="sxs-lookup"><span data-stu-id="30485-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="30485-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30485-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30485-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30485-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30485-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="30485-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> <dt>

[<span data-ttu-id="30485-142">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="30485-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="30485-143">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="30485-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




