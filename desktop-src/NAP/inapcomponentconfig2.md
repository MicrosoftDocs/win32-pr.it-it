---
title: Interfaccia INapComponentConfig2 (NapCommon. h)
description: Fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per configurare un'interfaccia utente di server dei criteri di rete in modalità remota.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- NAP interfaccia INapComponentConfig2
- Interfaccia NAP di INapComponentConfig2, descrizione
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301368"
---
# <a name="inapcomponentconfig2-interface"></a><span data-ttu-id="db0e1-105">Interfaccia INapComponentConfig2</span><span class="sxs-lookup"><span data-stu-id="db0e1-105">INapComponentConfig2 interface</span></span>

> [!Note]  
> <span data-ttu-id="db0e1-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="db0e1-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="db0e1-107">L'interfaccia **INapComponentConfig2** fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per configurare un'interfaccia utente di server dei criteri di rete in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="db0e1-107">The **INapComponentConfig2** interface provides NAP system configuration methods for system health validators (SHVs) to configure a network policy server (NPS) user interface remotely.</span></span>

> [!Note]  
> <span data-ttu-id="db0e1-108">Questa interfaccia eredita tutti i metodi di [**INapComponentConfig**](inapcomponentconfig.md) e deve essere usata in alternativa.</span><span class="sxs-lookup"><span data-stu-id="db0e1-108">This interface inherits all the methods of [**INapComponentConfig**](inapcomponentconfig.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="db0e1-109">Membri</span><span class="sxs-lookup"><span data-stu-id="db0e1-109">Members</span></span>

<span data-ttu-id="db0e1-110">L'interfaccia **INapComponentConfig2** eredita da [**INapComponentConfig**](inapcomponentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="db0e1-110">The **INapComponentConfig2** interface inherits from [**INapComponentConfig**](inapcomponentconfig.md).</span></span> <span data-ttu-id="db0e1-111">**INapComponentConfig2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="db0e1-111">**INapComponentConfig2** also has these types of members:</span></span>

-   [<span data-ttu-id="db0e1-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="db0e1-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="db0e1-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="db0e1-113">Methods</span></span>

<span data-ttu-id="db0e1-114">L'interfaccia **INapComponentConfig2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="db0e1-114">The **INapComponentConfig2** interface has these methods.</span></span>



| <span data-ttu-id="db0e1-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="db0e1-115">Method</span></span>                                                                                                | <span data-ttu-id="db0e1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db0e1-116">Description</span></span>                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db0e1-117">**INapComponentConfig2::InvokeUIForMachine**</span><span class="sxs-lookup"><span data-stu-id="db0e1-117">**INapComponentConfig2::InvokeUIForMachine**</span></span>](inapcomponentconfig2-invokeuiformachine.md)           | <span data-ttu-id="db0e1-118">Implementato da SHV in base alle esigenze per gestire la configurazione remota direttamente nel computer specificato.</span><span class="sxs-lookup"><span data-stu-id="db0e1-118">Implemented by SHVs as needed to manage remote configuration directly on the machine specified.</span></span><br/>                                                                 |
| [<span data-ttu-id="db0e1-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="db0e1-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span></span>](inapcomponentconfig2-invokeuifromconfigblob.md)   | <span data-ttu-id="db0e1-120">Implementata da SHV in base alle esigenze per caricare la configurazione del computer remoto in memoria e visualizzare un'interfaccia utente che consente la modifica dei dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="db0e1-120">Implemented by SHVs as needed to load the configuration of the remote machine in memory and to display a UI that allows manipulation of the configuration data.</span></span><br/> |
| [<span data-ttu-id="db0e1-121">**INapComponentConfig2::IsRemoteConfigSupported**</span><span class="sxs-lookup"><span data-stu-id="db0e1-121">**INapComponentConfig2::IsRemoteConfigSupported**</span></span>](inapcomponentconfig2-isremoteconfigsupported.md) | <span data-ttu-id="db0e1-122">Implementato da SHV per indicare se la configurazione remota è supportata.</span><span class="sxs-lookup"><span data-stu-id="db0e1-122">Implemented by SHVs to indicate whether remote configuration is supported.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="db0e1-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="db0e1-123">Remarks</span></span>

<span data-ttu-id="db0e1-124">Questa interfaccia non deve essere implementata dagli agenti di integrità del sistema (SHAs) o dai client di imposizione di quarantena (QeC).</span><span class="sxs-lookup"><span data-stu-id="db0e1-124">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="db0e1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db0e1-125">Requirements</span></span>



| <span data-ttu-id="db0e1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="db0e1-126">Requirement</span></span> | <span data-ttu-id="db0e1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="db0e1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db0e1-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db0e1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="db0e1-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="db0e1-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="db0e1-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db0e1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="db0e1-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db0e1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db0e1-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db0e1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="db0e1-133"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="db0e1-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="db0e1-134">IDL</span><span class="sxs-lookup"><span data-stu-id="db0e1-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db0e1-135"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db0e1-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db0e1-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db0e1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db0e1-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="db0e1-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="db0e1-138">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="db0e1-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="db0e1-139">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="db0e1-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





