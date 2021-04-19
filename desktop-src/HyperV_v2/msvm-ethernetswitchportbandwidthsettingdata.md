---
description: Rappresenta le impostazioni della larghezza di banda della porta.
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Classe Msvm_EthernetSwitchPortBandwidthSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 932207a8157e34c5f42894c31efa78090a6a80f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317187"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a><span data-ttu-id="a2eba-103">\_Classe MSVM EthernetSwitchPortBandwidthSettingData</span><span class="sxs-lookup"><span data-stu-id="a2eba-103">Msvm\_EthernetSwitchPortBandwidthSettingData class</span></span>

<span data-ttu-id="a2eba-104">Rappresenta le impostazioni della larghezza di banda della porta.</span><span class="sxs-lookup"><span data-stu-id="a2eba-104">Represents the port bandwidth settings.</span></span>

<span data-ttu-id="a2eba-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a2eba-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2eba-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2eba-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a><span data-ttu-id="a2eba-107">Members</span><span class="sxs-lookup"><span data-stu-id="a2eba-107">Members</span></span>

<span data-ttu-id="a2eba-108">La **classe \_ EthernetSwitchPortBandwidthSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a2eba-108">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a2eba-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a2eba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2eba-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a2eba-110">Properties</span></span>

<span data-ttu-id="a2eba-111">La **classe \_ EthernetSwitchPortBandwidthSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a2eba-111">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2eba-112">**BurstLimit**</span><span class="sxs-lookup"><span data-stu-id="a2eba-112">**BurstLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2eba-113">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2eba-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a2eba-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-115">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="a2eba-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a2eba-116">Larghezza di banda massima consentita dalla porta durante i picchi.</span><span class="sxs-lookup"><span data-stu-id="a2eba-116">The peak bandwidth allowed from the port during bursts.</span></span>

</dd> <dt>

<span data-ttu-id="a2eba-117">**BurstSize**</span><span class="sxs-lookup"><span data-stu-id="a2eba-117">**BurstSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2eba-118">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2eba-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a2eba-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-120">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="a2eba-120">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a2eba-121">Dimensioni massime di espansione consentite.</span><span class="sxs-lookup"><span data-stu-id="a2eba-121">The maximum burst size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="a2eba-122">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a2eba-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2eba-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a2eba-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a2eba-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2eba-125">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a2eba-125">A short description of the object.</span></span> <span data-ttu-id="a2eba-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Bandwidth Settings".</span><span class="sxs-lookup"><span data-stu-id="a2eba-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a2eba-127">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a2eba-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2eba-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a2eba-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a2eba-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2eba-130">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="a2eba-130">A description of the object.</span></span> <span data-ttu-id="a2eba-131">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "rappresenta le impostazioni della larghezza di banda della porta".</span><span class="sxs-lookup"><span data-stu-id="a2eba-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="a2eba-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a2eba-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2eba-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a2eba-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a2eba-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2eba-135">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a2eba-135">A display name for the object.</span></span> <span data-ttu-id="a2eba-136">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port Bandwidth Settings".</span><span class="sxs-lookup"><span data-stu-id="a2eba-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a2eba-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a2eba-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2eba-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a2eba-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a2eba-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-140">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="a2eba-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a2eba-141">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="a2eba-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a2eba-142">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a2eba-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a2eba-143">**Limite**</span><span class="sxs-lookup"><span data-stu-id="a2eba-143">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2eba-144">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2eba-144">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a2eba-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-146">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="a2eba-146">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a2eba-147">Limite della larghezza di banda consentito per la porta.</span><span class="sxs-lookup"><span data-stu-id="a2eba-147">The bandwidth limit allowed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="a2eba-148">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="a2eba-148">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2eba-149">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2eba-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a2eba-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-151">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="a2eba-151">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a2eba-152">Larghezza di banda minima assoluta garantita per la porta.</span><span class="sxs-lookup"><span data-stu-id="a2eba-152">The minimum absolute bandwidth guaranteed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="a2eba-153">**Weight**</span><span class="sxs-lookup"><span data-stu-id="a2eba-153">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2eba-154">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2eba-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a2eba-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a2eba-156">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="a2eba-156">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a2eba-157">Larghezza di banda minima garantita per la porta.</span><span class="sxs-lookup"><span data-stu-id="a2eba-157">The minimum bandwidth in weight guaranteed for the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2eba-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2eba-158">Requirements</span></span>



| <span data-ttu-id="a2eba-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2eba-159">Requirement</span></span> | <span data-ttu-id="a2eba-160">Valore</span><span class="sxs-lookup"><span data-stu-id="a2eba-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2eba-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2eba-161">Minimum supported client</span></span><br/> | <span data-ttu-id="a2eba-162">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a2eba-162">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a2eba-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2eba-163">Minimum supported server</span></span><br/> | <span data-ttu-id="a2eba-164">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a2eba-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2eba-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a2eba-165">Namespace</span></span><br/>                | <span data-ttu-id="a2eba-166">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a2eba-166">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a2eba-167">MOF</span><span class="sxs-lookup"><span data-stu-id="a2eba-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2eba-168"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2eba-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2eba-169">DLL</span><span class="sxs-lookup"><span data-stu-id="a2eba-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2eba-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2eba-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

