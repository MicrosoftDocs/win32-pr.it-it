---
description: Associazione utilizzata per stabilire relazioni tra un'istanza di un EmulatedEthernetPortSettingData di MSVM \_ e una o più istanze di un \_ EthernetSwitchFeatureSettingData MSVM.
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Classe Msvm_EthernetPortFailoverSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 50fff8688beea91495014dd75b1f1c33020869f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529257"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a><span data-ttu-id="a52a5-103">\_Classe MSVM EthernetPortFailoverSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="a52a5-103">Msvm\_EthernetPortFailoverSettingDataComponent class</span></span>

<span data-ttu-id="a52a5-104">Associazione utilizzata per stabilire relazioni tra un'istanza di un [**\_ EmulatedEthernetPortSettingData di MSVM**](msvm-emulatedethernetportsettingdata.md) e una o più istanze di un [**\_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="a52a5-104">An association used to establish relationships between one instance of an [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="a52a5-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a52a5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a52a5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a52a5-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a52a5-107">Members</span><span class="sxs-lookup"><span data-stu-id="a52a5-107">Members</span></span>

<span data-ttu-id="a52a5-108">La **classe \_ EthernetPortFailoverSettingDataComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a52a5-108">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a52a5-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a52a5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a52a5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a52a5-110">Properties</span></span>

<span data-ttu-id="a52a5-111">La **classe \_ EthernetPortFailoverSettingDataComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a52a5-111">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a52a5-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a52a5-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a52a5-113">Tipo di dati: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="a52a5-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="a52a5-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a52a5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a52a5-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a52a5-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a52a5-116">Riferimento a un'istanza della classe [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) che rappresenta la porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a52a5-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="a52a5-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a52a5-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a52a5-118">Tipo di dati: **[ **MSVM \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="a52a5-118">Data type: **[**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a52a5-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a52a5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a52a5-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="a52a5-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a52a5-121">Riferimento a un'istanza della classe [**MSVM \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) che rappresenta la configurazione della scheda di rete Guest.</span><span class="sxs-lookup"><span data-stu-id="a52a5-121">A reference to an instance of the [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) class that represents the guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a52a5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a52a5-122">Requirements</span></span>



| <span data-ttu-id="a52a5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a52a5-123">Requirement</span></span> | <span data-ttu-id="a52a5-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a52a5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a52a5-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a52a5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a52a5-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a52a5-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a52a5-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a52a5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a52a5-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a52a5-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a52a5-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a52a5-129">Namespace</span></span><br/>                | <span data-ttu-id="a52a5-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a52a5-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a52a5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a52a5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a52a5-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a52a5-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a52a5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a52a5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a52a5-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a52a5-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

