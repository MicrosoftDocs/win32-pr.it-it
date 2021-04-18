---
description: Rappresenta le impostazioni per il servizio migrazione del sistema virtuale in un host.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Classe Msvm_VirtualSystemMigrationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305988"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a><span data-ttu-id="50d80-103">\_Classe MSVM VirtualSystemMigrationServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="50d80-103">Msvm\_VirtualSystemMigrationServiceSettingData class</span></span>

<span data-ttu-id="50d80-104">Rappresenta le impostazioni per il servizio migrazione del sistema virtuale in un host.</span><span class="sxs-lookup"><span data-stu-id="50d80-104">Represents the settings for the virtual system migration service on a host.</span></span> <span data-ttu-id="50d80-105">Non è possibile modificare direttamente le proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="50d80-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="50d80-106">Il client deve chiamare il metodo **MSVM \_ VirtualSystemMigrationService. ModifyServiceSettings** per modificare una di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="50d80-106">The client must call the **Msvm\_VirtualSystemMigrationService.ModifyServiceSettings** method to modify any of these properties.</span></span>

<span data-ttu-id="50d80-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="50d80-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d80-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50d80-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a><span data-ttu-id="50d80-109">Members</span><span class="sxs-lookup"><span data-stu-id="50d80-109">Members</span></span>

<span data-ttu-id="50d80-110">La **classe \_ VirtualSystemMigrationServiceSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="50d80-110">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="50d80-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50d80-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50d80-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50d80-112">Properties</span></span>

<span data-ttu-id="50d80-113">La **classe \_ VirtualSystemMigrationServiceSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="50d80-113">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50d80-114">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="50d80-114">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-115">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50d80-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50d80-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50d80-117">Specifica il meccanismo di autenticazione utilizzato per le connessioni di rete di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="50d80-117">Specifies the authentication mechanism used for virtual system migration network connections.</span></span> <span data-ttu-id="50d80-118">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="50d80-118">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

<span data-ttu-id="50d80-119">**CredSSP** (0)</span><span class="sxs-lookup"><span data-stu-id="50d80-119">**CredSSP** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

<span data-ttu-id="50d80-120">**Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="50d80-120">**Kerberos** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="50d80-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="50d80-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50d80-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50d80-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50d80-124">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="50d80-124">A short description of the object.</span></span> <span data-ttu-id="50d80-125">Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="50d80-125">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="50d80-126">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="50d80-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50d80-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50d80-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50d80-129">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="50d80-129">A description of the object.</span></span> <span data-ttu-id="50d80-130">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="50d80-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="50d80-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="50d80-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50d80-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50d80-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50d80-134">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="50d80-134">A display name for the object.</span></span> <span data-ttu-id="50d80-135">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="50d80-135">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="50d80-136">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="50d80-136">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-137">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="50d80-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="50d80-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="50d80-139">Indica se la compressione del traffico della migrazione in tempo reale è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="50d80-139">Indicates whether compression of live migration traffic is enabled or disabled.</span></span> <span data-ttu-id="50d80-140">True indica Enabled.</span><span class="sxs-lookup"><span data-stu-id="50d80-140">True indicates enabled.</span></span>

<span data-ttu-id="50d80-141">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="50d80-141">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="50d80-142">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="50d80-142">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="50d80-143">**EnableSmbTransport**</span><span class="sxs-lookup"><span data-stu-id="50d80-143">**EnableSmbTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-144">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="50d80-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="50d80-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="50d80-146">Indica se l'utilizzo di SMB come tipo di trasporto per il trasferimento dello stato della macchina virtuale tra gli host Hyper-V durante la migrazione del sistema virtuale è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="50d80-146">Indicates whether use of SMB as a transport type for transferring VM state between the Hyper-V hosts during virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="50d80-147">**True** indica Enabled.</span><span class="sxs-lookup"><span data-stu-id="50d80-147">**True** indicates enabled.</span></span> <span data-ttu-id="50d80-148">Se le NIC RDMA sono configurate per il trasporto SMB durante la migrazione in tempo reale della macchina virtuale, si ottengono prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="50d80-148">A higher performance is achieved if RDMA NICs are configured for SMB transport during VM live migration.</span></span> <span data-ttu-id="50d80-149">Se il valore di **EnableSmbTransport** è true, il valore di **EnableCompression** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="50d80-149">If **EnableSmbTransport** value is true, the value of **EnableCompression** is ignored.</span></span>

<span data-ttu-id="50d80-150">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="50d80-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="50d80-151">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="50d80-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="50d80-152">**EnableVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="50d80-152">**EnableVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-153">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="50d80-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50d80-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50d80-155">Specifica se la migrazione del sistema virtuale è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="50d80-155">Specifies whether virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="50d80-156">La migrazione dell'archiviazione è sempre abilitata.</span><span class="sxs-lookup"><span data-stu-id="50d80-156">Storage migration is always enabled.</span></span> <span data-ttu-id="50d80-157">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="50d80-157">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="50d80-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="50d80-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50d80-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50d80-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50d80-161">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="50d80-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="50d80-162">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="50d80-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="50d80-163">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="50d80-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="50d80-164">**MaximumActiveStorageMigration**</span><span class="sxs-lookup"><span data-stu-id="50d80-164">**MaximumActiveStorageMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50d80-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50d80-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50d80-167">Specifica il numero massimo di migrazioni di archiviazione attive consentite.</span><span class="sxs-lookup"><span data-stu-id="50d80-167">Specifies the maximum number of active storage migrations allowed.</span></span> <span data-ttu-id="50d80-168">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="50d80-168">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="50d80-169">**MaximumActiveVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="50d80-169">**MaximumActiveVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d80-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50d80-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50d80-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50d80-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50d80-172">Specifica il numero massimo di migrazioni attive del sistema virtuale consentite.</span><span class="sxs-lookup"><span data-stu-id="50d80-172">Specifies the maximum number of active virtual system migrations allowed.</span></span> <span data-ttu-id="50d80-173">Si tratta di una proprietà di sola lettura, ma può essere modificata tramite il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) della classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="50d80-173">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50d80-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50d80-174">Requirements</span></span>



| <span data-ttu-id="50d80-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="50d80-175">Requirement</span></span> | <span data-ttu-id="50d80-176">Valore</span><span class="sxs-lookup"><span data-stu-id="50d80-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d80-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50d80-177">Minimum supported client</span></span><br/> | <span data-ttu-id="50d80-178">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="50d80-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="50d80-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50d80-179">Minimum supported server</span></span><br/> | <span data-ttu-id="50d80-180">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="50d80-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50d80-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50d80-181">Namespace</span></span><br/>                | <span data-ttu-id="50d80-182">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="50d80-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="50d80-183">MOF</span><span class="sxs-lookup"><span data-stu-id="50d80-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50d80-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50d80-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50d80-185">DLL</span><span class="sxs-lookup"><span data-stu-id="50d80-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50d80-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50d80-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50d80-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50d80-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d80-188">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="50d80-188">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="50d80-189">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="50d80-189">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

