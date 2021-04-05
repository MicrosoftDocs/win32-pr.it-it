---
title: Classe MDM_PassportForWork_Remote03
description: La \_ classe MDM PassportForWork \_ Remote03 definisce le impostazioni dei criteri remoti di Windows Hello for business.
ms.assetid: 221701be-944f-42cd-847e-553d41281749
keywords:
- Classe MDM_PassportForWork_Remote03
- Classe MDM_PassportForWork_Remote03, descritta
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03.InstanceID
- MDM_PassportForWork_Remote03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae111389ad0f7c46b1f0b217bffc016e451ca9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048180"
---
# <a name="mdm_passportforwork_remote03-class"></a><span data-ttu-id="4f23f-105">\_Classe MDM PassportForWork \_ Remote03</span><span class="sxs-lookup"><span data-stu-id="4f23f-105">MDM\_PassportForWork\_Remote03 class</span></span>

<span data-ttu-id="4f23f-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="4f23f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4f23f-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="4f23f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4f23f-108">La classe **MDM \_ PassportForWork \_ Remote03** definisce le impostazioni dei criteri remoti di Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="4f23f-108">The **MDM\_PassportForWork\_Remote03** class defines the Windows Hello for Business remote policy settings.</span></span>

<span data-ttu-id="4f23f-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4f23f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f23f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f23f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Remote03
{
  string  InstanceID;
  string  ParentID;
  boolean UseRemotePassport;
};
```

## <a name="members"></a><span data-ttu-id="4f23f-111">Members</span><span class="sxs-lookup"><span data-stu-id="4f23f-111">Members</span></span>

<span data-ttu-id="4f23f-112">La classe **MDM \_ PassportForWork \_ Remote03** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4f23f-112">The **MDM\_PassportForWork\_Remote03** class has these types of members:</span></span>

-   [<span data-ttu-id="4f23f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f23f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f23f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f23f-114">Properties</span></span>

<span data-ttu-id="4f23f-115">La classe **MDM \_ PassportForWork \_ Remote03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4f23f-115">The **MDM\_PassportForWork\_Remote03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f23f-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4f23f-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f23f-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f23f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f23f-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f23f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f23f-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4f23f-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4f23f-120">Nodo interno per la definizione di criteri remoti di Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="4f23f-120">Interior node for defining remote Windows Hello for Business policies.</span></span> <span data-ttu-id="4f23f-121">Questo nodo è stato aggiunto in Windows 10, versione 1511.</span><span class="sxs-lookup"><span data-stu-id="4f23f-121">This node was added in Windows 10, version 1511.</span></span>

</dd> <dt>

<span data-ttu-id="4f23f-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4f23f-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f23f-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f23f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f23f-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f23f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f23f-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4f23f-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4f23f-126">Nodo per la definizione delle impostazioni dei criteri di Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="4f23f-126">Node for defining the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

[<span data-ttu-id="4f23f-127">UseRemotePassport</span><span class="sxs-lookup"><span data-stu-id="4f23f-127">UseRemotePassport</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f23f-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4f23f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f23f-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4f23f-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f23f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f23f-130">Requirements</span></span>



| <span data-ttu-id="4f23f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f23f-131">Requirement</span></span> | <span data-ttu-id="4f23f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4f23f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f23f-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f23f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4f23f-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4f23f-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f23f-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f23f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4f23f-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4f23f-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4f23f-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f23f-137">Namespace</span></span><br/>                | <span data-ttu-id="4f23f-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="4f23f-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4f23f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4f23f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f23f-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f23f-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f23f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4f23f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f23f-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f23f-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f23f-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f23f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f23f-144">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="4f23f-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

