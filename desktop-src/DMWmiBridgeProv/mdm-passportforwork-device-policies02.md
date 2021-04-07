---
title: Classe MDM_PassportForWork_Device_Policies02
description: La \_ \_ classe Policies02 del dispositivo MDM PassportForWork \_ definisce le impostazioni dei criteri di Windows Hello for business.
ms.assetid: 7581ea7e-0360-4695-a4ad-566df24a8841
keywords:
- Classe MDM_PassportForWork_Device_Policies02
- Classe MDM_PassportForWork_Device_Policies02, descritta
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Device_Policies02
- MDM_PassportForWork_Device_Policies02.InstanceID
- MDM_PassportForWork_Device_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66d642fb796d3b7af009197580f1eda21ab0bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964029"
---
# <a name="mdm_passportforwork_device_policies02-class"></a><span data-ttu-id="15f8c-105">MDM \_ PassportForWork \_ Device \_ Policies02 Class</span><span class="sxs-lookup"><span data-stu-id="15f8c-105">MDM\_PassportForWork\_Device\_Policies02 class</span></span>

<span data-ttu-id="15f8c-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="15f8c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="15f8c-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="15f8c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="15f8c-108">La **classe \_ \_ \_ Policies02 del dispositivo MDM PassportForWork** definisce le impostazioni dei criteri di Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="15f8c-108">The **MDM\_PassportForWork\_Device\_Policies02** class defines the Windows Hello for Business policy settings.</span></span>

<span data-ttu-id="15f8c-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="15f8c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f8c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15f8c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Device_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UseCertificateForOnPremAuth;
};
```

## <a name="members"></a><span data-ttu-id="15f8c-111">Members</span><span class="sxs-lookup"><span data-stu-id="15f8c-111">Members</span></span>

<span data-ttu-id="15f8c-112">La **classe \_ \_ \_ Policies02 del dispositivo MDM PassportForWork** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="15f8c-112">The **MDM\_PassportForWork\_Device\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="15f8c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15f8c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15f8c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15f8c-114">Properties</span></span>

<span data-ttu-id="15f8c-115">La **classe \_ \_ \_ Policies02 del dispositivo MDM PassportForWork** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="15f8c-115">The **MDM\_PassportForWork\_Device\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15f8c-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="15f8c-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f8c-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="15f8c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15f8c-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15f8c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f8c-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15f8c-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="15f8c-120">Nodo per le impostazioni dei criteri di Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="15f8c-120">Node for the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

<span data-ttu-id="15f8c-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="15f8c-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f8c-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="15f8c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15f8c-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15f8c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f8c-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15f8c-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="15f8c-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="15f8c-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="15f8c-126">Per questa classe la stringa è "./Device/Vendor/MSFT/PassPortForWork/*TenantId*/"</span><span class="sxs-lookup"><span data-stu-id="15f8c-126">For this class, the string is "./Device/Vendor/MSFT/PassPortForWork/*TenantID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="15f8c-127">UseCertificateForOnPremAuth</span><span class="sxs-lookup"><span data-stu-id="15f8c-127">UseCertificateForOnPremAuth</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f8c-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="15f8c-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15f8c-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="15f8c-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15f8c-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15f8c-130">Requirements</span></span>



| <span data-ttu-id="15f8c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="15f8c-131">Requirement</span></span> | <span data-ttu-id="15f8c-132">Valore</span><span class="sxs-lookup"><span data-stu-id="15f8c-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15f8c-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15f8c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="15f8c-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="15f8c-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15f8c-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15f8c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="15f8c-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="15f8c-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="15f8c-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="15f8c-137">Namespace</span></span><br/>                | <span data-ttu-id="15f8c-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="15f8c-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="15f8c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="15f8c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15f8c-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15f8c-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="15f8c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="15f8c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15f8c-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15f8c-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

