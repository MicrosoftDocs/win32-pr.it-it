---
title: Classe MDM_Policy_Result01_Connectivity02
description: La \_ \_ classe Result01 Connectivity02 dei criteri MDM \_ rappresenta i criteri di connessione disponibili.
ms.assetid: af5f21f8-8010-4e5a-b75f-30032333d87d
keywords:
- Classe MDM_Policy_Result01_Connectivity02
- Classe MDM_Policy_Result01_Connectivity02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Connectivity02
- MDM_Policy_Result01_Connectivity02.InstanceID
- MDM_Policy_Result01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723e8fa3287f99994d45fcc0a8bc5a09473a7563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873469"
---
# <a name="mdm_policy_result01_connectivity02-class"></a><span data-ttu-id="a0db6-105">\_ \_ Classe Result01 Connectivity02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="a0db6-105">MDM\_Policy\_Result01\_Connectivity02 class</span></span>

<span data-ttu-id="a0db6-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="a0db6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a0db6-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="a0db6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a0db6-108">La **classe \_ \_ Result01 \_ Connectivity02 dei criteri MDM** rappresenta i criteri di connessione disponibili.</span><span class="sxs-lookup"><span data-stu-id="a0db6-108">The **MDM\_Policy\_Result01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="a0db6-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a0db6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0db6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0db6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Connectivity02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBluetooth;
  sint32 AllowCellularData;
  sint32 AllowCellularDataRoaming;
  sint32 AllowVPNOverCellular;
  sint32 AllowVPNRoamingOverCellular;
  string DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards;
  string DisableDownloadingOfPrintDriversOverHTTP;
  string DiablePrintingOverHTTP;
  string HardenedUNCPaths;
  string ProhibitInstallationAndConfigurationOfNetworkBridge;
  sint32 DisallowNetworkConnectivityActiveTests;
  sint32 AllowConnectedDevices;
};
```

## <a name="members"></a><span data-ttu-id="a0db6-111">Members</span><span class="sxs-lookup"><span data-stu-id="a0db6-111">Members</span></span>

<span data-ttu-id="a0db6-112">La **classe \_ \_ Result01 \_ Connectivity02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a0db6-112">The **MDM\_Policy\_Result01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="a0db6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0db6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0db6-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a0db6-114">Properties</span></span>

<span data-ttu-id="a0db6-115">La **classe \_ \_ \_ Connectivity02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a0db6-115">The **MDM\_Policy\_Result01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a0db6-116">AllowBluetooth consente</span><span class="sxs-lookup"><span data-stu-id="a0db6-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a0db6-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-119">AllowCellularData</span><span class="sxs-lookup"><span data-stu-id="a0db6-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a0db6-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-122">AllowCellularDataRoaming</span><span class="sxs-lookup"><span data-stu-id="a0db6-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a0db6-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-125">AllowConnectedDevices</span><span class="sxs-lookup"><span data-stu-id="a0db6-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a0db6-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="a0db6-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a0db6-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-131">AllowVPNRoamingOverCellular</span><span class="sxs-lookup"><span data-stu-id="a0db6-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a0db6-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-134">DiablePrintingOverHTTP</span><span class="sxs-lookup"><span data-stu-id="a0db6-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0db6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-137">DisableDownloadingOfPrintDriversOverHTTP</span><span class="sxs-lookup"><span data-stu-id="a0db6-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0db6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span><span class="sxs-lookup"><span data-stu-id="a0db6-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0db6-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-143">DisallowNetworkConnectivityActiveTests</span><span class="sxs-lookup"><span data-stu-id="a0db6-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a0db6-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0db6-146">HardenedUNCPaths</span><span class="sxs-lookup"><span data-stu-id="a0db6-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0db6-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0db6-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a0db6-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0db6-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0db6-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0db6-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a0db6-153">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="a0db6-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="a0db6-154">Per questa classe la stringa è "Connectivity".</span><span class="sxs-lookup"><span data-stu-id="a0db6-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="a0db6-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a0db6-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0db6-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a0db6-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-158">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0db6-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a0db6-159">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="a0db6-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="a0db6-160">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="a0db6-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="a0db6-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span><span class="sxs-lookup"><span data-stu-id="a0db6-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0db6-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a0db6-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0db6-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a0db6-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0db6-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0db6-164">Requirements</span></span>



| <span data-ttu-id="a0db6-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0db6-165">Requirement</span></span> | <span data-ttu-id="a0db6-166">Valore</span><span class="sxs-lookup"><span data-stu-id="a0db6-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0db6-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0db6-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a0db6-168">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a0db6-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0db6-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0db6-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a0db6-170">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a0db6-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a0db6-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0db6-171">Namespace</span></span><br/>                | <span data-ttu-id="a0db6-172">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="a0db6-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="a0db6-173">MOF</span><span class="sxs-lookup"><span data-stu-id="a0db6-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0db6-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0db6-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0db6-175">DLL</span><span class="sxs-lookup"><span data-stu-id="a0db6-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0db6-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0db6-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0db6-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0db6-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0db6-178">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="a0db6-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

