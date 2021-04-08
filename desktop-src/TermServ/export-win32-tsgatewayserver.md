---
title: Metodo Export della classe Win32_TSGatewayServer
description: Restituisce la configurazione del server Gateway Desktop remoto (Gateway Desktop remoto) come stringa XML.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Esporta il metodo Servizi Desktop remoto
- Metodo Export Servizi Desktop remoto, classe Win32_TSGatewayServer
- Classe Win32_TSGatewayServer Servizi Desktop remoto, metodo Export
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964982"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="322c6-106">Metodo Export della classe Win32 \_ TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="322c6-106">Export method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="322c6-107">Restituisce la configurazione del server Gateway Desktop remoto (Gateway Desktop remoto) come stringa XML.</span><span class="sxs-lookup"><span data-stu-id="322c6-107">Returns the Remote Desktop Gateway (RD Gateway) server configuration as an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="322c6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="322c6-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a><span data-ttu-id="322c6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="322c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="322c6-110">*ExportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="322c6-110">*ExportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="322c6-111">Contenuto da esportare.</span><span class="sxs-lookup"><span data-stu-id="322c6-111">The content to export.</span></span> <span data-ttu-id="322c6-112">Impostare il tipo di esportazione impostando i bit corrispondenti nel parametro *ExportType* .</span><span class="sxs-lookup"><span data-stu-id="322c6-112">Set the export type by setting the corresponding bits in the *ExportType* parameter.</span></span> <span data-ttu-id="322c6-113">È possibile impostare più tipi di esportazione.</span><span class="sxs-lookup"><span data-stu-id="322c6-113">You can set multiple export types.</span></span> <span data-ttu-id="322c6-114">Se, ad esempio, è impostato il bit 0, verranno esportati Servizi Desktop remoto i criteri di autorizzazione della connessione.</span><span class="sxs-lookup"><span data-stu-id="322c6-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be exported.</span></span> <span data-ttu-id="322c6-115">Se è impostato sia il bit 0 che il secondo bit, verranno esportati sia i criteri di autorizzazione connessioni Desktop remoto che i criteri di autorizzazione risorse Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="322c6-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be exported.</span></span>

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span data-ttu-id="322c6-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Esporta tutti i limiti** (1)</span><span class="sxs-lookup"><span data-stu-id="322c6-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Export all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="322c6-117">Esporta tutti i tappi desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="322c6-117">Export all RD CAPs.</span></span>

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="322c6-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Esporta tutti i server RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="322c6-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Export all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="322c6-119">Esportare un elenco di tutti i server dei criteri di rete (NPS).</span><span class="sxs-lookup"><span data-stu-id="322c6-119">Export a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span data-ttu-id="322c6-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Esporta tutti i rap** (4)</span><span class="sxs-lookup"><span data-stu-id="322c6-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Export all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="322c6-121">Esporta tutti i rap RD.</span><span class="sxs-lookup"><span data-stu-id="322c6-121">Export all RD RAPs.</span></span>

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span data-ttu-id="322c6-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Esporta tutti i RGS** (8)</span><span class="sxs-lookup"><span data-stu-id="322c6-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Export all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="322c6-123">Esportare tutti i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="322c6-123">Export all resource groups.</span></span>

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="322c6-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Esporta tutti i Server Loadbalancing** (16)</span><span class="sxs-lookup"><span data-stu-id="322c6-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Export all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="322c6-125">Esportare un elenco di tutti i server di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="322c6-125">Export a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="322c6-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Esporta tutte le impostazioni del server** (32)</span><span class="sxs-lookup"><span data-stu-id="322c6-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Export all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="322c6-127">Esportare tutte le impostazioni del server correlate a Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="322c6-127">Export all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="322c6-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Esporta tutti i criteri di integrità** (64)</span><span class="sxs-lookup"><span data-stu-id="322c6-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Export all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="322c6-129">Esportare tutti i criteri di integrità.</span><span class="sxs-lookup"><span data-stu-id="322c6-129">Export all health policies.</span></span>

<span data-ttu-id="322c6-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="322c6-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="322c6-131">Questo valore non è supportato prima di Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="322c6-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="322c6-132">*XmlString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="322c6-132">*XmlString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="322c6-133">Stringa dell'XML.</span><span class="sxs-lookup"><span data-stu-id="322c6-133">The XML string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="322c6-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="322c6-134">Remarks</span></span>

<span data-ttu-id="322c6-135">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="322c6-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="322c6-136">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="322c6-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="322c6-137">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="322c6-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="322c6-138">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="322c6-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="322c6-139">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="322c6-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="322c6-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="322c6-140">Requirements</span></span>



| <span data-ttu-id="322c6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="322c6-141">Requirement</span></span> | <span data-ttu-id="322c6-142">Valore</span><span class="sxs-lookup"><span data-stu-id="322c6-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="322c6-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="322c6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="322c6-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="322c6-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="322c6-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="322c6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="322c6-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="322c6-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="322c6-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="322c6-147">Namespace</span></span><br/>                | <span data-ttu-id="322c6-148">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="322c6-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="322c6-149">MOF</span><span class="sxs-lookup"><span data-stu-id="322c6-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="322c6-150"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="322c6-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="322c6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="322c6-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="322c6-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="322c6-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="322c6-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="322c6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="322c6-154">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="322c6-154">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

