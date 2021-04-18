---
description: Rappresenta un servizio che gestisce i sistemi virtuali.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: Classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311142"
---
# <a name="cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="d467b-103">CIM \_ VirtualSystemManagementService (classe)</span><span class="sxs-lookup"><span data-stu-id="d467b-103">CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d467b-104">Rappresenta un servizio che gestisce i sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="d467b-104">Represents a service that manages virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="d467b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d467b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="d467b-106">Members</span><span class="sxs-lookup"><span data-stu-id="d467b-106">Members</span></span>

<span data-ttu-id="d467b-107">La classe **CIM \_ VirtualSystemManagementService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d467b-107">The **CIM\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="d467b-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="d467b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d467b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d467b-109">Methods</span></span>

<span data-ttu-id="d467b-110">La classe **CIM \_ VirtualSystemManagementService** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d467b-110">The **CIM\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="d467b-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="d467b-111">Method</span></span>                                                                                      | <span data-ttu-id="d467b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d467b-112">Description</span></span>                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d467b-113">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="d467b-113">**AddResourceSettings**</span></span>](cim-virtualsystemmanagementservice-addresourcesettings.md)       | <span data-ttu-id="d467b-114">Aggiunge risorse a una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d467b-114">Adds resources to a virtual system configuration.</span></span><br/>                          |
| [<span data-ttu-id="d467b-115">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="d467b-115">**DefineSystem**</span></span>](cim-virtualsystemmanagementservice-definesystem.md)                     | <span data-ttu-id="d467b-116">Definisce un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d467b-116">Defines a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="d467b-117">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="d467b-117">**DestroySystem**</span></span>](cim-virtualsystemmanagementservice-destroysystem.md)                   | <span data-ttu-id="d467b-118">Elimina un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d467b-118">Deletes a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="d467b-119">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="d467b-119">**ModifyResourceSettings**</span></span>](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | <span data-ttu-id="d467b-120">Modifica le impostazioni delle risorse virtuali per una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d467b-120">Modifies the virtual resource settings for a virtual system configuration.</span></span><br/> |
| [<span data-ttu-id="d467b-121">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="d467b-121">**ModifySystemSettings**</span></span>](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | <span data-ttu-id="d467b-122">Modifica le impostazioni del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d467b-122">Modifies virtual system settings.</span></span><br/>                                          |
| [<span data-ttu-id="d467b-123">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="d467b-123">**RemoveResourceSettings**</span></span>](cim-virtualsystemmanagementservice-removeresourcesettings.md) | <span data-ttu-id="d467b-124">Rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d467b-124">Removes virtual resource settings from a virtual system configuration.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="d467b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d467b-125">Requirements</span></span>



| <span data-ttu-id="d467b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d467b-126">Requirement</span></span> | <span data-ttu-id="d467b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d467b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d467b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d467b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d467b-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d467b-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d467b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d467b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d467b-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d467b-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d467b-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d467b-132">Namespace</span></span><br/>                | <span data-ttu-id="d467b-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d467b-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d467b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d467b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d467b-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d467b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d467b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d467b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d467b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d467b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d467b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d467b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d467b-139">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="d467b-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




