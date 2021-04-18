---
description: Il metodo GetEmailNames ottiene una matrice di nomi di posta elettronica associati al BLOB della conferenza.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'Metodo ITSdp:: GetEmailNames (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f0200b5cc6ea0422f47a323cd1c57d7e0f9a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324761"
---
# <a name="itsdpgetemailnames-method"></a><span data-ttu-id="01fc6-103">Metodo ITSdp:: GetEmailNames</span><span class="sxs-lookup"><span data-stu-id="01fc6-103">ITSdp::GetEmailNames method</span></span>

<span data-ttu-id="01fc6-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="01fc6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="01fc6-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="01fc6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="01fc6-106">Il metodo **GetEmailNames** ottiene una matrice di nomi di posta elettronica associati al BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="01fc6-106">The **GetEmailNames** method gets an array of e-mail names associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="01fc6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01fc6-107">Syntax</span></span>


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="01fc6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="01fc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01fc6-109">*pAddresses* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="01fc6-109">*pAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01fc6-110">Puntatore **Variant** a un SAFEARRAY di **BSTR** s che elenca indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="01fc6-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="01fc6-111">*pNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="01fc6-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01fc6-112">Puntatore **Variant** a un SAFEARRAY di nomi di elenco di **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="01fc6-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01fc6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01fc6-113">Return value</span></span>

<span data-ttu-id="01fc6-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="01fc6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="01fc6-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="01fc6-115">Return code</span></span>                                                                                   | <span data-ttu-id="01fc6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01fc6-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01fc6-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01fc6-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="01fc6-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="01fc6-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="01fc6-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="01fc6-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="01fc6-120">Il parametro *pAddresses* o *pNames* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="01fc6-120">The *pAddresses* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="01fc6-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="01fc6-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="01fc6-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="01fc6-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="01fc6-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="01fc6-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="01fc6-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="01fc6-124">Unspecified error.</span></span><br/>                                             |
| <dl> <span data-ttu-id="01fc6-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="01fc6-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="01fc6-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="01fc6-126">This method is not yet implemented.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="01fc6-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="01fc6-127">Remarks</span></span>

<span data-ttu-id="01fc6-128">Gli elenchi a cui *pAddresses* e *pNames* puntano sono della stessa lunghezza.</span><span class="sxs-lookup"><span data-stu-id="01fc6-128">The lists that *pAddresses* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="01fc6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01fc6-129">Requirements</span></span>



| <span data-ttu-id="01fc6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="01fc6-130">Requirement</span></span> | <span data-ttu-id="01fc6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="01fc6-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01fc6-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="01fc6-132">TAPI version</span></span><br/> | <span data-ttu-id="01fc6-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="01fc6-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="01fc6-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01fc6-134">Header</span></span><br/>       | <dl> <span data-ttu-id="01fc6-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="01fc6-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="01fc6-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="01fc6-136">Library</span></span><br/>      | <dl> <span data-ttu-id="01fc6-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01fc6-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="01fc6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="01fc6-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="01fc6-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01fc6-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01fc6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01fc6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01fc6-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="01fc6-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




