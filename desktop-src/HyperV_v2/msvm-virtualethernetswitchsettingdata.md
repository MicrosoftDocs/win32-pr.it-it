---
description: Rappresenta la configurazione corrente di un commutire Ethernet virtuale.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Classe Msvm_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310001"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="b486b-103">\_Classe MSVM VirtualEthernetSwitchSettingData</span><span class="sxs-lookup"><span data-stu-id="b486b-103">Msvm\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="b486b-104">Rappresenta la configurazione corrente di un commutire Ethernet virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-104">Represents the current configuration of a virtual Ethernet switch.</span></span>

<span data-ttu-id="b486b-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b486b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b486b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b486b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="b486b-107">Members</span><span class="sxs-lookup"><span data-stu-id="b486b-107">Members</span></span>

<span data-ttu-id="b486b-108">La **classe \_ VirtualEthernetSwitchSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b486b-108">The **Msvm\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b486b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b486b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b486b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b486b-110">Properties</span></span>

<span data-ttu-id="b486b-111">La **classe \_ VirtualEthernetSwitchSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b486b-111">The **Msvm\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b486b-112">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="b486b-112">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-113">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b486b-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b486b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-115">Elenco di pool di risorse host da associare o attualmente associati al comcambio Ethernet allo scopo di allocazione delle connessioni Ethernet tra una macchina virtuale e un Commuter Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b486b-115">A list of host resource pools to be associated or that are currently associated with the Ethernet switch for the purpose of the allocation of Ethernet connections between a virtual machine and an Ethernet switch.</span></span> <span data-ttu-id="b486b-116">Ogni valore deve essere conforme all'URI WBEM di produzione \_ \_ UntypedInstancePath come definito in DSP0207.</span><span class="sxs-lookup"><span data-stu-id="b486b-116">Each value must conform to the production WBEM\_URI\_UntypedInstancePath as defined in DSP0207.</span></span> <span data-ttu-id="b486b-117">Questa proprietà viene ereditata da **CIM \_ VirtualEthernetSwitchSettingData**.</span><span class="sxs-lookup"><span data-stu-id="b486b-117">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-118">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="b486b-118">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-119">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b486b-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-121">Azione da eseguire per la macchina virtuale quando il software eseguito dalla macchina virtuale ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b486b-121">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="b486b-122">Gli errori in questo caso indicano un errore rilevabile dalla piattaforma host, ad esempio una condizione di stato di attesa non interrompibili.</span><span class="sxs-lookup"><span data-stu-id="b486b-122">Failures in this case means a failure that is detectable by the host platform, such as a non-interruptible wait state condition.</span></span> <span data-ttu-id="b486b-123">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-123">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-124">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="b486b-124">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b486b-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-127">Azione da eseguire per la macchina virtuale quando l'host viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="b486b-127">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="b486b-128">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-128">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-129">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="b486b-129">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b486b-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-132">Azione da eseguire per la macchina virtuale all'avvio dell'host.</span><span class="sxs-lookup"><span data-stu-id="b486b-132">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="b486b-133">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-133">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-134">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="b486b-134">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-135">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b486b-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-137">Tempo di ritardo prima che la macchina virtuale venga avviata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b486b-137">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="b486b-138">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-138">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-139">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="b486b-139">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b486b-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-142">Numero che indica la sequenza relativa di attivazione della macchina virtuale all'avvio del sistema host.</span><span class="sxs-lookup"><span data-stu-id="b486b-142">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="b486b-143">Un numero inferiore indica l'attivazione precedente.</span><span class="sxs-lookup"><span data-stu-id="b486b-143">A lower number indicates earlier activation.</span></span> <span data-ttu-id="b486b-144">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-144">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-145">**BandwidthReservationMode**</span><span class="sxs-lookup"><span data-stu-id="b486b-145">**BandwidthReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b486b-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b486b-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b486b-148">Modalità di prenotazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="b486b-148">The bandwidth reservation mode.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="b486b-149">**Valore predefinito** (0)</span><span class="sxs-lookup"><span data-stu-id="b486b-149">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="b486b-150">**Peso** (1)</span><span class="sxs-lookup"><span data-stu-id="b486b-150">**Weight** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="b486b-151">**Assoluta** (2)</span><span class="sxs-lookup"><span data-stu-id="b486b-151">**Absolute** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b486b-152">**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="b486b-152">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b486b-153">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b486b-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-156">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b486b-156">A short description of the object.</span></span> <span data-ttu-id="b486b-157">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Virtual Ethernet Switch Settings".</span><span class="sxs-lookup"><span data-stu-id="b486b-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Ethernet Switch Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b486b-158">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="b486b-158">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-161">Percorso di una directory in cui vengono archiviate le informazioni sulla configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-161">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="b486b-162">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-162">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-163">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="b486b-163">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-166">Il percorso relativo e il nome file di un file in cui vengono archiviate le informazioni sulla configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-166">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="b486b-167">Questo percorso è relativo alla proprietà **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="b486b-167">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="b486b-168">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-169">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="b486b-169">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-172">Identificatore univoco della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-172">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="b486b-173">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-173">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-174">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="b486b-174">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-175">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b486b-175">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-177">Data e ora in cui sono state create le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b486b-177">The date and time at which the settings were created.</span></span> <span data-ttu-id="b486b-178">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b486b-178">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b486b-179">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b486b-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-182">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="b486b-182">A description of the object.</span></span> <span data-ttu-id="b486b-183">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Active Settings for the Virtual Ethernet Switch".</span><span class="sxs-lookup"><span data-stu-id="b486b-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Active settings for the virtual Ethernet switch".</span></span>

</dd> <dt>

<span data-ttu-id="b486b-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b486b-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-187">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b486b-187">A display name for the object.</span></span> <span data-ttu-id="b486b-188">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b486b-188">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b486b-189">**ExtensionOrder**</span><span class="sxs-lookup"><span data-stu-id="b486b-189">**ExtensionOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-190">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b486b-190">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b486b-191">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b486b-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b486b-192">Matrice di istanze incorporate della classe [**\_ EthernetSwitchExtension MSVM**](msvm-ethernetswitchextension.md) che rappresentano le estensioni del commutire associate a questa opzione, nell'ordine in cui vengono applicate.</span><span class="sxs-lookup"><span data-stu-id="b486b-192">An array of embedded instances of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represent the switch extensions bound to this switch, in the order in which they are applied.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b486b-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b486b-196">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b486b-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b486b-197">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b486b-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b486b-198">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ed è sempre impostata su "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="b486b-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="b486b-199">**IOVPreferred**</span><span class="sxs-lookup"><span data-stu-id="b486b-199">**IOVPreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-200">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b486b-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-201">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b486b-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b486b-202">Specifica se la virtualizzazione IO (Single root IO Virtualization) (SR-IOV) è preferibile o meno, se disponibile, nell'adapter sottostante.</span><span class="sxs-lookup"><span data-stu-id="b486b-202">Specifies whether single root IO virtualization (SR-IOV) is preferred or not, if available, on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-203">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="b486b-203">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-206">Percorso di una directory in cui vengono archiviate le informazioni di log per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-206">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="b486b-207">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-208">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="b486b-208">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-209">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b486b-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-211">Specifica il numero massimo di indirizzi MAC univoci che possono essere appresi dall'opzione per supportare l'apprendimento degli indirizzi MAC, come definito nello standard IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="b486b-211">Specifies the maximum number of unique MAC addresses that can be learned by the switch to support MAC Address Learning, as defined in the IEEE 802.1 standard.</span></span> <span data-ttu-id="b486b-212">Questa proprietà viene ereditata da **CIM \_ VirtualEthernetSwitchSettingData**.</span><span class="sxs-lookup"><span data-stu-id="b486b-212">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-213">**Note**</span><span class="sxs-lookup"><span data-stu-id="b486b-213">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-214">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b486b-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b486b-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-216">Note fornite dall'utente correlate alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-216">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="b486b-217">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b486b-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b486b-218">**PacketDirectEnabled**</span><span class="sxs-lookup"><span data-stu-id="b486b-218">**PacketDirectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-219">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b486b-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-220">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b486b-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b486b-221">Specifica se è necessario usare PacketDirect, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="b486b-221">Specifies whether PacketDirect should be used, if available.</span></span> <span data-ttu-id="b486b-222">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="b486b-222">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="b486b-223">Questa proprietà è stata aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b486b-223">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="b486b-224">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="b486b-224">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-227">Percorso completo di un file in cui sono archiviate le informazioni relative al ripristino per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-227">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="b486b-228">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-228">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-229">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="b486b-229">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-232">Percorso di una directory in cui vengono archiviate le informazioni sugli snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-232">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="b486b-233">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-233">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-234">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="b486b-234">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-237">Percorso di una directory in cui vengono archiviate informazioni sulle informazioni relative alla sospensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-237">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="b486b-238">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-238">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-239">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="b486b-239">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-242">Percorso di una directory in cui vengono archiviati i file di scambio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b486b-242">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="b486b-243">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b486b-243">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b486b-244">**TeamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="b486b-244">**TeamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-245">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b486b-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-246">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b486b-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b486b-247">Specifica se deve essere utilizzato il gruppo NIC.</span><span class="sxs-lookup"><span data-stu-id="b486b-247">Specifies whether NIC Teaming should be used.</span></span> <span data-ttu-id="b486b-248">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="b486b-248">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="b486b-249">Questa proprietà è stata aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="b486b-249">This property was added inWindows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="b486b-250">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="b486b-250">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-253">Nome dell'oggetto [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) a cui appartengono i dati dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="b486b-253">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="b486b-254">Questa proprietà è una sostituzione da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b486b-254">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b486b-255">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="b486b-255">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-256">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b486b-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b486b-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-258">Specifica il tipo di macchina virtuale rappresentata dai dati di impostazione.</span><span class="sxs-lookup"><span data-stu-id="b486b-258">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="b486b-259">Questa proprietà viene ereditata dal [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b486b-259">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b486b-260">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="b486b-260">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b486b-261">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b486b-261">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b486b-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b486b-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b486b-263">Elenco di identificatori VLAN a cui può accedere questa opzione.</span><span class="sxs-lookup"><span data-stu-id="b486b-263">A list of VLAN identifiers that this switch can access.</span></span> <span data-ttu-id="b486b-264">Questa proprietà viene ereditata da **CIM \_ VirtualEthernetSwitchSettingData**.</span><span class="sxs-lookup"><span data-stu-id="b486b-264">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b486b-265">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b486b-265">Requirements</span></span>



| <span data-ttu-id="b486b-266">Requisito</span><span class="sxs-lookup"><span data-stu-id="b486b-266">Requirement</span></span> | <span data-ttu-id="b486b-267">Valore</span><span class="sxs-lookup"><span data-stu-id="b486b-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b486b-268">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b486b-268">Minimum supported client</span></span><br/> | <span data-ttu-id="b486b-269">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b486b-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b486b-270">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b486b-270">Minimum supported server</span></span><br/> | <span data-ttu-id="b486b-271">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b486b-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b486b-272">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b486b-272">Namespace</span></span><br/>                | <span data-ttu-id="b486b-273">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b486b-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b486b-274">MOF</span><span class="sxs-lookup"><span data-stu-id="b486b-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b486b-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b486b-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b486b-276">DLL</span><span class="sxs-lookup"><span data-stu-id="b486b-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b486b-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b486b-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

