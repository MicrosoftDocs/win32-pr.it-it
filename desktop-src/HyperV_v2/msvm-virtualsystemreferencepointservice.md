---
description: Descrive un servizio del punto di riferimento del sistema virtuale.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320560"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="d1883-103">\_Classe MSVM VirtualSystemReferencePointService</span><span class="sxs-lookup"><span data-stu-id="d1883-103">Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="d1883-104">Descrive un servizio del punto di riferimento del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1883-104">Describes a virtual system reference point service.</span></span>

<span data-ttu-id="d1883-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d1883-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1883-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1883-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="d1883-107">Members</span><span class="sxs-lookup"><span data-stu-id="d1883-107">Members</span></span>

<span data-ttu-id="d1883-108">La **classe \_ VirtualSystemReferencePointService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d1883-108">The **Msvm\_VirtualSystemReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="d1883-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d1883-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d1883-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="d1883-110">Methods</span></span>

<span data-ttu-id="d1883-111">La **classe \_ VirtualSystemReferencePointService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d1883-111">The **Msvm\_VirtualSystemReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="d1883-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="d1883-112">Method</span></span>                                                                                                       | <span data-ttu-id="d1883-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1883-113">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="d1883-114">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="d1883-114">**CreateReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | <span data-ttu-id="d1883-115">Crea un punto di riferimento di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1883-115">Creates a reference point of a virtual system.</span></span><br/>            |
| [<span data-ttu-id="d1883-116">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="d1883-116">**DestroyReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | <span data-ttu-id="d1883-117">Elimina il punto di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="d1883-117">Deletes the specified reference point.</span></span><br/>                    |
| [<span data-ttu-id="d1883-118">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="d1883-118">**ExportReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | <span data-ttu-id="d1883-119">Esporta il punto di riferimento del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1883-119">Exports the reference point of the virtual system.</span></span><br/>        |
| [<span data-ttu-id="d1883-120">**ImportReferencePointMetadata**</span><span class="sxs-lookup"><span data-stu-id="d1883-120">**ImportReferencePointMetadata**</span></span>](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | <span data-ttu-id="d1883-121">Importa i metadati del punto di riferimento del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1883-121">Imports reference point metadata of the virtual system.</span></span><br/>   |
| [<span data-ttu-id="d1883-122">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="d1883-122">**RemoveAssociatedData**</span></span>](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | <span data-ttu-id="d1883-123">Rimuove il log dei dati associato al punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="d1883-123">Removes the data log associated with the reference point.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d1883-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1883-124">Requirements</span></span>



| <span data-ttu-id="d1883-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1883-125">Requirement</span></span> | <span data-ttu-id="d1883-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d1883-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1883-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1883-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d1883-128">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d1883-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d1883-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1883-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d1883-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d1883-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d1883-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d1883-131">Namespace</span></span><br/>                | <span data-ttu-id="d1883-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d1883-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d1883-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d1883-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1883-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1883-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1883-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d1883-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1883-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1883-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d1883-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1883-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1883-138">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="d1883-138">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




