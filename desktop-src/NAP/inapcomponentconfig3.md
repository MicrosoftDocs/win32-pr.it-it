---
title: Interfaccia INapComponentConfig3 (NapCommon. h)
description: Fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per impostare e modificare i dati di configurazione per un ID configurazione specifico.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- NAP interfaccia INapComponentConfig3
- Interfaccia NAP di INapComponentConfig3, descrizione
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301068"
---
# <a name="inapcomponentconfig3-interface"></a><span data-ttu-id="3002a-105">Interfaccia INapComponentConfig3</span><span class="sxs-lookup"><span data-stu-id="3002a-105">INapComponentConfig3 interface</span></span>

> [!Note]  
> <span data-ttu-id="3002a-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="3002a-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3002a-107">L'interfaccia **INapComponentConfig3** fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per impostare e modificare i dati di configurazione per un ID configurazione specifico.</span><span class="sxs-lookup"><span data-stu-id="3002a-107">The **INapComponentConfig3** interface provides NAP system configuration methods for system health validators (SHVs) to set and modify configuration data for a specific configuration ID.</span></span>

> [!Note]  
> <span data-ttu-id="3002a-108">Questa interfaccia eredita tutti i metodi di [**INapComponentConfig2**](inapcomponentconfig2.md) e deve essere usata in alternativa.</span><span class="sxs-lookup"><span data-stu-id="3002a-108">This interface inherits all the methods of [**INapComponentConfig2**](inapcomponentconfig2.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="3002a-109">Membri</span><span class="sxs-lookup"><span data-stu-id="3002a-109">Members</span></span>

<span data-ttu-id="3002a-110">L'interfaccia **INapComponentConfig3** eredita da [**INapComponentConfig2**](inapcomponentconfig2.md).</span><span class="sxs-lookup"><span data-stu-id="3002a-110">The **INapComponentConfig3** interface inherits from [**INapComponentConfig2**](inapcomponentconfig2.md).</span></span> <span data-ttu-id="3002a-111">**INapComponentConfig3** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3002a-111">**INapComponentConfig3** also has these types of members:</span></span>

-   [<span data-ttu-id="3002a-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="3002a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3002a-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="3002a-113">Methods</span></span>

<span data-ttu-id="3002a-114">L'interfaccia **INapComponentConfig3** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3002a-114">The **INapComponentConfig3** interface has these methods.</span></span>



| <span data-ttu-id="3002a-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="3002a-115">Method</span></span>                                                                                | <span data-ttu-id="3002a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3002a-116">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3002a-117">**INapComponentConfig3::D eleteAllConfig**</span><span class="sxs-lookup"><span data-stu-id="3002a-117">**INapComponentConfig3::DeleteAllConfig**</span></span>](inapcomponentconfig3-deleteallconfig.md) | <span data-ttu-id="3002a-118">Implementata da SHV per fornire un modo per reimpostare l'archivio di convalida integrità di sistema sullo stato originale dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="3002a-118">Implemented by SHVs to provide a way to reset the SHV store to its original state after setup.</span></span><br/>      |
| [<span data-ttu-id="3002a-119">**INapComponentConfig3::D eleteConfig**</span><span class="sxs-lookup"><span data-stu-id="3002a-119">**INapComponentConfig3::DeleteConfig**</span></span>](inapcomponentconfig3-deleteconfig.md)       | <span data-ttu-id="3002a-120">Implementato da SHV per fornire un modo per eliminare i dati di configurazione per un ID configurazione specifico.</span><span class="sxs-lookup"><span data-stu-id="3002a-120">Implemented by SHVs to provide a way to delete configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="3002a-121">**INapComponentConfig3::GetConfigFromID**</span><span class="sxs-lookup"><span data-stu-id="3002a-121">**INapComponentConfig3::GetConfigFromID**</span></span>](inapcomponentconfig3-getconfigfromid.md) | <span data-ttu-id="3002a-122">Implementato da SHV per fornire un modo per ottenere i dati di configurazione per un ID configurazione specifico.</span><span class="sxs-lookup"><span data-stu-id="3002a-122">Implemented by SHVs to provide a way to obtain configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="3002a-123">**INapComponentConfig3:: NewConfig**</span><span class="sxs-lookup"><span data-stu-id="3002a-123">**INapComponentConfig3::NewConfig**</span></span>](inapcomponentconfig3-newconfig.md)             | <span data-ttu-id="3002a-124">Implementato da SHV per fornire un modo per creare i dati di configurazione per un ID configurazione specifico.</span><span class="sxs-lookup"><span data-stu-id="3002a-124">Implemented by SHVs to provide a way to create configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="3002a-125">**INapComponentConfig3::SetConfigToID**</span><span class="sxs-lookup"><span data-stu-id="3002a-125">**INapComponentConfig3::SetConfigToID**</span></span>](inapcomponentconfig3-setconfigtoid.md)     | <span data-ttu-id="3002a-126">Implementato da SHV per fornire un modo per impostare i dati di configurazione per un ID configurazione specifico.</span><span class="sxs-lookup"><span data-stu-id="3002a-126">Implemented by SHVs to provide a way to set the configuration data for a specific configuration ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3002a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="3002a-127">Remarks</span></span>

<span data-ttu-id="3002a-128">Questa interfaccia non deve essere implementata dagli agenti di integrità del sistema (SHAs) o dai client di imposizione di quarantena (QeC).</span><span class="sxs-lookup"><span data-stu-id="3002a-128">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="3002a-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3002a-129">Requirements</span></span>



| <span data-ttu-id="3002a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3002a-130">Requirement</span></span> | <span data-ttu-id="3002a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3002a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3002a-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3002a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3002a-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3002a-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3002a-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3002a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3002a-135">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3002a-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3002a-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3002a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3002a-137"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3002a-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="3002a-138">IDL</span><span class="sxs-lookup"><span data-stu-id="3002a-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3002a-139"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3002a-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3002a-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3002a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3002a-141">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="3002a-141">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> <dt>

[<span data-ttu-id="3002a-142">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="3002a-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3002a-143">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="3002a-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





