---
title: Metodo di importazione della classe Win32_TSGatewayServer
description: Importa una determinata configurazione nel server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo di importazione
- Servizi Desktop remoto metodo di importazione, classe Win32_TSGatewayServer
- Classe Win32_TSGatewayServer Servizi Desktop remoto, metodo Import
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964430"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="40553-106">Metodo Import della classe Win32 \_ TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="40553-106">Import method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="40553-107">Importa una determinata configurazione nel server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="40553-107">Imports a given configuration to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="40553-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40553-108">Syntax</span></span>


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a><span data-ttu-id="40553-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="40553-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40553-110">*ImportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40553-110">*ImportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40553-111">Contenuto da importare.</span><span class="sxs-lookup"><span data-stu-id="40553-111">The content to import.</span></span> <span data-ttu-id="40553-112">Impostare il tipo di importazione impostando i bit corrispondenti nel parametro *ImportType* .</span><span class="sxs-lookup"><span data-stu-id="40553-112">Set the import type by setting the corresponding bits in the *ImportType* parameter.</span></span> <span data-ttu-id="40553-113">È possibile impostare più tipi di importazione.</span><span class="sxs-lookup"><span data-stu-id="40553-113">You can set multiple import types.</span></span> <span data-ttu-id="40553-114">Se, ad esempio, è impostato il bit 0, verranno importati Servizi Desktop remoto i criteri di autorizzazione della connessione.</span><span class="sxs-lookup"><span data-stu-id="40553-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be imported.</span></span> <span data-ttu-id="40553-115">Se è impostato sia il bit 0 che il secondo bit, verranno importati sia i criteri di autorizzazione connessioni Desktop remoto che i criteri di autorizzazione risorse Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="40553-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be imported.</span></span>

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span data-ttu-id="40553-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importa tutti i Caps** (1)</span><span class="sxs-lookup"><span data-stu-id="40553-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Import all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="40553-117">Importa tutti i tappi desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="40553-117">Import all RD CAPs.</span></span>

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="40553-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importa tutti i server RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="40553-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Import all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="40553-119">Importare un elenco di tutti i server dei criteri di rete (NPS).</span><span class="sxs-lookup"><span data-stu-id="40553-119">Import a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span data-ttu-id="40553-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importa tutti i rap** (4)</span><span class="sxs-lookup"><span data-stu-id="40553-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Import all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="40553-121">Importa tutti i rap RD.</span><span class="sxs-lookup"><span data-stu-id="40553-121">Import all RD RAPs.</span></span>

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span data-ttu-id="40553-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importa tutti i RGS** (8)</span><span class="sxs-lookup"><span data-stu-id="40553-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Import all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="40553-123">Importare tutti i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="40553-123">Import all resource groups.</span></span>

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="40553-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importa tutti i Server Loadbalancing** (16)</span><span class="sxs-lookup"><span data-stu-id="40553-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Import all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="40553-125">Importare un elenco di tutti i server di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="40553-125">Import a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="40553-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importa tutte le impostazioni del server** (32)</span><span class="sxs-lookup"><span data-stu-id="40553-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Import all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="40553-127">Importa tutte le impostazioni del server correlate a Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="40553-127">Import all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="40553-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importa tutti i criteri di integrità** (64)</span><span class="sxs-lookup"><span data-stu-id="40553-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Import all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="40553-129">Importa tutti i criteri di integrità.</span><span class="sxs-lookup"><span data-stu-id="40553-129">Import all health policies.</span></span>

<span data-ttu-id="40553-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="40553-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="40553-131">Questo valore non è supportato prima di Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="40553-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="40553-132">*XmlString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40553-132">*XmlString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40553-133">Configurazione come stringa XML.</span><span class="sxs-lookup"><span data-stu-id="40553-133">The configuration as an XML string.</span></span>

</dd> <dt>

<span data-ttu-id="40553-134">*MergeOrReplace* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40553-134">*MergeOrReplace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40553-135">Indica se unire o sostituire i dati quando si verifica un conflitto.</span><span class="sxs-lookup"><span data-stu-id="40553-135">Indicates whether to merge or replace data when a conflict occurs.</span></span>

> [!Note]  
> <span data-ttu-id="40553-136">Merge non ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="40553-136">Merge is not yet implemented.</span></span> <span data-ttu-id="40553-137">Pertanto, il valore di questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="40553-137">Therefore, this parameter value is ignored.</span></span>

 

</dd> <dt>

<span data-ttu-id="40553-138">*LogString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="40553-138">*LogString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40553-139">Informazioni del log generate durante l'operazione di importazione.</span><span class="sxs-lookup"><span data-stu-id="40553-139">The log information that is generated during the import operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40553-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="40553-140">Remarks</span></span>

<span data-ttu-id="40553-141">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="40553-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="40553-142">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="40553-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="40553-143">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="40553-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="40553-144">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="40553-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="40553-145">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="40553-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="40553-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40553-146">Requirements</span></span>



| <span data-ttu-id="40553-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="40553-147">Requirement</span></span> | <span data-ttu-id="40553-148">Valore</span><span class="sxs-lookup"><span data-stu-id="40553-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="40553-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40553-149">Minimum supported client</span></span><br/> | <span data-ttu-id="40553-150">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="40553-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="40553-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40553-151">Minimum supported server</span></span><br/> | <span data-ttu-id="40553-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40553-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="40553-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="40553-153">Namespace</span></span><br/>                | <span data-ttu-id="40553-154">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="40553-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="40553-155">MOF</span><span class="sxs-lookup"><span data-stu-id="40553-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40553-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40553-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="40553-157">DLL</span><span class="sxs-lookup"><span data-stu-id="40553-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40553-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40553-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="40553-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40553-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40553-160">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="40553-160">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

