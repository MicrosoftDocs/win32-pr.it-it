---
description: Il \_ metodo Get Item ottiene un puntatore ITmedia corrispondente all'indice specificato.
ms.assetid: ad218357-82c8-4fcb-b71b-ba17564a5ca5
title: 'Metodo ITMediaCollection:: get_Item (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c68f3571dbd1f66e325dd7fa1bb30dfe6d6bc35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330264"
---
# <a name="itmediacollectionget_item-method"></a><span data-ttu-id="0e27b-103">Metodo ITMediaCollection:: Get \_ Item</span><span class="sxs-lookup"><span data-stu-id="0e27b-103">ITMediaCollection::get\_Item method</span></span>

<span data-ttu-id="0e27b-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0e27b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0e27b-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0e27b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0e27b-106">Il metodo **get \_ Item** ottiene un puntatore [**ITmedia**](itmedia.md) corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="0e27b-106">The **get\_Item** method gets an [**ITMedia**](itmedia.md) pointer corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e27b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e27b-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG    Index,
  [out] ITMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0e27b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e27b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e27b-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0e27b-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e27b-110">Indice dell'elemento multimediale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0e27b-110">Index of media item to get.</span></span>

</dd> <dt>

<span data-ttu-id="0e27b-111">*pval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0e27b-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e27b-112">Puntatore all'interfaccia [**ITmedia**](itmedia.md) per l'elemento desiderato.</span><span class="sxs-lookup"><span data-stu-id="0e27b-112">Pointer to the [**ITMedia**](itmedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e27b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e27b-113">Return value</span></span>

<span data-ttu-id="0e27b-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="0e27b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0e27b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0e27b-115">Value</span></span>                                                                                         | <span data-ttu-id="0e27b-116">Significato</span><span class="sxs-lookup"><span data-stu-id="0e27b-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0e27b-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e27b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0e27b-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0e27b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0e27b-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="0e27b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0e27b-120">Il parametro *pval* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="0e27b-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="0e27b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0e27b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0e27b-122">Il parametro di *Indice* non è valido.</span><span class="sxs-lookup"><span data-stu-id="0e27b-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="0e27b-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0e27b-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0e27b-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0e27b-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0e27b-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="0e27b-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0e27b-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0e27b-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0e27b-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0e27b-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0e27b-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="0e27b-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0e27b-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e27b-129">Remarks</span></span>

<span data-ttu-id="0e27b-130">La maggior parte degli elenchi C e C++ sono basati su 0, ma questo indice è basato su 1 per la compatibilità con Visual Basic, ovvero il primo elemento ha un numero di indice pari a 1.</span><span class="sxs-lookup"><span data-stu-id="0e27b-130">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e27b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e27b-131">Requirements</span></span>



| <span data-ttu-id="0e27b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e27b-132">Requirement</span></span> | <span data-ttu-id="0e27b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0e27b-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e27b-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0e27b-134">TAPI version</span></span><br/> | <span data-ttu-id="0e27b-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0e27b-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0e27b-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e27b-136">Header</span></span><br/>       | <dl> <span data-ttu-id="0e27b-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e27b-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e27b-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e27b-138">Library</span></span><br/>      | <dl> <span data-ttu-id="0e27b-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e27b-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0e27b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0e27b-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="0e27b-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e27b-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e27b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e27b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e27b-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="0e27b-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="0e27b-144">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="0e27b-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




