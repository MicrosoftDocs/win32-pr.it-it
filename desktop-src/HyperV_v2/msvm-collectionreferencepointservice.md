---
description: Servizio per la creazione, l'eliminazione e l'esportazione di punti di riferimento.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308338"
---
# <a name="msvm_collectionreferencepointservice-class"></a><span data-ttu-id="a0c09-103">\_Classe MSVM CollectionReferencePointService</span><span class="sxs-lookup"><span data-stu-id="a0c09-103">Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="a0c09-104">Servizio per la creazione, l'eliminazione e l'esportazione di punti di riferimento</span><span class="sxs-lookup"><span data-stu-id="a0c09-104">Service to create, destroy and export reference points</span></span>

<span data-ttu-id="a0c09-105">delle raccolte di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="a0c09-105">of virtual system collections.</span></span>

<span data-ttu-id="a0c09-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a0c09-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0c09-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0c09-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="a0c09-108">Members</span><span class="sxs-lookup"><span data-stu-id="a0c09-108">Members</span></span>

<span data-ttu-id="a0c09-109">La **classe \_ CollectionReferencePointService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a0c09-109">The **Msvm\_CollectionReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="a0c09-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a0c09-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0c09-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a0c09-111">Methods</span></span>

<span data-ttu-id="a0c09-112">La **classe \_ CollectionReferencePointService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a0c09-112">The **Msvm\_CollectionReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="a0c09-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="a0c09-113">Method</span></span>                                                                                      | <span data-ttu-id="a0c09-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0c09-114">Description</span></span>                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0c09-115">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="a0c09-115">**CreateReferencePoint**</span></span>](msvm-collectionreferencepointservice-createreferencepoint.md)   | <span data-ttu-id="a0c09-116">Crea un punto di riferimento di una raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="a0c09-116">Creates a reference point of a virtual system collection.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="a0c09-117">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="a0c09-117">**DestroyReferencePoint**</span></span>](msvm-collectionreferencepointservice-destroyreferencepoint.md) | <span data-ttu-id="a0c09-118">Elimina definitivamente una raccolta di punti di riferimento esistente.</span><span class="sxs-lookup"><span data-stu-id="a0c09-118">Destroys an existing reference point collection.</span></span> <span data-ttu-id="a0c09-119">Questo metodo può essere un effetto collaterale per eliminare altri punti di riferimento che dipendono dalla raccolta di punti di riferimento interessata.</span><span class="sxs-lookup"><span data-stu-id="a0c09-119">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span><br/>                      |
| [<span data-ttu-id="a0c09-120">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="a0c09-120">**ExportReferencePoint**</span></span>](msvm-collectionreferencepointservice-exportreferencepoint.md)   | <span data-ttu-id="a0c09-121">Esporta una raccolta di punti di riferimento in un file.</span><span class="sxs-lookup"><span data-stu-id="a0c09-121">Exports a reference point collection to a file.</span></span> <span data-ttu-id="a0c09-122">La raccolta di punti di riferimento, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.</span><span class="sxs-lookup"><span data-stu-id="a0c09-122">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |
| [<span data-ttu-id="a0c09-123">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="a0c09-123">**RemoveAssociatedData**</span></span>](msvm-collectionreferencepointservice-removeassociateddata.md)   | <span data-ttu-id="a0c09-124">Rimuove il log dei dati associato al punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a0c09-124">Removes the data log associated with the reference point.</span></span><br/>                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="a0c09-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0c09-125">Requirements</span></span>



| <span data-ttu-id="a0c09-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0c09-126">Requirement</span></span> | <span data-ttu-id="a0c09-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a0c09-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0c09-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0c09-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a0c09-129">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a0c09-129">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a0c09-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0c09-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a0c09-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a0c09-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a0c09-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0c09-132">Namespace</span></span><br/>                | <span data-ttu-id="a0c09-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a0c09-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a0c09-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a0c09-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0c09-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0c09-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0c09-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a0c09-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0c09-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0c09-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0c09-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0c09-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0c09-139">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="a0c09-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




