---
title: Classe MDM_PassportForWork_Policies02
description: La \_ classe MDM PassportForWork Policies02 effettua il \_ provisioning di Windows Hello for business.
ms.assetid: 362fe819-a68a-4433-8b43-201d9678a8da
keywords:
- Classe MDM_PassportForWork_Policies02
- Classe MDM_PassportForWork_Policies02, descritta
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Policies02
- MDM_PassportForWork_Policies02.InstanceID
- MDM_PassportForWork_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf407289f93f5ecff0e57ebf7b7fa8d9844183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964026"
---
# <a name="mdm_passportforwork_policies02-class"></a><span data-ttu-id="5627f-105">\_Classe MDM PassportForWork \_ Policies02</span><span class="sxs-lookup"><span data-stu-id="5627f-105">MDM\_PassportForWork\_Policies02 class</span></span>

<span data-ttu-id="5627f-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5627f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5627f-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5627f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5627f-108">La classe **MDM \_ PassportForWork \_ Policies02** effettua il provisioning di Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="5627f-108">The **MDM\_PassportForWork\_Policies02** class provisions Windows Hello for Business.</span></span>

<span data-ttu-id="5627f-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5627f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5627f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5627f-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UsePassportForWork;
  boolean RequireSecurityDevice;
};
```

## <a name="members"></a><span data-ttu-id="5627f-111">Members</span><span class="sxs-lookup"><span data-stu-id="5627f-111">Members</span></span>

<span data-ttu-id="5627f-112">La classe **MDM \_ PassportForWork \_ Policies02** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5627f-112">The **MDM\_PassportForWork\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="5627f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5627f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5627f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5627f-114">Properties</span></span>

<span data-ttu-id="5627f-115">La classe **MDM \_ PassportForWork \_ Policies02** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5627f-115">The **MDM\_PassportForWork\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5627f-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5627f-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5627f-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5627f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5627f-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5627f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5627f-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5627f-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5627f-120">Nodo radice per i criteri di Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="5627f-120">Root node for Windows Hello for Business policies.</span></span>

</dd> <dt>

<span data-ttu-id="5627f-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5627f-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5627f-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5627f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5627f-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5627f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5627f-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5627f-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5627f-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5627f-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="5627f-126">Per questa classe la stringa è "./Vendor/MSFT/PassPortForWork/*TenantId*"</span><span class="sxs-lookup"><span data-stu-id="5627f-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*"</span></span>

</dd> <dt>

[<span data-ttu-id="5627f-127">RequireSecurityDevice</span><span class="sxs-lookup"><span data-stu-id="5627f-127">RequireSecurityDevice</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-requiresecuritydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5627f-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5627f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5627f-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5627f-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5627f-130">UsePassportForWork</span><span class="sxs-lookup"><span data-stu-id="5627f-130">UsePassportForWork</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-usepassportforwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5627f-131">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5627f-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5627f-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5627f-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5627f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5627f-133">Requirements</span></span>



| <span data-ttu-id="5627f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5627f-134">Requirement</span></span> | <span data-ttu-id="5627f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5627f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5627f-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5627f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5627f-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5627f-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5627f-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5627f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5627f-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5627f-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5627f-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5627f-140">Namespace</span></span><br/>                | <span data-ttu-id="5627f-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5627f-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5627f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="5627f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5627f-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5627f-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5627f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5627f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5627f-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5627f-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5627f-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5627f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5627f-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5627f-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

