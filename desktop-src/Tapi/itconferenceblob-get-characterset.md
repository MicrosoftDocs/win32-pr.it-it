---
description: Il \_ metodo Get charactert ottiene un \_ \_ descrittore del set di caratteri BLOB del set di caratteri usato nel BLOB della conferenza corrente.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'Metodo ITConferenceBlob:: get_CharacterSet (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328236"
---
# <a name="itconferenceblobget_characterset-method"></a><span data-ttu-id="96151-103">Metodo ITConferenceBlob:: Get \_ charactert</span><span class="sxs-lookup"><span data-stu-id="96151-103">ITConferenceBlob::get\_CharacterSet method</span></span>

<span data-ttu-id="96151-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="96151-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="96151-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="96151-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="96151-106">Il metodo **get \_ charactert** ottiene un descrittore del [**\_ \_ set di caratteri BLOB**](blob-character-set.md) del set di caratteri usato nel BLOB della conferenza corrente.</span><span class="sxs-lookup"><span data-stu-id="96151-106">The **get\_CharacterSet** method gets a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set used in the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="96151-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96151-107">Syntax</span></span>


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a><span data-ttu-id="96151-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="96151-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96151-109">*pCharacterSet* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="96151-109">*pCharacterSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96151-110">Puntatore a un descrittore del [**\_ \_ set di caratteri BLOB**](blob-character-set.md) del set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="96151-110">Pointer to a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96151-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96151-111">Return value</span></span>

<span data-ttu-id="96151-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="96151-112">This method can return one of these values.</span></span>



| <span data-ttu-id="96151-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="96151-113">Return code</span></span>                                                                                                   | <span data-ttu-id="96151-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96151-114">Description</span></span>                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="96151-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="96151-115"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="96151-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="96151-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="96151-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="96151-117"><dt>**E\_POINTER**</dt></span></span> </dl>                     | <span data-ttu-id="96151-118">Il parametro *pCharacterSet* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="96151-118">The *pCharacterSet* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="96151-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="96151-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                 | <span data-ttu-id="96151-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="96151-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="96151-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="96151-121"><dt>**E\_FAIL**</dt></span></span> </dl>                        | <span data-ttu-id="96151-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="96151-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="96151-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="96151-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                     | <span data-ttu-id="96151-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="96151-124">This method is not yet implemented.</span></span><br/>                   |
| <dl> <span data-ttu-id="96151-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="96151-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                  | <span data-ttu-id="96151-126">*pCharacterSet* è **null**.</span><span class="sxs-lookup"><span data-stu-id="96151-126">*pCharacterSet* is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="96151-127"><dt>**HRESULT ERRORE \_ dati non validi \_**</dt></span><span class="sxs-lookup"><span data-stu-id="96151-127"><dt>**(HRESULT) ERROR\_INVALID\_DATA**</dt></span></span> </dl> | <span data-ttu-id="96151-128">Il set di caratteri corrente non è valido o non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="96151-128">The current character set is invalid or unavailable.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="96151-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96151-129">Requirements</span></span>



| <span data-ttu-id="96151-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="96151-130">Requirement</span></span> | <span data-ttu-id="96151-131">Valore</span><span class="sxs-lookup"><span data-stu-id="96151-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96151-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="96151-132">TAPI version</span></span><br/> | <span data-ttu-id="96151-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="96151-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="96151-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96151-134">Header</span></span><br/>       | <dl> <span data-ttu-id="96151-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="96151-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="96151-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="96151-136">Library</span></span><br/>      | <dl> <span data-ttu-id="96151-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96151-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="96151-138">DLL</span><span class="sxs-lookup"><span data-stu-id="96151-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="96151-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96151-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96151-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96151-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96151-141">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="96151-141">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="96151-142">**\_set di caratteri BLOB \_**</span><span class="sxs-lookup"><span data-stu-id="96151-142">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

 




