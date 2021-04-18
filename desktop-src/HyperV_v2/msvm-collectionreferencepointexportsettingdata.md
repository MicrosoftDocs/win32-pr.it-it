---
description: Esportare i dati delle impostazioni da passare al metodo ExportReferencePoint della \_ classe CollectionReferencePointService di MSVM.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Classe Msvm_CollectionReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317197"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a><span data-ttu-id="2557f-103">\_Classe MSVM CollectionReferencePointExportSettingData</span><span class="sxs-lookup"><span data-stu-id="2557f-103">Msvm\_CollectionReferencePointExportSettingData class</span></span>

<span data-ttu-id="2557f-104">Esportare i dati delle impostazioni da passare al metodo [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) della classe [**\_ CollectionReferencePointService di MSVM**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="2557f-104">Export setting data to be passed in to the [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="2557f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2557f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2557f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2557f-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="2557f-107">Members</span><span class="sxs-lookup"><span data-stu-id="2557f-107">Members</span></span>

<span data-ttu-id="2557f-108">La **classe \_ CollectionReferencePointExportSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2557f-108">The **Msvm\_CollectionReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2557f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2557f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2557f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2557f-110">Properties</span></span>

<span data-ttu-id="2557f-111">La **classe \_ CollectionReferencePointExportSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2557f-111">The **Msvm\_CollectionReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2557f-112">**BaseReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="2557f-112">**BaseReferencePointCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2557f-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2557f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2557f-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2557f-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2557f-115">Percorso di un'istanza di [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) che rappresenta la raccolta di punti di riferimento di base da utilizzare per l'esportazione differenziale.</span><span class="sxs-lookup"><span data-stu-id="2557f-115">Path to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the base reference point collection to be used for differential export.</span></span>

</dd> <dt>

<span data-ttu-id="2557f-116">**VirtualMachinesToDisksToExport**</span><span class="sxs-lookup"><span data-stu-id="2557f-116">**VirtualMachinesToDisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2557f-117">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2557f-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2557f-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2557f-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2557f-119">Qualificatori: **HyperVEmbeddedInstance** ("MSVM \_ VirtualMachineToDisks")</span><span class="sxs-lookup"><span data-stu-id="2557f-119">Qualifiers: **HyperVEmbeddedInstance** ("Msvm\_VirtualMachineToDisks")</span></span>
</dt> </dl>

<span data-ttu-id="2557f-120">Elenco di informazioni della mappa "VirtualMachines to DisksToExport" per cui è necessario esportare i dati.</span><span class="sxs-lookup"><span data-stu-id="2557f-120">List of "VirtualMachines To DisksToExport" map information for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2557f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2557f-121">Requirements</span></span>



| <span data-ttu-id="2557f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2557f-122">Requirement</span></span> | <span data-ttu-id="2557f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2557f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2557f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2557f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2557f-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2557f-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2557f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2557f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2557f-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2557f-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2557f-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2557f-128">Namespace</span></span><br/>                | <span data-ttu-id="2557f-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2557f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2557f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2557f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2557f-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2557f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2557f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2557f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2557f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2557f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2557f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2557f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2557f-135">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="2557f-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




