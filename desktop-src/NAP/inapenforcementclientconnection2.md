---
title: Interfaccia INapEnforcementClientConnection2 (NapEnforcementClient. h)
description: Consente la gestione della connessione client. | Interfaccia INapEnforcementClientConnection2 (NapEnforcementClient. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- NAP interfaccia INapEnforcementClientConnection2
- Interfaccia NAP di INapEnforcementClientConnection2, descrizione
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886099"
---
# <a name="inapenforcementclientconnection2-interface"></a><span data-ttu-id="940f5-106">Interfaccia INapEnforcementClientConnection2</span><span class="sxs-lookup"><span data-stu-id="940f5-106">INapEnforcementClientConnection2 interface</span></span>

> [!Note]  
> <span data-ttu-id="940f5-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="940f5-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="940f5-108">**INapEnforcementClientConnection2** fornisce metodi che consentono la gestione della connessione client.</span><span class="sxs-lookup"><span data-stu-id="940f5-108">The **INapEnforcementClientConnection2** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="940f5-109">Questa interfaccia eredita tutti i metodi di [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) e deve essere usata in alternativa.</span><span class="sxs-lookup"><span data-stu-id="940f5-109">This interface inherits all the methods of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="940f5-110">Membri</span><span class="sxs-lookup"><span data-stu-id="940f5-110">Members</span></span>

<span data-ttu-id="940f5-111">L'interfaccia **INapEnforcementClientConnection2** eredita da [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span><span class="sxs-lookup"><span data-stu-id="940f5-111">The **INapEnforcementClientConnection2** interface inherits from [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span></span> <span data-ttu-id="940f5-112">**INapEnforcementClientConnection2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="940f5-112">**INapEnforcementClientConnection2** also has these types of members:</span></span>

-   [<span data-ttu-id="940f5-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="940f5-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="940f5-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="940f5-114">Methods</span></span>

<span data-ttu-id="940f5-115">L'interfaccia **INapEnforcementClientConnection2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="940f5-115">The **INapEnforcementClientConnection2** interface has these methods.</span></span>



| <span data-ttu-id="940f5-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="940f5-116">Method</span></span>                                                                                                              | <span data-ttu-id="940f5-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="940f5-117">Description</span></span>                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="940f5-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="940f5-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span></span>](inapenforcementclientconnection2-getinstalledshvs.md)     | <span data-ttu-id="940f5-119">Utilizzato per ottenere gli ID del SHV installato per il client.</span><span class="sxs-lookup"><span data-stu-id="940f5-119">Used to get the IDs of the installed SHVs for the client.</span></span><br/>             |
| [<span data-ttu-id="940f5-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="940f5-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-getisolationinfoex.md) | <span data-ttu-id="940f5-121">Utilizzato per ottenere le informazioni di isolamento per il client.</span><span class="sxs-lookup"><span data-stu-id="940f5-121">Used to get the isolation information for the client.</span></span><br/>                 |
| [<span data-ttu-id="940f5-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="940f5-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span></span>](inapenforcementclientconnection2-setinstalledshvs.md)     | <span data-ttu-id="940f5-123">Utilizzato da NapAgent per impostare gli ID di convalida integrità sistema installati per il client.</span><span class="sxs-lookup"><span data-stu-id="940f5-123">Used by the NapAgent to set the installed SHV IDs for the client.</span></span><br/>     |
| [<span data-ttu-id="940f5-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="940f5-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-setisolationinfoex.md) | <span data-ttu-id="940f5-125">Utilizzato da NapAgent per impostare le informazioni di isolamento per il client.</span><span class="sxs-lookup"><span data-stu-id="940f5-125">Used by the NapAgent to set the isolation information for the client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="940f5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="940f5-126">Requirements</span></span>



| <span data-ttu-id="940f5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="940f5-127">Requirement</span></span> | <span data-ttu-id="940f5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="940f5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="940f5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="940f5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="940f5-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="940f5-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="940f5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="940f5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="940f5-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="940f5-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="940f5-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="940f5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="940f5-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="940f5-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="940f5-135">IDL</span><span class="sxs-lookup"><span data-stu-id="940f5-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="940f5-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="940f5-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="940f5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="940f5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="940f5-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="940f5-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="940f5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="940f5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940f5-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="940f5-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> <dt>

[<span data-ttu-id="940f5-141">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="940f5-141">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="940f5-142">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="940f5-142">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





