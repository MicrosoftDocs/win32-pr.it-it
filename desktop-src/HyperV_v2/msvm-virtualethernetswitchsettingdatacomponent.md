---
description: Associazione utilizzata per stabilire &\# 0034; parte di&\# 0034; relazioni tra un'istanza di MSVM \_ VirtualEthernetSwitchSettingData e una o più istanze di MSVM \_ EthernetSwitchFeatureSettingData.
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Classe Msvm_VirtualEthernetSwitchSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8fa53514c5db3128e13f0504bb883cb802021c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226862"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a><span data-ttu-id="a65ce-103">\_Classe MSVM VirtualEthernetSwitchSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="a65ce-103">Msvm\_VirtualEthernetSwitchSettingDataComponent class</span></span>

<span data-ttu-id="a65ce-104">Associazione utilizzata per stabilire relazioni "parte di" tra un'istanza di [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) e una o più istanze di [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="a65ce-104">An association used to establish "part of" relationships between one instance of [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) and one or more instances of [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="a65ce-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a65ce-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65ce-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a65ce-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a65ce-107">Members</span><span class="sxs-lookup"><span data-stu-id="a65ce-107">Members</span></span>

<span data-ttu-id="a65ce-108">La **classe \_ VirtualEthernetSwitchSettingDataComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a65ce-108">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a65ce-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a65ce-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a65ce-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a65ce-110">Properties</span></span>

<span data-ttu-id="a65ce-111">La **classe \_ VirtualEthernetSwitchSettingDataComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a65ce-111">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a65ce-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a65ce-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a65ce-113">Tipo di dati: **MSVM \_ VirtualEthernetSwitchSettingData**</span><span class="sxs-lookup"><span data-stu-id="a65ce-113">Data type: **Msvm\_VirtualEthernetSwitchSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="a65ce-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a65ce-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a65ce-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a65ce-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a65ce-116">Riferimento a un'istanza della classe [**\_ VirtualEthernetSwitchSettingData MSVM**](msvm-virtualethernetswitchsettingdata.md) che rappresenta una porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a65ce-116">Reference to an instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="a65ce-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a65ce-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a65ce-118">Tipo di dati: **MSVM \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="a65ce-118">Data type: **Msvm\_EthernetSwitchFeatureSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="a65ce-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a65ce-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a65ce-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="a65ce-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a65ce-121">Riferimento a un'istanza della classe [**\_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md) che rappresenta le impostazioni applicate all'opzione.</span><span class="sxs-lookup"><span data-stu-id="a65ce-121">Reference to an instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that represents the settings applied to the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a65ce-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a65ce-122">Requirements</span></span>



| <span data-ttu-id="a65ce-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65ce-123">Requirement</span></span> | <span data-ttu-id="a65ce-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a65ce-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65ce-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a65ce-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a65ce-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a65ce-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a65ce-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a65ce-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a65ce-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a65ce-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a65ce-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a65ce-129">Namespace</span></span><br/>                | <span data-ttu-id="a65ce-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a65ce-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a65ce-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a65ce-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a65ce-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a65ce-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a65ce-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a65ce-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a65ce-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a65ce-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

