---
title: Interfaccia INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
description: SHAs usare per comunicare con NapAgent. | Interfaccia INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- NAP interfaccia INapSystemHealthAgentBinding2
- Interfaccia NAP di INapSystemHealthAgentBinding2, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352796"
---
# <a name="inapsystemhealthagentbinding2-interface"></a><span data-ttu-id="f695c-106">Interfaccia INapSystemHealthAgentBinding2</span><span class="sxs-lookup"><span data-stu-id="f695c-106">INapSystemHealthAgentBinding2 interface</span></span>

> [!Note]  
> <span data-ttu-id="f695c-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="f695c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f695c-108">**INapSystemHealthAgentBinding2** fornisce i metodi usati da Shas per comunicare con napagent.</span><span class="sxs-lookup"><span data-stu-id="f695c-108">The **INapSystemHealthAgentBinding2** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="f695c-109">Questa interfaccia eredita tutti i metodi di [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) e deve essere usata in alternativa.</span><span class="sxs-lookup"><span data-stu-id="f695c-109">This interface inherits all the methods of [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="f695c-110">Membri</span><span class="sxs-lookup"><span data-stu-id="f695c-110">Members</span></span>

<span data-ttu-id="f695c-111">L'interfaccia **INapSystemHealthAgentBinding2** eredita da [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span><span class="sxs-lookup"><span data-stu-id="f695c-111">The **INapSystemHealthAgentBinding2** interface inherits from [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span></span> <span data-ttu-id="f695c-112">**INapSystemHealthAgentBinding2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f695c-112">**INapSystemHealthAgentBinding2** also has these types of members:</span></span>

-   [<span data-ttu-id="f695c-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="f695c-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f695c-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="f695c-114">Methods</span></span>

<span data-ttu-id="f695c-115">L'interfaccia **INapSystemHealthAgentBinding2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f695c-115">The **INapSystemHealthAgentBinding2** interface has these methods.</span></span>



| <span data-ttu-id="f695c-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="f695c-116">Method</span></span>                                                                                                                    | <span data-ttu-id="f695c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f695c-117">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f695c-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="f695c-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span></span>](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | <span data-ttu-id="f695c-119">Chiamata eseguita da SHAs per determinare lo stato di isolamento del sistema e lo stato di isolamento esteso.</span><span class="sxs-lookup"><span data-stu-id="f695c-119">Called by SHAs to determine the system isolation state and extended isolation state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f695c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f695c-120">Remarks</span></span>

<span data-ttu-id="f695c-121">Tutte le API in questa interfaccia restituiranno **RPC \_ E \_ disconnesse** se il NapAgent è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="f695c-121">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="f695c-122">Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.</span><span class="sxs-lookup"><span data-stu-id="f695c-122">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="f695c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f695c-123">Requirements</span></span>



| <span data-ttu-id="f695c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f695c-124">Requirement</span></span> | <span data-ttu-id="f695c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f695c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f695c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f695c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f695c-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f695c-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f695c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f695c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f695c-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f695c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f695c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f695c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f695c-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="f695c-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="f695c-132">IDL</span><span class="sxs-lookup"><span data-stu-id="f695c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f695c-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f695c-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="f695c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f695c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f695c-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f695c-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f695c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f695c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f695c-137">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="f695c-137">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> <dt>

[<span data-ttu-id="f695c-138">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="f695c-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f695c-139">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="f695c-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





