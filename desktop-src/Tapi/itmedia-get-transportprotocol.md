---
description: Il \_ metodo Get TransportProtocol ottiene il protocollo di trasporto.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'Metodo ITMedia:: get_TransportProtocol (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf2bc66a98e181674bbf6f7956579bbaa0b5a72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324885"
---
# <a name="itmediaget_transportprotocol-method"></a><span data-ttu-id="7ebe4-103">Metodo ITMedia:: Get \_ TransportProtocol</span><span class="sxs-lookup"><span data-stu-id="7ebe4-103">ITMedia::get\_TransportProtocol method</span></span>

<span data-ttu-id="7ebe4-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7ebe4-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="7ebe4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7ebe4-106">Il metodo **get \_ TransportProtocol** ottiene il protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-106">The **get\_TransportProtocol** method gets the transport protocol.</span></span> <span data-ttu-id="7ebe4-107">Questo valore viene specificato in aggiunta al formato multimediale, in modo che lo stesso formato multimediale standard possa essere trasferito su protocolli di trasporto diversi anche quando il protocollo di rete è lo stesso, ad esempio con l'audio PCM IVA e l'audio PCM RTP.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ebe4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ebe4-108">Syntax</span></span>


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="7ebe4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ebe4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ebe4-110">*ppProtocol* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ebe4-110">*ppProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebe4-111">Puntatore alla rappresentazione **BSTR** del protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-111">Pointer to the **BSTR** representation of the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ebe4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ebe4-112">Return value</span></span>

<span data-ttu-id="7ebe4-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-113">This method can return one of these values.</span></span>



| <span data-ttu-id="7ebe4-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7ebe4-114">Return code</span></span>                                                                                   | <span data-ttu-id="7ebe4-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ebe4-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7ebe4-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebe4-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7ebe4-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7ebe4-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebe4-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7ebe4-119">Il parametro *ppProtocol* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-119">The *ppProtocol* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="7ebe4-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebe4-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7ebe4-121">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7ebe4-122"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebe4-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7ebe4-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7ebe4-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebe4-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7ebe4-125">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="7ebe4-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="7ebe4-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ebe4-126">Remarks</span></span>

<span data-ttu-id="7ebe4-127">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppProtocol* .</span><span class="sxs-lookup"><span data-stu-id="7ebe4-127">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppProtocol* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ebe4-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ebe4-128">Requirements</span></span>



| <span data-ttu-id="7ebe4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ebe4-129">Requirement</span></span> | <span data-ttu-id="7ebe4-130">Valore</span><span class="sxs-lookup"><span data-stu-id="7ebe4-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ebe4-131">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7ebe4-131">TAPI version</span></span><br/> | <span data-ttu-id="7ebe4-132">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7ebe4-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7ebe4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ebe4-133">Header</span></span><br/>       | <dl> <span data-ttu-id="7ebe4-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ebe4-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ebe4-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ebe4-135">Library</span></span><br/>      | <dl> <span data-ttu-id="7ebe4-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ebe4-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7ebe4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7ebe4-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="7ebe4-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ebe4-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ebe4-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ebe4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ebe4-140">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="7ebe4-140">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="7ebe4-141">**ITMedia::p UT \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="7ebe4-141">**ITMedia::put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md)
</dt> </dl>

 

