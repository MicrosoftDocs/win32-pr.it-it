---
title: Classe MDM_Policy_Config01_Connectivity02
description: La \_ \_ classe Config01 Connectivity02 dei criteri MDM \_ rappresenta i criteri di connessione disponibili.
ms.assetid: 670e48c2-1af1-45e9-81c6-cdf3a310240f
keywords:
- Classe MDM_Policy_Config01_Connectivity02
- Classe MDM_Policy_Config01_Connectivity02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Connectivity02
- MDM_Policy_Config01_Connectivity02.InstanceID
- MDM_Policy_Config01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b39b897998bf47c5f5411456ccae7fcb6927aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740967"
---
# <a name="mdm_policy_config01_connectivity02-class"></a><span data-ttu-id="1465a-105">\_ \_ Classe Config01 Connectivity02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="1465a-105">MDM\_Policy\_Config01\_Connectivity02 class</span></span>

<span data-ttu-id="1465a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="1465a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1465a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="1465a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1465a-108">La **classe \_ \_ Config01 \_ Connectivity02 dei criteri MDM** rappresenta i criteri di connessione disponibili.</span><span class="sxs-lookup"><span data-stu-id="1465a-108">The **MDM\_Policy\_Config01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="1465a-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1465a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1465a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1465a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Connectivity02
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

## <a name="members"></a><span data-ttu-id="1465a-111">Members</span><span class="sxs-lookup"><span data-stu-id="1465a-111">Members</span></span>

<span data-ttu-id="1465a-112">La **classe \_ \_ Config01 \_ Connectivity02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1465a-112">The **MDM\_Policy\_Config01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="1465a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1465a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1465a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1465a-114">Properties</span></span>

<span data-ttu-id="1465a-115">La **classe \_ \_ \_ Connectivity02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1465a-115">The **MDM\_Policy\_Config01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1465a-116">AllowBluetooth consente</span><span class="sxs-lookup"><span data-stu-id="1465a-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1465a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-119">AllowCellularData</span><span class="sxs-lookup"><span data-stu-id="1465a-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1465a-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-122">AllowCellularDataRoaming</span><span class="sxs-lookup"><span data-stu-id="1465a-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1465a-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-125">AllowConnectedDevices</span><span class="sxs-lookup"><span data-stu-id="1465a-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1465a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="1465a-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1465a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-131">AllowVPNRoamingOverCellular</span><span class="sxs-lookup"><span data-stu-id="1465a-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1465a-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-134">DiablePrintingOverHTTP</span><span class="sxs-lookup"><span data-stu-id="1465a-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1465a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-137">DisableDownloadingOfPrintDriversOverHTTP</span><span class="sxs-lookup"><span data-stu-id="1465a-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1465a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span><span class="sxs-lookup"><span data-stu-id="1465a-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1465a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-143">DisallowNetworkConnectivityActiveTests</span><span class="sxs-lookup"><span data-stu-id="1465a-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1465a-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1465a-146">HardenedUNCPaths</span><span class="sxs-lookup"><span data-stu-id="1465a-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1465a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1465a-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1465a-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1465a-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1465a-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1465a-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1465a-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1465a-153">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="1465a-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="1465a-154">Per questa classe la stringa è "Connectivity".</span><span class="sxs-lookup"><span data-stu-id="1465a-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="1465a-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1465a-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1465a-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1465a-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1465a-158">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1465a-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1465a-159">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="1465a-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="1465a-160">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="1465a-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="1465a-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span><span class="sxs-lookup"><span data-stu-id="1465a-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1465a-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1465a-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1465a-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1465a-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1465a-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1465a-164">Requirements</span></span>



| <span data-ttu-id="1465a-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="1465a-165">Requirement</span></span> | <span data-ttu-id="1465a-166">Valore</span><span class="sxs-lookup"><span data-stu-id="1465a-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1465a-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1465a-167">Minimum supported client</span></span><br/> | <span data-ttu-id="1465a-168">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1465a-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1465a-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1465a-169">Minimum supported server</span></span><br/> | <span data-ttu-id="1465a-170">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1465a-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1465a-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1465a-171">Namespace</span></span><br/>                | <span data-ttu-id="1465a-172">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="1465a-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1465a-173">MOF</span><span class="sxs-lookup"><span data-stu-id="1465a-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1465a-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1465a-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1465a-175">DLL</span><span class="sxs-lookup"><span data-stu-id="1465a-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1465a-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1465a-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1465a-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1465a-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1465a-178">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="1465a-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

