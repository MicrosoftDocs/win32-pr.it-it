---
description: Il \_ metodo Put TransportProtocol imposta il protocollo di trasporto.
ms.assetid: d2f74d4a-a65d-4829-ad17-7548ef06cfeb
title: 'ITMedia: metodo:p ut_TransportProtocol (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6b4228a5d2a6ea49ae3f87b9306ea80e94fc36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328733"
---
# <a name="itmediaput_transportprotocol-method"></a><span data-ttu-id="767ef-103">ITMedia::p UT \_ TransportProtocol metodo</span><span class="sxs-lookup"><span data-stu-id="767ef-103">ITMedia::put\_TransportProtocol method</span></span>

<span data-ttu-id="767ef-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="767ef-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="767ef-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="767ef-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="767ef-106">Il metodo **put \_ TransportProtocol** imposta il protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="767ef-106">The **put\_TransportProtocol** method sets the transport protocol.</span></span> <span data-ttu-id="767ef-107">Questo valore viene specificato in aggiunta al formato multimediale, in modo che lo stesso formato multimediale standard possa essere trasferito su protocolli di trasporto diversi anche quando il protocollo di rete è lo stesso, ad esempio con l'audio PCM IVA e l'audio PCM RTP.</span><span class="sxs-lookup"><span data-stu-id="767ef-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="767ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="767ef-108">Syntax</span></span>


```C++
HRESULT put_TransportProtocol(
  [in] BSTR pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="767ef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="767ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="767ef-110">*pProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="767ef-110">*pProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="767ef-111">Puntatore a un **BSTR** che contiene il protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="767ef-111">Pointer to a **BSTR** containing the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="767ef-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="767ef-112">Return value</span></span>

<span data-ttu-id="767ef-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="767ef-113">This method can return one of these values.</span></span>



| <span data-ttu-id="767ef-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="767ef-114">Return code</span></span>                                                                                   | <span data-ttu-id="767ef-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="767ef-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="767ef-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="767ef-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="767ef-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="767ef-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="767ef-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="767ef-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="767ef-119">Il parametro *pProtocol* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="767ef-119">The *pProtocol* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="767ef-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="767ef-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="767ef-121">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="767ef-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="767ef-122"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="767ef-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="767ef-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="767ef-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="767ef-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="767ef-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="767ef-125">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="767ef-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="767ef-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="767ef-126">Remarks</span></span>

<span data-ttu-id="767ef-127">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PProtocol* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="767ef-127">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pProtocol* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="767ef-128">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="767ef-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="767ef-129">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="767ef-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="767ef-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="767ef-130">Requirements</span></span>



| <span data-ttu-id="767ef-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="767ef-131">Requirement</span></span> | <span data-ttu-id="767ef-132">Valore</span><span class="sxs-lookup"><span data-stu-id="767ef-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="767ef-133">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="767ef-133">TAPI version</span></span><br/> | <span data-ttu-id="767ef-134">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="767ef-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="767ef-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="767ef-135">Header</span></span><br/>       | <dl> <span data-ttu-id="767ef-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="767ef-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="767ef-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="767ef-137">Library</span></span><br/>      | <dl> <span data-ttu-id="767ef-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="767ef-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="767ef-139">DLL</span><span class="sxs-lookup"><span data-stu-id="767ef-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="767ef-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="767ef-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="767ef-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="767ef-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767ef-142">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="767ef-142">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="767ef-143">**ITMedia:: Get \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="767ef-143">**ITMedia::get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md)
</dt> </dl>

 

