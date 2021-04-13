---
title: Funzione di callback PxeProviderRecvRequest
description: Chiamato quando viene ricevuta una richiesta da un client.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Funzione di callback PxeProviderRecvRequest servizi di distribuzione Windows
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400627"
---
# <a name="pxeproviderrecvrequest-callback-function"></a><span data-ttu-id="0cb10-104">Funzione di callback PxeProviderRecvRequest</span><span class="sxs-lookup"><span data-stu-id="0cb10-104">PxeProviderRecvRequest callback function</span></span>

<span data-ttu-id="0cb10-105">Chiamato quando viene ricevuta una richiesta da un client.</span><span class="sxs-lookup"><span data-stu-id="0cb10-105">Called when a request is received from a client.</span></span> <span data-ttu-id="0cb10-106">Questa funzione viene registrata chiamando la funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con il parametro *CallbackType* impostato su **Request PXE \_ callback \_ ricezione \_**.</span><span class="sxs-lookup"><span data-stu-id="0cb10-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_RECV\_REQUEST**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb10-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cb10-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a><span data-ttu-id="0cb10-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cb10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb10-109">*hClientRequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb10-109">*hClientRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb10-110">Handle per una richiesta ricevuta da un client.</span><span class="sxs-lookup"><span data-stu-id="0cb10-110">Handle to a request received from a client.</span></span>

</dd> <dt>

<span data-ttu-id="0cb10-111">*pPacket* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb10-111">*pPacket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb10-112">Puntatore al buffer di memoria che contiene il pacchetto ricevuto.</span><span class="sxs-lookup"><span data-stu-id="0cb10-112">Pointer to the memory buffer that contains the received packet.</span></span>

</dd> <dt>

<span data-ttu-id="0cb10-113">*uPacketLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb10-113">*uPacketLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb10-114">Lunghezza, in byte, del buffer a cui punta il parametro *pPacket* .</span><span class="sxs-lookup"><span data-stu-id="0cb10-114">Length, in bytes, of the buffer pointed to by the *pPacket* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0cb10-115">*pLocalAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb10-115">*pLocalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb10-116">Puntatore a una struttura di [**\_ indirizzi PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) che contiene l'indirizzo locale in cui è stato ricevuto il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0cb10-116">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the local address on which the packet was received.</span></span>

</dd> <dt>

<span data-ttu-id="0cb10-117">*pRemoteAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb10-117">*pRemoteAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb10-118">Puntatore a una struttura di [**\_ indirizzi PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) che contiene l'indirizzo di origine del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0cb10-118">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the source address of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="0cb10-119">*patto* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cb10-119">*pAction* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb10-120">Specifica l'azione che deve essere eseguita dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0cb10-120">Specifies the action that the system should take.</span></span>



| <span data-ttu-id="0cb10-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0cb10-121">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="0cb10-122">Significato</span><span class="sxs-lookup"><span data-stu-id="0cb10-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <span data-ttu-id="0cb10-123"><dt>**PXE \_ BA \_ avvio**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0cb10-123"><dt>**PXE\_BA\_NBP**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="0cb10-124">Il provider ha risposto a un client con un pacchetto di risposta DHCP standard che contiene un percorso del programma di avvio di rete.</span><span class="sxs-lookup"><span data-stu-id="0cb10-124">The provider replied to a client with a standard DHCP response packet that contains a path to the Network Boot Program.</span></span> <span data-ttu-id="0cb10-125">La restituzione di questa azione significa che il provider ha completato correttamente la richiesta del client chiamando la funzione [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) almeno una volta.</span><span class="sxs-lookup"><span data-stu-id="0cb10-125">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <span data-ttu-id="0cb10-126"><dt>**PXE \_ BA \_ personalizzata**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0cb10-126"><dt>**PXE\_BA\_CUSTOM**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="0cb10-127">Il provider ha risposto a un client usando una risposta personalizzata che non è conforme alle specifiche DHCP.</span><span class="sxs-lookup"><span data-stu-id="0cb10-127">The provider replied to a client by using a custom response that does not conform to DHCP specifications.</span></span> <span data-ttu-id="0cb10-128">La restituzione di questa azione significa che il provider ha completato correttamente la richiesta del client chiamando la funzione [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) almeno una volta.</span><span class="sxs-lookup"><span data-stu-id="0cb10-128">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <span data-ttu-id="0cb10-129"><dt>**PXE \_ BA \_ ignorare**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0cb10-129"><dt>**PXE\_BA\_IGNORE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="0cb10-130">Il provider non desidera servire la richiesta client e la richiesta non deve essere passata al provider successivo.</span><span class="sxs-lookup"><span data-stu-id="0cb10-130">The provider does not want to service the client request and the request should not be passed to the next provider.</span></span> <span data-ttu-id="0cb10-131">Tutte le risorse associate alla richiesta client vengono rilasciate e la richiesta del client viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0cb10-131">All resources associated with the client request are released and the client request is ignored.</span></span> <span data-ttu-id="0cb10-132">I provider possono anche usare questo valore se riconoscono il client ma la richiesta non è valida.</span><span class="sxs-lookup"><span data-stu-id="0cb10-132">Providers can also use this value if they recognize the client but the request was malformed.</span></span><br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <span data-ttu-id="0cb10-133"><dt>**PXE \_ BA \_ rifiutato**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0cb10-133"><dt>**PXE\_BA\_REJECTED**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="0cb10-134">Il provider non desidera servire la richiesta client.</span><span class="sxs-lookup"><span data-stu-id="0cb10-134">The provider does not want to service the client request.</span></span> <span data-ttu-id="0cb10-135">Il sistema passa la richiesta al provider successivo nell'elenco dei provider registrati.</span><span class="sxs-lookup"><span data-stu-id="0cb10-135">The system passes the request to the next provider in the list of registered providers.</span></span> <span data-ttu-id="0cb10-136">Se questo è l'ultimo provider nell'elenco, vengono rilasciate tutte le risorse associate alla richiesta client e la richiesta del client viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0cb10-136">If this was the last provider in the list, then all resources associated with the client request are released and client request is ignored.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="0cb10-137">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb10-137">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb10-138">Valore di contesto passato alla funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="0cb10-138">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb10-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cb10-139">Return value</span></span>

<span data-ttu-id="0cb10-140">Se il provider ha elaborato correttamente la richiesta del client, il callback deve restituire un **errore di \_ esito positivo** e l' **\_ \_ azione di avvio PXE** a cui punta il parametro di *patto* contiene l'azione di avvio appropriata per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0cb10-140">If the provider successfully processed the client request, the callback should return **ERROR\_SUCCESS** and the **PXE\_BOOT\_ACTION** pointed to by the *pAction* parameter contains the appropriate boot action for this request.</span></span> <span data-ttu-id="0cb10-141">Se il provider elaborerà la richiesta client in modo asincrono, il callback deve restituire l' **errore \_ io \_ in sospeso** e chiamare la funzione [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) quando la richiesta client è stata elaborata.</span><span class="sxs-lookup"><span data-stu-id="0cb10-141">If the provider will process the client request asynchronously, the callback should return **ERROR\_IO\_PENDING** and call the [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) function when the client request has been processed.</span></span> <span data-ttu-id="0cb10-142">In caso di errore, dovrebbe essere restituito un codice di errore appropriato e il sistema continuerà come se fosse stata specificata l'azione di avvio **\_ \_ rifiutato da PXE BA** .</span><span class="sxs-lookup"><span data-stu-id="0cb10-142">In case of failure, an appropriate error code should be returned and the system will proceed as if the **PXE\_BA\_REJECTED** boot action was specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb10-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cb10-143">Remarks</span></span>

<span data-ttu-id="0cb10-144">Il tipo di pacchetti visualizzati da un provider può essere modificato con la funzione [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) .</span><span class="sxs-lookup"><span data-stu-id="0cb10-144">The type of packets seen by a provider can be changed with the [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb10-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cb10-145">Requirements</span></span>



| <span data-ttu-id="0cb10-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb10-146">Requirement</span></span> | <span data-ttu-id="0cb10-147">Valore</span><span class="sxs-lookup"><span data-stu-id="0cb10-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb10-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cb10-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb10-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0cb10-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="0cb10-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cb10-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb10-151">Windows Server 2008, Windows Server 2003 con \[ solo app desktop SP2\]</span><span class="sxs-lookup"><span data-stu-id="0cb10-151">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0cb10-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cb10-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb10-153">Funzioni server di servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="0cb10-153">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="0cb10-154">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="0cb10-154">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[<span data-ttu-id="0cb10-155">**PxeSendReply**</span><span class="sxs-lookup"><span data-stu-id="0cb10-155">**PxeSendReply**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[<span data-ttu-id="0cb10-156">**PxeProviderSetAttribute**</span><span class="sxs-lookup"><span data-stu-id="0cb10-156">**PxeProviderSetAttribute**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





