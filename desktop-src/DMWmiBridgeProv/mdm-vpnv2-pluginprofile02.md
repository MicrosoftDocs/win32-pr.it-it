---
title: Classe MDM_VPNv2_PluginProfile02
description: La \_ classe MDM VPNv2 \_ PlugInProfile02 descrive le informazioni necessarie quando si usa un plug-in VPN basato su Windows Store.
ms.assetid: 522c32e5-74f9-46b2-b590-ca6ade241e97
keywords:
- Classe MDM_VPNv2_PluginProfile02
- Classe MDM_VPNv2_PluginProfile02, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02.InstanceID
- MDM_VPNv2_PluginProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 008d60b28ec1d2cec9431cc63ac4d0c406d18060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964231"
---
# <a name="mdm_vpnv2_pluginprofile02-class"></a><span data-ttu-id="19820-105">\_Classe MDM VPNv2 \_ PluginProfile02</span><span class="sxs-lookup"><span data-stu-id="19820-105">MDM\_VPNv2\_PluginProfile02 class</span></span>

<span data-ttu-id="19820-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="19820-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="19820-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="19820-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="19820-108">La classe **MDM \_ VPNv2 \_ PlugInProfile02** descrive le informazioni necessarie quando si usa un plug-in VPN basato su Windows Store.</span><span class="sxs-lookup"><span data-stu-id="19820-108">The **MDM\_VPNv2\_PlugInProfile02** class describes the information needed when using a Windows Store based VPN plugin.</span></span>

<span data-ttu-id="19820-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="19820-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19820-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19820-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_PluginProfile02
{
  string InstanceID;
  string ParentID;
  string ServerUrlList;
  string CustomConfiguration;
  string PluginPackageFamilyName;
  string CustomStoreUrl;
};
```

## <a name="members"></a><span data-ttu-id="19820-111">Members</span><span class="sxs-lookup"><span data-stu-id="19820-111">Members</span></span>

<span data-ttu-id="19820-112">La classe **MDM \_ VPNv2 \_ PluginProfile02** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="19820-112">The **MDM\_VPNv2\_PluginProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="19820-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19820-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19820-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="19820-114">Properties</span></span>

<span data-ttu-id="19820-115">La classe **MDM \_ VPNv2 \_ PluginProfile02** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="19820-115">The **MDM\_VPNv2\_PluginProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="19820-116">CustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="19820-116">CustomConfiguration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19820-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19820-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19820-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="19820-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19820-119">CustomStoreUrl</span><span class="sxs-lookup"><span data-stu-id="19820-119">CustomStoreUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customstoreurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19820-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19820-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19820-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="19820-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19820-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="19820-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19820-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19820-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19820-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19820-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19820-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19820-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19820-126">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="19820-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="19820-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="19820-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19820-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19820-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19820-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="19820-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19820-130">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19820-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19820-131">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="19820-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="19820-132">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="19820-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="19820-133">PluginPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="19820-133">PluginPackageFamilyName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-pluginpackagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19820-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19820-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19820-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="19820-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19820-136">ServerUrlList</span><span class="sxs-lookup"><span data-stu-id="19820-136">ServerUrlList</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-serverurllist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19820-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="19820-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19820-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="19820-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19820-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19820-139">Requirements</span></span>



| <span data-ttu-id="19820-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="19820-140">Requirement</span></span> | <span data-ttu-id="19820-141">Valore</span><span class="sxs-lookup"><span data-stu-id="19820-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19820-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19820-142">Minimum supported client</span></span><br/> | <span data-ttu-id="19820-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="19820-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19820-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19820-144">Minimum supported server</span></span><br/> | <span data-ttu-id="19820-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="19820-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="19820-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19820-146">Namespace</span></span><br/>                | <span data-ttu-id="19820-147">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="19820-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="19820-148">MOF</span><span class="sxs-lookup"><span data-stu-id="19820-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19820-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19820-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="19820-150">DLL</span><span class="sxs-lookup"><span data-stu-id="19820-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19820-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19820-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19820-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19820-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19820-153">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="19820-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

