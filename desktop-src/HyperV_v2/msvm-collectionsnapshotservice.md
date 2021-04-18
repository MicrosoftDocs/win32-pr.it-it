---
description: Servizio per la creazione, l'eliminazione e l'esportazione di raccolte di snapshot di sistemi virtuali.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310015"
---
# <a name="msvm_collectionsnapshotservice-class"></a><span data-ttu-id="c079b-103">\_Classe MSVM CollectionSnapshotService</span><span class="sxs-lookup"><span data-stu-id="c079b-103">Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="c079b-104">Servizio per la creazione, l'eliminazione e l'esportazione di raccolte di snapshot di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="c079b-104">Service to create, destroy and export snapshot collection of virtual systems.</span></span>

<span data-ttu-id="c079b-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c079b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c079b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c079b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="c079b-107">Members</span><span class="sxs-lookup"><span data-stu-id="c079b-107">Members</span></span>

<span data-ttu-id="c079b-108">La **classe \_ CollectionSnapshotService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c079b-108">The **Msvm\_CollectionSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="c079b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="c079b-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c079b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="c079b-110">Methods</span></span>

<span data-ttu-id="c079b-111">La **classe \_ CollectionSnapshotService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c079b-111">The **Msvm\_CollectionSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="c079b-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="c079b-112">Method</span></span>                                                                                    | <span data-ttu-id="c079b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c079b-113">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c079b-114">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="c079b-114">**ApplySnapshot**</span></span>](msvm-collectionsnapshotservice-applysnapshot.md)                     | <span data-ttu-id="c079b-115">Applica una raccolta snapshot alla raccolta del sistema di computer virtuale.</span><span class="sxs-lookup"><span data-stu-id="c079b-115">Applies a snapshot collection to the collection of virtual computer system.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="c079b-116">**ConvertToReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="c079b-116">**ConvertToReferencePoint**</span></span>](msvm-collectionsnapshotservice-converttoreferencepoint.md) | <span data-ttu-id="c079b-117">Converte uno snapshot di raccolta esistente in una raccolta di punti di riferimento.</span><span class="sxs-lookup"><span data-stu-id="c079b-117">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="c079b-118">La raccolta snapshot viene eliminata come effetto collaterale.</span><span class="sxs-lookup"><span data-stu-id="c079b-118">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="c079b-119">Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.</span><span class="sxs-lookup"><span data-stu-id="c079b-119">Only recovery snapshots can be converted to reference points.</span></span><br/>                      |
| [<span data-ttu-id="c079b-120">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="c079b-120">**CreateSnapshot**</span></span>](msvm-collectionsnapshotservice-createsnapshot.md)                   | <span data-ttu-id="c079b-121">Crea uno snapshot di una raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="c079b-121">Creates a snapshot of a virtual system collection.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="c079b-122">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="c079b-122">**DestroySnapshot**</span></span>](msvm-collectionsnapshotservice-destroysnapshot.md)                 | <span data-ttu-id="c079b-123">Elimina uno snapshot esistente della raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="c079b-123">Destroy an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="c079b-124">Questo metodo può essere un effetto collaterale per eliminare altri snapshot che dipendono dallo snapshot interessato.</span><span class="sxs-lookup"><span data-stu-id="c079b-124">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span><br/>                                                   |
| [<span data-ttu-id="c079b-125">**ExportSnapshot**</span><span class="sxs-lookup"><span data-stu-id="c079b-125">**ExportSnapshot**</span></span>](msvm-collectionsnapshotservice-exportsnapshot.md)                   | <span data-ttu-id="c079b-126">Esporta in un file una raccolta snapshot di sistemi di computer virtuali.</span><span class="sxs-lookup"><span data-stu-id="c079b-126">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="c079b-127">La raccolta di snapshot, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.</span><span class="sxs-lookup"><span data-stu-id="c079b-127">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c079b-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c079b-128">Requirements</span></span>



| <span data-ttu-id="c079b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c079b-129">Requirement</span></span> | <span data-ttu-id="c079b-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c079b-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c079b-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c079b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c079b-132">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c079b-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c079b-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c079b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c079b-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c079b-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c079b-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c079b-135">Namespace</span></span><br/>                | <span data-ttu-id="c079b-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c079b-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c079b-137">MOF</span><span class="sxs-lookup"><span data-stu-id="c079b-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c079b-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c079b-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c079b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c079b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c079b-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c079b-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c079b-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c079b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c079b-142">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="c079b-142">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




