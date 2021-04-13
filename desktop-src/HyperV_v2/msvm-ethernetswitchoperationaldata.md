---
description: Rappresenta parametri operativi switch.
ms.assetid: f225d321-8f40-4e6c-b30d-8fab3f84761d
title: Classe Msvm_EthernetSwitchOperationalData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchOperationalData
- Msvm_EthernetSwitchOperationalData.InstanceID
- Msvm_EthernetSwitchOperationalData.Caption
- Msvm_EthernetSwitchOperationalData.Description
- Msvm_EthernetSwitchOperationalData.ElementName
- Msvm_EthernetSwitchOperationalData.SystemCreationClassName
- Msvm_EthernetSwitchOperationalData.SystemName
- Msvm_EthernetSwitchOperationalData.CreationClassName
- Msvm_EthernetSwitchOperationalData.Name
- Msvm_EthernetSwitchOperationalData.CurrentSwitchingMode
- Msvm_EthernetSwitchOperationalData.SupportedSwitchingModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d9aacd8380650ddaf2790aeacf4a2327b54f973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350661"
---
# <a name="msvm_ethernetswitchoperationaldata-class"></a><span data-ttu-id="4628a-103">\_Classe MSVM EthernetSwitchOperationalData</span><span class="sxs-lookup"><span data-stu-id="4628a-103">Msvm\_EthernetSwitchOperationalData class</span></span>

<span data-ttu-id="4628a-104">Rappresenta parametri operativi switch.</span><span class="sxs-lookup"><span data-stu-id="4628a-104">Represents switch operational parameters.</span></span>

<span data-ttu-id="4628a-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4628a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4628a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4628a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1D18CDCF-209E-4172-875D-6D208A0A8375"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Modes Supported "), AMENDMENT]
class Msvm_EthernetSwitchOperationalData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Modes Supported";
  string Description = "Represents switch operational parameters.";
  string ElementName = "Ethernet Switch Modes Supported";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchOperationalData";
  string Name;
  uint32 CurrentSwitchingMode = 1;
  uint32 SupportedSwitchingModes[] = {1};
};
```

## <a name="members"></a><span data-ttu-id="4628a-107">Members</span><span class="sxs-lookup"><span data-stu-id="4628a-107">Members</span></span>

<span data-ttu-id="4628a-108">La **classe \_ EthernetSwitchOperationalData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4628a-108">The **Msvm\_EthernetSwitchOperationalData** class has these types of members:</span></span>

-   [<span data-ttu-id="4628a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4628a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4628a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4628a-110">Properties</span></span>

<span data-ttu-id="4628a-111">La **classe \_ EthernetSwitchOperationalData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4628a-111">The **Msvm\_EthernetSwitchOperationalData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4628a-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="4628a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4628a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4628a-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4628a-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4628a-115">A short description of the object.</span></span> <span data-ttu-id="4628a-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4628a-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4628a-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4628a-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4628a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4628a-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4628a-120">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="4628a-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4628a-121">Nome della classe o della sottoclasse utilizzata per la creazione di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="4628a-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="4628a-122">Questa proprietà viene ereditata da [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="4628a-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="4628a-123">**CurrentSwitchingMode**</span><span class="sxs-lookup"><span data-stu-id="4628a-123">**CurrentSwitchingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4628a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4628a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4628a-126">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4628a-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4628a-127">Modalità di commutazione corrente sull'opzione.</span><span class="sxs-lookup"><span data-stu-id="4628a-127">The current switching mode on the switch.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4628a-128">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4628a-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>

<span data-ttu-id="4628a-129">**802.1 q** (1)</span><span class="sxs-lookup"><span data-stu-id="4628a-129">**802.1Q** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbg"></span><span id="802.1qbg"></span><span id="802.1QBG"></span>

<span data-ttu-id="4628a-130">**802.1 Qbg** (2)</span><span class="sxs-lookup"><span data-stu-id="4628a-130">**802.1Qbg** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbh"></span><span id="802.1qbh"></span><span id="802.1QBH"></span>

<span data-ttu-id="4628a-131">**802.1 QBH** (3)</span><span class="sxs-lookup"><span data-stu-id="4628a-131">**802.1Qbh** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4628a-132">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4628a-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4628a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4628a-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4628a-135">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="4628a-135">A description of the object.</span></span> <span data-ttu-id="4628a-136">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4628a-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4628a-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4628a-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4628a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4628a-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4628a-140">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4628a-140">A display name for the object.</span></span> <span data-ttu-id="4628a-141">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4628a-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4628a-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4628a-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4628a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4628a-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4628a-145">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="4628a-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4628a-146">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="4628a-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4628a-147">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4628a-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4628a-148">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4628a-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4628a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4628a-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4628a-151">Qualificatori: **chiave**, **override**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="4628a-151">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4628a-152">Nome univoco della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4628a-152">The unique name of the resource.</span></span> <span data-ttu-id="4628a-153">Questa proprietà viene ereditata da [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="4628a-153">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="4628a-154">**SupportedSwitchingModes**</span><span class="sxs-lookup"><span data-stu-id="4628a-154">**SupportedSwitchingModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-155">Tipo di dati: matrice **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4628a-155">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="4628a-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4628a-157">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4628a-157">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4628a-158">Modalità di commutazione supportate dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="4628a-158">The switching modes supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="4628a-159">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4628a-159">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4628a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4628a-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4628a-162">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="4628a-162">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4628a-163">Nome della classe di creazione del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="4628a-163">The hosting system's creation class name.</span></span> <span data-ttu-id="4628a-164">Questa proprietà viene ereditata da [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="4628a-164">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="4628a-165">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4628a-165">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4628a-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4628a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4628a-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4628a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4628a-168">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="4628a-168">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4628a-169">Nome del commutire virtuale a cui è associata l'istanza della risorsa associata.</span><span class="sxs-lookup"><span data-stu-id="4628a-169">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="4628a-170">Questa proprietà viene ereditata da [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="4628a-170">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4628a-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4628a-171">Requirements</span></span>



| <span data-ttu-id="4628a-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="4628a-172">Requirement</span></span> | <span data-ttu-id="4628a-173">Valore</span><span class="sxs-lookup"><span data-stu-id="4628a-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4628a-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4628a-174">Minimum supported client</span></span><br/> | <span data-ttu-id="4628a-175">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4628a-175">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4628a-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4628a-176">Minimum supported server</span></span><br/> | <span data-ttu-id="4628a-177">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4628a-177">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4628a-178">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4628a-178">Namespace</span></span><br/>                | <span data-ttu-id="4628a-179">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4628a-179">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4628a-180">MOF</span><span class="sxs-lookup"><span data-stu-id="4628a-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4628a-181"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4628a-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4628a-182">DLL</span><span class="sxs-lookup"><span data-stu-id="4628a-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4628a-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4628a-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

