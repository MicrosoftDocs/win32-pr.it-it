---
title: Classe MDM_Policy_User_Result01_Education02
description: La \_ \_ classe Result01 Education02 dell'utente dei criteri MDM \_ \_ rappresenta i criteri di istruzione.
ms.assetid: 34dcc478-5f39-4e1a-908b-46cbbf2ff4fd
keywords:
- Classe MDM_Policy_User_Result01_Education02
- Classe MDM_Policy_User_Result01_Education02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Education02
- MDM_Policy_User_Result01_Education02.InstanceID
- MDM_Policy_User_Result01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ce82ae1131287ec04c77e084e822609a0e0ab07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400655"
---
# <a name="mdm_policy_user_result01_education02-class"></a><span data-ttu-id="b65b7-105">\_Utente criteri \_ MDM \_ Result01 \_ classe Education02</span><span class="sxs-lookup"><span data-stu-id="b65b7-105">MDM\_Policy\_User\_Result01\_Education02 class</span></span>

<span data-ttu-id="b65b7-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b65b7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b65b7-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b65b7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b65b7-108">La \_ \_ classe Result01 Education02 dell'utente dei criteri MDM \_ \_ rappresenta i criteri di istruzione.</span><span class="sxs-lookup"><span data-stu-id="b65b7-108">The MDM\_Policy\_User\_Result01\_Education02 class represents the education policies.</span></span>

<span data-ttu-id="b65b7-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b65b7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b65b7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b65b7-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a><span data-ttu-id="b65b7-111">Members</span><span class="sxs-lookup"><span data-stu-id="b65b7-111">Members</span></span>

<span data-ttu-id="b65b7-112">La **classe \_ \_ \_ Result01 \_ Education02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b65b7-112">The **MDM\_Policy\_User\_Result01\_Education02** class has these types of members:</span></span>

-   [<span data-ttu-id="b65b7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b65b7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b65b7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b65b7-114">Properties</span></span>

<span data-ttu-id="b65b7-115">La **classe \_ \_ \_ Result01 \_ Education02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b65b7-115">The **MDM\_Policy\_User\_Result01\_Education02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b65b7-116">DefaultPrinterName</span><span class="sxs-lookup"><span data-stu-id="b65b7-116">DefaultPrinterName</span></span>](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b65b7-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b65b7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b65b7-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b65b7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b65b7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b65b7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b65b7-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b65b7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b65b7-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b65b7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b65b7-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b65b7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b65b7-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b65b7-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b65b7-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b65b7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b65b7-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b65b7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b65b7-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b65b7-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b65b7-127">PreventAddingNewPrinters</span><span class="sxs-lookup"><span data-stu-id="b65b7-127">PreventAddingNewPrinters</span></span>](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b65b7-128">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b65b7-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b65b7-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b65b7-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b65b7-130">PrinterNames</span><span class="sxs-lookup"><span data-stu-id="b65b7-130">PrinterNames</span></span>](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b65b7-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b65b7-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b65b7-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b65b7-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b65b7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b65b7-133">Requirements</span></span>



| <span data-ttu-id="b65b7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b65b7-134">Requirement</span></span> | <span data-ttu-id="b65b7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b65b7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b65b7-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b65b7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b65b7-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b65b7-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b65b7-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b65b7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b65b7-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b65b7-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b65b7-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b65b7-140">Namespace</span></span><br/>                | <span data-ttu-id="b65b7-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b65b7-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b65b7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b65b7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b65b7-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b65b7-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b65b7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b65b7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b65b7-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b65b7-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

