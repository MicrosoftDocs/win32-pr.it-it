---
title: Interfaccia INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: SHAs usare per comunicare con NapAgent. | Interfaccia INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- NAP interfaccia INapSystemHealthAgentBinding
- Interfaccia NAP di INapSystemHealthAgentBinding, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321961"
---
# <a name="inapsystemhealthagentbinding-interface"></a><span data-ttu-id="abe23-106">Interfaccia INapSystemHealthAgentBinding</span><span class="sxs-lookup"><span data-stu-id="abe23-106">INapSystemHealthAgentBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="abe23-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="abe23-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="abe23-108">**INapSystemHealthAgentBinding** fornisce i metodi usati da Shas per comunicare con napagent.</span><span class="sxs-lookup"><span data-stu-id="abe23-108">The **INapSystemHealthAgentBinding** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="abe23-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) eredita tutti i metodi di questa interfaccia e deve essere usato in alternativa.</span><span class="sxs-lookup"><span data-stu-id="abe23-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="abe23-110">Membri</span><span class="sxs-lookup"><span data-stu-id="abe23-110">Members</span></span>

<span data-ttu-id="abe23-111">L'interfaccia **INapSystemHealthAgentBinding** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="abe23-111">The **INapSystemHealthAgentBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="abe23-112">**INapSystemHealthAgentBinding** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="abe23-112">**INapSystemHealthAgentBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="abe23-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="abe23-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="abe23-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="abe23-114">Methods</span></span>

<span data-ttu-id="abe23-115">L'interfaccia **INapSystemHealthAgentBinding** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="abe23-115">The **INapSystemHealthAgentBinding** interface has these methods.</span></span>



| <span data-ttu-id="abe23-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="abe23-116">Method</span></span>                                                                                                                     | <span data-ttu-id="abe23-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abe23-117">Description</span></span>                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="abe23-118">**INapSystemHealthAgentBinding:: FlushCache**</span><span class="sxs-lookup"><span data-stu-id="abe23-118">**INapSystemHealthAgentBinding::FlushCache**</span></span>](inapsystemhealthagentbinding-flushcache-method.md)                         | <span data-ttu-id="abe23-119">Chiamato da un SHA per scaricare la cache del rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="abe23-119">Called by an SHA to flush its SoH cache.</span></span><br/>                                                |
| [<span data-ttu-id="abe23-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="abe23-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span></span>](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | <span data-ttu-id="abe23-121">Chiamato da SHAs per determinare lo stato di isolamento del sistema.</span><span class="sxs-lookup"><span data-stu-id="abe23-121">Called by SHAs to determine the system isolation state.</span></span><br/>                                 |
| [<span data-ttu-id="abe23-122">**INapSystemHealthAgentBinding:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="abe23-122">**INapSystemHealthAgentBinding::Initialize**</span></span>](inapsystemhealthagentbinding-initialize-method.md)                         | <span data-ttu-id="abe23-123">Inizializza l'SHA e associa l'SHA al servizio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="abe23-123">Initializes the SHA and binds the SHA to the NapAgent service.</span></span> <br/>                         |
| [<span data-ttu-id="abe23-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="abe23-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span></span>](inapsystemhealthagentbinding-notifysohchange-method.md)               | <span data-ttu-id="abe23-125">Chiamato da SHAs quando cambia il rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="abe23-125">Called by SHAs when their SoH changes.</span></span><br/>                                                  |
| [<span data-ttu-id="abe23-126">**INapSystemHealthAgentBinding:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="abe23-126">**INapSystemHealthAgentBinding::Uninitialize**</span></span>](inapsystemhealthagentbinding-uninitialize-method.md)                     | <span data-ttu-id="abe23-127">Chiamato da SHAs per fare in modo che NapAgent rilasci tutti i relativi riferimenti ai puntatori SHA COM.</span><span class="sxs-lookup"><span data-stu-id="abe23-127">Called by SHAs to cause the NapAgent to release all its references to SHA COM pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="abe23-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="abe23-128">Remarks</span></span>

<span data-ttu-id="abe23-129">Tutte le API in questa interfaccia restituiranno **RPC \_ E \_ disconnesse** se il NapAgent è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="abe23-129">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="abe23-130">Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.</span><span class="sxs-lookup"><span data-stu-id="abe23-130">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe23-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abe23-131">Requirements</span></span>



| <span data-ttu-id="abe23-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="abe23-132">Requirement</span></span> | <span data-ttu-id="abe23-133">Valore</span><span class="sxs-lookup"><span data-stu-id="abe23-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abe23-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abe23-134">Minimum supported client</span></span><br/> | <span data-ttu-id="abe23-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abe23-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="abe23-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abe23-136">Minimum supported server</span></span><br/> | <span data-ttu-id="abe23-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abe23-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="abe23-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abe23-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="abe23-139"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="abe23-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="abe23-140">IDL</span><span class="sxs-lookup"><span data-stu-id="abe23-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="abe23-141"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="abe23-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="abe23-142">DLL</span><span class="sxs-lookup"><span data-stu-id="abe23-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abe23-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abe23-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="abe23-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abe23-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe23-145">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="abe23-145">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="abe23-146">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="abe23-146">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

