---
title: Classe MDM_VPNv2_Certificate04
description: Riservato per usi futuri.
ms.assetid: 0fa831e0-918a-472f-88bf-7e40c4081417
keywords:
- Classe MDM_VPNv2_Certificate04
- Classe MDM_VPNv2_Certificate04, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_Certificate04
- MDM_VPNv2_Certificate04.InstanceID
- MDM_VPNv2_Certificate04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88bd26e8dc9916e7e2db97b980065d7a8733ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964234"
---
# <a name="mdm_vpnv2_certificate04-class"></a><span data-ttu-id="8da3f-105">\_Classe MDM VPNv2 \_ Certificate04</span><span class="sxs-lookup"><span data-stu-id="8da3f-105">MDM\_VPNv2\_Certificate04 class</span></span>

<span data-ttu-id="8da3f-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="8da3f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8da3f-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="8da3f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8da3f-108">Riservato per utilizzi futuri</span><span class="sxs-lookup"><span data-stu-id="8da3f-108">Reserved for future Use</span></span>

<span data-ttu-id="8da3f-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8da3f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da3f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8da3f-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Certificate04
{
  string InstanceID;
  string ParentID;
  string Issuer;
  string Eku;
};
```

## <a name="members"></a><span data-ttu-id="8da3f-111">Members</span><span class="sxs-lookup"><span data-stu-id="8da3f-111">Members</span></span>

<span data-ttu-id="8da3f-112">La classe **MDM \_ VPNv2 \_ Certificate04** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8da3f-112">The **MDM\_VPNv2\_Certificate04** class has these types of members:</span></span>

-   [<span data-ttu-id="8da3f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8da3f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8da3f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8da3f-114">Properties</span></span>

<span data-ttu-id="8da3f-115">La classe **MDM \_ VPNv2 \_ Certificate04** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8da3f-115">The **MDM\_VPNv2\_Certificate04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8da3f-116">EKU</span><span class="sxs-lookup"><span data-stu-id="8da3f-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da3f-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8da3f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da3f-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8da3f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8da3f-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8da3f-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da3f-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8da3f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da3f-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8da3f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8da3f-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8da3f-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8da3f-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="8da3f-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="8da3f-124">Per questa classe la stringa è "EAP"</span><span class="sxs-lookup"><span data-stu-id="8da3f-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

[<span data-ttu-id="8da3f-125">Issuer</span><span class="sxs-lookup"><span data-stu-id="8da3f-125">Issuer</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-issuer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da3f-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8da3f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da3f-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8da3f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8da3f-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8da3f-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da3f-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8da3f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da3f-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8da3f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8da3f-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8da3f-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8da3f-132">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="8da3f-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="8da3f-133">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span><span class="sxs-lookup"><span data-stu-id="8da3f-133">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8da3f-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8da3f-134">Requirements</span></span>



| <span data-ttu-id="8da3f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da3f-135">Requirement</span></span> | <span data-ttu-id="8da3f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="8da3f-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8da3f-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8da3f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8da3f-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8da3f-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8da3f-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8da3f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8da3f-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8da3f-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8da3f-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8da3f-141">Namespace</span></span><br/>                | <span data-ttu-id="8da3f-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="8da3f-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8da3f-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8da3f-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8da3f-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8da3f-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8da3f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8da3f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8da3f-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8da3f-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da3f-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8da3f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da3f-148">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="8da3f-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

