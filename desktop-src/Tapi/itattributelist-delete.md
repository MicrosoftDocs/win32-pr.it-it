---
description: Il metodo Delete Elimina l'attributo in corrispondenza dell'indice specificato.
ms.assetid: 6bc6f3d2-d630-4a00-9d74-fb5fa7626e3f
title: Metodo ITAttributeList::D Elimina (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729dd79b88198f671949aeb79caf06289abd9a75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332743"
---
# <a name="itattributelistdelete-method"></a><span data-ttu-id="c6fee-103">ITAttributeList::D Metodo Elimina</span><span class="sxs-lookup"><span data-stu-id="c6fee-103">ITAttributeList::Delete method</span></span>

<span data-ttu-id="c6fee-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c6fee-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c6fee-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c6fee-106">Il metodo **Delete** Elimina l'attributo in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="c6fee-106">The **Delete** method deletes the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6fee-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6fee-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="c6fee-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6fee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6fee-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-110">Indice dell'attributo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="c6fee-110">Index of the attribute to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6fee-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6fee-111">Return value</span></span>

<span data-ttu-id="c6fee-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c6fee-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c6fee-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c6fee-113">Return code</span></span>                                                                                   | <span data-ttu-id="c6fee-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6fee-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c6fee-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c6fee-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="c6fee-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c6fee-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c6fee-118">Il parametro di *Indice* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c6fee-118">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="c6fee-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c6fee-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c6fee-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c6fee-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c6fee-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c6fee-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c6fee-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c6fee-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="c6fee-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="c6fee-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6fee-125">Requirements</span></span>



| <span data-ttu-id="c6fee-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6fee-126">Requirement</span></span> | <span data-ttu-id="c6fee-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c6fee-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6fee-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="c6fee-128">TAPI version</span></span><br/> | <span data-ttu-id="c6fee-129">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c6fee-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c6fee-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6fee-130">Header</span></span><br/>       | <dl> <span data-ttu-id="c6fee-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6fee-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6fee-132">Library</span></span><br/>      | <dl> <span data-ttu-id="c6fee-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c6fee-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c6fee-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="c6fee-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6fee-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6fee-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6fee-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="c6fee-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

 




