---
title: Classe MDM_EnterpriseAPN_Settings01
description: La \_ classe MDM EnterpriseAPN \_ Settings01 viene usata dall'azienda per modificare le impostazioni globali di APN.
ms.assetid: 3f2d3d38-c389-4945-b519-5f2d7dedb86c
keywords:
- Classe MDM_EnterpriseAPN_Settings01
- Classe MDM_EnterpriseAPN_Settings01, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01.InstanceID
- MDM_EnterpriseAPN_Settings01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74704451790690df8f9cc11fec8bc1ed80d3c2dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120646"
---
# <a name="mdm_enterpriseapn_settings01-class"></a><span data-ttu-id="6202d-105">\_Classe MDM EnterpriseAPN \_ Settings01</span><span class="sxs-lookup"><span data-stu-id="6202d-105">MDM\_EnterpriseAPN\_Settings01 class</span></span>

<span data-ttu-id="6202d-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="6202d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6202d-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="6202d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6202d-108">La classe **MDM \_ EnterpriseAPN \_ Settings01** viene usata dall'azienda per modificare le impostazioni globali di APN.</span><span class="sxs-lookup"><span data-stu-id="6202d-108">The **MDM\_EnterpriseAPN\_Settings01** class is used by the enterprise to change APN global settings.</span></span>

<span data-ttu-id="6202d-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6202d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6202d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6202d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_Settings01
{
  string  InstanceID;
  string  ParentID;
  boolean AllowUserControl;
  boolean HideView;
};
```

## <a name="members"></a><span data-ttu-id="6202d-111">Members</span><span class="sxs-lookup"><span data-stu-id="6202d-111">Members</span></span>

<span data-ttu-id="6202d-112">La classe **MDM \_ EnterpriseAPN \_ Settings01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6202d-112">The **MDM\_EnterpriseAPN\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="6202d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6202d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6202d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6202d-114">Properties</span></span>

<span data-ttu-id="6202d-115">La classe **MDM \_ EnterpriseAPN \_ Settings01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6202d-115">The **MDM\_EnterpriseAPN\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6202d-116">AllowUserControl</span><span class="sxs-lookup"><span data-stu-id="6202d-116">AllowUserControl</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-allowusercontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-117">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6202d-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6202d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6202d-119">HideView</span><span class="sxs-lookup"><span data-stu-id="6202d-119">HideView</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-hideview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6202d-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6202d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6202d-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6202d-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6202d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6202d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6202d-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6202d-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6202d-126">Nodo che contiene le impostazioni globali APN.</span><span class="sxs-lookup"><span data-stu-id="6202d-126">Node that contains APN global settings.</span></span>

</dd> <dt>

<span data-ttu-id="6202d-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6202d-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202d-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6202d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6202d-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6202d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6202d-130">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6202d-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6202d-131">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="6202d-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="6202d-132">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseAPN/Settings"</span><span class="sxs-lookup"><span data-stu-id="6202d-132">For this class, the string is "./Vendor/MSFT/EnterpriseAPN/Settings"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6202d-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6202d-133">Requirements</span></span>



| <span data-ttu-id="6202d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6202d-134">Requirement</span></span> | <span data-ttu-id="6202d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6202d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6202d-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6202d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6202d-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6202d-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6202d-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6202d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6202d-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6202d-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6202d-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6202d-140">Namespace</span></span><br/>                | <span data-ttu-id="6202d-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="6202d-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6202d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6202d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6202d-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6202d-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6202d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6202d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6202d-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6202d-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

