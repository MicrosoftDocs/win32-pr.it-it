---
title: Interfaccia INapServerManagement (NapServerManagement. h)
description: Consentono di gestire il server di protezione accesso alla rete.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- NAP interfaccia INapServerManagement
- Interfaccia NAP di INapServerManagement, descrizione
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120082"
---
# <a name="inapservermanagement-interface"></a><span data-ttu-id="92551-105">Interfaccia INapServerManagement</span><span class="sxs-lookup"><span data-stu-id="92551-105">INapServerManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="92551-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="92551-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="92551-107">**INapServerManagement** fornisce i metodi utilizzati per gestire il server di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="92551-107">The **INapServerManagement** provides methods that are used to manage the NAP Server.</span></span>

## <a name="members"></a><span data-ttu-id="92551-108">Membri</span><span class="sxs-lookup"><span data-stu-id="92551-108">Members</span></span>

<span data-ttu-id="92551-109">L'interfaccia **INapServerManagement** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="92551-109">The **INapServerManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="92551-110">**INapServerManagement** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="92551-110">**INapServerManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="92551-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="92551-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="92551-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="92551-112">Methods</span></span>

<span data-ttu-id="92551-113">L'interfaccia **INapServerManagement** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="92551-113">The **INapServerManagement** interface has these methods.</span></span>



| <span data-ttu-id="92551-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="92551-114">Method</span></span>                                                                                                                       | <span data-ttu-id="92551-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92551-115">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="92551-116">**INapServerManagement::RegisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="92551-116">**INapServerManagement::RegisterSystemHealthValidator**</span></span>](inapservermanagement-registersystemhealthvalidator-method.md)     | <span data-ttu-id="92551-117">Registra un servizio di convalida dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="92551-117">Registers an SHV.</span></span><br/>                         |
| [<span data-ttu-id="92551-118">**INapServerManagement::SetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="92551-118">**INapServerManagement::SetFailureCategoryMappings**</span></span>](inapservermanagement-setfailurecategorymappings-method.md)           | <span data-ttu-id="92551-119">Imposta i mapping delle categorie di errori di convalida.</span><span class="sxs-lookup"><span data-stu-id="92551-119">Sets the SHV's failure category mappings.</span></span><br/> |
| [<span data-ttu-id="92551-120">**INapServerManagement::UnregisterSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="92551-120">**INapServerManagement::UnregisterSystemHealthValidator**</span></span>](inapservermanagement-unregistersystemhealthvalidator-method.md) | <span data-ttu-id="92551-121">Annulla la registrazione di un servizio di convalida integrità dal server protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="92551-121">Deregisters an SHV from the NAP server.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="92551-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92551-122">Requirements</span></span>



| <span data-ttu-id="92551-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="92551-123">Requirement</span></span> | <span data-ttu-id="92551-124">Valore</span><span class="sxs-lookup"><span data-stu-id="92551-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92551-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92551-125">Minimum supported client</span></span><br/> | <span data-ttu-id="92551-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="92551-126">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="92551-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92551-127">Minimum supported server</span></span><br/> | <span data-ttu-id="92551-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92551-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="92551-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92551-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="92551-130"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="92551-130"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="92551-131">IDL</span><span class="sxs-lookup"><span data-stu-id="92551-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92551-132"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="92551-132"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="92551-133">DLL</span><span class="sxs-lookup"><span data-stu-id="92551-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92551-134"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92551-134"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="92551-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92551-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92551-136">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="92551-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="92551-137">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="92551-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

