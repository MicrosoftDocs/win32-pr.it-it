---
title: Classe MDM_Policy_Config01_WiFi02
description: La \_ classe WiFi02 dei criteri MDM \_ Config01 \_ rappresenta i criteri di Wi-Fi disponibili.
ms.assetid: 68CFBB5E-F365-4D1A-8EF1-CC070E9A7982
keywords:
- Classe MDM_Policy_Config01_WiFi02
- Classe MDM_Policy_Config01_WiFi02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WiFi02
- MDM_Policy_Config01_WiFi02.InstanceID
- MDM_Policy_Config01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00848613f1f0e9fd4ab6db9dc4afdabe54ce538c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873873"
---
# <a name="mdm_policy_config01_wifi02-class"></a><span data-ttu-id="594c3-105">\_ \_ Classe Config01 WiFi02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="594c3-105">MDM\_Policy\_Config01\_WiFi02 class</span></span>

<span data-ttu-id="594c3-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="594c3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="594c3-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="594c3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="594c3-108">La **classe \_ \_ \_ WiFi02 dei criteri MDM Config01** rappresenta i criteri di Wi-Fi disponibili.</span><span class="sxs-lookup"><span data-stu-id="594c3-108">The **MDM\_Policy\_Config01\_WiFi02** class represents the Wi-Fi policies available.</span></span> <span data-ttu-id="594c3-109">Questi criteri determinano Wi-Fi configurazioni consentite.</span><span class="sxs-lookup"><span data-stu-id="594c3-109">These policies determine Wi-Fi configurations that are allowed.</span></span>

<span data-ttu-id="594c3-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="594c3-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="594c3-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="594c3-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WiFi02
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

## <a name="members"></a><span data-ttu-id="594c3-112">Members</span><span class="sxs-lookup"><span data-stu-id="594c3-112">Members</span></span>

<span data-ttu-id="594c3-113">La **classe \_ \_ Config01 \_ WiFi02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="594c3-113">The **MDM\_Policy\_Config01\_WiFi02** class has these types of members:</span></span>

-   [<span data-ttu-id="594c3-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="594c3-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="594c3-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="594c3-115">Properties</span></span>

<span data-ttu-id="594c3-116">La **classe \_ \_ \_ WiFi02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="594c3-116">The **MDM\_Policy\_Config01\_WiFi02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="594c3-117">AllowAutoConnectToWiFiSenseHotspots</span><span class="sxs-lookup"><span data-stu-id="594c3-117">AllowAutoConnectToWiFiSenseHotspots</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

<span data-ttu-id="594c3-118">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="594c3-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="594c3-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="594c3-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="594c3-120">AllowInternetSharing</span><span class="sxs-lookup"><span data-stu-id="594c3-120">AllowInternetSharing</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="594c3-121">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="594c3-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="594c3-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="594c3-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="594c3-123">AllowManualWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="594c3-123">AllowManualWiFiConfiguration</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="594c3-124">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="594c3-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="594c3-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="594c3-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="594c3-126">AllowWiFi consente</span><span class="sxs-lookup"><span data-stu-id="594c3-126">AllowWiFi</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="594c3-127">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="594c3-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="594c3-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="594c3-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="594c3-129">AllowWiFiDirect</span><span class="sxs-lookup"><span data-stu-id="594c3-129">AllowWiFiDirect</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="594c3-130">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="594c3-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="594c3-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="594c3-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="594c3-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="594c3-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="594c3-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="594c3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="594c3-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="594c3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="594c3-135">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="594c3-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="594c3-136">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="594c3-136">Identifies the name of the parent node.</span></span> <span data-ttu-id="594c3-137">Per questa classe la stringa è "WiFi".</span><span class="sxs-lookup"><span data-stu-id="594c3-137">For this class, the string is "WiFi".</span></span>

</dd> <dt>

<span data-ttu-id="594c3-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="594c3-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="594c3-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="594c3-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="594c3-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="594c3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="594c3-141">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="594c3-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="594c3-142">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="594c3-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="594c3-143">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="594c3-143">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="594c3-144">WLANScanMode</span><span class="sxs-lookup"><span data-stu-id="594c3-144">WLANScanMode</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="594c3-145">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="594c3-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="594c3-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="594c3-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="594c3-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="594c3-147">Requirements</span></span>



| <span data-ttu-id="594c3-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="594c3-148">Requirement</span></span> | <span data-ttu-id="594c3-149">Valore</span><span class="sxs-lookup"><span data-stu-id="594c3-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="594c3-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="594c3-150">Minimum supported client</span></span><br/> | <span data-ttu-id="594c3-151">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="594c3-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="594c3-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="594c3-152">Minimum supported server</span></span><br/> | <span data-ttu-id="594c3-153">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="594c3-153">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="594c3-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="594c3-154">Namespace</span></span><br/>                | <span data-ttu-id="594c3-155">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="594c3-155">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="594c3-156">MOF</span><span class="sxs-lookup"><span data-stu-id="594c3-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="594c3-157"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="594c3-157"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="594c3-158">DLL</span><span class="sxs-lookup"><span data-stu-id="594c3-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="594c3-159"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="594c3-159"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="594c3-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="594c3-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="594c3-161">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="594c3-161">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

