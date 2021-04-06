---
description: Gestisce le raccolte nell'host Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760496"
---
# <a name="msvm_collectionmanagementservice-class"></a><span data-ttu-id="5d673-103">\_Classe MSVM CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="5d673-103">Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="5d673-104">Gestisce le raccolte nell'host Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="5d673-104">Manages the collections on the Hyper-V host.</span></span>

<span data-ttu-id="5d673-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5d673-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d673-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d673-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="5d673-107">Members</span><span class="sxs-lookup"><span data-stu-id="5d673-107">Members</span></span>

<span data-ttu-id="5d673-108">La **classe \_ CollectionManagementService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5d673-108">The **Msvm\_CollectionManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="5d673-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="5d673-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d673-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="5d673-110">Methods</span></span>

<span data-ttu-id="5d673-111">La **classe \_ CollectionManagementService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5d673-111">The **Msvm\_CollectionManagementService** class has these methods.</span></span>



| <span data-ttu-id="5d673-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="5d673-112">Method</span></span>                                                                          | <span data-ttu-id="5d673-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d673-113">Description</span></span>                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d673-114">**AddMember**</span><span class="sxs-lookup"><span data-stu-id="5d673-114">**AddMember**</span></span>](msvm-collectionmanagementservice-addmember.md)                 | <span data-ttu-id="5d673-115">Aggiunge il Managementelement specificato come membro dell'oggetto [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="5d673-115">Adds the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                           |
| [<span data-ttu-id="5d673-116">**Definecollection**</span><span class="sxs-lookup"><span data-stu-id="5d673-116">**DefineCollection**</span></span>](msvm-collectionmanagementservice-definecollection.md)   | <span data-ttu-id="5d673-117">Crea un nuovo [**oggetto \_ CollectionOfMSEs CIM**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="5d673-117">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="5d673-118">**Distruttore**</span><span class="sxs-lookup"><span data-stu-id="5d673-118">**DestroyCollection**</span></span>](msvm-collectionmanagementservice-destroycollection.md) | <span data-ttu-id="5d673-119">Elimina l'oggetto [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="5d673-119">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="5d673-120">**RemoveMember**</span><span class="sxs-lookup"><span data-stu-id="5d673-120">**RemoveMember**</span></span>](msvm-collectionmanagementservice-removemember.md)           | <span data-ttu-id="5d673-121">Rimuove il Managementelement specificato come membro dell'oggetto [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="5d673-121">Removes the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="5d673-122">**RemoveMemberById**</span><span class="sxs-lookup"><span data-stu-id="5d673-122">**RemoveMemberById**</span></span>](msvm-collectionmanagementservice-removememberbyid.md)   | <span data-ttu-id="5d673-123">Rimuove l'oggetto gestito specificato come membro del [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="5d673-123">Removes the specified ManagedElement as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="5d673-124">Questa operazione avrà esito positivo anche se l'oggetto con tale identificatore non è presente.</span><span class="sxs-lookup"><span data-stu-id="5d673-124">This will succeed even if the object with that identifier is not present.</span></span><br/> |
| [<span data-ttu-id="5d673-125">**Rinominacollection**</span><span class="sxs-lookup"><span data-stu-id="5d673-125">**RenameCollection**</span></span>](msvm-collectionmanagementservice-renamecollection.md)   | <span data-ttu-id="5d673-126">Aggiorna l'elemento ElementName dell' [**oggetto \_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="5d673-126">Updates the ElementName the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="5d673-127">**StartService**</span><span class="sxs-lookup"><span data-stu-id="5d673-127">**StartService**</span></span>](msvm-collectionmanagementservice-startservice.md)           | <span data-ttu-id="5d673-128">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="5d673-128">Starts the service.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="5d673-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="5d673-129">**StopService**</span></span>](msvm-collectionmanagementservice-stopservice.md)             | <span data-ttu-id="5d673-130">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="5d673-130">Stops the service.</span></span><br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="5d673-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d673-131">Requirements</span></span>



| <span data-ttu-id="5d673-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d673-132">Requirement</span></span> | <span data-ttu-id="5d673-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5d673-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d673-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d673-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5d673-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5d673-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5d673-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d673-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5d673-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5d673-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5d673-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5d673-138">Namespace</span></span><br/>                | <span data-ttu-id="5d673-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5d673-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5d673-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5d673-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d673-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d673-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d673-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5d673-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d673-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5d673-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5d673-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d673-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d673-145">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="5d673-145">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




