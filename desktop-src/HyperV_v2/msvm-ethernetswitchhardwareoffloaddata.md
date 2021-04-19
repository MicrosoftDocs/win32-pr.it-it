---
description: Rappresenta lo stato dell'offload hardware del Commuter.
ms.assetid: 77a34df7-e3c4-4d91-af5a-91a03dd8246d
title: Classe Msvm_EthernetSwitchHardwareOffloadData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadData
- Msvm_EthernetSwitchHardwareOffloadData.InstanceID
- Msvm_EthernetSwitchHardwareOffloadData.Caption
- Msvm_EthernetSwitchHardwareOffloadData.Description
- Msvm_EthernetSwitchHardwareOffloadData.ElementName
- Msvm_EthernetSwitchHardwareOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.SystemName
- Msvm_EthernetSwitchHardwareOffloadData.CreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.Name
- Msvm_EthernetSwitchHardwareOffloadData.IovVfCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovVfUsage
- Msvm_EthernetSwitchHardwareOffloadData.VmqCapacity
- Msvm_EthernetSwitchHardwareOffloadData.VmqUsage
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSACapacity
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSAUsage
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchHardwareOffloadData.PacketDirectInUse
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssMinQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b64762b824cea7d3b064636e7f7f87777e053daf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320033"
---
# <a name="msvm_ethernetswitchhardwareoffloaddata-class"></a><span data-ttu-id="e01a6-103">\_Classe MSVM EthernetSwitchHardwareOffloadData</span><span class="sxs-lookup"><span data-stu-id="e01a6-103">Msvm\_EthernetSwitchHardwareOffloadData class</span></span>

<span data-ttu-id="e01a6-104">Rappresenta lo stato dell'offload hardware del Commuter.</span><span class="sxs-lookup"><span data-stu-id="e01a6-104">Represents the switch hardware offload status.</span></span>

<span data-ttu-id="e01a6-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e01a6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e01a6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e01a6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1C37E01C-0CD6-496F-9076-90C131033DC2"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Offload Resource Status"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadData : Msvm_EthernetSwitchData
{
  string  InstanceID;
  string  Caption = Ethernet Switch Offload Resource Status;
  string  Description = Represents the switch hardware offload status.;
  string  ElementName = Ethernet Switch Offload Resource Status;
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  CreationClassName = "Msvm_EthernetSwitchHardwareOffloadData";
  string  Name;
  uint32  IovVfCapacity = 0;
  uint32  IovVfUsage = 0;
  uint32  VmqCapacity = 0;
  uint32  VmqUsage = 0;
  uint32  IPsecSACapacity = 0;
  uint32  IPsecSAUsage = 0;
  uint32  IovQueuePairCapacity = 0;
  uint32  IovQueuePairUsage = 0;
  boolean PacketDirectInUse = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 0;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 0;
  uint32  DefaultQueueVrssMinQueuePairs = 0;
  boolean DefaultQueueVmmqEnabled = FALSE;
  boolean DefaultQueueVrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="e01a6-107">Members</span><span class="sxs-lookup"><span data-stu-id="e01a6-107">Members</span></span>

<span data-ttu-id="e01a6-108">La **classe \_ EthernetSwitchHardwareOffloadData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e01a6-108">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="e01a6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e01a6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e01a6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e01a6-110">Properties</span></span>

<span data-ttu-id="e01a6-111">La **classe \_ EthernetSwitchHardwareOffloadData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e01a6-111">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e01a6-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e01a6-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e01a6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e01a6-115">A short description of the object.</span></span> <span data-ttu-id="e01a6-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e01a6-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e01a6-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e01a6-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-120">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e01a6-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-121">Nome della classe o della sottoclasse utilizzata per la creazione di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="e01a6-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="e01a6-122">Questa proprietà viene ereditata da [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="e01a6-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-123">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="e01a6-123">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-124">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e01a6-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-126">Qualificatori: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-126">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-127">Impostazione corrente di VMMQ per la coda predefinita</span><span class="sxs-lookup"><span data-stu-id="e01a6-127">The current VMMQ setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="e01a6-128">Proprietà aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="e01a6-128">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="e01a6-129">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="e01a6-129">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-132">Qualificatori: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-132">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-133">Numero corrente di code allocate per la coda predefinita</span><span class="sxs-lookup"><span data-stu-id="e01a6-133">The current number of queues allocated for the default queue</span></span>

> [!Note]  
> <span data-ttu-id="e01a6-134">Proprietà aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="e01a6-134">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="e01a6-135">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="e01a6-135">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-136">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e01a6-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-138">Qualificatori: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-138">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-139">Impostazione corrente di VRss per la coda predefinita</span><span class="sxs-lookup"><span data-stu-id="e01a6-139">The current VRss setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="e01a6-140">Proprietà aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="e01a6-140">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="e01a6-141">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="e01a6-141">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e01a6-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-144">Qualificatori: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-144">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-145">Indica se la CPU VMQ primaria è esclusa dalla tabella di riferimento indiretto VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="e01a6-145">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="e01a6-146">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="e01a6-146">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e01a6-147">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="e01a6-147">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e01a6-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-150">Qualificatori: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-150">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-151">Indica se eseguire sempre la distribuzione VRSS per la coda predefinita, indipendentemente dallo stato RSS del vPort esterno.</span><span class="sxs-lookup"><span data-stu-id="e01a6-151">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="e01a6-152">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="e01a6-152">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e01a6-153">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="e01a6-153">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-154">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-156">Qualificatori: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-156">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-157">Indica il numero minimo di code utilizzate per VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="e01a6-157">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="e01a6-158">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="e01a6-158">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e01a6-159">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="e01a6-159">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-162">Qualificatori: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-162">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-163">Indica il modo in cui le code VRSS/VMMQ vengono indirizzate a processori host diversi.</span><span class="sxs-lookup"><span data-stu-id="e01a6-163">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="e01a6-164">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="e01a6-164">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e01a6-165">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e01a6-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e01a6-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-168">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="e01a6-168">A description of the object.</span></span> <span data-ttu-id="e01a6-169">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e01a6-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-170">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e01a6-170">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e01a6-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-173">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e01a6-173">A display name for the object.</span></span> <span data-ttu-id="e01a6-174">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e01a6-174">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-175">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e01a6-175">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e01a6-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-178">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="e01a6-178">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-179">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e01a6-179">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e01a6-180">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e01a6-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-181">**IovQueuePairCapacity**</span><span class="sxs-lookup"><span data-stu-id="e01a6-181">**IovQueuePairCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-182">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-184">Qualificatori: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-184">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-185">Numero massimo di coppie di code supportate dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="e01a6-185">The maximum number of queue pairs supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-186">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="e01a6-186">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-187">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-189">Qualificatori: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-189">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-190">Numero corrente di coppie di code utilizzate dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="e01a6-190">The current number of queue pairs being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-191">**IovVfCapacity**</span><span class="sxs-lookup"><span data-stu-id="e01a6-191">**IovVfCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-192">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-194">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-194">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-195">Numero massimo di funzioni virtuali supportate dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="e01a6-195">The maximum number of virtual functions supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-196">**IovVfUsage**</span><span class="sxs-lookup"><span data-stu-id="e01a6-196">**IovVfUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-197">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-199">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-200">Numero corrente di funzioni virtuali utilizzate dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="e01a6-200">The current number of virtual functions being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-201">**IPsecSACapacity**</span><span class="sxs-lookup"><span data-stu-id="e01a6-201">**IPsecSACapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-202">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-204">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-204">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-205">Numero massimo di offload dell'associazione di sicurezza IPsec supportati dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="e01a6-205">The maximum number of IPsec security association offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-206">**IPsecSAUsage**</span><span class="sxs-lookup"><span data-stu-id="e01a6-206">**IPsecSAUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-207">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-209">Qualificatori: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-209">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-210">Numero corrente di offload dell'associazione di sicurezza IPsec utilizzati dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="e01a6-210">The current number of IPsec security association offloads being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-211">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e01a6-211">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-212">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e01a6-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-214">Qualificatori: **chiave**, **override**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e01a6-214">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-215">Nome univoco della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e01a6-215">The unique name of the resource.</span></span> <span data-ttu-id="e01a6-216">Questa proprietà viene ereditata da [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="e01a6-216">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-217">**PacketDirectInUse**</span><span class="sxs-lookup"><span data-stu-id="e01a6-217">**PacketDirectInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-218">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e01a6-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-220">Qualificatori: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-220">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-221">Indica se il pacchetto è usato direttamente dall'opzione</span><span class="sxs-lookup"><span data-stu-id="e01a6-221">Indicates if packet direct is being used by the switch</span></span>

> [!Note]  
> <span data-ttu-id="e01a6-222">Proprietà aggiunta in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e01a6-222">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="e01a6-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e01a6-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e01a6-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-226">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e01a6-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-227">Nome della classe di creazione del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="e01a6-227">The hosting system's creation class name.</span></span> <span data-ttu-id="e01a6-228">Questa proprietà viene ereditata da [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="e01a6-228">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e01a6-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e01a6-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-232">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e01a6-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-233">Nome del commutire virtuale a cui è associata l'istanza della risorsa associata.</span><span class="sxs-lookup"><span data-stu-id="e01a6-233">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="e01a6-234">Questa proprietà viene ereditata da [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="e01a6-234">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-235">**VmqCapacity**</span><span class="sxs-lookup"><span data-stu-id="e01a6-235">**VmqCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-236">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-238">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-238">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-239">Numero massimo di offload della coda della macchina virtuale supportati dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="e01a6-239">The maximum number of virtual machine queue offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="e01a6-240">**VmqUsage**</span><span class="sxs-lookup"><span data-stu-id="e01a6-240">**VmqUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01a6-241">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e01a6-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e01a6-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01a6-243">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e01a6-243">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e01a6-244">Numero corrente di offload della coda della macchina virtuale utilizzati dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="e01a6-244">The current number of virtual machine queue offloads being used by the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e01a6-245">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e01a6-245">Requirements</span></span>



| <span data-ttu-id="e01a6-246">Requisito</span><span class="sxs-lookup"><span data-stu-id="e01a6-246">Requirement</span></span> | <span data-ttu-id="e01a6-247">Valore</span><span class="sxs-lookup"><span data-stu-id="e01a6-247">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e01a6-248">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e01a6-248">Minimum supported client</span></span><br/> | <span data-ttu-id="e01a6-249">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e01a6-249">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e01a6-250">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e01a6-250">Minimum supported server</span></span><br/> | <span data-ttu-id="e01a6-251">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e01a6-251">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e01a6-252">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e01a6-252">Namespace</span></span><br/>                | <span data-ttu-id="e01a6-253">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e01a6-253">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e01a6-254">MOF</span><span class="sxs-lookup"><span data-stu-id="e01a6-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e01a6-255"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e01a6-255"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e01a6-256">DLL</span><span class="sxs-lookup"><span data-stu-id="e01a6-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e01a6-257"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e01a6-257"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

