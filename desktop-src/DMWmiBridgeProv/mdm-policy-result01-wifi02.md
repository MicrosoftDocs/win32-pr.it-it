---
title: Classe MDM_Policy_Result01_WiFi02
description: La \_ classe WiFi02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di Wi-Fi disponibili.
ms.assetid: 074C4428-401D-4564-B7AC-45C2221EEC3A
keywords:
- Classe MDM_Policy_Result01_WiFi02
- Classe MDM_Policy_Result01_WiFi02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WiFi02
- MDM_Policy_Result01_WiFi02.InstanceID
- MDM_Policy_Result01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff9e0349f7a18da3320fab333d5b5fd36715999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963793"
---
# <a name="mdm_policy_result01_wifi02-class"></a><span data-ttu-id="8c372-105">\_ \_ Classe Result01 WiFi02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="8c372-105">MDM\_Policy\_Result01\_WiFi02 class</span></span>

<span data-ttu-id="8c372-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="8c372-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8c372-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="8c372-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8c372-108">La **classe \_ \_ \_ WiFi02 dei criteri MDM Result01** rappresenta i criteri di Wi-Fi disponibili.</span><span class="sxs-lookup"><span data-stu-id="8c372-108">The **MDM\_Policy\_Result01\_WiFi02** class represents the Wi-Fi policies available.</span></span> <span data-ttu-id="8c372-109">Questi criteri determinano Wi-Fi configurazioni consentite.</span><span class="sxs-lookup"><span data-stu-id="8c372-109">These policies determine Wi-Fi configurations that are allowed.</span></span>

<span data-ttu-id="8c372-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8c372-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c372-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c372-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WiFi02
{
  string InstanceID;
  string ParentID;
  sint32 AllowInternetSharing;
  sint32 AllowWiFi;
  sint32 AllowWiFiDirect;
  sint32 AllowManualWiFiConfiguration;
  sint32 AllowAutoConnectToWiFiSenseHotspots;
  sint32 WLANScanMode;
};
```

## <a name="members"></a><span data-ttu-id="8c372-112">Members</span><span class="sxs-lookup"><span data-stu-id="8c372-112">Members</span></span>

<span data-ttu-id="8c372-113">La **classe \_ \_ Result01 \_ WiFi02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8c372-113">The **MDM\_Policy\_Result01\_WiFi02** class has these types of members:</span></span>

-   [<span data-ttu-id="8c372-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c372-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c372-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c372-115">Properties</span></span>

<span data-ttu-id="8c372-116">La **classe \_ \_ \_ WiFi02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c372-116">The **MDM\_Policy\_Result01\_WiFi02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8c372-117">AllowAutoConnectToWiFiSenseHotspots</span><span class="sxs-lookup"><span data-stu-id="8c372-117">AllowAutoConnectToWiFiSenseHotspots</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c372-118">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8c372-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c372-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8c372-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c372-120">AllowInternetSharing</span><span class="sxs-lookup"><span data-stu-id="8c372-120">AllowInternetSharing</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c372-121">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8c372-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c372-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8c372-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c372-123">AllowManualWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c372-123">AllowManualWiFiConfiguration</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c372-124">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8c372-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c372-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8c372-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c372-126">AllowWiFi consente</span><span class="sxs-lookup"><span data-stu-id="8c372-126">AllowWiFi</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c372-127">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8c372-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c372-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8c372-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c372-129">AllowWiFiDirect</span><span class="sxs-lookup"><span data-stu-id="8c372-129">AllowWiFiDirect</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c372-130">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8c372-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c372-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8c372-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c372-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8c372-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c372-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c372-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c372-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c372-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c372-135">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c372-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8c372-136">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="8c372-136">Identifies the name of the parent node.</span></span> <span data-ttu-id="8c372-137">Per questa classe la stringa è "WiFi".</span><span class="sxs-lookup"><span data-stu-id="8c372-137">For this class, the string is "WiFi".</span></span>

</dd> <dt>

<span data-ttu-id="8c372-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8c372-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c372-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c372-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c372-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c372-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c372-141">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c372-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8c372-142">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="8c372-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="8c372-143">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="8c372-143">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="8c372-144">WLANScanMode</span><span class="sxs-lookup"><span data-stu-id="8c372-144">WLANScanMode</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c372-145">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8c372-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c372-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8c372-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c372-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c372-147">Requirements</span></span>



| <span data-ttu-id="8c372-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c372-148">Requirement</span></span> | <span data-ttu-id="8c372-149">Valore</span><span class="sxs-lookup"><span data-stu-id="8c372-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c372-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c372-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8c372-151">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8c372-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c372-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c372-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8c372-153">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8c372-153">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8c372-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c372-154">Namespace</span></span><br/>                | <span data-ttu-id="8c372-155">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="8c372-155">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="8c372-156">MOF</span><span class="sxs-lookup"><span data-stu-id="8c372-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c372-157"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c372-157"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c372-158">DLL</span><span class="sxs-lookup"><span data-stu-id="8c372-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c372-159"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c372-159"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c372-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c372-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c372-161">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="8c372-161">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

