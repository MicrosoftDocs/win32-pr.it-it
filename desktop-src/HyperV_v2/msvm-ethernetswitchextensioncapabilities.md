---
description: Rappresenta l'associazione tra le estensioni Ethernet e le rispettive funzionalità.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Classe Msvm_EthernetSwitchExtensionCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 950a8a0288487bf557e9dd201100b2a894417641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760856"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a><span data-ttu-id="6f89c-103">\_Classe MSVM EthernetSwitchExtensionCapabilities</span><span class="sxs-lookup"><span data-stu-id="6f89c-103">Msvm\_EthernetSwitchExtensionCapabilities class</span></span>

<span data-ttu-id="6f89c-104">Rappresenta l'associazione tra le estensioni Ethernet e le rispettive funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6f89c-104">Represents the association between Ethernet extensions and their capabilities.</span></span>

<span data-ttu-id="6f89c-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6f89c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f89c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f89c-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="6f89c-107">Members</span><span class="sxs-lookup"><span data-stu-id="6f89c-107">Members</span></span>

<span data-ttu-id="6f89c-108">La **classe \_ EthernetSwitchExtensionCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6f89c-108">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="6f89c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f89c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f89c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f89c-110">Properties</span></span>

<span data-ttu-id="6f89c-111">La **classe \_ EthernetSwitchExtensionCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6f89c-111">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f89c-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="6f89c-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f89c-113">Tipo di dati: **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="6f89c-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6f89c-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f89c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f89c-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("funzionalità")</span><span class="sxs-lookup"><span data-stu-id="6f89c-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="6f89c-116">Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) che rappresenta l'oggetto funzionalità associato all'opzione.</span><span class="sxs-lookup"><span data-stu-id="6f89c-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the capabilities object associated with the switch.</span></span> <span data-ttu-id="6f89c-117">Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="6f89c-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="6f89c-118">**Caratteristiche**</span><span class="sxs-lookup"><span data-stu-id="6f89c-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f89c-119">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f89c-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f89c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f89c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f89c-121">Fornisce informazioni descrittive sulle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6f89c-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="6f89c-122">Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="6f89c-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="6f89c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6f89c-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="6f89c-124">Significato</span><span class="sxs-lookup"><span data-stu-id="6f89c-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="6f89c-125"><dt>**Impostazione predefinita**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6f89c-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="6f89c-126">Le funzionalità associate rappresentano le funzionalità predefinite dell'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="6f89c-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="6f89c-127"><dt>**Corrente**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6f89c-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="6f89c-128">Le funzionalità associate rappresentano le funzionalità correnti dell'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="6f89c-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6f89c-129">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="6f89c-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f89c-130">Tipo di dati: **[ **MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="6f89c-130">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6f89c-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f89c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f89c-132">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Managed")</span><span class="sxs-lookup"><span data-stu-id="6f89c-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="6f89c-133">Riferimento a un'istanza della classe [**MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) che rappresenta l'estensione installata.</span><span class="sxs-lookup"><span data-stu-id="6f89c-133">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents the installed extension.</span></span> <span data-ttu-id="6f89c-134">Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="6f89c-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f89c-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f89c-135">Requirements</span></span>



| <span data-ttu-id="6f89c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f89c-136">Requirement</span></span> | <span data-ttu-id="6f89c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="6f89c-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f89c-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f89c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6f89c-139">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6f89c-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6f89c-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f89c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6f89c-141">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6f89c-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f89c-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6f89c-142">Namespace</span></span><br/>                | <span data-ttu-id="6f89c-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6f89c-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f89c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="6f89c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f89c-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f89c-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f89c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6f89c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f89c-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f89c-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

