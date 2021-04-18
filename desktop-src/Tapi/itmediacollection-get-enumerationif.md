---
description: Il \_ metodo Get EnumerationIf ottiene un puntatore a un'interfaccia di enumerazione dei supporti.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'Metodo ITMediaCollection:: get_EnumerationIf (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a7e7d85c1f7a433a31360fabc8b5dac71e68ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330266"
---
# <a name="itmediacollectionget_enumerationif-method"></a><span data-ttu-id="53f1b-103">Metodo ITMediaCollection:: Get \_ EnumerationIf</span><span class="sxs-lookup"><span data-stu-id="53f1b-103">ITMediaCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="53f1b-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53f1b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="53f1b-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="53f1b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="53f1b-106">Il metodo **get \_ EnumerationIf** ottiene un puntatore a un'interfaccia di enumerazione dei supporti.</span><span class="sxs-lookup"><span data-stu-id="53f1b-106">The **get\_EnumerationIf** method gets a pointer to a media enumeration interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f1b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53f1b-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="53f1b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53f1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f1b-109">*pval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="53f1b-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53f1b-110">Puntatore all'interfaccia [**IEnumMedia**](ienummedia.md) per l'elemento desiderato.</span><span class="sxs-lookup"><span data-stu-id="53f1b-110">Pointer to the [**IEnumMedia**](ienummedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f1b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53f1b-111">Return value</span></span>

<span data-ttu-id="53f1b-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="53f1b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="53f1b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="53f1b-113">Value</span></span>                                                                                         | <span data-ttu-id="53f1b-114">Significato</span><span class="sxs-lookup"><span data-stu-id="53f1b-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="53f1b-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="53f1b-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="53f1b-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="53f1b-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1b-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="53f1b-118">Il parametro *pval* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="53f1b-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="53f1b-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="53f1b-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="53f1b-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="53f1b-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1b-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="53f1b-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="53f1b-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="53f1b-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="53f1b-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="53f1b-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="53f1b-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="53f1b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="53f1b-125">Remarks</span></span>

<span data-ttu-id="53f1b-126">Questo metodo è interscambiabile con [**get \_ \_ NewEnum**](itmediacollection-get--newenum.md) , ad eccezione del fatto che restituisce [**IEnumMedia**](ienummedia.md) anziché **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="53f1b-126">This method is interchangeable with [**get\_\_NewEnum**](itmediacollection-get--newenum.md) except that it returns [**IEnumMedia**](ienummedia.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="53f1b-127">TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumMedia**](ienummedia.md) restituita da **ITMediaCollection:: Get \_ Enumerationlf**.</span><span class="sxs-lookup"><span data-stu-id="53f1b-127">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **ITMediaCollection::get\_Enumerationlf**.</span></span> <span data-ttu-id="53f1b-128">L'applicazione deve chiamare **Release** sull'interfaccia **IEnumMedia** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="53f1b-128">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f1b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53f1b-129">Requirements</span></span>



| <span data-ttu-id="53f1b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="53f1b-130">Requirement</span></span> | <span data-ttu-id="53f1b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="53f1b-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53f1b-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="53f1b-132">TAPI version</span></span><br/> | <span data-ttu-id="53f1b-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="53f1b-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="53f1b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53f1b-134">Header</span></span><br/>       | <dl> <span data-ttu-id="53f1b-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f1b-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="53f1b-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="53f1b-136">Library</span></span><br/>      | <dl> <span data-ttu-id="53f1b-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53f1b-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="53f1b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="53f1b-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="53f1b-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53f1b-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f1b-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53f1b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f1b-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="53f1b-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> <dt>

[<span data-ttu-id="53f1b-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="53f1b-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




