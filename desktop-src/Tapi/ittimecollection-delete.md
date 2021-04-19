---
description: Il metodo Delete Elimina un componente ITTime.
ms.assetid: 0445d659-7b83-4462-b199-511fd8270f32
title: Metodo ITTimeCollection::D Elimina (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9aad562660a2d563193e5074b52f4d1a513bb39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326754"
---
# <a name="ittimecollectiondelete-method"></a><span data-ttu-id="bb9d0-103">ITTimeCollection::D Metodo Elimina</span><span class="sxs-lookup"><span data-stu-id="bb9d0-103">ITTimeCollection::Delete method</span></span>

<span data-ttu-id="bb9d0-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bb9d0-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bb9d0-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bb9d0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bb9d0-106">Il metodo **Delete** Elimina un componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="bb9d0-106">The **Delete** method deletes an [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb9d0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb9d0-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="bb9d0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb9d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb9d0-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="bb9d0-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb9d0-110">Indice del componente [**ITTime**](ittime.md) da eliminare.</span><span class="sxs-lookup"><span data-stu-id="bb9d0-110">Index of the [**ITTime**](ittime.md) component to be deleted.</span></span> <span data-ttu-id="bb9d0-111">La matrice di indici è in base uno.</span><span class="sxs-lookup"><span data-stu-id="bb9d0-111">(The index array is one-based.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb9d0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb9d0-112">Return value</span></span>

<span data-ttu-id="bb9d0-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="bb9d0-113">This method can return one of these values.</span></span>



| <span data-ttu-id="bb9d0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="bb9d0-114">Value</span></span>                                                                                         | <span data-ttu-id="bb9d0-115">Significato</span><span class="sxs-lookup"><span data-stu-id="bb9d0-115">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bb9d0-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb9d0-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bb9d0-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bb9d0-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bb9d0-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bb9d0-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bb9d0-119">Il parametro di *Indice* non è valido.</span><span class="sxs-lookup"><span data-stu-id="bb9d0-119">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="bb9d0-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="bb9d0-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bb9d0-121">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bb9d0-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bb9d0-122"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="bb9d0-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="bb9d0-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="bb9d0-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bb9d0-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="bb9d0-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="bb9d0-125">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="bb9d0-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="bb9d0-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb9d0-126">Requirements</span></span>



| <span data-ttu-id="bb9d0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb9d0-127">Requirement</span></span> | <span data-ttu-id="bb9d0-128">Valore</span><span class="sxs-lookup"><span data-stu-id="bb9d0-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9d0-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="bb9d0-129">TAPI version</span></span><br/> | <span data-ttu-id="bb9d0-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bb9d0-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bb9d0-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb9d0-131">Header</span></span><br/>       | <dl> <span data-ttu-id="bb9d0-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb9d0-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb9d0-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb9d0-133">Library</span></span><br/>      | <dl> <span data-ttu-id="bb9d0-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb9d0-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bb9d0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bb9d0-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="bb9d0-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb9d0-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb9d0-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb9d0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9d0-138">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="bb9d0-138">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="bb9d0-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="bb9d0-139">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




