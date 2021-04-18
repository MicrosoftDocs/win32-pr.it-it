---
description: Rappresenta lo stato configurato di una porta PCI Express.
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Classe Msvm_PciExpressSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318317"
---
# <a name="msvm_pciexpresssettingdata-class"></a><span data-ttu-id="19145-103">\_Classe MSVM PciExpressSettingData</span><span class="sxs-lookup"><span data-stu-id="19145-103">Msvm\_PciExpressSettingData class</span></span>

<span data-ttu-id="19145-104">Rappresenta lo stato configurato di una porta PCI Express.</span><span class="sxs-lookup"><span data-stu-id="19145-104">Represents the configured state of a PCI Express port.</span></span>

<span data-ttu-id="19145-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="19145-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19145-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19145-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="19145-107">Members</span><span class="sxs-lookup"><span data-stu-id="19145-107">Members</span></span>

<span data-ttu-id="19145-108">La **classe \_ PciExpressSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="19145-108">The **Msvm\_PciExpressSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="19145-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19145-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19145-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19145-110">Properties</span></span>

<span data-ttu-id="19145-111">La **classe \_ PciExpressSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="19145-111">The **Msvm\_PciExpressSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19145-112">**VirtualFunctions**</span><span class="sxs-lookup"><span data-stu-id="19145-112">**VirtualFunctions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19145-113">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="19145-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="19145-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="19145-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="19145-115">Numero della funzione virtuale da assegnare alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="19145-115">The virtual function number to assign to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="19145-116">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="19145-116">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19145-117">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="19145-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="19145-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19145-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19145-119">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="19145-119">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="19145-120">Matrice di stringhe in formato libero di identificatori di questa risorsa presentata al sistema operativo del computer virtuale.</span><span class="sxs-lookup"><span data-stu-id="19145-120">A free-form string array of identifiers of this resource presented to the virtual computer system's operating system.</span></span> <span data-ttu-id="19145-121">Gli indici e i valori per indice vengono definiti in base alle singole risorse, ovvero per ogni valore di **ResourceType** enumerato.</span><span class="sxs-lookup"><span data-stu-id="19145-121">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="19145-122">Questa proprietà è impostata su "GUID".</span><span class="sxs-lookup"><span data-stu-id="19145-122">This property is set to "GUID".</span></span>

<span data-ttu-id="19145-123">Si tratta di una proprietà di sola lettura, ma può essere modificata usando il metodo [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) della classe SD.</span><span class="sxs-lookup"><span data-stu-id="19145-123">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the sd class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19145-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19145-124">Requirements</span></span>



| <span data-ttu-id="19145-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="19145-125">Requirement</span></span> | <span data-ttu-id="19145-126">Valore</span><span class="sxs-lookup"><span data-stu-id="19145-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19145-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19145-127">Minimum supported client</span></span><br/> | <span data-ttu-id="19145-128">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="19145-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="19145-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19145-129">Minimum supported server</span></span><br/> | <span data-ttu-id="19145-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="19145-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="19145-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19145-131">Namespace</span></span><br/>                | <span data-ttu-id="19145-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="19145-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="19145-133">MOF</span><span class="sxs-lookup"><span data-stu-id="19145-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19145-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19145-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19145-135">DLL</span><span class="sxs-lookup"><span data-stu-id="19145-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19145-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19145-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="19145-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19145-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19145-138">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="19145-138">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

