---
title: Classe MDM_Policy_Result01_DataUsage02
description: La \_ \_ classe Result01 DataUsage02 dei criteri MDM \_ rappresenta i criteri di utilizzo dei dati disponibili.
ms.assetid: 4efcab61-2060-44dc-bc3c-7b23802fa284
keywords:
- Classe MDM_Policy_Result01_DataUsage02
- Classe MDM_Policy_Result01_DataUsage02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DataUsage02
- MDM_Policy_Result01_DataUsage02.InstanceID
- MDM_Policy_Result01_DataUsage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d97bcfba122bd3d974025975a69ba6a5be9c8ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478053"
---
# <a name="mdm_policy_result01_datausage02-class"></a><span data-ttu-id="8cca4-105">\_ \_ Classe Result01 DataUsage02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="8cca4-105">MDM\_Policy\_Result01\_DataUsage02 class</span></span>

<span data-ttu-id="8cca4-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="8cca4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8cca4-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="8cca4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8cca4-108">La \_ \_ classe Result01 DataUsage02 dei criteri MDM \_ rappresenta i criteri di utilizzo dei dati disponibili.</span><span class="sxs-lookup"><span data-stu-id="8cca4-108">The MDM\_Policy\_Result01\_DataUsage02 class represents the available data usage policies.</span></span>

<span data-ttu-id="8cca4-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8cca4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cca4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8cca4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DataUsage02
{
  string InstanceID;
  string ParentID;
  string SetCost3G;
  string SetCost4G;
};
```

## <a name="members"></a><span data-ttu-id="8cca4-111">Members</span><span class="sxs-lookup"><span data-stu-id="8cca4-111">Members</span></span>

<span data-ttu-id="8cca4-112">La **classe \_ \_ Result01 \_ DataUsage02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8cca4-112">The **MDM\_Policy\_Result01\_DataUsage02** class has these types of members:</span></span>

-   [<span data-ttu-id="8cca4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8cca4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8cca4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8cca4-114">Properties</span></span>

<span data-ttu-id="8cca4-115">La **classe \_ \_ \_ DataUsage02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8cca4-115">The **MDM\_Policy\_Result01\_DataUsage02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8cca4-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8cca4-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cca4-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8cca4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cca4-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8cca4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cca4-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8cca4-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8cca4-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8cca4-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cca4-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8cca4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cca4-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8cca4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8cca4-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8cca4-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8cca4-124">SetCost3G</span><span class="sxs-lookup"><span data-stu-id="8cca4-124">SetCost3G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost3g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cca4-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8cca4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cca4-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8cca4-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8cca4-127">SetCost4G</span><span class="sxs-lookup"><span data-stu-id="8cca4-127">SetCost4G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost4g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cca4-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8cca4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8cca4-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8cca4-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8cca4-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cca4-130">Requirements</span></span>



| <span data-ttu-id="8cca4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cca4-131">Requirement</span></span> | <span data-ttu-id="8cca4-132">Valore</span><span class="sxs-lookup"><span data-stu-id="8cca4-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cca4-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cca4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8cca4-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8cca4-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8cca4-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cca4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8cca4-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8cca4-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8cca4-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8cca4-137">Namespace</span></span><br/>                | <span data-ttu-id="8cca4-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="8cca4-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8cca4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8cca4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cca4-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8cca4-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cca4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8cca4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cca4-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cca4-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

