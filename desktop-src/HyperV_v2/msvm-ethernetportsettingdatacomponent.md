---
description: Associazione utilizzata per stabilire &\# 0034; parte di&\# 0034; relazioni tra un'istanza di un EthernetPortAllocationSettingData MSVM \_ e una o più istanze di un EthernetSwitchFeatureSettingData MSVM \_ .
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Classe Msvm_EthernetPortSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c00c056bd5095d945af12fde3556d92b9a2d7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312912"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a><span data-ttu-id="a0aac-103">\_Classe MSVM EthernetPortSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="a0aac-103">Msvm\_EthernetPortSettingDataComponent class</span></span>

<span data-ttu-id="a0aac-104">Associazione utilizzata per stabilire relazioni "parte di" tra un'istanza di un [**\_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) e una o più istanze di un [**\_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="a0aac-104">An association used to establish "part of" relationships between one instance of an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="a0aac-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a0aac-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0aac-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0aac-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a0aac-107">Members</span><span class="sxs-lookup"><span data-stu-id="a0aac-107">Members</span></span>

<span data-ttu-id="a0aac-108">La **classe \_ EthernetPortSettingDataComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a0aac-108">The **Msvm\_EthernetPortSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a0aac-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0aac-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0aac-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0aac-110">Properties</span></span>

<span data-ttu-id="a0aac-111">La **classe \_ EthernetPortSettingDataComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a0aac-111">The **Msvm\_EthernetPortSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0aac-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a0aac-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0aac-113">Tipo di dati: **[ **MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="a0aac-113">Data type: **[**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a0aac-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0aac-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0aac-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0aac-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0aac-116">Riferimento a un'istanza della classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) che rappresenta la porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a0aac-116">A reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="a0aac-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a0aac-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0aac-118">Tipo di dati: **[ **MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="a0aac-118">Data type: **[**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a0aac-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0aac-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0aac-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="a0aac-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="a0aac-121">Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) che rappresenta le impostazioni della funzionalità applicate alla porta.</span><span class="sxs-lookup"><span data-stu-id="a0aac-121">A reference to an instance of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the feature settings applied to the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0aac-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0aac-122">Requirements</span></span>



| <span data-ttu-id="a0aac-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0aac-123">Requirement</span></span> | <span data-ttu-id="a0aac-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a0aac-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0aac-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0aac-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a0aac-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a0aac-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a0aac-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0aac-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a0aac-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a0aac-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0aac-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0aac-129">Namespace</span></span><br/>                | <span data-ttu-id="a0aac-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a0aac-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a0aac-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a0aac-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0aac-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0aac-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0aac-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a0aac-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0aac-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0aac-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

