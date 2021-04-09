---
title: Classe MDM_VPNv2_01
description: La \_ classe MDM VPNv2 \_ 01 consente la configurazione del profilo VPN del dispositivo.
ms.assetid: cfef674b-880c-4c9f-a2c1-6c2cb03189da
keywords:
- Classe MDM_VPNv2_01
- Classe MDM_VPNv2_01, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_01
- MDM_VPNv2_01.InstanceID
- MDM_VPNv2_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3457220c438d0143db90c1955d48352353fee29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964380"
---
# <a name="mdm_vpnv2_01-class"></a><span data-ttu-id="77bb8-105">\_Classe MDM VPNv2 \_ 01</span><span class="sxs-lookup"><span data-stu-id="77bb8-105">MDM\_VPNv2\_01 class</span></span>

<span data-ttu-id="77bb8-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="77bb8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="77bb8-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="77bb8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="77bb8-108">La classe **MDM \_ VPNv2 \_ 01** consente la configurazione del profilo VPN del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77bb8-108">The **MDM\_VPNv2\_01** class allows configuration of the VPN profile of the device.</span></span>

<span data-ttu-id="77bb8-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="77bb8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="77bb8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77bb8-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_01
{
  string  InstanceID;
  string  ParentID;
  string  EdpModeId;
  boolean RememberCredentials;
  boolean AlwaysOn;
  string  DnsSuffix;
  boolean ByPassForLocal;
  string  TrustedNetworkDetection;
  string  ProfileXML;
  boolean LockDown;
};
```

## <a name="members"></a><span data-ttu-id="77bb8-111">Members</span><span class="sxs-lookup"><span data-stu-id="77bb8-111">Members</span></span>

<span data-ttu-id="77bb8-112">La classe **MDM \_ VPNv2 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="77bb8-112">The **MDM\_VPNv2\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="77bb8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="77bb8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77bb8-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="77bb8-114">Properties</span></span>

<span data-ttu-id="77bb8-115">La classe **MDM \_ VPNv2 \_ 01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="77bb8-115">The **MDM\_VPNv2\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="77bb8-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="77bb8-116">AlwaysOn</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-117">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="77bb8-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77bb8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="77bb8-119">ByPassForLocal</span><span class="sxs-lookup"><span data-stu-id="77bb8-119">ByPassForLocal</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-bypassforlocal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="77bb8-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77bb8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="77bb8-122">DnsSuffix</span><span class="sxs-lookup"><span data-stu-id="77bb8-122">DnsSuffix</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-dnssuffix)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="77bb8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77bb8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="77bb8-125">EdpModeId</span><span class="sxs-lookup"><span data-stu-id="77bb8-125">EdpModeId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-edpmodeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="77bb8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77bb8-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77bb8-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="77bb8-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="77bb8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="77bb8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77bb8-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77bb8-132">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="77bb8-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="77bb8-133">Per questa classe, la stringa è il nome del profilo VPN.</span><span class="sxs-lookup"><span data-stu-id="77bb8-133">For this class, the string is the VPN profile name.</span></span>

</dd> <dt>

[<span data-ttu-id="77bb8-134">Blocco</span><span class="sxs-lookup"><span data-stu-id="77bb8-134">LockDown</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-lockdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-135">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="77bb8-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77bb8-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77bb8-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="77bb8-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="77bb8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="77bb8-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-140">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77bb8-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77bb8-141">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="77bb8-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="77bb8-142">Per questa classe la stringa è "./Vendor/MSFT/VPNv2"</span><span class="sxs-lookup"><span data-stu-id="77bb8-142">For this class, the string is "./Vendor/MSFT/VPNv2"</span></span>

</dd> <dt>

[<span data-ttu-id="77bb8-143">ProfileXML</span><span class="sxs-lookup"><span data-stu-id="77bb8-143">ProfileXML</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-profilexml)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="77bb8-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77bb8-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="77bb8-146">RememberCredentials</span><span class="sxs-lookup"><span data-stu-id="77bb8-146">RememberCredentials</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-remembercredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-147">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="77bb8-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77bb8-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="77bb8-149">TrustedNetworkDetection</span><span class="sxs-lookup"><span data-stu-id="77bb8-149">TrustedNetworkDetection</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trustednetworkdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77bb8-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="77bb8-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77bb8-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="77bb8-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77bb8-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77bb8-152">Requirements</span></span>



| <span data-ttu-id="77bb8-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="77bb8-153">Requirement</span></span> | <span data-ttu-id="77bb8-154">Valore</span><span class="sxs-lookup"><span data-stu-id="77bb8-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77bb8-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77bb8-155">Minimum supported client</span></span><br/> | <span data-ttu-id="77bb8-156">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="77bb8-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77bb8-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77bb8-157">Minimum supported server</span></span><br/> | <span data-ttu-id="77bb8-158">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="77bb8-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="77bb8-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77bb8-159">Namespace</span></span><br/>                | <span data-ttu-id="77bb8-160">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="77bb8-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="77bb8-161">MOF</span><span class="sxs-lookup"><span data-stu-id="77bb8-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77bb8-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77bb8-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="77bb8-163">DLL</span><span class="sxs-lookup"><span data-stu-id="77bb8-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77bb8-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77bb8-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77bb8-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77bb8-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77bb8-166">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="77bb8-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

