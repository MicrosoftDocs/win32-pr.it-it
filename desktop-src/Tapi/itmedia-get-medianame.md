---
description: Il \_ metodo Get MEDIANAME ottiene il nome del supporto. I supporti definiti sono audio, video, lavagna, testo e dati.
ms.assetid: 4afb24f9-582e-420d-8bda-772a3dc4d96c
title: 'Metodo ITMedia:: get_MediaName (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9152994eac98d5e846ac147072a51a3334930da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332154"
---
# <a name="itmediaget_medianame-method"></a><span data-ttu-id="e0363-104">Metodo ITMedia:: Get \_ MEDIANAME</span><span class="sxs-lookup"><span data-stu-id="e0363-104">ITMedia::get\_MediaName method</span></span>

<span data-ttu-id="e0363-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e0363-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e0363-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e0363-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e0363-107">Il metodo **get \_ MEDIANAME** ottiene il nome del supporto.</span><span class="sxs-lookup"><span data-stu-id="e0363-107">The **get\_MediaName** method gets the media name.</span></span> <span data-ttu-id="e0363-108">I supporti definiti sono audio, video, lavagna, testo e dati.</span><span class="sxs-lookup"><span data-stu-id="e0363-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0363-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0363-109">Syntax</span></span>


```C++
HRESULT get_MediaName(
  [out] BSTR *ppMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="e0363-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0363-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0363-111">*ppMediaName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e0363-111">*ppMediaName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0363-112">Puntatore a un **BSTR** che contiene il nome del supporto, ad esempio audio.</span><span class="sxs-lookup"><span data-stu-id="e0363-112">Pointer to a **BSTR** containing the name of the media, such as audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0363-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0363-113">Return value</span></span>

<span data-ttu-id="e0363-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="e0363-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e0363-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e0363-115">Return code</span></span>                                                                                   | <span data-ttu-id="e0363-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0363-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e0363-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0363-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e0363-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e0363-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e0363-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0363-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e0363-120">Il parametro *ppMediaName* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="e0363-120">The *ppMediaName* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="e0363-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="e0363-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e0363-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e0363-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e0363-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="e0363-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e0363-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="e0363-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e0363-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e0363-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e0363-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="e0363-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e0363-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0363-127">Remarks</span></span>

<span data-ttu-id="e0363-128">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppMediaName* .</span><span class="sxs-lookup"><span data-stu-id="e0363-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0363-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0363-129">Requirements</span></span>



| <span data-ttu-id="e0363-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0363-130">Requirement</span></span> | <span data-ttu-id="e0363-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e0363-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0363-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e0363-132">TAPI version</span></span><br/> | <span data-ttu-id="e0363-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e0363-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e0363-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0363-134">Header</span></span><br/>       | <dl> <span data-ttu-id="e0363-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0363-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0363-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0363-136">Library</span></span><br/>      | <dl> <span data-ttu-id="e0363-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0363-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e0363-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e0363-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="e0363-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0363-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0363-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0363-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0363-141">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="e0363-141">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="e0363-142">**ITMedia::p UT \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="e0363-142">**ITMedia::put\_MediaName**</span></span>](itmedia-put-medianame.md)
</dt> </dl>

 

