---
description: Rappresenta le funzionalità di un \_ oggetto VIRTUALSYSTEMMIGRATIONSERVICE CIM.
ms.assetid: 5fe3a10b-c075-4c45-838d-0b5c2e491584
title: Classe CIM_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationCapabilities
- CIM_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a9a9a0a0f8e9ea344c7a37ad1168dcb5e059093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528896"
---
# <a name="cim_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="1d553-103">CIM \_ VirtualSystemMigrationCapabilities (classe)</span><span class="sxs-lookup"><span data-stu-id="1d553-103">CIM\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="1d553-104">Rappresenta le funzionalità di un [**oggetto \_ VirtualSystemMigrationService CIM**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1d553-104">Represents the capabilities of a [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d553-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d553-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationCapabilities : CIM_Capabilities
{
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="1d553-106">Members</span><span class="sxs-lookup"><span data-stu-id="1d553-106">Members</span></span>

<span data-ttu-id="1d553-107">La classe **CIM \_ VirtualSystemMigrationCapabilities** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1d553-107">The **CIM\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="1d553-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d553-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d553-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d553-109">Properties</span></span>

<span data-ttu-id="1d553-110">La classe **CIM \_ VirtualSystemMigrationCapabilities** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d553-110">The **CIM\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d553-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="1d553-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d553-112">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d553-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d553-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d553-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d553-114">Matrice che indica i metodi [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) supportati per le operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="1d553-114">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="1d553-115">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="1d553-115">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="1d553-116">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="1d553-116">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1d553-117">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1d553-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d553-118">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="1d553-118">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d553-119">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d553-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d553-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d553-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d553-121">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost (DestinationHost)**","**CIM \_ VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost (DestinationHost)**")</span><span class="sxs-lookup"><span data-stu-id="1d553-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost(DestinationHost)**", "**CIM\_VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost(DestinationHost)**")</span></span>
</dt> </dl>

<span data-ttu-id="1d553-122">Matrice che contiene i formati supportati per il parametro *DestinationHost* dei metodi [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) e [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) per l'oggetto [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1d553-122">An array that contains the supported formats for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) and [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) methods for the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

<dt>

<span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>

<span data-ttu-id="1d553-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="1d553-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1d553-124">Supporto del formato del testo del nome di dominio in base allo standard RFC 1035.</span><span class="sxs-lookup"><span data-stu-id="1d553-124">Support of the Domain Name text format according to RFC 1035.</span></span>

</dd> <dt>

<span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>

<span data-ttu-id="1d553-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="1d553-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d553-126">Supporto del formato decimale punteggiato IPv4 in base allo standard RFC 1208.</span><span class="sxs-lookup"><span data-stu-id="1d553-126">Support of the IPv4 dotted decimal format according to RFC 1208.</span></span>

</dd> <dt>

<span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>

<span data-ttu-id="1d553-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="1d553-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1d553-128">Supporto del formato di testo IPv6 in base allo standard RFC 4291</span><span class="sxs-lookup"><span data-stu-id="1d553-128">Support of the IPv6 text format according to RFC 4291</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1d553-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1d553-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d553-130">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="1d553-130">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d553-131">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d553-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d553-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d553-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d553-133">Matrice che indica i metodi [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) supportati per le operazioni sincrone.</span><span class="sxs-lookup"><span data-stu-id="1d553-133">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for synchronous operations.</span></span>

<span data-ttu-id="1d553-134">Enumerazione degli identificatori di metodo la cui implementazione può essere sincrona. ovvero, l'operazione può essere completata immediatamente e pertanto il metodo non può restituire un processo.</span><span class="sxs-lookup"><span data-stu-id="1d553-134">Enumeration of method identifiers whose implementation may be synchronous; that is, the operation may complete immediately and therefore the method may not return a job.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="1d553-135">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="1d553-135">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="1d553-136">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="1d553-136">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>

<span data-ttu-id="1d553-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="1d553-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>

<span data-ttu-id="1d553-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="1d553-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1d553-139">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1d553-139">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="1d553-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1d553-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1d553-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d553-141">Requirements</span></span>



| <span data-ttu-id="1d553-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d553-142">Requirement</span></span> | <span data-ttu-id="1d553-143">Valore</span><span class="sxs-lookup"><span data-stu-id="1d553-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d553-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d553-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1d553-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1d553-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1d553-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d553-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1d553-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d553-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1d553-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d553-148">Namespace</span></span><br/>                | <span data-ttu-id="1d553-149">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1d553-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1d553-150">MOF</span><span class="sxs-lookup"><span data-stu-id="1d553-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d553-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d553-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d553-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1d553-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d553-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d553-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1d553-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d553-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d553-155">**\_Funzionalità CIM**</span><span class="sxs-lookup"><span data-stu-id="1d553-155">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

