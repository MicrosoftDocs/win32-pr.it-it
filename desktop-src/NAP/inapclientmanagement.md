---
title: Interfaccia INapClientManagement (NapManagement. h)
description: Fornisce metodi per la gestione client di protezione accesso alla rete. | Interfaccia INapClientManagement (NapManagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- NAP interfaccia INapClientManagement
- Interfaccia NAP di INapClientManagement, descrizione
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969198"
---
# <a name="inapclientmanagement-interface"></a><span data-ttu-id="1fa7b-106">Interfaccia INapClientManagement</span><span class="sxs-lookup"><span data-stu-id="1fa7b-106">INapClientManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="1fa7b-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="1fa7b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1fa7b-108">L'interfaccia **INapClientManagement** fornisce metodi per la gestione client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-108">The **INapClientManagement** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="1fa7b-109">[**INapClientManagement2**](inapclientmanagement2.md) eredita tutti i metodi di questa interfaccia e deve essere usato in alternativa.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-109">[**INapClientManagement2**](inapclientmanagement2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="1fa7b-110">Membri</span><span class="sxs-lookup"><span data-stu-id="1fa7b-110">Members</span></span>

<span data-ttu-id="1fa7b-111">L'interfaccia **INapClientManagement** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1fa7b-111">The **INapClientManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1fa7b-112">**INapClientManagement** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1fa7b-112">**INapClientManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="1fa7b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="1fa7b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1fa7b-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="1fa7b-114">Methods</span></span>

<span data-ttu-id="1fa7b-115">L'interfaccia **INapClientManagement** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-115">The **INapClientManagement** interface has these methods.</span></span>



| <span data-ttu-id="1fa7b-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="1fa7b-116">Method</span></span>                                                                                                                | <span data-ttu-id="1fa7b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fa7b-117">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="1fa7b-118">**INapClientManagement::GetNapClientInfo**</span><span class="sxs-lookup"><span data-stu-id="1fa7b-118">**INapClientManagement::GetNapClientInfo**</span></span>](inapclientmanagement-getnapclientinfo.md)                               | <span data-ttu-id="1fa7b-119">Recupera le informazioni su un client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-119">Retrieves information about a NAP client.</span></span><br/>                          |
| [<span data-ttu-id="1fa7b-120">**INapClientManagement::GetRegisteredEnforcementClients**</span><span class="sxs-lookup"><span data-stu-id="1fa7b-120">**INapClientManagement::GetRegisteredEnforcementClients**</span></span>](inapclientmanagement-getregisteredenforcementclients.md) | <span data-ttu-id="1fa7b-121">Recupera le informazioni sui client di imposizione registrati.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-121">Retrieves information about the registered enforcement clients.</span></span><br/>    |
| [<span data-ttu-id="1fa7b-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span><span class="sxs-lookup"><span data-stu-id="1fa7b-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span></span>](inapclientmanagement-getregisteredsystemhealthagents.md) | <span data-ttu-id="1fa7b-123">Recuperare informazioni su un SHA registrato.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-123">Retrieve information about a registered SHA.</span></span><br/>                       |
| [<span data-ttu-id="1fa7b-124">**INapClientManagement::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="1fa7b-124">**INapClientManagement::GetSystemIsolationInfo**</span></span>](inapclientmanagement-getsystemisolationinfo.md)                   | <span data-ttu-id="1fa7b-125">Recupera le informazioni sullo stato di isolamento del client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-125">Retrieves information about the isolation state of the Nap client.</span></span><br/> |
| [<span data-ttu-id="1fa7b-126">**INapClientManagement::RegisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="1fa7b-126">**INapClientManagement::RegisterEnforcementClient**</span></span>](inapclientmanagement-registerenforcementclient.md)             | <span data-ttu-id="1fa7b-127">Registra un client di imposizione con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-127">Registers an enforcement client with the NAP system.</span></span><br/>               |
| [<span data-ttu-id="1fa7b-128">**INapClientManagement::RegisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="1fa7b-128">**INapClientManagement::RegisterSystemHealthAgent**</span></span>](inapclientmanagement-registersystemhealthagent.md)             | <span data-ttu-id="1fa7b-129">Registra un SHA con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-129">Registers an SHA with the NAP system.</span></span><br/>                              |
| [<span data-ttu-id="1fa7b-130">**INapClientManagement::UnregisterEnforcementClient**</span><span class="sxs-lookup"><span data-stu-id="1fa7b-130">**INapClientManagement::UnregisterEnforcementClient**</span></span>](inapclientmanagement-unregisterenforcementclient.md)         | <span data-ttu-id="1fa7b-131">Annulla la registrazione di un client di imposizione con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-131">Unregisters an enforcement client with the NAP system.</span></span><br/>             |
| [<span data-ttu-id="1fa7b-132">**INapClientManagement::UnregisterSystemHealthAgent**</span><span class="sxs-lookup"><span data-stu-id="1fa7b-132">**INapClientManagement::UnregisterSystemHealthAgent**</span></span>](inapclientmanagement-unregistersystemhealthagent.md)         | <span data-ttu-id="1fa7b-133">Annulla la registrazione di un SHA con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="1fa7b-133">Unregisters an SHA with the NAP system.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="1fa7b-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fa7b-134">Requirements</span></span>



| <span data-ttu-id="1fa7b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fa7b-135">Requirement</span></span> | <span data-ttu-id="1fa7b-136">Valore</span><span class="sxs-lookup"><span data-stu-id="1fa7b-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa7b-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fa7b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa7b-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1fa7b-138">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1fa7b-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fa7b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa7b-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1fa7b-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1fa7b-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fa7b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fa7b-142"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7b-142"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fa7b-143">IDL</span><span class="sxs-lookup"><span data-stu-id="1fa7b-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1fa7b-144"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7b-144"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="1fa7b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa7b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fa7b-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa7b-146"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="1fa7b-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fa7b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa7b-148">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="1fa7b-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1fa7b-149">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="1fa7b-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

