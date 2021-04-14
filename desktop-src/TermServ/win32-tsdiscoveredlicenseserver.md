---
title: Classe Win32_TSDiscoveredLicenseServer
description: Fornisce informazioni dettagliate sul server licenze Desktop remoto individuato.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSDiscoveredLicenseServer Servizi Desktop remoto
- Classe Win32_TSDiscoveredLicenseServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478826"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a><span data-ttu-id="5f577-105">Win32 \_ TSDiscoveredLicenseServer (classe)</span><span class="sxs-lookup"><span data-stu-id="5f577-105">Win32\_TSDiscoveredLicenseServer class</span></span>

<span data-ttu-id="5f577-106">Fornisce informazioni dettagliate sul server licenze Desktop remoto individuato.</span><span class="sxs-lookup"><span data-stu-id="5f577-106">Provides details about the discovered Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f577-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f577-107">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a><span data-ttu-id="5f577-108">Members</span><span class="sxs-lookup"><span data-stu-id="5f577-108">Members</span></span>

<span data-ttu-id="5f577-109">La classe **Win32 \_ TSDiscoveredLicenseServer** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5f577-109">The **Win32\_TSDiscoveredLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="5f577-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5f577-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f577-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5f577-111">Properties</span></span>

<span data-ttu-id="5f577-112">La classe **Win32 \_ TSDiscoveredLicenseServer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5f577-112">The **Win32\_TSDiscoveredLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f577-113">**HowDiscovered**</span><span class="sxs-lookup"><span data-stu-id="5f577-113">**HowDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f577-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f577-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f577-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5f577-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f577-116">Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f577-116">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f577-117">Questa proprietà non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="5f577-117">This property is no longer supported.</span></span>

<span data-ttu-id="5f577-118">**Windows Server 2008:** Metodo di individuazione del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5f577-118">**Windows Server 2008:** The Remote Desktop license server discovery method.</span></span>

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span data-ttu-id="5f577-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span><span class="sxs-lookup"><span data-stu-id="5f577-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-120">Il server licenze è stato individuato tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5f577-120">The license server was discovered by using group policy.</span></span>

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span data-ttu-id="5f577-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span><span class="sxs-lookup"><span data-stu-id="5f577-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-122">Il server licenze è stato individuato tramite un'impostazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5f577-122">The license server was discovered by using a registry setting.</span></span>

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span data-ttu-id="5f577-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span><span class="sxs-lookup"><span data-stu-id="5f577-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-124">Il server licenze è stato individuato utilizzando l'ambito di individuazione del gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5f577-124">The license server was discovered by using the workgroup discovery scope.</span></span>

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span data-ttu-id="5f577-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span><span class="sxs-lookup"><span data-stu-id="5f577-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-126">Il server licenze è stato individuato utilizzando l'ambito di individuazione dominio.</span><span class="sxs-lookup"><span data-stu-id="5f577-126">The license server was discovered by using the domain discovery scope.</span></span>

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span data-ttu-id="5f577-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span><span class="sxs-lookup"><span data-stu-id="5f577-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-128">Il server licenze è stato individuato utilizzando l'ambito di individuazione foresta.</span><span class="sxs-lookup"><span data-stu-id="5f577-128">The license server was discovered by using the forest discovery scope.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f577-129">**IsAdminOnLS**</span><span class="sxs-lookup"><span data-stu-id="5f577-129">**IsAdminOnLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f577-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f577-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f577-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5f577-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f577-132">Indica se l'account utilizzato per eseguire lo script o il file exe che utilizza la classe **Win32 \_ TSDiscoveredLicenseServer** dispone dell'accesso di amministratore al server licenze.</span><span class="sxs-lookup"><span data-stu-id="5f577-132">Indicates whether the account that is being used to run the script or .exe file that is using the **Win32\_TSDiscoveredLicenseServer** class has administrator access to the license server.</span></span>

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span data-ttu-id="5f577-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)</span><span class="sxs-lookup"><span data-stu-id="5f577-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-134">L'account utilizzato non dispone dell'accesso di amministratore al server licenze.</span><span class="sxs-lookup"><span data-stu-id="5f577-134">The account that is being used does not have administrator access to the license server.</span></span>

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span data-ttu-id="5f577-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Sì** (1)</span><span class="sxs-lookup"><span data-stu-id="5f577-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Yes** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-136">L'account utilizzato dispone di accesso amministrativo al server licenze.</span><span class="sxs-lookup"><span data-stu-id="5f577-136">The account that is being used has administrator access to the license server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="5f577-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Non **so** (2)</span><span class="sxs-lookup"><span data-stu-id="5f577-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-138">Non è possibile determinare se l'account utilizzato dispone di accesso amministrativo al server licenze.</span><span class="sxs-lookup"><span data-stu-id="5f577-138">It cannot be determined whether the account that is being used has administrator access to the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f577-139">**IsLSAvailable**</span><span class="sxs-lookup"><span data-stu-id="5f577-139">**IsLSAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f577-140">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f577-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f577-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5f577-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f577-142">Indica se il server licenze è disponibile, ovvero se è possibile stabilire \[ una \] connessione RPC al server.</span><span class="sxs-lookup"><span data-stu-id="5f577-142">Indicates whether the license server is available (whether a remote procedure call \[RPC\] connection can be made to the server).</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="5f577-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="5f577-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-144">Il server licenze non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="5f577-144">The license server is not available.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="5f577-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="5f577-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-146">Il server licenze è disponibile.</span><span class="sxs-lookup"><span data-stu-id="5f577-146">The license server is available.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f577-147">**IssuingCALs**</span><span class="sxs-lookup"><span data-stu-id="5f577-147">**IssuingCALs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f577-148">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f577-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f577-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5f577-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f577-150">Indica se il server licenze è autorizzato a emettere le licenze CAL (Client Access License) di Servizi Desktop remoto al server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5f577-150">Indicates whether the license server is allowed to issue Remote Desktop Services client access licenses (RDS CALs) to the RD Session Host server.</span></span>

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="5f577-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Non consentito** (0)</span><span class="sxs-lookup"><span data-stu-id="5f577-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not Allowed** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-152">Il server licenze non è autorizzato ad emettere licenze CAL Servizi Desktop remoto per il server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5f577-152">The license server is not allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span data-ttu-id="5f577-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Consentito** (1)</span><span class="sxs-lookup"><span data-stu-id="5f577-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Allowed** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-154">Il server licenze può emettere licenze CAL Servizi Desktop remoto per il server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5f577-154">The license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="5f577-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Non **so** (2)</span><span class="sxs-lookup"><span data-stu-id="5f577-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5f577-156">Non è possibile determinare se il server licenze è autorizzato a rilasciare licenze CAL Servizi Desktop remoto al server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5f577-156">It cannot be determined whether the license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f577-157">**LicenseServer**</span><span class="sxs-lookup"><span data-stu-id="5f577-157">**LicenseServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f577-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5f577-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f577-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5f577-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f577-160">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f577-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f577-161">Nome del server licenze Desktop remoto individuato.</span><span class="sxs-lookup"><span data-stu-id="5f577-161">Name of the discovered Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f577-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f577-162">Remarks</span></span>

<span data-ttu-id="5f577-163">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5f577-163">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="5f577-164">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="5f577-164">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="5f577-165">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="5f577-165">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="5f577-166">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5f577-166">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="5f577-167">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5f577-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5f577-168">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5f577-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5f577-169">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="5f577-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5f577-170">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5f577-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f577-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f577-171">Requirements</span></span>



| <span data-ttu-id="5f577-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f577-172">Requirement</span></span> | <span data-ttu-id="5f577-173">Valore</span><span class="sxs-lookup"><span data-stu-id="5f577-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f577-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f577-174">Minimum supported client</span></span><br/> | <span data-ttu-id="5f577-175">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5f577-175">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5f577-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f577-176">Minimum supported server</span></span><br/> | <span data-ttu-id="5f577-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f577-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f577-178">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5f577-178">Namespace</span></span><br/>                | <span data-ttu-id="5f577-179">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5f577-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5f577-180">MOF</span><span class="sxs-lookup"><span data-stu-id="5f577-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f577-181"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f577-181"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f577-182">DLL</span><span class="sxs-lookup"><span data-stu-id="5f577-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f577-183"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f577-183"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

