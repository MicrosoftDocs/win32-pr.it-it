---
title: Interfaccia INapEnforcementClientBinding (NapEnforcementClient. h)
description: I client di imposizione utilizzano per comunicare con NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- NAP interfaccia INapEnforcementClientBinding
- Interfaccia NAP di INapEnforcementClientBinding, descrizione
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874585"
---
# <a name="inapenforcementclientbinding-interface"></a><span data-ttu-id="f0d85-105">Interfaccia INapEnforcementClientBinding</span><span class="sxs-lookup"><span data-stu-id="f0d85-105">INapEnforcementClientBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="f0d85-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="f0d85-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f0d85-107">**INapEnforcementClientBinding** fornisce metodi che i client di imposizione utilizzano per comunicare con napagent.</span><span class="sxs-lookup"><span data-stu-id="f0d85-107">The **INapEnforcementClientBinding** provides methods that enforcement clients use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="f0d85-108">Membri</span><span class="sxs-lookup"><span data-stu-id="f0d85-108">Members</span></span>

<span data-ttu-id="f0d85-109">L'interfaccia **INapEnforcementClientBinding** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f0d85-109">The **INapEnforcementClientBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f0d85-110">**INapEnforcementClientBinding** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f0d85-110">**INapEnforcementClientBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="f0d85-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f0d85-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f0d85-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="f0d85-112">Methods</span></span>

<span data-ttu-id="f0d85-113">L'interfaccia **INapEnforcementClientBinding** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f0d85-113">The **INapEnforcementClientBinding** interface has these methods.</span></span>



| <span data-ttu-id="f0d85-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="f0d85-114">Method</span></span>                                                                                                                           | <span data-ttu-id="f0d85-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0d85-115">Description</span></span>                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0d85-116">**INapEnforcementClientBinding:: CreateConnection**</span><span class="sxs-lookup"><span data-stu-id="f0d85-116">**INapEnforcementClientBinding::CreateConnection**</span></span>](inapenforcementclientbinding-createconnection-method.md)                   | <span data-ttu-id="f0d85-117">Utilizzato dalle forze di esecuzione per creare oggetti connessione.</span><span class="sxs-lookup"><span data-stu-id="f0d85-117">Used by enforcers to create connection objects.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="f0d85-118">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="f0d85-118">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)                         | <span data-ttu-id="f0d85-119">Usato dal client di imposizione quando necessita di una richiesta di rapporto di integrità per una determinata connessione.</span><span class="sxs-lookup"><span data-stu-id="f0d85-119">Used by the enforcement client when it needs an SoH-request for a particular connection.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="f0d85-120">**INapEnforcementClientBinding:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="f0d85-120">**INapEnforcementClientBinding::Initialize**</span></span>](inapenforcementclientbinding-initialize-method.md)                               | <span data-ttu-id="f0d85-121">Avvia il servizio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="f0d85-121">Starts up the NapAgent service.</span></span> <span data-ttu-id="f0d85-122">Il client di imposizione deve chiamare questo metodo prima di chiamare qualsiasi altro metodo di questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f0d85-122">The enforcement client must call this method before calling any other method of this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="f0d85-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="f0d85-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | <span data-ttu-id="f0d85-124">Utilizzato per indicare al NapAgent che una connessione a un client di imposizione è diminuita.</span><span class="sxs-lookup"><span data-stu-id="f0d85-124">Used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="f0d85-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span><span class="sxs-lookup"><span data-stu-id="f0d85-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span></span>](inapenforcementclientbinding-notifysohchangefailure-method.md)       | <span data-ttu-id="f0d85-126">Utilizzato dal client di imposizione per informare NapAgent che non è stato possibile elaborare un [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)precedente.</span><span class="sxs-lookup"><span data-stu-id="f0d85-126">Used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span><br/> |
| [<span data-ttu-id="f0d85-127">**INapEnforcementClientBinding::P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="f0d85-127">**INapEnforcementClientBinding::ProcessSoHResponse**</span></span>](inapenforcementclientbinding-processsohresponse-method.md)               | <span data-ttu-id="f0d85-128">Usato dai client di imposizione ogni volta che ricevono un BLOB di dati SoH-Response dal server di imposizione.</span><span class="sxs-lookup"><span data-stu-id="f0d85-128">Used by enforcement clients whenever they get an SoH-Response data blob from the enforcement server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="f0d85-129">**INapEnforcementClientBinding:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="f0d85-129">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)                           | <span data-ttu-id="f0d85-130">Conclude il servizio NapAgent per la connessione client.</span><span class="sxs-lookup"><span data-stu-id="f0d85-130">Concludes the NapAgent service for this client connection.</span></span><br/>                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f0d85-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0d85-131">Remarks</span></span>

<span data-ttu-id="f0d85-132">Tutte le API in questa interfaccia restituiranno RPC \_ E \_ disconnesse se il NapAgent è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="f0d85-132">All the APIs in this interface will return RPC\_E\_DISCONNECTED if the NapAgent is stopped.</span></span> <span data-ttu-id="f0d85-133">Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.</span><span class="sxs-lookup"><span data-stu-id="f0d85-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0d85-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0d85-134">Requirements</span></span>



| <span data-ttu-id="f0d85-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0d85-135">Requirement</span></span> | <span data-ttu-id="f0d85-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f0d85-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d85-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0d85-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d85-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0d85-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f0d85-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0d85-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d85-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f0d85-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f0d85-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0d85-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0d85-142"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0d85-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0d85-143">IDL</span><span class="sxs-lookup"><span data-stu-id="f0d85-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0d85-144"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0d85-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="f0d85-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f0d85-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0d85-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0d85-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f0d85-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0d85-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d85-148">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="f0d85-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f0d85-149">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="f0d85-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

