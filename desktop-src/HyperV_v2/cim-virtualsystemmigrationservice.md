---
description: Rappresenta un servizio che controlla la migrazione di sistemi virtuali tra sistemi host. Questa classe verifica anche se è probabile che una migrazione in sospeso abbia esito positivo.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: Classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881217"
---
# <a name="cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="14f55-104">CIM \_ VirtualSystemMigrationService (classe)</span><span class="sxs-lookup"><span data-stu-id="14f55-104">CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="14f55-105">Rappresenta un servizio che controlla la migrazione di sistemi virtuali tra sistemi host.</span><span class="sxs-lookup"><span data-stu-id="14f55-105">Represents a service that controls the migration of virtual systems between host systems.</span></span> <span data-ttu-id="14f55-106">Questa classe verifica anche se è probabile che una migrazione in sospeso abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="14f55-106">This class also verifies whether a pending migration is likely to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f55-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14f55-107">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="14f55-108">Members</span><span class="sxs-lookup"><span data-stu-id="14f55-108">Members</span></span>

<span data-ttu-id="14f55-109">La classe **CIM \_ VirtualSystemMigrationService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="14f55-109">The **CIM\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="14f55-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="14f55-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="14f55-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="14f55-111">Methods</span></span>

<span data-ttu-id="14f55-112">La classe **CIM \_ VirtualSystemMigrationService** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="14f55-112">The **CIM\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="14f55-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="14f55-113">Method</span></span>                                                                                                                     | <span data-ttu-id="14f55-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14f55-114">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14f55-115">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="14f55-115">**CheckVirtualSystemIsMigratableToHost**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | <span data-ttu-id="14f55-116">Verifica se è probabile che la migrazione di un sistema virtuale in sospeso a un host abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="14f55-116">Verifies whether a pending virtual system migration to a host is likely to succeed.</span></span><br/>   |
| [<span data-ttu-id="14f55-117">**CheckVirtualSystemIsMigratableToSystem**</span><span class="sxs-lookup"><span data-stu-id="14f55-117">**CheckVirtualSystemIsMigratableToSystem**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | <span data-ttu-id="14f55-118">Verifica se una migrazione del sistema virtuale in sospeso a un sistema ha probabilmente esito positivo.</span><span class="sxs-lookup"><span data-stu-id="14f55-118">Verifies whether a pending virtual system migration to a system is likely to succeed.</span></span><br/> |
| [<span data-ttu-id="14f55-119">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="14f55-119">**MigrateVirtualSystemToHost**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | <span data-ttu-id="14f55-120">Esegue la migrazione di un sistema virtuale a un host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="14f55-120">Migrates a virtual system to a target host.</span></span><br/>                                           |
| [<span data-ttu-id="14f55-121">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="14f55-121">**MigrateVirtualSystemToSystem**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | <span data-ttu-id="14f55-122">Esegue la migrazione di un sistema virtuale al sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="14f55-122">Migrates a virtual system to target system.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="14f55-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14f55-123">Requirements</span></span>



| <span data-ttu-id="14f55-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="14f55-124">Requirement</span></span> | <span data-ttu-id="14f55-125">Valore</span><span class="sxs-lookup"><span data-stu-id="14f55-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f55-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14f55-126">Minimum supported client</span></span><br/> | <span data-ttu-id="14f55-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="14f55-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="14f55-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14f55-128">Minimum supported server</span></span><br/> | <span data-ttu-id="14f55-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14f55-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="14f55-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="14f55-130">Namespace</span></span><br/>                | <span data-ttu-id="14f55-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="14f55-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14f55-132">MOF</span><span class="sxs-lookup"><span data-stu-id="14f55-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14f55-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14f55-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14f55-134">DLL</span><span class="sxs-lookup"><span data-stu-id="14f55-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14f55-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14f55-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14f55-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14f55-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f55-137">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="14f55-137">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




