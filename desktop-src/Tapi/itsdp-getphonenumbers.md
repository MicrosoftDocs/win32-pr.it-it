---
description: Il metodo GetPhoneNumbers ottiene una matrice di numeri di telefono associati a un BLOB di conferenze.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'Metodo ITSdp:: GetPhoneNumbers (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332822"
---
# <a name="itsdpgetphonenumbers-method"></a><span data-ttu-id="fa759-103">Metodo ITSdp:: GetPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="fa759-103">ITSdp::GetPhoneNumbers method</span></span>

<span data-ttu-id="fa759-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fa759-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fa759-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="fa759-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fa759-106">Il metodo **GetPhoneNumbers** ottiene una matrice di numeri di telefono associati a un BLOB di conferenze.</span><span class="sxs-lookup"><span data-stu-id="fa759-106">The **GetPhoneNumbers** method gets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa759-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa759-107">Syntax</span></span>


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="fa759-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa759-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa759-109">*pNumbers* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fa759-109">*pNumbers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa759-110">Puntatore **Variant** a un SAFEARRAY di **BSTR** s che elenca i numeri di telefono.</span><span class="sxs-lookup"><span data-stu-id="fa759-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="fa759-111">*pNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fa759-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa759-112">Puntatore **Variant** a un SAFEARRAY di nomi di elenco di **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="fa759-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa759-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa759-113">Return value</span></span>

<span data-ttu-id="fa759-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="fa759-114">This method can return one of these values.</span></span>



| <span data-ttu-id="fa759-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fa759-115">Return code</span></span>                                                                                   | <span data-ttu-id="fa759-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa759-116">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa759-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa759-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fa759-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="fa759-118">Method succeeded.</span></span><br/>                                            |
| <dl> <span data-ttu-id="fa759-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="fa759-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fa759-120">Il parametro *pNumbers* o *pNames* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="fa759-120">The *pNumbers* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="fa759-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="fa759-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fa759-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa759-122">Insufficient memory exists to perform the operation.</span></span><br/>         |
| <dl> <span data-ttu-id="fa759-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="fa759-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fa759-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="fa759-124">Unspecified error.</span></span><br/>                                           |
| <dl> <span data-ttu-id="fa759-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="fa759-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fa759-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="fa759-126">This method is not yet implemented.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="fa759-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa759-127">Remarks</span></span>

<span data-ttu-id="fa759-128">Gli elenchi a cui *pNumbers* e *pNames* puntano sono della stessa lunghezza.</span><span class="sxs-lookup"><span data-stu-id="fa759-128">The lists that *pNumbers* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa759-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa759-129">Requirements</span></span>



| <span data-ttu-id="fa759-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa759-130">Requirement</span></span> | <span data-ttu-id="fa759-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fa759-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa759-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="fa759-132">TAPI version</span></span><br/> | <span data-ttu-id="fa759-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="fa759-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fa759-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa759-134">Header</span></span><br/>       | <dl> <span data-ttu-id="fa759-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa759-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa759-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa759-136">Library</span></span><br/>      | <dl> <span data-ttu-id="fa759-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa759-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fa759-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fa759-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="fa759-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa759-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa759-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa759-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa759-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="fa759-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




