---
title: Classe MDM_VPNv2_Proxy02
description: La \_ classe MDM VPNv2 \_ Proxy02 definisce un oggetto di configurazione per abilitare un supporto proxy post-connessione per VPN.
ms.assetid: 243f0824-4951-41c4-b8b4-b5c39aefd8ff
keywords:
- Classe MDM_VPNv2_Proxy02
- Classe MDM_VPNv2_Proxy02, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02.InstanceID
- MDM_VPNv2_Proxy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf8197379f5b1ff69433baa845af2cd53bb9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476768"
---
# <a name="mdm_vpnv2_proxy02-class"></a><span data-ttu-id="0ed3f-105">\_Classe MDM VPNv2 \_ Proxy02</span><span class="sxs-lookup"><span data-stu-id="0ed3f-105">MDM\_VPNv2\_Proxy02 class</span></span>

<span data-ttu-id="0ed3f-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="0ed3f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0ed3f-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="0ed3f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0ed3f-108">La classe **MDM \_ VPNv2 \_ Proxy02** definisce un oggetto di configurazione per abilitare un supporto proxy post-connessione per VPN.</span><span class="sxs-lookup"><span data-stu-id="0ed3f-108">The **MDM\_VPNv2\_Proxy02** class defines a configuration object to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="0ed3f-109">Il proxy definito per questo profilo viene applicato quando il profilo è attivo e connesso.</span><span class="sxs-lookup"><span data-stu-id="0ed3f-109">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

<span data-ttu-id="0ed3f-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0ed3f-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed3f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ed3f-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Proxy02
{
  string InstanceID;
  string ParentID;
  string AutoConfigUrl;
};
```

## <a name="members"></a><span data-ttu-id="0ed3f-112">Members</span><span class="sxs-lookup"><span data-stu-id="0ed3f-112">Members</span></span>

<span data-ttu-id="0ed3f-113">La classe **MDM \_ VPNv2 \_ Proxy02** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0ed3f-113">The **MDM\_VPNv2\_Proxy02** class has these types of members:</span></span>

-   [<span data-ttu-id="0ed3f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ed3f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ed3f-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ed3f-115">Properties</span></span>

<span data-ttu-id="0ed3f-116">La classe **MDM \_ VPNv2 \_ Proxy02** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0ed3f-116">The **MDM\_VPNv2\_Proxy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0ed3f-117">AutoConfigUrl</span><span class="sxs-lookup"><span data-stu-id="0ed3f-117">AutoConfigUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-autoconfigurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed3f-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ed3f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed3f-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ed3f-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ed3f-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0ed3f-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed3f-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ed3f-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed3f-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ed3f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ed3f-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ed3f-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ed3f-124">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="0ed3f-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="0ed3f-125">Raccolta di oggetti di configurazione per abilitare un supporto proxy post-connessione per VPN.</span><span class="sxs-lookup"><span data-stu-id="0ed3f-125">A collection of configuration objects to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="0ed3f-126">Il proxy definito per questo profilo viene applicato quando il profilo è attivo e connesso.</span><span class="sxs-lookup"><span data-stu-id="0ed3f-126">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

</dd> <dt>

<span data-ttu-id="0ed3f-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0ed3f-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed3f-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ed3f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed3f-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ed3f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ed3f-130">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ed3f-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ed3f-131">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="0ed3f-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="0ed3f-132">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="0ed3f-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ed3f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ed3f-133">Requirements</span></span>



| <span data-ttu-id="0ed3f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ed3f-134">Requirement</span></span> | <span data-ttu-id="0ed3f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="0ed3f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed3f-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ed3f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0ed3f-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0ed3f-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ed3f-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ed3f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0ed3f-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0ed3f-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0ed3f-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0ed3f-140">Namespace</span></span><br/>                | <span data-ttu-id="0ed3f-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="0ed3f-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0ed3f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0ed3f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ed3f-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ed3f-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ed3f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0ed3f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ed3f-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ed3f-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed3f-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ed3f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed3f-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="0ed3f-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

