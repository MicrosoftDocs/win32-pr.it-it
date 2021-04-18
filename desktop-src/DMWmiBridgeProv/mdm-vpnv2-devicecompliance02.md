---
title: Classe MDM_VPNv2_DeviceCompliance02
description: Riservato per usi futuri. | Classe MDM_VPNv2_DeviceCompliance02
ms.assetid: f84f4812-3083-46c4-a60c-919ec92c844f
keywords:
- Classe MDM_VPNv2_DeviceCompliance02
- Classe MDM_VPNv2_DeviceCompliance02, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_DeviceCompliance02
- MDM_VPNv2_DeviceCompliance02.InstanceID
- MDM_VPNv2_DeviceCompliance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a454a5cce3a40066c7cf14a60bdeeb81dcabab9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321943"
---
# <a name="mdm_vpnv2_devicecompliance02-class"></a><span data-ttu-id="59320-106">\_Classe MDM VPNv2 \_ DeviceCompliance02</span><span class="sxs-lookup"><span data-stu-id="59320-106">MDM\_VPNv2\_DeviceCompliance02 class</span></span>

<span data-ttu-id="59320-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="59320-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="59320-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="59320-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="59320-109">Riservato per utilizzi futuri</span><span class="sxs-lookup"><span data-stu-id="59320-109">Reserved for Future Use</span></span>

<span data-ttu-id="59320-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="59320-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="59320-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59320-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DeviceCompliance02
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
};
```

## <a name="members"></a><span data-ttu-id="59320-112">Members</span><span class="sxs-lookup"><span data-stu-id="59320-112">Members</span></span>

<span data-ttu-id="59320-113">La classe **MDM \_ VPNv2 \_ DeviceCompliance02** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="59320-113">The **MDM\_VPNv2\_DeviceCompliance02** class has these types of members:</span></span>

-   [<span data-ttu-id="59320-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59320-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59320-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="59320-115">Properties</span></span>

<span data-ttu-id="59320-116">La classe **MDM \_ VPNv2 \_ DeviceCompliance02** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="59320-116">The **MDM\_VPNv2\_DeviceCompliance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="59320-117">Enabled</span><span class="sxs-lookup"><span data-stu-id="59320-117">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59320-118">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="59320-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59320-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="59320-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="59320-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="59320-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59320-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59320-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59320-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59320-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59320-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59320-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="59320-124">Aggiunta in Windows 10, versione 1607.</span><span class="sxs-lookup"><span data-stu-id="59320-124">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="59320-125">I nodi in DeviceCompliance possono essere usati per abilitare l'accesso condizionale basato su AAD per la VPN.</span><span class="sxs-lookup"><span data-stu-id="59320-125">Nodes under DeviceCompliance can be used to enable AAD-based Conditional Access for VPN.</span></span>

</dd> <dt>

<span data-ttu-id="59320-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="59320-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59320-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="59320-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59320-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="59320-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59320-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59320-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="59320-130">Aggiunta in Windows 10, versione 1607.</span><span class="sxs-lookup"><span data-stu-id="59320-130">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="59320-131">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="59320-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="59320-132">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="59320-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59320-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59320-133">Requirements</span></span>



| <span data-ttu-id="59320-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="59320-134">Requirement</span></span> | <span data-ttu-id="59320-135">Valore</span><span class="sxs-lookup"><span data-stu-id="59320-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59320-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59320-136">Minimum supported client</span></span><br/> | <span data-ttu-id="59320-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="59320-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59320-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59320-138">Minimum supported server</span></span><br/> | <span data-ttu-id="59320-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="59320-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="59320-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59320-140">Namespace</span></span><br/>                | <span data-ttu-id="59320-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="59320-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="59320-142">MOF</span><span class="sxs-lookup"><span data-stu-id="59320-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59320-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59320-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="59320-144">DLL</span><span class="sxs-lookup"><span data-stu-id="59320-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59320-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59320-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59320-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59320-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59320-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="59320-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

