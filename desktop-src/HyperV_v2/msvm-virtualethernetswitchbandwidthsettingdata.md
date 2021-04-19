---
description: Rappresenta le impostazioni della larghezza di banda per un commutire virtuale.
ms.assetid: bc6f8cd3-f74a-4f4a-9ffe-a88def3966d9
title: Classe Msvm_VirtualEthernetSwitchBandwidthSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchBandwidthSettingData
- Msvm_VirtualEthernetSwitchBandwidthSettingData.InstanceID
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Caption
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Description
- Msvm_VirtualEthernetSwitchBandwidthSettingData.ElementName
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowReservation
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec94409366761ee208d3e8a6af59a4d07527d82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314323"
---
# <a name="msvm_virtualethernetswitchbandwidthsettingdata-class"></a><span data-ttu-id="450c7-103">\_Classe MSVM VirtualEthernetSwitchBandwidthSettingData</span><span class="sxs-lookup"><span data-stu-id="450c7-103">Msvm\_VirtualEthernetSwitchBandwidthSettingData class</span></span>

<span data-ttu-id="450c7-104">Rappresenta le impostazioni della larghezza di banda per un commutire virtuale.</span><span class="sxs-lookup"><span data-stu-id="450c7-104">Represents the bandwidth settings for a virtual switch.</span></span>

<span data-ttu-id="450c7-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="450c7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="450c7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="450c7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("3EB2B8E8-4ABF-4DBF-9071-16DD47481FBE"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchBandwidthSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  string InstanceID = "Microsoft:Definition\GUID\Default";
  string Caption = "Ethernet Switch Bandwidth Settings";
  string Description = "Represents the switch bandwidth settings.";
  string ElementName = "Ethernet Switch Bandwidth Settings";
  UINT64 DefaultFlowReservation = 0;
  UINT64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="450c7-107">Members</span><span class="sxs-lookup"><span data-stu-id="450c7-107">Members</span></span>

<span data-ttu-id="450c7-108">La **classe \_ VirtualEthernetSwitchBandwidthSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="450c7-108">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="450c7-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="450c7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="450c7-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="450c7-110">Properties</span></span>

<span data-ttu-id="450c7-111">La **classe \_ VirtualEthernetSwitchBandwidthSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="450c7-111">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="450c7-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="450c7-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="450c7-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="450c7-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="450c7-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="450c7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="450c7-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="450c7-115">A short description of the object.</span></span> <span data-ttu-id="450c7-116">Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ed è sempre impostata su "Ethernet Switch Bandwidth Settings".</span><span class="sxs-lookup"><span data-stu-id="450c7-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="450c7-117">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="450c7-117">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="450c7-118">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="450c7-118">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="450c7-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="450c7-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="450c7-120">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="450c7-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="450c7-121">Specifica la prenotazione di larghezza di banda assoluta per i flussi non classificati nell'adapter sottostante.</span><span class="sxs-lookup"><span data-stu-id="450c7-121">Specifies the absolute bandwidth reservation for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="450c7-122">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="450c7-122">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="450c7-123">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="450c7-123">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="450c7-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="450c7-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="450c7-125">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="450c7-125">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="450c7-126">Specifica la prenotazione di larghezza di banda in peso per i flussi non classificati nell'adapter sottostante.</span><span class="sxs-lookup"><span data-stu-id="450c7-126">Specifies the bandwidth reservation in weight for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="450c7-127">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="450c7-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="450c7-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="450c7-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="450c7-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="450c7-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="450c7-130">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="450c7-130">A description of the object.</span></span> <span data-ttu-id="450c7-131">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "rappresenta le impostazioni della larghezza di banda del Commuter".</span><span class="sxs-lookup"><span data-stu-id="450c7-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the switch bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="450c7-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="450c7-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="450c7-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="450c7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="450c7-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="450c7-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="450c7-135">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="450c7-135">A display name for the object.</span></span> <span data-ttu-id="450c7-136">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su "Ethernet Switch Bandwidth Settings".</span><span class="sxs-lookup"><span data-stu-id="450c7-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="450c7-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="450c7-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="450c7-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="450c7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="450c7-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="450c7-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="450c7-140">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="450c7-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="450c7-141">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="450c7-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="450c7-142">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ed è sempre impostata su "Microsoft: Definition \\ *GUID* \\ default".</span><span class="sxs-lookup"><span data-stu-id="450c7-142">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:Definition\\*GUID*\\Default".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="450c7-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="450c7-143">Requirements</span></span>



| <span data-ttu-id="450c7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="450c7-144">Requirement</span></span> | <span data-ttu-id="450c7-145">Valore</span><span class="sxs-lookup"><span data-stu-id="450c7-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="450c7-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="450c7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="450c7-147">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="450c7-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="450c7-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="450c7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="450c7-149">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="450c7-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="450c7-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="450c7-150">Namespace</span></span><br/>                | <span data-ttu-id="450c7-151">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="450c7-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="450c7-152">MOF</span><span class="sxs-lookup"><span data-stu-id="450c7-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="450c7-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="450c7-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="450c7-154">DLL</span><span class="sxs-lookup"><span data-stu-id="450c7-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="450c7-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="450c7-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

