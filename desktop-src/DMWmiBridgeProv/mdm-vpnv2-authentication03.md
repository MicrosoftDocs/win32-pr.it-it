---
title: Classe MDM_VPNv2_Authentication03
description: La \_ classe MDM VPNv2 \_ Authentication03 contiene le informazioni di autenticazione per il profilo VPN nativo.
ms.assetid: 931752a9-6de5-46d4-b9d9-2c59c49e8ed9
keywords:
- Classe MDM_VPNv2_Authentication03
- Classe MDM_VPNv2_Authentication03, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03.InstanceID
- MDM_VPNv2_Authentication03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ca50bcc83df01b4aa5e7ec900985cf15f7e67d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048382"
---
# <a name="mdm_vpnv2_authentication03-class"></a><span data-ttu-id="f7ae2-105">\_Classe MDM VPNv2 \_ Authentication03</span><span class="sxs-lookup"><span data-stu-id="f7ae2-105">MDM\_VPNv2\_Authentication03 class</span></span>

<span data-ttu-id="f7ae2-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f7ae2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f7ae2-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f7ae2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f7ae2-108">La classe [**MDM \_ VPNv2 \_ Authentication03**](mdm-vpnv2-01.md) contiene le informazioni di autenticazione per il profilo VPN nativo.</span><span class="sxs-lookup"><span data-stu-id="f7ae2-108">The [**MDM\_VPNv2\_Authentication03**](mdm-vpnv2-01.md) class contains authentication information for the native VPN profile.</span></span>

<span data-ttu-id="f7ae2-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f7ae2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ae2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7ae2-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Authentication03
{
  string InstanceID;
  string ParentID;
  string UserMethod;
  string MachineMethod;
};
```

## <a name="members"></a><span data-ttu-id="f7ae2-111">Members</span><span class="sxs-lookup"><span data-stu-id="f7ae2-111">Members</span></span>

<span data-ttu-id="f7ae2-112">La classe **MDM \_ VPNv2 \_ Authentication03** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f7ae2-112">The **MDM\_VPNv2\_Authentication03** class has these types of members:</span></span>

-   [<span data-ttu-id="f7ae2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7ae2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7ae2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7ae2-114">Properties</span></span>

<span data-ttu-id="f7ae2-115">La classe **MDM \_ VPNv2 \_ Authentication03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7ae2-115">The **MDM\_VPNv2\_Authentication03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7ae2-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f7ae2-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7ae2-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7ae2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7ae2-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7ae2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7ae2-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7ae2-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f7ae2-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f7ae2-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="f7ae2-121">MachineMethod</span><span class="sxs-lookup"><span data-stu-id="f7ae2-121">MachineMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-machinemethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7ae2-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7ae2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7ae2-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7ae2-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f7ae2-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f7ae2-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7ae2-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7ae2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7ae2-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7ae2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7ae2-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7ae2-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f7ae2-128">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f7ae2-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="f7ae2-129">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span><span class="sxs-lookup"><span data-stu-id="f7ae2-129">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="f7ae2-130">UserMethod</span><span class="sxs-lookup"><span data-stu-id="f7ae2-130">UserMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-usermethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7ae2-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7ae2-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7ae2-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f7ae2-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7ae2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7ae2-133">Requirements</span></span>



| <span data-ttu-id="f7ae2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7ae2-134">Requirement</span></span> | <span data-ttu-id="f7ae2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f7ae2-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ae2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7ae2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f7ae2-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f7ae2-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7ae2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7ae2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f7ae2-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f7ae2-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f7ae2-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f7ae2-140">Namespace</span></span><br/>                | <span data-ttu-id="f7ae2-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f7ae2-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f7ae2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f7ae2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7ae2-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7ae2-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7ae2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f7ae2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7ae2-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7ae2-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7ae2-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7ae2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ae2-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="f7ae2-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

