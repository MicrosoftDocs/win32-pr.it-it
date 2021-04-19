---
description: Rappresenta i dati di stato della funzionalità di offload delle porte.
ms.assetid: 1117b9e4-cff7-4c9e-bf5e-74499297e84e
title: Classe Msvm_EthernetSwitchPortOffloadData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadData
- Msvm_EthernetSwitchPortOffloadData.InstanceID
- Msvm_EthernetSwitchPortOffloadData.Caption
- Msvm_EthernetSwitchPortOffloadData.Description
- Msvm_EthernetSwitchPortOffloadData.ElementName
- Msvm_EthernetSwitchPortOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchPortOffloadData.SystemName
- Msvm_EthernetSwitchPortOffloadData.DeviceCreationClassName
- Msvm_EthernetSwitchPortOffloadData.DeviceID
- Msvm_EthernetSwitchPortOffloadData.CreationClassName
- Msvm_EthernetSwitchPortOffloadData.Name
- Msvm_EthernetSwitchPortOffloadData.IpsecCurrentOffloadSaCount
- Msvm_EthernetSwitchPortOffloadData.IovOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQId
- Msvm_EthernetSwitchPortOffloadData.IovVfId
- Msvm_EthernetSwitchPortOffloadData.IovVfDataPathActive
- Msvm_EthernetSwitchPortOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchPortOffloadData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadData.VrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fd60e98c8df12b539bb51c60b34e7931b762dc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320025"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a><span data-ttu-id="42adf-103">\_Classe MSVM EthernetSwitchPortOffloadData</span><span class="sxs-lookup"><span data-stu-id="42adf-103">Msvm\_EthernetSwitchPortOffloadData class</span></span>

<span data-ttu-id="42adf-104">Rappresenta i dati di stato della funzionalità di offload delle porte.</span><span class="sxs-lookup"><span data-stu-id="42adf-104">Represents the port offload feature status data.</span></span>

<span data-ttu-id="42adf-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="42adf-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42adf-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42adf-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadData : Msvm_EthernetPortData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Feature Status";
  string  Description = "Represents the port offload feature status data.";
  string  ElementName = "Ethernet Switch Port Offload Feature Status";
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string  DeviceID;
  string  CreationClassName = "Msvm_EthernetSwitchPortOffloadData";
  string  Name;
  uint32  IpsecCurrentOffloadSaCount = 0;
  uint32  IovOffloadUsage = 0;
  uint32  VMQOffloadUsage = 0;
  uint32  VMQId = 0;
  uint16  IovVfId = 0;
  boolean IovVfDataPathActive = FALSE;
  uint32  IovQueuePairUsage = 0;
  uint32  VmmqQueuePairs = 0;
  uint32  VrssVmbusChannelAffinityPolicy = 0;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 0;
  uint32  VrssMinQueuePairs = 0;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="42adf-107">Members</span><span class="sxs-lookup"><span data-stu-id="42adf-107">Members</span></span>

<span data-ttu-id="42adf-108">La **classe \_ EthernetSwitchPortOffloadData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="42adf-108">The **Msvm\_EthernetSwitchPortOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="42adf-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="42adf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42adf-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="42adf-110">Properties</span></span>

<span data-ttu-id="42adf-111">La **classe \_ EthernetSwitchPortOffloadData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="42adf-111">The **Msvm\_EthernetSwitchPortOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42adf-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="42adf-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42adf-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42adf-115">A short description of the object.</span></span> <span data-ttu-id="42adf-116">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port offload feature status".</span><span class="sxs-lookup"><span data-stu-id="42adf-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="42adf-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="42adf-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-120">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="42adf-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="42adf-121">Nome della sottoclasse utilizzata per la creazione di questa istanza di dati di porta.</span><span class="sxs-lookup"><span data-stu-id="42adf-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="42adf-122">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)ed è sempre impostata su "MSVM \_ EthernetSwitchPortOffloadData".</span><span class="sxs-lookup"><span data-stu-id="42adf-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortOffloadData".</span></span>

</dd> <dt>

<span data-ttu-id="42adf-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="42adf-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42adf-126">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="42adf-126">A description of the object.</span></span> <span data-ttu-id="42adf-127">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "rappresenta i dati di stato della funzionalità di offload della porta".</span><span class="sxs-lookup"><span data-stu-id="42adf-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="42adf-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="42adf-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-131">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="42adf-131">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="42adf-132">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="42adf-132">The scoping system's creation class name.</span></span> <span data-ttu-id="42adf-133">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)ed è sempre impostata su "MSVM \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="42adf-133">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="42adf-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="42adf-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-137">Qualificatori: **Key**, **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="42adf-137">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="42adf-138">ID dispositivo della porta che ha come ambito questa istanza di dati di porta.</span><span class="sxs-lookup"><span data-stu-id="42adf-138">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="42adf-139">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="42adf-139">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="42adf-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="42adf-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42adf-143">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42adf-143">A display name for the object.</span></span> <span data-ttu-id="42adf-144">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port offload feature status".</span><span class="sxs-lookup"><span data-stu-id="42adf-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="42adf-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="42adf-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-148">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="42adf-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="42adf-149">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="42adf-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="42adf-150">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="42adf-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="42adf-151">**IovOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="42adf-151">**IovOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42adf-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="42adf-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42adf-154">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-154">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-155">Utilizzo di offload di I/O Virtualization (IOV) corrente.</span><span class="sxs-lookup"><span data-stu-id="42adf-155">The current I/O virtualization (IOV) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="42adf-156">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="42adf-156">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42adf-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="42adf-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42adf-159">Qualificatori: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-160">Numero corrente di coppie di code utilizzate dalla porta.</span><span class="sxs-lookup"><span data-stu-id="42adf-160">The current number of queue pairs being used by the port.</span></span>

</dd> <dt>

<span data-ttu-id="42adf-161">**IovVfDataPathActive**</span><span class="sxs-lookup"><span data-stu-id="42adf-161">**IovVfDataPathActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-162">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="42adf-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="42adf-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42adf-164">Qualificatori: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-164">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-165">Indica se il percorso dati VF IOV è attivo.</span><span class="sxs-lookup"><span data-stu-id="42adf-165">Indicates whether the IOV VF data path is active.</span></span>

</dd> <dt>

<span data-ttu-id="42adf-166">**IovVfId**</span><span class="sxs-lookup"><span data-stu-id="42adf-166">**IovVfId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42adf-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-168">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="42adf-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42adf-169">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-169">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-170">Identificatore VF IOV corrente assegnato alla porta.</span><span class="sxs-lookup"><span data-stu-id="42adf-170">The current IOV VF identifier that is assigned to the port.</span></span> <span data-ttu-id="42adf-171">Questa operazione è valida se **IovOffloadUsage** è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="42adf-171">This is valid if **IovOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="42adf-172">**IpsecCurrentOffloadSaCount**</span><span class="sxs-lookup"><span data-stu-id="42adf-172">**IpsecCurrentOffloadSaCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-173">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42adf-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-174">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="42adf-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42adf-175">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-175">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-176">Numero corrente di slot di offload dell'associazione di sicurezza (SA) in uso sulla porta.</span><span class="sxs-lookup"><span data-stu-id="42adf-176">The current number of security association (SA) offload slots in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="42adf-177">**Nome**</span><span class="sxs-lookup"><span data-stu-id="42adf-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-180">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="42adf-180">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="42adf-181">Stringa che identifica in modo univoco questa istanza di dati di porta nell'ambito dell'opzione e della porta.</span><span class="sxs-lookup"><span data-stu-id="42adf-181">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="42adf-182">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="42adf-182">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="42adf-183">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="42adf-183">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-186">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="42adf-186">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-187">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="42adf-187">The scoping system's creation class name.</span></span> <span data-ttu-id="42adf-188">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)ed è sempre impostata su "MSVM \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="42adf-188">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="42adf-189">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="42adf-189">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="42adf-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-192">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="42adf-192">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="42adf-193">Nome del Commuter virtuale che ha come ambito questa istanza di dati di porta.</span><span class="sxs-lookup"><span data-stu-id="42adf-193">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="42adf-194">Questa proprietà viene ereditata da [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="42adf-194">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="42adf-195">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="42adf-195">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-196">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="42adf-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-198">Qualificatori: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-198">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-199">Indica se VMMQ è attivo.</span><span class="sxs-lookup"><span data-stu-id="42adf-199">Indicates if VMMQ is active.</span></span>

> [!Note]  
> <span data-ttu-id="42adf-200">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="42adf-200">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="42adf-201">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="42adf-201">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-202">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42adf-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-204">Qualificatori: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-204">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-205">Indica il numero di code utilizzate per VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="42adf-205">Indicates how many queues are used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="42adf-206">Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="42adf-206">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="42adf-207">**VMQId**</span><span class="sxs-lookup"><span data-stu-id="42adf-207">**VMQId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-208">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42adf-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-209">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="42adf-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42adf-210">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-210">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-211">Identificatore corrente della coda della macchina virtuale assegnato alla porta.</span><span class="sxs-lookup"><span data-stu-id="42adf-211">The current virtual machine queue identifier that is assigned to the port.</span></span> <span data-ttu-id="42adf-212">Questa operazione è valida se **VMQOffloadUsage** è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="42adf-212">This is valid if **VMQOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="42adf-213">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="42adf-213">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-214">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42adf-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-215">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="42adf-215">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="42adf-216">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-216">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-217">Utilizzo dell'offload della coda della macchina virtuale (VMQ) corrente.</span><span class="sxs-lookup"><span data-stu-id="42adf-217">The current virtual machine queue (VMQ) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="42adf-218">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="42adf-218">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-219">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="42adf-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-221">Qualificatori: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-221">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-222">Indica se vRSS è attivo.</span><span class="sxs-lookup"><span data-stu-id="42adf-222">Indicates if vRSS is active.</span></span>

> [!Note]  
> <span data-ttu-id="42adf-223">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="42adf-223">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="42adf-224">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="42adf-224">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-225">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="42adf-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-227">Qualificatori: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-227">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-228">Indica se la CPU VMQ primaria è esclusa dalla tabella di riferimento indiretto VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="42adf-228">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="42adf-229">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="42adf-229">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="42adf-230">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="42adf-230">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-231">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="42adf-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-233">Qualificatori: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-233">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-234">Indica se viene eseguita la distribuzione del lato host VRSS/VMMQ, indipendentemente dalle impostazioni RSS della scheda di interfaccia di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="42adf-234">Indicates whether host side VRSS/VMMQ spreading happens, regardless of RSS settings of the virtual NIC.</span></span>

> [!Note]  
> <span data-ttu-id="42adf-235">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="42adf-235">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="42adf-236">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="42adf-236">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-237">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42adf-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-239">Qualificatori: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-239">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-240">Indica il numero minimo di code utilizzate per VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="42adf-240">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="42adf-241">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="42adf-241">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="42adf-242">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="42adf-242">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-243">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42adf-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-245">Qualificatori: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-245">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-246">Indica il modo in cui le code VRSS/VMMQ vengono indirizzate a processori host diversi.</span><span class="sxs-lookup"><span data-stu-id="42adf-246">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="42adf-247">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="42adf-247">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="42adf-248">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="42adf-248">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42adf-249">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42adf-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42adf-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="42adf-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42adf-251">Qualificatori: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="42adf-251">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42adf-252">Indica il modo in cui i canali VMBus sono creata un'affinità ai processori host.</span><span class="sxs-lookup"><span data-stu-id="42adf-252">Indicates how Vmbus channels are affinitized to host processors.</span></span>

> [!Note]  
> <span data-ttu-id="42adf-253">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="42adf-253">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42adf-254">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42adf-254">Requirements</span></span>



| <span data-ttu-id="42adf-255">Requisito</span><span class="sxs-lookup"><span data-stu-id="42adf-255">Requirement</span></span> | <span data-ttu-id="42adf-256">Valore</span><span class="sxs-lookup"><span data-stu-id="42adf-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42adf-257">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42adf-257">Minimum supported client</span></span><br/> | <span data-ttu-id="42adf-258">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="42adf-258">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42adf-259">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42adf-259">Minimum supported server</span></span><br/> | <span data-ttu-id="42adf-260">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="42adf-260">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42adf-261">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="42adf-261">Namespace</span></span><br/>                | <span data-ttu-id="42adf-262">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="42adf-262">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42adf-263">MOF</span><span class="sxs-lookup"><span data-stu-id="42adf-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42adf-264"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42adf-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42adf-265">DLL</span><span class="sxs-lookup"><span data-stu-id="42adf-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42adf-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42adf-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

