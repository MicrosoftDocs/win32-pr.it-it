---
description: Rappresenta i dati dell'impostazione della funzionalità di offload delle porte.
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Classe Msvm_EthernetSwitchPortOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 150a7b5e54e371c11741dd7c763b0ae145354b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320021"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a><span data-ttu-id="4f452-103">\_Classe MSVM EthernetSwitchPortOffloadSettingData</span><span class="sxs-lookup"><span data-stu-id="4f452-103">Msvm\_EthernetSwitchPortOffloadSettingData class</span></span>

<span data-ttu-id="4f452-104">Rappresenta i dati dell'impostazione della funzionalità di offload delle porte.</span><span class="sxs-lookup"><span data-stu-id="4f452-104">Represents the port offload feature setting data.</span></span>

<span data-ttu-id="4f452-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4f452-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f452-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f452-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a><span data-ttu-id="4f452-107">Members</span><span class="sxs-lookup"><span data-stu-id="4f452-107">Members</span></span>

<span data-ttu-id="4f452-108">La **classe \_ EthernetSwitchPortOffloadSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4f452-108">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4f452-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f452-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f452-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f452-110">Properties</span></span>

<span data-ttu-id="4f452-111">La **classe \_ EthernetSwitchPortOffloadSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4f452-111">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f452-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="4f452-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f452-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f452-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f452-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4f452-115">A short description of the object.</span></span> <span data-ttu-id="4f452-116">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port offload Settings".</span><span class="sxs-lookup"><span data-stu-id="4f452-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="4f452-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4f452-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f452-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f452-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f452-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="4f452-120">A description of the object.</span></span> <span data-ttu-id="4f452-121">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "rappresenta i dati dell'impostazione della funzionalità di offload della porta".</span><span class="sxs-lookup"><span data-stu-id="4f452-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="4f452-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4f452-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f452-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f452-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f452-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4f452-125">A display name for the object.</span></span> <span data-ttu-id="4f452-126">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Switch Port offload Settings".</span><span class="sxs-lookup"><span data-stu-id="4f452-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="4f452-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4f452-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f452-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f452-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f452-130">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="4f452-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4f452-131">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="4f452-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4f452-132">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4f452-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4f452-133">**IOVInterruptModeration**</span><span class="sxs-lookup"><span data-stu-id="4f452-133">**IOVInterruptModeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-136">Qualificatori: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-136">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-137">Valore di moderazione interrupt per l'offload di I/O Virtualization (IOV).</span><span class="sxs-lookup"><span data-stu-id="4f452-137">The interrupt moderation value for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="4f452-138">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="4f452-138">The default is 0.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="4f452-139">**Valore predefinito** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-139">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

<span data-ttu-id="4f452-140">**Adattivo** (1)</span><span class="sxs-lookup"><span data-stu-id="4f452-140">**Adaptive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="4f452-141">**Disattivato** (2)</span><span class="sxs-lookup"><span data-stu-id="4f452-141">**Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="4f452-142">**Bassa** (100)</span><span class="sxs-lookup"><span data-stu-id="4f452-142">**Low** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="4f452-143">**Media** (200)</span><span class="sxs-lookup"><span data-stu-id="4f452-143">**Medium** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="4f452-144">**Alto** (300)</span><span class="sxs-lookup"><span data-stu-id="4f452-144">**High** (300)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4f452-145">**IOVOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="4f452-145">**IOVOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-148">Qualificatori: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-148">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-149">Peso assegnato a questa porta per l'offload di I/O Virtualization (IOV).</span><span class="sxs-lookup"><span data-stu-id="4f452-149">The weight assigned to this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="4f452-150">Il peso è l'importanza relativa durante l'assegnazione delle risorse IOV.</span><span class="sxs-lookup"><span data-stu-id="4f452-150">The weight is the relative importance when assigning IOV resources.</span></span> <span data-ttu-id="4f452-151">L'impostazione della proprietà **IOVOffloadWeight** su 0 Disabilita l'offload IOV sulla porta.</span><span class="sxs-lookup"><span data-stu-id="4f452-151">Setting the **IOVOffloadWeight** property to 0 disables IOV offloading on the port.</span></span> <span data-ttu-id="4f452-152">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="4f452-152">The default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="4f452-153">**IOVQueuePairsRequested**</span><span class="sxs-lookup"><span data-stu-id="4f452-153">**IOVQueuePairsRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-154">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-156">Qualificatori: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-156">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-157">Numero di coppie di code richieste per questa porta per l'offload di I/O Virtualization (IOV).</span><span class="sxs-lookup"><span data-stu-id="4f452-157">The number of queue pairs requested for this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="4f452-158">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="4f452-158">The default is 1.</span></span>

</dd> <dt>

<span data-ttu-id="4f452-159">**IPSecOffloadLimit**</span><span class="sxs-lookup"><span data-stu-id="4f452-159">**IPSecOffloadLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-161">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-162">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-162">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-163">Numero massimo di slot di offload dell'associazione di sicurezza consentiti dalla porta.</span><span class="sxs-lookup"><span data-stu-id="4f452-163">The maximum number of security association (SA) offload slots allowed from the port.</span></span>

</dd> <dt>

<span data-ttu-id="4f452-164">**PacketDirectModerationCount**</span><span class="sxs-lookup"><span data-stu-id="4f452-164">**PacketDirectModerationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-167">Qualificatori: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-167">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-168">Valore del conteggio di moderazione interrupt per Packet Direct (PD). Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="4f452-168">The interrupt moderation count value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-169">Proprietà aggiunta in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4f452-169">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-170">**PacketDirectModerationInterval**</span><span class="sxs-lookup"><span data-stu-id="4f452-170">**PacketDirectModerationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-171">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-173">Qualificatori: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-173">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-174">Valore dell'intervallo di moderazione dell'interrupt per il pacchetto diretto (PD). Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="4f452-174">The interrupt moderation interval value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-175">Proprietà aggiunta in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4f452-175">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-176">**PacketDirectNumProcs**</span><span class="sxs-lookup"><span data-stu-id="4f452-176">**PacketDirectNumProcs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-177">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-178">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-179">Qualificatori: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-179">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-180">Il numero di processori utilizzati dall'host per l'elaborazione dei pacchetti inviati da questa porta in modalità pacchetto diretto.</span><span class="sxs-lookup"><span data-stu-id="4f452-180">The number of processors used by the host for processing packets sent from this port in Packet Direct mode.</span></span> <span data-ttu-id="4f452-181">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="4f452-181">The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-182">Proprietà aggiunta in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4f452-182">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-183">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="4f452-183">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4f452-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-185">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-186">Qualificatori: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-186">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-187">Abilitare l'offload VMMQ se supportato dall'hardware. Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="4f452-187">Enable VMMQ offload if supported by hardware.The default is False.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-188">Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4f452-188">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-189">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="4f452-189">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-190">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-191">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-192">Qualificatori: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-192">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-193">Numero di code da allocare quando VRSS è abilitato.</span><span class="sxs-lookup"><span data-stu-id="4f452-193">The number of queues to allocate when VRSS is enabled.</span></span> <span data-ttu-id="4f452-194">Il valore predefinito è 16.</span><span class="sxs-lookup"><span data-stu-id="4f452-194">The default is 16.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-195">Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4f452-195">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-196">**VMQOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="4f452-196">**VMQOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-197">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-198">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-199">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-200">Il peso assegnato a questa porta per l'offload della coda della macchina virtuale (VMQ).</span><span class="sxs-lookup"><span data-stu-id="4f452-200">The weight assigned to this port for virtual machine queue (VMQ) offloading.</span></span> <span data-ttu-id="4f452-201">Il peso è l'importanza relativa durante l'assegnazione delle risorse VMQ.</span><span class="sxs-lookup"><span data-stu-id="4f452-201">The weight is the relative importance when assigning VMQ resources.</span></span> <span data-ttu-id="4f452-202">L'impostazione della proprietà **VMQOffloadWeight** su 0 Disabilita VMQ sulla porta.</span><span class="sxs-lookup"><span data-stu-id="4f452-202">Setting the **VMQOffloadWeight** property to 0 disables VMQ on the port.</span></span> <span data-ttu-id="4f452-203">Il valore predefinito è 100.</span><span class="sxs-lookup"><span data-stu-id="4f452-203">The default is 100.</span></span>

</dd> <dt>

<span data-ttu-id="4f452-204">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="4f452-204">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-205">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4f452-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-206">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-207">Qualificatori: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-207">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-208">Abilitare VRSS.</span><span class="sxs-lookup"><span data-stu-id="4f452-208">Enable VRSS.</span></span> <span data-ttu-id="4f452-209">Il valore predefinito è true.</span><span class="sxs-lookup"><span data-stu-id="4f452-209">The default is true.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-210">Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4f452-210">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-211">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="4f452-211">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-212">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4f452-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-213">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-213">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-214">Qualificatori: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-214">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-215">Indica se escludere il processore VMQ primario dalla tabella di riferimento indiretto VRSS quando è abilitato VRSS. Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="4f452-215">Whether to exclude primary VMQ processor from the VRSS indirection table when VRSS is enabled.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-216">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="4f452-216">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-217">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="4f452-217">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-218">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4f452-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-219">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-219">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-220">Qualificatori: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-220">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-221">Indica se eseguire sempre VRSS sul lato host quando VRSS è abilitato, indipendentemente dall'impostazione RSS della scheda di interfaccia di rete virtuale. Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="4f452-221">Whether to always do host-side VRSS when VRSS is enabled, regardless of RSS setting of the virtual NIC.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-222">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="4f452-222">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-223">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="4f452-223">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-224">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-225">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-225">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-226">Qualificatori: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-226">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-227">Numero minimo di code da allocare quando VRSS è abilitato. Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="4f452-227">The minimum number of queues to allocate when VRSS is enabled.The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-228">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="4f452-228">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-229">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="4f452-229">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-230">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-231">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-231">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-232">Qualificatori: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-232">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-233">Modalità di pianificazione della coda da usare quando VRSS è abilitato. Il valore predefinito è la pianificazione statica.</span><span class="sxs-lookup"><span data-stu-id="4f452-233">The queue scheduling mode to use when VRSS is enabled.The default is static scheduling.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-234">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="4f452-234">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f452-235">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="4f452-235">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f452-236">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f452-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f452-237">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f452-237">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4f452-238">Qualificatori: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4f452-238">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4f452-239">Criteri di affinità del canale VMBus da usare quando VRSS è abilitato. Il valore predefinito è Strong.</span><span class="sxs-lookup"><span data-stu-id="4f452-239">The vmbus channel affinity policy to use when VRSS is enabled.The default is strong.</span></span>

> [!Note]  
> <span data-ttu-id="4f452-240">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="4f452-240">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f452-241">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f452-241">Requirements</span></span>



| <span data-ttu-id="4f452-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f452-242">Requirement</span></span> | <span data-ttu-id="4f452-243">Valore</span><span class="sxs-lookup"><span data-stu-id="4f452-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f452-244">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f452-244">Minimum supported client</span></span><br/> | <span data-ttu-id="4f452-245">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4f452-245">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4f452-246">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f452-246">Minimum supported server</span></span><br/> | <span data-ttu-id="4f452-247">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4f452-247">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f452-248">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f452-248">Namespace</span></span><br/>                | <span data-ttu-id="4f452-249">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4f452-249">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4f452-250">MOF</span><span class="sxs-lookup"><span data-stu-id="4f452-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f452-251"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f452-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f452-252">DLL</span><span class="sxs-lookup"><span data-stu-id="4f452-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f452-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f452-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

