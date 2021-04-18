---
description: Descrive i dati delle impostazioni per un Commuter Ethernet virtuale.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: Classe CIM_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310557"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="f7766-103">CIM \_ VirtualEthernetSwitchSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="f7766-103">CIM\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="f7766-104">Descrive i dati delle impostazioni per un Commuter Ethernet virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7766-104">Describes settings data for a virtual ethernet switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7766-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7766-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="f7766-106">Members</span><span class="sxs-lookup"><span data-stu-id="f7766-106">Members</span></span>

<span data-ttu-id="f7766-107">La classe **CIM \_ VirtualEthernetSwitchSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f7766-107">The **CIM\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f7766-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7766-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7766-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7766-109">Properties</span></span>

<span data-ttu-id="f7766-110">La classe **CIM \_ VirtualEthernetSwitchSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7766-110">The **CIM\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7766-111">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="f7766-111">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7766-112">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f7766-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f7766-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7766-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7766-114">Matrice che contiene i pool di risorse host attualmente associati o da associare al compartitore Ethernet, allo scopo di allocare connessioni Ethernet tra il compartitore Ethernet e una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7766-114">An array that contains the host resource pools that are currently associated, or to associate with the ethernet switch, in order to allocate ethernet connections between the ethernet switch and a virtual machine.</span></span> <span data-ttu-id="f7766-115">Ogni valore non null di questa proprietà deve essere conforme **all' \_ URI WBEM \_ UntypedInstancePath** come definito nella specifica DMTF "DSP0207".</span><span class="sxs-lookup"><span data-stu-id="f7766-115">Each non-Null value of this property must conform to **WBEM\_URI\_UntypedInstancePath** as defined in the DMTF "DSP0207" specification.</span></span>

</dd> <dt>

<span data-ttu-id="f7766-116">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="f7766-116">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7766-117">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7766-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7766-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7766-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7766-119">Il numero di indirizzi MAC univoci che il Commuter può apprendere per l'apprendimento degli indirizzi MAC, come definito nello standard IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="f7766-119">The number of unique MAC addresses that the switch can learn for MAC address learning, as defined in the IEEE 802.1 standard.</span></span>

</dd> <dt>

<span data-ttu-id="f7766-120">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="f7766-120">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7766-121">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f7766-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f7766-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7766-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7766-123">Matrice che contiene gli ID VLAN a cui l'opzione può accedere.</span><span class="sxs-lookup"><span data-stu-id="f7766-123">An array that contains the VLAN IDs that the switch can access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7766-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7766-124">Requirements</span></span>



| <span data-ttu-id="f7766-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7766-125">Requirement</span></span> | <span data-ttu-id="f7766-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f7766-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7766-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7766-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f7766-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f7766-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f7766-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7766-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f7766-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7766-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f7766-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f7766-131">Namespace</span></span><br/>                | <span data-ttu-id="f7766-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f7766-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f7766-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f7766-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7766-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7766-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7766-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f7766-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7766-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7766-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f7766-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7766-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7766-138">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="f7766-138">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




