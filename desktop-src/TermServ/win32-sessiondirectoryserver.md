---
title: Classe Win32_SessionDirectoryServer
description: Fornisce le proprietà per la visualizzazione delle proprietà di un server Gestore connessione Desktop remoto (Connessione Desktop remoto Broker).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionDirectoryServer Servizi Desktop remoto
- Classe Win32_SessionDirectoryServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964077"
---
# <a name="win32_sessiondirectoryserver-class"></a><span data-ttu-id="636a7-105">Win32 \_ SessionDirectoryServer (classe)</span><span class="sxs-lookup"><span data-stu-id="636a7-105">Win32\_SessionDirectoryServer class</span></span>

<span data-ttu-id="636a7-106">Fornisce le proprietà per la visualizzazione delle proprietà di un server Gestore connessione Desktop remoto (Connessione Desktop remoto Broker).</span><span class="sxs-lookup"><span data-stu-id="636a7-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) server.</span></span>

> [!Note]  
> <span data-ttu-id="636a7-107">In Windows Server 2008 R2 il nome di gestore sessioni Servizi terminal è stato modificato in Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="636a7-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="636a7-108">Queste proprietà si applicano a tutti i sistemi operativi supportati se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="636a7-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="636a7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="636a7-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a><span data-ttu-id="636a7-110">Members</span><span class="sxs-lookup"><span data-stu-id="636a7-110">Members</span></span>

<span data-ttu-id="636a7-111">La classe **Win32 \_ SessionDirectoryServer** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="636a7-111">The **Win32\_SessionDirectoryServer** class has these types of members:</span></span>

-   [<span data-ttu-id="636a7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="636a7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="636a7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="636a7-113">Properties</span></span>

<span data-ttu-id="636a7-114">La classe **Win32 \_ SessionDirectoryServer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="636a7-114">The **Win32\_SessionDirectoryServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="636a7-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="636a7-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="636a7-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="636a7-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="636a7-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="636a7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="636a7-118">Nome della farm che include il server.</span><span class="sxs-lookup"><span data-stu-id="636a7-118">Name of the farm that includes the server.</span></span>

</dd> <dt>

<span data-ttu-id="636a7-119">**LoadIndicator**</span><span class="sxs-lookup"><span data-stu-id="636a7-119">**LoadIndicator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="636a7-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="636a7-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="636a7-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="636a7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="636a7-122">Numero relativo che rappresenta il carico del server Host sessione Desktop remoto quando viene utilizzato l'algoritmo di bilanciamento del carico predefinito.</span><span class="sxs-lookup"><span data-stu-id="636a7-122">A relative number that represents the RD Session Host server load when the default load-balancing algorithm is used.</span></span> <span data-ttu-id="636a7-123">Il valore della proprietà *LoadIndicator* è basato sul numero di sessioni, sul numero di richieste di reindirizzamento in sospeso e sul valore del peso del server.</span><span class="sxs-lookup"><span data-stu-id="636a7-123">The *LoadIndicator* property value is based on the number of sessions, the number of pending redirection requests, and the server weight value.</span></span>

</dd> <dt>

<span data-ttu-id="636a7-124">**NumberOfSessions**</span><span class="sxs-lookup"><span data-stu-id="636a7-124">**NumberOfSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="636a7-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="636a7-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="636a7-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="636a7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="636a7-127">Numero di sessioni nel server Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="636a7-127">Number of sessions in the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="636a7-128">**NumPendRedir**</span><span class="sxs-lookup"><span data-stu-id="636a7-128">**NumPendRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="636a7-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="636a7-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="636a7-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="636a7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="636a7-131">Numero di richieste di reindirizzamento in sospeso.</span><span class="sxs-lookup"><span data-stu-id="636a7-131">Number of pending redirection requests.</span></span>

</dd> <dt>

<span data-ttu-id="636a7-132">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="636a7-132">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="636a7-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="636a7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="636a7-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="636a7-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="636a7-135">Indirizzo IP del server Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="636a7-135">IP address of the RD Connection Broker server.</span></span> <span data-ttu-id="636a7-136">Se il server è configurato per gli indirizzi IPv4 e IPv6, questo conterrà l'indirizzo IPv4.</span><span class="sxs-lookup"><span data-stu-id="636a7-136">If the server is configured for both IPv4 and IPv6 addresses, this will contain the IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="636a7-137">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="636a7-137">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="636a7-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="636a7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="636a7-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="636a7-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="636a7-140">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="636a7-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="636a7-141">Nome del server Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="636a7-141">Name of the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="636a7-142">**ServerWeight**</span><span class="sxs-lookup"><span data-stu-id="636a7-142">**ServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="636a7-143">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="636a7-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="636a7-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="636a7-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="636a7-145">Valore del peso del server, usato per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="636a7-145">Server weight value, used in load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="636a7-146">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="636a7-146">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="636a7-147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="636a7-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="636a7-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="636a7-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="636a7-149">Impostazione della modalità sessione singola del server Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="636a7-149">Single session mode setting of the RD Connection Broker server.</span></span>

<dt>

<span data-ttu-id="636a7-150">0</span><span class="sxs-lookup"><span data-stu-id="636a7-150">0</span></span>
</dt> <dd>

<span data-ttu-id="636a7-151">La farm non è in modalità sessione singola.</span><span class="sxs-lookup"><span data-stu-id="636a7-151">The farm is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="636a7-152">1</span><span class="sxs-lookup"><span data-stu-id="636a7-152">1</span></span>
</dt> <dd>

<span data-ttu-id="636a7-153">La farm in è in modalità sessione singola.</span><span class="sxs-lookup"><span data-stu-id="636a7-153">The farm in is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="636a7-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="636a7-154">Remarks</span></span>

<span data-ttu-id="636a7-155">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="636a7-155">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="636a7-156">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="636a7-156">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="636a7-157">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="636a7-157">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="636a7-158">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="636a7-158">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="636a7-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="636a7-159">Requirements</span></span>



| <span data-ttu-id="636a7-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="636a7-160">Requirement</span></span> | <span data-ttu-id="636a7-161">Valore</span><span class="sxs-lookup"><span data-stu-id="636a7-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="636a7-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="636a7-162">Minimum supported client</span></span><br/> | <span data-ttu-id="636a7-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="636a7-163">None supported</span></span><br/>                                                              |
| <span data-ttu-id="636a7-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="636a7-164">Minimum supported server</span></span><br/> | <span data-ttu-id="636a7-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="636a7-165">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="636a7-166">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="636a7-166">Namespace</span></span><br/>                | <span data-ttu-id="636a7-167">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="636a7-167">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="636a7-168">MOF</span><span class="sxs-lookup"><span data-stu-id="636a7-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="636a7-169"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="636a7-169"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="636a7-170">DLL</span><span class="sxs-lookup"><span data-stu-id="636a7-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="636a7-171"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="636a7-171"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="636a7-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="636a7-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636a7-173">**\_SessionDirectoryCluster Win32**</span><span class="sxs-lookup"><span data-stu-id="636a7-173">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="636a7-174">**\_SessionDirectorySession Win32**</span><span class="sxs-lookup"><span data-stu-id="636a7-174">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

