---
description: Rappresenta un servizio in grado di creare, applicare ed eliminare snapshot di sistemi virtuali.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: Classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ae74f85d1af9867b7a95c23aeda670b8f06f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885869"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="2a581-103">CIM \_ VirtualSystemSnapshotService (classe)</span><span class="sxs-lookup"><span data-stu-id="2a581-103">CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="2a581-104">Rappresenta un servizio in grado di creare, applicare ed eliminare snapshot di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="2a581-104">Represents a service that can create, apply, and delete snapshots of virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a581-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a581-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="2a581-106">Members</span><span class="sxs-lookup"><span data-stu-id="2a581-106">Members</span></span>

<span data-ttu-id="2a581-107">La classe **CIM \_ VirtualSystemSnapshotService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2a581-107">The **CIM\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="2a581-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="2a581-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2a581-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="2a581-109">Methods</span></span>

<span data-ttu-id="2a581-110">La classe **CIM \_ VirtualSystemSnapshotService** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2a581-110">The **CIM\_VirtualSystemSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="2a581-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="2a581-111">Method</span></span>                                                                      | <span data-ttu-id="2a581-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a581-112">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a581-113">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="2a581-113">**ApplySnapshot**</span></span>](cim-virtualsystemsnapshotservice-applysnapshot.md)     | <span data-ttu-id="2a581-114">Applica uno snapshot del sistema virtuale al sistema virtuale di origine.</span><span class="sxs-lookup"><span data-stu-id="2a581-114">Applies a virtual system snapshot to the virtual system to the source virtual system.</span></span><br/> |
| [<span data-ttu-id="2a581-115">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="2a581-115">**CreateSnapshot**</span></span>](cim-virtualsystemsnapshotservice-createsnapshot.md)   | <span data-ttu-id="2a581-116">Crea uno snapshot di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="2a581-116">Creates a snapshot of a virtual system.</span></span><br/>                                               |
| [<span data-ttu-id="2a581-117">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="2a581-117">**DestroySnapshot**</span></span>](cim-virtualsystemsnapshotservice-destroysnapshot.md) | <span data-ttu-id="2a581-118">Elimina uno snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="2a581-118">Deletes a virtual system snapshot.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="2a581-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a581-119">Requirements</span></span>



| <span data-ttu-id="2a581-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a581-120">Requirement</span></span> | <span data-ttu-id="2a581-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2a581-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a581-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a581-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a581-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2a581-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2a581-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a581-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a581-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a581-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2a581-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2a581-126">Namespace</span></span><br/>                | <span data-ttu-id="2a581-127">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2a581-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2a581-128">MOF</span><span class="sxs-lookup"><span data-stu-id="2a581-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a581-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a581-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a581-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2a581-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a581-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a581-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a581-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a581-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a581-133">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="2a581-133">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




