---
description: Il metodo Delete Elimina il supporto corrispondente all'indice specificato.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: Metodo ITMediaCollection::D Elimina (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329735"
---
# <a name="itmediacollectiondelete-method"></a><span data-ttu-id="8f822-103">ITMediaCollection::D Metodo Elimina</span><span class="sxs-lookup"><span data-stu-id="8f822-103">ITMediaCollection::Delete method</span></span>

<span data-ttu-id="8f822-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8f822-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8f822-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8f822-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8f822-106">Il metodo **Delete** Elimina il supporto corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="8f822-106">The **Delete** method deletes the media corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f822-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f822-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="8f822-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f822-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f822-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8f822-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f822-110">Indice del supporto da eliminare.</span><span class="sxs-lookup"><span data-stu-id="8f822-110">Index of media to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f822-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f822-111">Return value</span></span>

<span data-ttu-id="8f822-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="8f822-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8f822-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8f822-113">Return code</span></span>                                                                                                                              | <span data-ttu-id="8f822-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f822-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f822-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8f822-115"><dt>**S\_OK**</dt></span></span> </dl>                                                     | <span data-ttu-id="8f822-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8f822-116">Method succeeded.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="8f822-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8f822-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                             | <span data-ttu-id="8f822-118">Il valore del parametro *index* è minore di 1 o maggiore del numero corrente di elementi.</span><span class="sxs-lookup"><span data-stu-id="8f822-118">The *Index* parameter has a value less than 1 or greater than the current number of elements.</span></span><br/> |
| <dl> <span data-ttu-id="8f822-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8f822-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                            | <span data-ttu-id="8f822-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8f822-120">Insufficient memory exists to perform the operation.</span></span><br/>                                          |
| <dl> <span data-ttu-id="8f822-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="8f822-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                                   | <span data-ttu-id="8f822-122">Errore interno (dovrebbe verificarsi solo se una chiamata precedente ha restituito un errore).</span><span class="sxs-lookup"><span data-stu-id="8f822-122">Internal error (should only occur if a previous call returned an error).</span></span><br/>                      |
| <dl> <span data-ttu-id="8f822-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8f822-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                                | <span data-ttu-id="8f822-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="8f822-124">This method is not yet implemented.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="8f822-125"><dt>**HRESULT \_ dal \_ codice di errore \_ ( \_ BLOB SDPBLB conf \_ \_ distrutto)**</dt></span><span class="sxs-lookup"><span data-stu-id="8f822-125"><dt>**HRESULT\_FROM\_ERROR\_CODE(SDPBLB\_CONF\_BLOB\_DESTROYED)**</dt></span></span> </dl> | <span data-ttu-id="8f822-126">Il BLOB SDP non esiste.</span><span class="sxs-lookup"><span data-stu-id="8f822-126">The SDP blob doesn't exist.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="8f822-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f822-127">Remarks</span></span>

<span data-ttu-id="8f822-128">La maggior parte degli elenchi C e C++ sono basati su 0, ma questo indice è basato su 1 per la compatibilità con Visual Basic, ovvero il primo elemento ha un numero di indice pari a 1.</span><span class="sxs-lookup"><span data-stu-id="8f822-128">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f822-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f822-129">Requirements</span></span>



| <span data-ttu-id="8f822-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f822-130">Requirement</span></span> | <span data-ttu-id="8f822-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8f822-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f822-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="8f822-132">TAPI version</span></span><br/> | <span data-ttu-id="8f822-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8f822-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8f822-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f822-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8f822-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f822-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f822-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="8f822-136">Library</span></span><br/>      | <dl> <span data-ttu-id="8f822-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f822-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8f822-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8f822-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="8f822-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f822-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f822-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f822-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f822-141">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="8f822-141">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




