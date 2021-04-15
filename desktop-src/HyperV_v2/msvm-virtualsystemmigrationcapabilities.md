---
description: Definisce i mezzi mediante i quali un client può individuare i metodi forniti dal servizio di migrazione e un intervallo valido di dati dell'impostazione della migrazione del sistema virtuale.
ms.assetid: 704fa81d-54a4-4d12-9b85-8836581d2784
title: Classe Msvm_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationCapabilities
- Msvm_VirtualSystemMigrationCapabilities.InstanceID
- Msvm_VirtualSystemMigrationCapabilities.Caption
- Msvm_VirtualSystemMigrationCapabilities.Description
- Msvm_VirtualSystemMigrationCapabilities.ElementName
- Msvm_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c89e898cbf861d2bc3643e43a8bd9089062a2d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525194"
---
# <a name="msvm_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="ca89f-103">\_Classe MSVM VirtualSystemMigrationCapabilities</span><span class="sxs-lookup"><span data-stu-id="ca89f-103">Msvm\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="ca89f-104">Definisce i mezzi mediante i quali un client può individuare i metodi forniti dal servizio di migrazione e un intervallo valido di dati dell'impostazione della migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="ca89f-104">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span> <span data-ttu-id="ca89f-105">L' **oggetto \_ VirtualSystemMigrationCapabilities di MSVM** è associato a oggetti [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="ca89f-105">The **Msvm\_VirtualSystemMigrationCapabilities** object is associated with [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) objects.</span></span> <span data-ttu-id="ca89f-106">Queste associazioni definiscono la gamma valida di servizi di migrazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="ca89f-106">These associations define the valid range of migration services available.</span></span>

<span data-ttu-id="ca89f-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ca89f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca89f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca89f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationCapabilities : CIM_VirtualSystemMigrationCapabilities
{
  string InstanceID;
  string Caption = "Migration Capabilities";
  string Description = "Virtual System Migration Capabilities";
  string ElementName;
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="ca89f-109">Members</span><span class="sxs-lookup"><span data-stu-id="ca89f-109">Members</span></span>

<span data-ttu-id="ca89f-110">La **classe \_ VirtualSystemMigrationCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ca89f-110">The **Msvm\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="ca89f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca89f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca89f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca89f-112">Properties</span></span>

<span data-ttu-id="ca89f-113">La **classe \_ VirtualSystemMigrationCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca89f-113">The **Msvm\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca89f-114">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="ca89f-114">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca89f-115">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca89f-115">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca89f-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-117">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="ca89f-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="ca89f-118">Identifica i metodi la cui implementazione può essere asincrona. ovvero l'operazione non verrà completata immediatamente e restituirà un processo.</span><span class="sxs-lookup"><span data-stu-id="ca89f-118">Identifies the methods whose implementation may be asynchronous; that is, the operation will not be completed immediately and will return a job.</span></span> <span data-ttu-id="ca89f-119">Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="ca89f-119">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="ca89f-120">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="ca89f-120">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="ca89f-121">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="ca89f-121">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableSupported"></span><span id="checkvirtualsystemismigratablesupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLESUPPORTED"></span>

<span data-ttu-id="ca89f-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span><span class="sxs-lookup"><span data-stu-id="ca89f-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca89f-123">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ca89f-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca89f-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca89f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca89f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca89f-126">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca89f-126">A short description of the object.</span></span> <span data-ttu-id="ca89f-127">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "funzionalità di migrazione".</span><span class="sxs-lookup"><span data-stu-id="ca89f-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ca89f-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ca89f-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca89f-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca89f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca89f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca89f-131">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="ca89f-131">A description of the object.</span></span> <span data-ttu-id="ca89f-132">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "funzionalità di migrazione del sistema virtuale".</span><span class="sxs-lookup"><span data-stu-id="ca89f-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual System Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ca89f-133">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="ca89f-133">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca89f-134">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca89f-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca89f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca89f-136">Matrice di formati dei nomi supportati per il parametro *DestinationHost* dei metodi [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) e [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ca89f-136">An array of name formats that are supported for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) and [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) methods.</span></span> <span data-ttu-id="ca89f-137">Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="ca89f-137">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>



| <span data-ttu-id="ca89f-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ca89f-138">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="ca89f-139">Significato</span><span class="sxs-lookup"><span data-stu-id="ca89f-139">Meaning</span></span>                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span><dl> <span data-ttu-id="ca89f-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ca89f-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="ca89f-141">Supporto del formato del nome di dominio in base allo standard RFC 10353.</span><span class="sxs-lookup"><span data-stu-id="ca89f-141">Support of the domain name format according to RFC 10353.</span></span><br/>         |
| <span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span><dl> <span data-ttu-id="ca89f-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ca89f-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="ca89f-143">Supporto del formato decimale punteggiato IPv4 in base allo standard RFC 12084.</span><span class="sxs-lookup"><span data-stu-id="ca89f-143">Support of the IPv4 dotted decimal format according to RFC 12084.</span></span><br/> |
| <span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span><dl> <span data-ttu-id="ca89f-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ca89f-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="ca89f-145">Supporto del formato di testo IPv6 in base allo standard RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="ca89f-145">Support of the IPv6 text format according to RFC 4291.</span></span><br/>            |



 

</dd> <dt>

<span data-ttu-id="ca89f-146">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ca89f-146">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca89f-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca89f-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca89f-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca89f-149">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca89f-149">A display name for the object.</span></span> <span data-ttu-id="ca89f-150">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca89f-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca89f-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ca89f-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca89f-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ca89f-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca89f-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-154">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="ca89f-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ca89f-155">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="ca89f-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ca89f-156">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca89f-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca89f-157">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="ca89f-157">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca89f-158">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca89f-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca89f-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca89f-160">Identifica i metodi la cui implementazione può essere sincrona. ovvero, l'operazione verrà completata immediatamente e non verrà restituito alcun processo.</span><span class="sxs-lookup"><span data-stu-id="ca89f-160">Identifies the methods whose implementation may be synchronous; that is, the operation will be completed immediately and will not return a job.</span></span> <span data-ttu-id="ca89f-161">Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="ca89f-161">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="ca89f-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="ca89f-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="ca89f-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="ca89f-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="ca89f-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ca89f-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="ca89f-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="ca89f-167">)</span><span class="sxs-lookup"><span data-stu-id="ca89f-167">)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca89f-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca89f-168">Requirements</span></span>



| <span data-ttu-id="ca89f-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca89f-169">Requirement</span></span> | <span data-ttu-id="ca89f-170">Valore</span><span class="sxs-lookup"><span data-stu-id="ca89f-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca89f-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca89f-171">Minimum supported client</span></span><br/> | <span data-ttu-id="ca89f-172">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ca89f-172">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ca89f-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca89f-173">Minimum supported server</span></span><br/> | <span data-ttu-id="ca89f-174">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ca89f-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca89f-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca89f-175">Namespace</span></span><br/>                | <span data-ttu-id="ca89f-176">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ca89f-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ca89f-177">MOF</span><span class="sxs-lookup"><span data-stu-id="ca89f-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca89f-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca89f-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca89f-179">DLL</span><span class="sxs-lookup"><span data-stu-id="ca89f-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca89f-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca89f-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

