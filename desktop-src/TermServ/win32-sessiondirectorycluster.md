---
title: Classe Win32_SessionDirectoryCluster
description: Fornisce le proprietà per la visualizzazione delle proprietà di una farm in Connessione Desktop remoto broker (gestore connessione Desktop remoto).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionDirectoryCluster Servizi Desktop remoto
- Classe Win32_SessionDirectoryCluster Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476204"
---
# <a name="win32_sessiondirectorycluster-class"></a><span data-ttu-id="09075-105">Win32 \_ SessionDirectoryCluster (classe)</span><span class="sxs-lookup"><span data-stu-id="09075-105">Win32\_SessionDirectoryCluster class</span></span>

<span data-ttu-id="09075-106">Fornisce le proprietà per la visualizzazione delle proprietà di una farm in Connessione Desktop remoto broker (gestore connessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="09075-106">Provides properties for viewing the properties of a farm in Remote Desktop Connection Broker (RD Connection Broker).</span></span>

> [!Note]  
> <span data-ttu-id="09075-107">In Windows Server 2008 R2 il nome di gestore sessioni Servizi terminal è stato modificato in Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="09075-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="09075-108">Queste proprietà si applicano a tutti i sistemi operativi supportati se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="09075-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="09075-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09075-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a><span data-ttu-id="09075-110">Members</span><span class="sxs-lookup"><span data-stu-id="09075-110">Members</span></span>

<span data-ttu-id="09075-111">La classe **Win32 \_ SessionDirectoryCluster** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="09075-111">The **Win32\_SessionDirectoryCluster** class has these types of members:</span></span>

-   [<span data-ttu-id="09075-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="09075-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09075-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="09075-113">Properties</span></span>

<span data-ttu-id="09075-114">La classe **Win32 \_ SessionDirectoryCluster** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="09075-114">The **Win32\_SessionDirectoryCluster** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09075-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="09075-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09075-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09075-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09075-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09075-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09075-118">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09075-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="09075-119">Nome della farm in Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="09075-119">Name of the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="09075-120">**NumberOfServers**</span><span class="sxs-lookup"><span data-stu-id="09075-120">**NumberOfServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09075-121">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09075-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09075-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09075-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09075-123">Numero di server nella farm in Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="09075-123">Number of servers in the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="09075-124">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="09075-124">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09075-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09075-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09075-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09075-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09075-127">Modalità a sessione singola della farm in Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="09075-127">Single session mode of the farm in RD Connection Broker.</span></span>

<dt>

<span data-ttu-id="09075-128">0</span><span class="sxs-lookup"><span data-stu-id="09075-128">0</span></span>
</dt> <dd>

<span data-ttu-id="09075-129">La farm in Gestore connessione Desktop remoto non è in modalità sessione singola.</span><span class="sxs-lookup"><span data-stu-id="09075-129">The farm in RD Connection Broker is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="09075-130">1</span><span class="sxs-lookup"><span data-stu-id="09075-130">1</span></span>
</dt> <dd>

<span data-ttu-id="09075-131">La farm in Gestore connessione Desktop remoto è in modalità sessione singola.</span><span class="sxs-lookup"><span data-stu-id="09075-131">The farm in RD Connection Broker is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09075-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="09075-132">Remarks</span></span>

<span data-ttu-id="09075-133">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="09075-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="09075-134">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="09075-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="09075-135">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="09075-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="09075-136">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="09075-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="09075-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09075-137">Requirements</span></span>



| <span data-ttu-id="09075-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="09075-138">Requirement</span></span> | <span data-ttu-id="09075-139">Valore</span><span class="sxs-lookup"><span data-stu-id="09075-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09075-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09075-140">Minimum supported client</span></span><br/> | <span data-ttu-id="09075-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="09075-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="09075-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09075-142">Minimum supported server</span></span><br/> | <span data-ttu-id="09075-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09075-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="09075-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="09075-144">Namespace</span></span><br/>                | <span data-ttu-id="09075-145">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="09075-145">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="09075-146">MOF</span><span class="sxs-lookup"><span data-stu-id="09075-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09075-147"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09075-147"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="09075-148">DLL</span><span class="sxs-lookup"><span data-stu-id="09075-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09075-149"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09075-149"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09075-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09075-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09075-151">**\_SessionDirectoryServer Win32**</span><span class="sxs-lookup"><span data-stu-id="09075-151">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> <dt>

[<span data-ttu-id="09075-152">**\_SessionDirectorySession Win32**</span><span class="sxs-lookup"><span data-stu-id="09075-152">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

