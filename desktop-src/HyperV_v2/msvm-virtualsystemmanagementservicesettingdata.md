---
description: Rappresenta le impostazioni per il servizio di virtualizzazione presenti in un singolo sistema host.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Classe Msvm_VirtualSystemManagementServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 782f196fdbd3a09126a7b4d14be6789bb633f043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305997"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a><span data-ttu-id="23dcc-103">\_Classe MSVM VirtualSystemManagementServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="23dcc-103">Msvm\_VirtualSystemManagementServiceSettingData class</span></span>

<span data-ttu-id="23dcc-104">Rappresenta le impostazioni per il servizio di virtualizzazione presenti in un singolo sistema host.</span><span class="sxs-lookup"><span data-stu-id="23dcc-104">Represents the settings for the virtualization service present on a single host system.</span></span> <span data-ttu-id="23dcc-105">Non è possibile modificare direttamente le proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="23dcc-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="23dcc-106">Il client deve chiamare il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per modificare una di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="23dcc-106">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify any of these properties.</span></span>

<span data-ttu-id="23dcc-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="23dcc-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23dcc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23dcc-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a><span data-ttu-id="23dcc-109">Members</span><span class="sxs-lookup"><span data-stu-id="23dcc-109">Members</span></span>

<span data-ttu-id="23dcc-110">La **classe \_ VirtualSystemManagementServiceSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="23dcc-110">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="23dcc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23dcc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23dcc-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23dcc-112">Properties</span></span>

<span data-ttu-id="23dcc-113">La **classe \_ VirtualSystemManagementServiceSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="23dcc-113">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23dcc-114">**BiosLockString**</span><span class="sxs-lookup"><span data-stu-id="23dcc-114">**BiosLockString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span><span class="sxs-lookup"><span data-stu-id="23dcc-117">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-118">Utilizzato dagli OEM per consentire l'esecuzione dei sistemi operativi Windows bloccati dal BIOS nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23dcc-118">Used by OEMs to allow BIOS-locked Windows operating systems to run in the virtual machine.</span></span> <span data-ttu-id="23dcc-119">La lunghezza della stringa deve corrispondere esattamente a 32 caratteri.</span><span class="sxs-lookup"><span data-stu-id="23dcc-119">This string must be exactly 32 characters in length.</span></span>

<span data-ttu-id="23dcc-120">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-120">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="23dcc-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-124">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23dcc-124">A short description of the object.</span></span> <span data-ttu-id="23dcc-125">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual System Management Service".</span><span class="sxs-lookup"><span data-stu-id="23dcc-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-126">**CurrentWWNNAddress**</span><span class="sxs-lookup"><span data-stu-id="23dcc-126">**CurrentWWNNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-129">Indirizzo del nome del nodo universale (WWNN) per gli indirizzi del nome universale generati dinamicamente utilizzati per le schede del bus host sintetico.</span><span class="sxs-lookup"><span data-stu-id="23dcc-129">The world wide node name (WWNN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="23dcc-130">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-130">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-131">**DefaultExternalDataRoot**</span><span class="sxs-lookup"><span data-stu-id="23dcc-131">**DefaultExternalDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-134">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span><span class="sxs-lookup"><span data-stu-id="23dcc-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-135">Radice dati esterna predefinita.</span><span class="sxs-lookup"><span data-stu-id="23dcc-135">The default external data root.</span></span> <span data-ttu-id="23dcc-136">Per impostazione predefinita, "*root* \\ ProgramData \\ Microsoft \\ Windows \\ Virtualization".</span><span class="sxs-lookup"><span data-stu-id="23dcc-136">By default, "*root*\\ProgramData\\Microsoft\\Windows\\Virtualization".</span></span>

<span data-ttu-id="23dcc-137">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-137">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-138">**DefaultVirtualHardDiskCachingMode**</span><span class="sxs-lookup"><span data-stu-id="23dcc-138">**DefaultVirtualHardDiskCachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23dcc-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-141">Indica se la memorizzazione nella cache dei file in memoria deve essere utilizzata per i dischi per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="23dcc-141">Indicates whether in-memory file caching should be used for disks by default.</span></span> <span data-ttu-id="23dcc-142">È possibile eseguire l'override di questo valore in base al disco nel campo **CachingMode** della classe [**\_ StorageAllocationSettingData di MSVM**](msvm-storageallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-142">This value can be overridden on a per-disk basis in the **CachingMode** field of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="23dcc-143">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="23dcc-143">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="23dcc-144">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="23dcc-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="23dcc-145">**Nessuna memorizzazione nella cache** (3)</span><span class="sxs-lookup"><span data-stu-id="23dcc-145">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="23dcc-146">**Memorizzare nella cache elementi padre condivisibili** (4)</span><span class="sxs-lookup"><span data-stu-id="23dcc-146">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23dcc-147">**DefaultVirtualHardDiskPath**</span><span class="sxs-lookup"><span data-stu-id="23dcc-147">**DefaultVirtualHardDiskPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-150">Percorso predefinito del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="23dcc-150">The default virtual hard disk path.</span></span> <span data-ttu-id="23dcc-151">Per impostazione predefinita, "utenti *radice* \\ \\ \\ documenti pubblici \\ dischi rigidi virtuali".</span><span class="sxs-lookup"><span data-stu-id="23dcc-151">By default, "*root*\\Users\\Public\\Documents\\Virtual Hard Disks".</span></span>

<span data-ttu-id="23dcc-152">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-152">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-153">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="23dcc-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-156">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="23dcc-156">A description of the object.</span></span> <span data-ttu-id="23dcc-157">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Settings for the Virtual System Management Service".</span><span class="sxs-lookup"><span data-stu-id="23dcc-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-158">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="23dcc-158">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-161">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23dcc-161">A display name for the object.</span></span> <span data-ttu-id="23dcc-162">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual System Management Service".</span><span class="sxs-lookup"><span data-stu-id="23dcc-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span> <span data-ttu-id="23dcc-163">La modifica di questa proprietà comporterà la modifica della proprietà **ElementName** del derivato [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associato.</span><span class="sxs-lookup"><span data-stu-id="23dcc-163">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-164">**EnhancedSessionModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="23dcc-164">**EnhancedSessionModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-165">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23dcc-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-167">Indica se nel server è consentita la modalità sessione avanzata.</span><span class="sxs-lookup"><span data-stu-id="23dcc-167">Indicates whether enhanced session mode is permitted on the server.</span></span> <span data-ttu-id="23dcc-168">**True** indica consentito, in caso contrario **false**.</span><span class="sxs-lookup"><span data-stu-id="23dcc-168">**True** indicates permitted, otherwise **False**.</span></span>

<span data-ttu-id="23dcc-169">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="23dcc-169">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-170">**HbaLunTimeout**</span><span class="sxs-lookup"><span data-stu-id="23dcc-170">**HbaLunTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-171">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23dcc-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-173">Specifica il periodo di tempo durante il quale il dispositivo virtuale Fibre Channel sintetico attenderà che venga visualizzato un numero di unità logica (LUN) prima di avviare una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23dcc-173">Specifies the amount of time that the synthetic Fibre Channel virtual device will wait for a logical unit number (LUN) to appear before starting a virtual machine.</span></span>

<span data-ttu-id="23dcc-174">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-174">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-175">**HypervisorRootSchedulerEnabled**</span><span class="sxs-lookup"><span data-stu-id="23dcc-175">**HypervisorRootSchedulerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-176">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23dcc-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-178">Indica se l'utilità di pianificazione radice dell'hypervisor è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="23dcc-178">Whether or not the hypervisor root scheduler is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="23dcc-179">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="23dcc-179">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="23dcc-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="23dcc-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-183">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="23dcc-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-184">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="23dcc-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="23dcc-185">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su "Microsoft:*host*", dove *host* è il nome NetBIOS del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="23dcc-185">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*host*", where *host* is the NetBIOS name of the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-186">**MaximumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="23dcc-186">**MaximumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-189">Indirizzo MAC massimo per gli indirizzi MAC generati dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="23dcc-189">The maximum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="23dcc-190">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-190">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-191">**MaximumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="23dcc-191">**MaximumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-194">Indirizzo WWPN (World Wide Port Name) per gli indirizzi del nome universale generati dinamicamente utilizzati per le schede del bus host sintetico.</span><span class="sxs-lookup"><span data-stu-id="23dcc-194">The maximum world wide port name (WWPN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="23dcc-195">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-195">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-196">**MinimumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="23dcc-196">**MinimumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-199">Indirizzo MAC minimo per gli indirizzi MAC generati dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="23dcc-199">The minimum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="23dcc-200">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-200">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-201">**MinimumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="23dcc-201">**MinimumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-204">Indirizzo del nome della porta universale minimo per gli indirizzi del nome universale generati dinamicamente utilizzati per le schede del bus host sintetico.</span><span class="sxs-lookup"><span data-stu-id="23dcc-204">The minimum world wide port name address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="23dcc-205">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-205">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-206">**NumaSpanningEnabled**</span><span class="sxs-lookup"><span data-stu-id="23dcc-206">**NumaSpanningEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-207">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="23dcc-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-209">Specifica se è possibile allocare memoria dai nodi NUMA (non-Uniform Memory Access) remoti quando si avvia una macchina virtuale o quando si assegna memoria a una macchina virtuale tramite la memoria dinamica.</span><span class="sxs-lookup"><span data-stu-id="23dcc-209">Specifies whether memory can be allocated from remote nonuniform memory access (NUMA) nodes when starting a virtual machine or when assigning memory to a virtual machine by dynamic memory.</span></span> <span data-ttu-id="23dcc-210">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="23dcc-210">This can be one of the following values.</span></span>



| <span data-ttu-id="23dcc-211">Valore</span><span class="sxs-lookup"><span data-stu-id="23dcc-211">Value</span></span>                                                                                | <span data-ttu-id="23dcc-212">Significato</span><span class="sxs-lookup"><span data-stu-id="23dcc-212">Meaning</span></span>                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23dcc-213"><dt>**Vero**</dt></span><span class="sxs-lookup"><span data-stu-id="23dcc-213"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="23dcc-214">La memoria può essere allocata dai nodi NUMA locali e remoti.</span><span class="sxs-lookup"><span data-stu-id="23dcc-214">Memory can be allocated from both local and remote NUMA nodes.</span></span><br/>                   |
| <dl> <span data-ttu-id="23dcc-215"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="23dcc-215"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="23dcc-216">La memoria può essere allocata solo dal nodo NUMA assegnato alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23dcc-216">Memory can be allocated only from the NUMA node assigned to the virtual machine.</span></span><br/> |



 

<span data-ttu-id="23dcc-217">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-217">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-218">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="23dcc-218">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-221">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="23dcc-221">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-222">Viene descritto come è possibile raggiungere il proprietario del sistema primario, ad esempio il numero di telefono o l'indirizzo di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="23dcc-222">Describes how the primary system owner can be reached (for example, phone number or email address).</span></span> <span data-ttu-id="23dcc-223">Per impostazione predefinita, è vuoto.</span><span class="sxs-lookup"><span data-stu-id="23dcc-223">By default, empty.</span></span> <span data-ttu-id="23dcc-224">Il nome non può superare i 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="23dcc-224">This name may not exceed 256 characters in length.</span></span>

<span data-ttu-id="23dcc-225">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-225">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="23dcc-226">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="23dcc-226">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dcc-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="23dcc-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="23dcc-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23dcc-229">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="23dcc-229">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="23dcc-230">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="23dcc-230">The name of the primary system owner.</span></span> <span data-ttu-id="23dcc-231">Per impostazione predefinita, "Administrators".</span><span class="sxs-lookup"><span data-stu-id="23dcc-231">By default, "Administrators".</span></span> <span data-ttu-id="23dcc-232">Questo valore non può superare i 64 caratteri.</span><span class="sxs-lookup"><span data-stu-id="23dcc-232">This value may not exceed 64 characters in length.</span></span>

<span data-ttu-id="23dcc-233">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23dcc-233">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23dcc-234">Commenti</span><span class="sxs-lookup"><span data-stu-id="23dcc-234">Remarks</span></span>

<span data-ttu-id="23dcc-235">L'accesso alla **classe \_ VirtualSystemManagementServiceSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="23dcc-235">Access to the **Msvm\_VirtualSystemManagementServiceSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="23dcc-236">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="23dcc-236">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="23dcc-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23dcc-237">Requirements</span></span>



| <span data-ttu-id="23dcc-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="23dcc-238">Requirement</span></span> | <span data-ttu-id="23dcc-239">Valore</span><span class="sxs-lookup"><span data-stu-id="23dcc-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23dcc-240">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23dcc-240">Minimum supported client</span></span><br/> | <span data-ttu-id="23dcc-241">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="23dcc-241">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23dcc-242">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23dcc-242">Minimum supported server</span></span><br/> | <span data-ttu-id="23dcc-243">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="23dcc-243">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23dcc-244">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="23dcc-244">Namespace</span></span><br/>                | <span data-ttu-id="23dcc-245">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="23dcc-245">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23dcc-246">MOF</span><span class="sxs-lookup"><span data-stu-id="23dcc-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23dcc-247"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23dcc-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23dcc-248">DLL</span><span class="sxs-lookup"><span data-stu-id="23dcc-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23dcc-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23dcc-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="23dcc-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23dcc-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23dcc-251">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="23dcc-251">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="23dcc-252">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="23dcc-252">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="23dcc-253">[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="23dcc-253">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="23dcc-254">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="23dcc-254">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

