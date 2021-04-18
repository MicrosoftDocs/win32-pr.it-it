---
description: Il \_ metodo Get ConferenceBlob ottiene un puntatore al BLOB di conferenza testuale attualmente archiviato nell'oggetto BLOB della conferenza.
ms.assetid: eb378f84-11bc-4f6e-9133-bc303e07eb53
title: 'Metodo ITConferenceBlob:: get_ConferenceBlob (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5642f60f7abc1cb10734de1897d35bd5222dd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328235"
---
# <a name="itconferenceblobget_conferenceblob-method"></a><span data-ttu-id="17894-103">Metodo ITConferenceBlob:: Get \_ ConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="17894-103">ITConferenceBlob::get\_ConferenceBlob method</span></span>

<span data-ttu-id="17894-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="17894-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="17894-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="17894-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="17894-106">Il metodo **get \_ ConferenceBlob** ottiene un puntatore al BLOB di conferenza testuale attualmente archiviato nell'oggetto BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="17894-106">The **get\_ConferenceBlob** method gets a pointer to the textual conference blob currently stored in the conference blob object.</span></span>

## <a name="syntax"></a><span data-ttu-id="17894-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17894-107">Syntax</span></span>


```C++
HRESULT get_ConferenceBlob(
  [out] BSTR *ppBlob
);
```



## <a name="parameters"></a><span data-ttu-id="17894-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="17894-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17894-109">*ppBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="17894-109">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17894-110">Puntatore a un **BSTR** che contiene il BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="17894-110">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17894-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17894-111">Return value</span></span>

<span data-ttu-id="17894-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="17894-112">This method can return one of these values.</span></span>



| <span data-ttu-id="17894-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="17894-113">Return code</span></span>                                                                                   | <span data-ttu-id="17894-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17894-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="17894-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17894-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="17894-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="17894-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="17894-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="17894-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="17894-118">Il parametro *ppBlob* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="17894-118">The *ppBlob* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="17894-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="17894-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="17894-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="17894-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="17894-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="17894-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="17894-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="17894-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="17894-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="17894-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="17894-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="17894-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="17894-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="17894-125">Remarks</span></span>

<span data-ttu-id="17894-126">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppBlob* .</span><span class="sxs-lookup"><span data-stu-id="17894-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppBlob* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="17894-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17894-127">Requirements</span></span>



| <span data-ttu-id="17894-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="17894-128">Requirement</span></span> | <span data-ttu-id="17894-129">Valore</span><span class="sxs-lookup"><span data-stu-id="17894-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17894-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="17894-130">TAPI version</span></span><br/> | <span data-ttu-id="17894-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="17894-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="17894-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17894-132">Header</span></span><br/>       | <dl> <span data-ttu-id="17894-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="17894-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="17894-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="17894-134">Library</span></span><br/>      | <dl> <span data-ttu-id="17894-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17894-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="17894-136">DLL</span><span class="sxs-lookup"><span data-stu-id="17894-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="17894-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17894-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17894-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17894-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17894-139">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="17894-139">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="17894-140">**\_set di caratteri BLOB \_**</span><span class="sxs-lookup"><span data-stu-id="17894-140">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

