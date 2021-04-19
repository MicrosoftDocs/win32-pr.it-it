---
description: Il metodo Create crea un nuovo componente ITTime.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: 'Metodo ITTimeCollection:: Create (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df62bbc8f1ad2a24a9b80a7f5d0a25bc01f713d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326758"
---
# <a name="ittimecollectioncreate-method"></a><span data-ttu-id="177bd-103">Metodo ITTimeCollection:: create</span><span class="sxs-lookup"><span data-stu-id="177bd-103">ITTimeCollection::Create method</span></span>

<span data-ttu-id="177bd-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="177bd-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="177bd-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="177bd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="177bd-106">Il metodo **create** crea un nuovo componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="177bd-106">The **Create** method creates a new [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="177bd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="177bd-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a><span data-ttu-id="177bd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="177bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="177bd-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="177bd-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="177bd-110">Indice dell'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="177bd-110">Index of the item to create.</span></span> <span data-ttu-id="177bd-111">La matrice di indici è in base uno.</span><span class="sxs-lookup"><span data-stu-id="177bd-111">(The index array is one-based.)</span></span>

</dd> <dt>

<span data-ttu-id="177bd-112">*ppTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="177bd-112">*ppTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="177bd-113">Puntatore al componente b creato.</span><span class="sxs-lookup"><span data-stu-id="177bd-113">Pointer to the b component created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="177bd-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="177bd-114">Return value</span></span>

<span data-ttu-id="177bd-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="177bd-115">This method can return one of these values.</span></span>



| <span data-ttu-id="177bd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="177bd-116">Value</span></span>                                                                                         | <span data-ttu-id="177bd-117">Significato</span><span class="sxs-lookup"><span data-stu-id="177bd-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="177bd-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="177bd-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="177bd-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="177bd-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="177bd-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="177bd-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="177bd-121">Il parametro *ppTime* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="177bd-121">The *ppTime* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="177bd-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="177bd-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="177bd-123">Il parametro di *Indice* non è valido.</span><span class="sxs-lookup"><span data-stu-id="177bd-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="177bd-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="177bd-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="177bd-125">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="177bd-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="177bd-126"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="177bd-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="177bd-127">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="177bd-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="177bd-128"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="177bd-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="177bd-129">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="177bd-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="177bd-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="177bd-130">Remarks</span></span>

<span data-ttu-id="177bd-131">TAPI chiama il metodo **AddRef** sull'interfaccia [**ITTime**](ittime.md) restituita da **ITTimeCollection:: create**.</span><span class="sxs-lookup"><span data-stu-id="177bd-131">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **ITTimeCollection::Create**.</span></span> <span data-ttu-id="177bd-132">Per liberare le risorse associate, l'applicazione deve chiamare **Release** sull'interfaccia v.</span><span class="sxs-lookup"><span data-stu-id="177bd-132">The application must call **Release** on the v interface to free resources associated with it.</span></span>

<span data-ttu-id="177bd-133">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="177bd-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="177bd-134">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="177bd-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="177bd-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="177bd-135">Requirements</span></span>



| <span data-ttu-id="177bd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="177bd-136">Requirement</span></span> | <span data-ttu-id="177bd-137">Valore</span><span class="sxs-lookup"><span data-stu-id="177bd-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="177bd-138">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="177bd-138">TAPI version</span></span><br/> | <span data-ttu-id="177bd-139">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="177bd-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="177bd-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="177bd-140">Header</span></span><br/>       | <dl> <span data-ttu-id="177bd-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="177bd-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="177bd-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="177bd-142">Library</span></span><br/>      | <dl> <span data-ttu-id="177bd-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="177bd-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="177bd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="177bd-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="177bd-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="177bd-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="177bd-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="177bd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177bd-147">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="177bd-147">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="177bd-148">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="177bd-148">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




