---
title: Classe MDM_PassportForWork_ExcludeSecurityDevices03
description: La \_ classe MDM PassportForWork \_ ExcludeSecurityDevices03 definisce i moduli della piattaforma attendibile che possono essere usati con Windows Hello for business.
ms.assetid: ca8fba3a-736b-4bd3-ac93-e0d44d54798d
keywords:
- Classe MDM_PassportForWork_ExcludeSecurityDevices03
- Classe MDM_PassportForWork_ExcludeSecurityDevices03, descritta
topic_type:
- apiref
api_name:
- MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03.InstanceID
- MDM_PassportForWork_ExcludeSecurityDevices03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cc0374a3c313a118e5ee72791380225cc760
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048183"
---
# <a name="mdm_passportforwork_excludesecuritydevices03-class"></a><span data-ttu-id="8acb3-105">\_Classe MDM PassportForWork \_ ExcludeSecurityDevices03</span><span class="sxs-lookup"><span data-stu-id="8acb3-105">MDM\_PassportForWork\_ExcludeSecurityDevices03 class</span></span>

<span data-ttu-id="8acb3-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="8acb3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8acb3-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="8acb3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8acb3-108">La \_ classe MDM PassportForWork \_ ExcludeSecurityDevices03 definisce i moduli della piattaforma attendibile che possono essere usati con Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="8acb3-108">The MDM\_PassportForWork\_ExcludeSecurityDevices03 class defines the Trusted Platform Modules allowed to use with Windows Hello for Business.</span></span>

<span data-ttu-id="8acb3-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8acb3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8acb3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8acb3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_ExcludeSecurityDevices03
{
  string  InstanceID;
  string  ParentID;
  boolean TPM12;
};
```

## <a name="members"></a><span data-ttu-id="8acb3-111">Members</span><span class="sxs-lookup"><span data-stu-id="8acb3-111">Members</span></span>

<span data-ttu-id="8acb3-112">La classe **MDM \_ PassportForWork \_ ExcludeSecurityDevices03** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8acb3-112">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these types of members:</span></span>

-   [<span data-ttu-id="8acb3-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8acb3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8acb3-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8acb3-114">Properties</span></span>

<span data-ttu-id="8acb3-115">La classe **MDM \_ PassportForWork \_ ExcludeSecurityDevices03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8acb3-115">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8acb3-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8acb3-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8acb3-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8acb3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8acb3-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8acb3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8acb3-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8acb3-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8acb3-120">Nodo radice.</span><span class="sxs-lookup"><span data-stu-id="8acb3-120">Root node.</span></span>

</dd> <dt>

<span data-ttu-id="8acb3-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8acb3-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8acb3-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8acb3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8acb3-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8acb3-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8acb3-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8acb3-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8acb3-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="8acb3-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="8acb3-126">Per ulteriori informazioni, vedere [PASSPORTFORWORK CSP](/windows/client-management/mdm/passportforwork-csp).</span><span class="sxs-lookup"><span data-stu-id="8acb3-126">For more information, see [PassportForWork CSP](/windows/client-management/mdm/passportforwork-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="8acb3-127">TPM12</span><span class="sxs-lookup"><span data-stu-id="8acb3-127">TPM12</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8acb3-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8acb3-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8acb3-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8acb3-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8acb3-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8acb3-130">Requirements</span></span>



| <span data-ttu-id="8acb3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8acb3-131">Requirement</span></span> | <span data-ttu-id="8acb3-132">Valore</span><span class="sxs-lookup"><span data-stu-id="8acb3-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acb3-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8acb3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8acb3-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8acb3-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8acb3-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8acb3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8acb3-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8acb3-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8acb3-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8acb3-137">Namespace</span></span><br/>                | <span data-ttu-id="8acb3-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="8acb3-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8acb3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8acb3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8acb3-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8acb3-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8acb3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8acb3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8acb3-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8acb3-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

