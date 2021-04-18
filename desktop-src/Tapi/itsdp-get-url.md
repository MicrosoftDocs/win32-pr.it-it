---
description: Il \_ metodo Get URL ottiene l'URL.
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: 'Metodo ITSdp:: get_Url (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a207c158d405ac0931e42aa19995d1d4b3078fd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333957"
---
# <a name="itsdpget_url-method"></a><span data-ttu-id="bb714-103">Metodo ITSdp:: Get \_ URL</span><span class="sxs-lookup"><span data-stu-id="bb714-103">ITSdp::get\_Url method</span></span>

<span data-ttu-id="bb714-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bb714-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bb714-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bb714-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bb714-106">Il metodo **get \_ URL** Ottiene l'URL.</span><span class="sxs-lookup"><span data-stu-id="bb714-106">The **get\_Url** method gets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb714-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb714-107">Syntax</span></span>


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a><span data-ttu-id="bb714-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb714-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb714-109">*ppUrl* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bb714-109">*ppUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb714-110">Puntatore a una rappresentazione **BSTR** dell'URL.</span><span class="sxs-lookup"><span data-stu-id="bb714-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb714-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb714-111">Return value</span></span>

<span data-ttu-id="bb714-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="bb714-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bb714-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bb714-113">Return code</span></span>                                                                                   | <span data-ttu-id="bb714-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb714-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bb714-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb714-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bb714-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bb714-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bb714-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="bb714-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bb714-118">Il parametro *ppUrl* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="bb714-118">The *ppUrl* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="bb714-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="bb714-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bb714-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bb714-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bb714-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="bb714-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="bb714-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="bb714-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bb714-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="bb714-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="bb714-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="bb714-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="bb714-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb714-125">Remarks</span></span>

<span data-ttu-id="bb714-126">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppUrl* .</span><span class="sxs-lookup"><span data-stu-id="bb714-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppUrl* parameter.</span></span>

<span data-ttu-id="bb714-127">Un URL viene in genere usato per fare riferimento a una pagina Web contenente risorse aggiuntive o informazioni complementari su una conferenza.</span><span class="sxs-lookup"><span data-stu-id="bb714-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb714-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb714-128">Requirements</span></span>



| <span data-ttu-id="bb714-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb714-129">Requirement</span></span> | <span data-ttu-id="bb714-130">Valore</span><span class="sxs-lookup"><span data-stu-id="bb714-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb714-131">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="bb714-131">TAPI version</span></span><br/> | <span data-ttu-id="bb714-132">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bb714-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bb714-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb714-133">Header</span></span><br/>       | <dl> <span data-ttu-id="bb714-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb714-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb714-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb714-135">Library</span></span><br/>      | <dl> <span data-ttu-id="bb714-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb714-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bb714-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bb714-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="bb714-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb714-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb714-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb714-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb714-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="bb714-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="bb714-141">**ITSdp: URL UT:p \_**</span><span class="sxs-lookup"><span data-stu-id="bb714-141">**ITSdp::put\_Url**</span></span>](itsdp-put-url.md)
</dt> </dl>

 

