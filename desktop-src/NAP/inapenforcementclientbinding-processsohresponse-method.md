---
title: Metodo INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient. h)
description: Viene usato dai client di imposizione per elaborare un SoHResponse ogni volta che ricevono un BLOB di dati SoHResponse dal server di imposizione.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- NAP metodo ProcessSoHResponse
- Metodo ProcessSoHResponse NAP, interfaccia INapEnforcementClientBinding
- Interfaccia INapEnforcementClientBinding NAP, metodo ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519174"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a><span data-ttu-id="5ebeb-106">INapEnforcementClientBinding::P metodo rocessSoHResponse</span><span class="sxs-lookup"><span data-stu-id="5ebeb-106">INapEnforcementClientBinding::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="5ebeb-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="5ebeb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5ebeb-108">Il metodo **INapEnforcementClientBinding::P rocesssohresponse** viene usato dai client di imposizione per elaborare un SoHResponse ogni volta che ricevono un BLOB di dati SoHResponse dal server di imposizione.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-108">The **INapEnforcementClientBinding::ProcessSoHResponse** method is used by enforcement clients to process an SoHResponse whenever they receive an SoHResponse data blob from the enforcement server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebeb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ebeb-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a><span data-ttu-id="5ebeb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ebeb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ebeb-111">*connessione* \[ a in\]</span><span class="sxs-lookup"><span data-stu-id="5ebeb-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebeb-112">Puntatore COM all'interfaccia [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) della connessione client.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the client connection.</span></span> <span data-ttu-id="5ebeb-113">Il NapAgent non tiene i riferimenti all'oggetto associato a questa interfaccia dopo il completamento della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-113">The NapAgent does not hold references to the object associated with this interface after this method call completes.</span></span>

<span data-ttu-id="5ebeb-114">È necessario usare una connessione stabilita in precedenza per elaborare i BLOB di dati SOHResponse.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-114">You must use a previously established connection for processing SOHResponse data blobs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ebeb-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ebeb-115">Return value</span></span>

<span data-ttu-id="5ebeb-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5ebeb-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5ebeb-117">Return code</span></span>                                                                                             | <span data-ttu-id="5ebeb-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ebeb-118">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ebeb-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-119"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="5ebeb-120">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-120">The operation is successful.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="5ebeb-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="5ebeb-122">Nessuna connessione è stata creata in precedenza nel client di imposizione.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-122">No connections have previously been created on the enforcement client.</span></span> <br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="5ebeb-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="5ebeb-124">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-124">Permissions error, access denied.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="5ebeb-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="5ebeb-126">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-126">System resource limit, could not perform the operation.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="5ebeb-127"><dt>**NAP \_ E \_ pacchetto non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-127"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl>  | <span data-ttu-id="5ebeb-128">Se questo valore viene restituito, il client di imposizione deve eliminare il pacchetto se NapAgent restituisce NAP \_ E \_ pacchetto non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="5ebeb-128">If this value is returned the enforcement client must drop the packet if the NapAgent returns NAP\_E\_INVALID\_PACKET.</span></span> <span data-ttu-id="5ebeb-129">In questo caso, l'applicazione deve presupporre che il server a cui si sta comunicando non sia abilitato per la protezione accesso alla rete e rimuovere la connessione dall'elenco attivo (ad esempio, notificare il NapAgent di uno stato di connessione).</span><span class="sxs-lookup"><span data-stu-id="5ebeb-129">In this case, the enforcer must assume that the server it is talking to is not NAP-enabled and remove the connection from the active list (i.e. notify the NapAgent of a connection state down).</span></span><br/> |
| <dl> <span data-ttu-id="5ebeb-130"><dt>**\_ID NAP E non \_ corrispondente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-130"><dt>**NAP\_E\_MISMATCHED\_ID**</dt></span></span> </dl>   | <span data-ttu-id="5ebeb-131">Se questo valore viene restituito, significa che l'ID di correlazione nel pacchetto di SoH-Response non corrisponde alla risposta con rapporto di integrità in attesa.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-131">If this value is returned it indicates that the correlation id in the SoH-Response packet did not match the outstanding SoH-Response.</span></span> <span data-ttu-id="5ebeb-132">In questo caso, l'applicazione deve eliminare il pacchetto e attendere un altro pacchetto di SoH-Response più recente.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-132">In this case, the enforcer should drop the packet and wait for another newer SoH-Response packet.</span></span><br/> <span data-ttu-id="5ebeb-133">Questo problema può essere causato da una risposta a un messaggio di richiesta precedente.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-133">This may be caused by a response to an older request message.</span></span><br/>        |
| <dl> <span data-ttu-id="5ebeb-134"><dt>**NAP \_ E \_ non \_ inizializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-134"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="5ebeb-135">L'applicazione non è stata inizializzata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-135">The enforcer has not been previously initialized.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="5ebeb-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ebeb-136">Remarks</span></span>

<span data-ttu-id="5ebeb-137">Il NapAgent interroga il BLOB di dati SoH-Response dall'oggetto connessione, lo elabora e imposta la decisione risultante, ad esempio</span><span class="sxs-lookup"><span data-stu-id="5ebeb-137">The NapAgent queries the SoH-Response data blob from the connection object, processes it, and sets the resulting decision (eg.</span></span> <span data-ttu-id="5ebeb-138">accesso completo/limitato/e così via) per l'oggetto connessione.</span><span class="sxs-lookup"><span data-stu-id="5ebeb-138">full/restricted access/etc) on the connection object.</span></span>

<span data-ttu-id="5ebeb-139">Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="5ebeb-139">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ebeb-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ebeb-140">Requirements</span></span>



| <span data-ttu-id="5ebeb-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ebeb-141">Requirement</span></span> | <span data-ttu-id="5ebeb-142">Valore</span><span class="sxs-lookup"><span data-stu-id="5ebeb-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebeb-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ebeb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebeb-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ebeb-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ebeb-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ebeb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebeb-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ebeb-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5ebeb-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ebeb-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ebeb-148"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-148"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ebeb-149">IDL</span><span class="sxs-lookup"><span data-stu-id="5ebeb-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ebeb-150"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-150"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5ebeb-151">DLL</span><span class="sxs-lookup"><span data-stu-id="5ebeb-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ebeb-152"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-152"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5ebeb-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ebeb-153">See also</span></span>

<dl> <span data-ttu-id="5ebeb-154"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5ebeb-154"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="5ebeb-155">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="5ebeb-155">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="5ebeb-156">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="5ebeb-156">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





