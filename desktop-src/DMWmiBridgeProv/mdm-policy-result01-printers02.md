---
title: Classe MDM_Policy_Result01_Printers02
description: La \_ classe Printers02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di stampa.
ms.assetid: f64fbb03-c62c-4f8e-97ad-e08e068a31d1
keywords:
- Classe MDM_Policy_Result01_Printers02
- Classe MDM_Policy_Result01_Printers02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Printers02
- MDM_Policy_Result01_Printers02.InstanceID
- MDM_Policy_Result01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042820825441928aa04d499a06df3a05ced3889d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400358"
---
# <a name="mdm_policy_result01_printers02-class"></a><span data-ttu-id="965af-105">\_ \_ Classe Result01 Printers02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="965af-105">MDM\_Policy\_Result01\_Printers02 class</span></span>

<span data-ttu-id="965af-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="965af-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="965af-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="965af-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="965af-108">La \_ classe Printers02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di stampa.</span><span class="sxs-lookup"><span data-stu-id="965af-108">The MDM\_Policy\_Result01\_Printers02 class represents the printer policies.</span></span>

<span data-ttu-id="965af-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="965af-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="965af-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="965af-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions;
  string PublishPrinters;
};
```

## <a name="members"></a><span data-ttu-id="965af-111">Members</span><span class="sxs-lookup"><span data-stu-id="965af-111">Members</span></span>

<span data-ttu-id="965af-112">La **classe \_ \_ Result01 \_ Printers02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="965af-112">The **MDM\_Policy\_Result01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="965af-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="965af-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="965af-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="965af-114">Properties</span></span>

<span data-ttu-id="965af-115">La **classe \_ \_ \_ Printers02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="965af-115">The **MDM\_Policy\_Result01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="965af-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="965af-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="965af-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965af-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965af-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="965af-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="965af-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="965af-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="965af-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="965af-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="965af-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965af-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965af-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="965af-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="965af-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="965af-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="965af-124">PointAndPrintRestrictions</span><span class="sxs-lookup"><span data-stu-id="965af-124">PointAndPrintRestrictions</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="965af-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965af-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965af-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="965af-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="965af-127">PublishPrinters</span><span class="sxs-lookup"><span data-stu-id="965af-127">PublishPrinters</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-publishprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="965af-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965af-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965af-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="965af-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="965af-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="965af-130">Requirements</span></span>



| <span data-ttu-id="965af-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="965af-131">Requirement</span></span> | <span data-ttu-id="965af-132">Valore</span><span class="sxs-lookup"><span data-stu-id="965af-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="965af-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="965af-133">Minimum supported client</span></span><br/> | <span data-ttu-id="965af-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="965af-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="965af-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="965af-135">Minimum supported server</span></span><br/> | <span data-ttu-id="965af-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="965af-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="965af-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="965af-137">Namespace</span></span><br/>                | <span data-ttu-id="965af-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="965af-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="965af-139">MOF</span><span class="sxs-lookup"><span data-stu-id="965af-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="965af-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="965af-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="965af-141">DLL</span><span class="sxs-lookup"><span data-stu-id="965af-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="965af-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="965af-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

