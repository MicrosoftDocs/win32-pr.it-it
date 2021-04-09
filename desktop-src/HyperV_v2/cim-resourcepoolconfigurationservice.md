---
description: Gestisce la configurazione dei pool di risorse utilizzando i processi.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: Classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879509"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="4b8aa-103">CIM \_ ResourcePoolConfigurationService (classe)</span><span class="sxs-lookup"><span data-stu-id="4b8aa-103">CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="4b8aa-104">Gestisce la configurazione dei pool di risorse utilizzando i processi.</span><span class="sxs-lookup"><span data-stu-id="4b8aa-104">Manages the configuration of resource pools by using jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b8aa-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="4b8aa-106">Members</span><span class="sxs-lookup"><span data-stu-id="4b8aa-106">Members</span></span>

<span data-ttu-id="4b8aa-107">La classe **CIM \_ ResourcePoolConfigurationService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4b8aa-107">The **CIM\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="4b8aa-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="4b8aa-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4b8aa-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="4b8aa-109">Methods</span></span>

<span data-ttu-id="4b8aa-110">La classe **CIM \_ ResourcePoolConfigurationService** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4b8aa-110">The **CIM\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="4b8aa-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="4b8aa-111">Method</span></span>                                                                                                          | <span data-ttu-id="4b8aa-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b8aa-112">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="4b8aa-113">**AddResourcesToResourcePool**</span><span class="sxs-lookup"><span data-stu-id="4b8aa-113">**AddResourcesToResourcePool**</span></span>](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | <span data-ttu-id="4b8aa-114">Avvia un processo per l'aggiunta di risorse a un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b8aa-114">Starts a job to add resources to a resource pool.</span></span><br/>                  |
| [<span data-ttu-id="4b8aa-115">**ChangeParentResourcePool**</span><span class="sxs-lookup"><span data-stu-id="4b8aa-115">**ChangeParentResourcePool**</span></span>](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | <span data-ttu-id="4b8aa-116">Avviare un processo per modificare il pool di risorse padre di un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b8aa-116">Start a job to change the parent resource pool of a resource pool.</span></span><br/> |
| [<span data-ttu-id="4b8aa-117">**CreateChildResourcePool**</span><span class="sxs-lookup"><span data-stu-id="4b8aa-117">**CreateChildResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | <span data-ttu-id="4b8aa-118">Avviare un processo per creare un pool di risorse da un pool di risorse padre.</span><span class="sxs-lookup"><span data-stu-id="4b8aa-118">Start a job to create a resource pool from a parent resource pool.</span></span><br/> |
| [<span data-ttu-id="4b8aa-119">**CreateResourcePool**</span><span class="sxs-lookup"><span data-stu-id="4b8aa-119">**CreateResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | <span data-ttu-id="4b8aa-120">Avvia un processo per creare un pool di risorse radice.</span><span class="sxs-lookup"><span data-stu-id="4b8aa-120">Starts a job to create a root resource pool.</span></span><br/>                       |
| [<span data-ttu-id="4b8aa-121">**DeleteResourcePool**</span><span class="sxs-lookup"><span data-stu-id="4b8aa-121">**DeleteResourcePool**</span></span>](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | <span data-ttu-id="4b8aa-122">Avviare un processo per eliminare un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b8aa-122">Start a job to delete a resource pool.</span></span><br/>                             |
| [<span data-ttu-id="4b8aa-123">**RemoveResourcesFromResourcePool**</span><span class="sxs-lookup"><span data-stu-id="4b8aa-123">**RemoveResourcesFromResourcePool**</span></span>](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | <span data-ttu-id="4b8aa-124">Avvia un processo per rimuovere le risorse da un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b8aa-124">Starts a job to remove resources from a resource pool.</span></span><br/>             |



 

## <a name="requirements"></a><span data-ttu-id="4b8aa-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b8aa-125">Requirements</span></span>



| <span data-ttu-id="4b8aa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b8aa-126">Requirement</span></span> | <span data-ttu-id="4b8aa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4b8aa-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8aa-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b8aa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4b8aa-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4b8aa-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4b8aa-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b8aa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4b8aa-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4b8aa-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4b8aa-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b8aa-132">Namespace</span></span><br/>                | <span data-ttu-id="4b8aa-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4b8aa-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b8aa-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4b8aa-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b8aa-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b8aa-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b8aa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4b8aa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b8aa-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b8aa-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b8aa-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b8aa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8aa-139">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="4b8aa-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




