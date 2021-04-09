---
title: Classe MDM_WindowsLicensing_Subscriptions01_01
description: La \_ classe MDM WindowsLicensing \_ Subscriptions01 \_ 01 è progettata per scenari di gestione delle licenze correlati alla sottoscrizione.
ms.assetid: dc3b7eae-89d3-4e66-a65f-f100e23ea9fd
keywords:
- Classe MDM_WindowsLicensing_Subscriptions01_01
- Classe MDM_WindowsLicensing_Subscriptions01_01, descritta
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing_Subscriptions01_01
- MDM_WindowsLicensing_Subscriptions01_01.InstanceID
- MDM_WindowsLicensing_Subscriptions01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911c578bd0e3cbc56c61f2cf85438660e8f437b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120610"
---
# <a name="mdm_windowslicensing_subscriptions01_01-class"></a><span data-ttu-id="b88d8-105">\_Classe MDM WindowsLicensing \_ Subscriptions01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="b88d8-105">MDM\_WindowsLicensing\_Subscriptions01\_01 class</span></span>

<span data-ttu-id="b88d8-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b88d8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b88d8-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b88d8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b88d8-108">La classe **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** è progettata per scenari di gestione delle licenze correlati alla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b88d8-108">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class is designed for subscription-related licensing management scenarios.</span></span>

<span data-ttu-id="b88d8-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b88d8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b88d8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b88d8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing_Subscriptions01_01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="b88d8-111">Members</span><span class="sxs-lookup"><span data-stu-id="b88d8-111">Members</span></span>

<span data-ttu-id="b88d8-112">La classe **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b88d8-112">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="b88d8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b88d8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b88d8-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b88d8-114">Properties</span></span>

<span data-ttu-id="b88d8-115">La classe **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b88d8-115">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b88d8-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b88d8-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b88d8-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b88d8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b88d8-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b88d8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b88d8-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b88d8-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b88d8-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b88d8-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="b88d8-121">Nome</span><span class="sxs-lookup"><span data-stu-id="b88d8-121">Name</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b88d8-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b88d8-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b88d8-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b88d8-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b88d8-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b88d8-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b88d8-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b88d8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b88d8-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b88d8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b88d8-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b88d8-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b88d8-128">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b88d8-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="b88d8-129">Per questa classe la stringa è "./Vendor/MSFT/WindowsLicensing"</span><span class="sxs-lookup"><span data-stu-id="b88d8-129">For this class, the string is "./Vendor/MSFT/WindowsLicensing"</span></span>

</dd> <dt>

[<span data-ttu-id="b88d8-130">Status</span><span class="sxs-lookup"><span data-stu-id="b88d8-130">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b88d8-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b88d8-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b88d8-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b88d8-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b88d8-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b88d8-133">Requirements</span></span>



| <span data-ttu-id="b88d8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b88d8-134">Requirement</span></span> | <span data-ttu-id="b88d8-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b88d8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b88d8-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b88d8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b88d8-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b88d8-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b88d8-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b88d8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b88d8-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b88d8-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b88d8-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b88d8-140">Namespace</span></span><br/>                | <span data-ttu-id="b88d8-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b88d8-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b88d8-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b88d8-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b88d8-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b88d8-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b88d8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b88d8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b88d8-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b88d8-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

