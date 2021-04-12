---
title: Classe MDM_Policy_User_Result01_ApplicationManagement02
description: La \_ classe del criterio MDM \_ utente \_ Result01 \_ ApplicationManagement02 rappresenta i criteri di avvio disponibili impostati per ogni singolo utente.
ms.assetid: 62545af1-9c26-481e-9668-cd253cf592e7
keywords:
- Classe MDM_Policy_User_Result01_ApplicationManagement02
- Classe MDM_Policy_User_Result01_ApplicationManagement02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_ApplicationManagement02
- MDM_Policy_User_Result01_ApplicationManagement02.InstanceID
- MDM_Policy_User_Result01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18177046691e5c9fe5ca8cb61ee0518a41533c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119890"
---
# <a name="mdm_policy_user_result01_applicationmanagement02-class"></a><span data-ttu-id="bf2af-105">\_Utente criteri \_ MDM \_ Result01 \_ classe ApplicationManagement02</span><span class="sxs-lookup"><span data-stu-id="bf2af-105">MDM\_Policy\_User\_Result01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="bf2af-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="bf2af-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bf2af-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="bf2af-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bf2af-108">La classe del **\_ criterio MDM \_ utente \_ Result01 \_ ApplicationManagement02** rappresenta i criteri di avvio disponibili impostati per ogni singolo utente.</span><span class="sxs-lookup"><span data-stu-id="bf2af-108">The **MDM\_Policy\_User\_Result01\_ApplicationManagement02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="bf2af-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bf2af-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2af-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf2af-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 RequirePrivateStoreOnly;
};
```

## <a name="members"></a><span data-ttu-id="bf2af-111">Members</span><span class="sxs-lookup"><span data-stu-id="bf2af-111">Members</span></span>

<span data-ttu-id="bf2af-112">La **classe \_ \_ \_ Result01 \_ ApplicationManagement02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bf2af-112">The **MDM\_Policy\_User\_Result01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="bf2af-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bf2af-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf2af-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bf2af-114">Properties</span></span>

<span data-ttu-id="bf2af-115">La **classe \_ \_ \_ Result01 \_ ApplicationManagement02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bf2af-115">The **MDM\_Policy\_User\_Result01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf2af-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bf2af-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf2af-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bf2af-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf2af-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf2af-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf2af-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf2af-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf2af-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="bf2af-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="bf2af-121">Per questa classe la stringa è "ApplicationManagement"</span><span class="sxs-lookup"><span data-stu-id="bf2af-121">For this class, the string is "ApplicationManagement"</span></span>

</dd> <dt>

<span data-ttu-id="bf2af-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bf2af-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf2af-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bf2af-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf2af-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf2af-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf2af-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf2af-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf2af-126">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="bf2af-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="bf2af-127">Per questa classe la stringa è "./User/Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="bf2af-127">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="bf2af-128">RequirePrivateStoreOnly</span><span class="sxs-lookup"><span data-stu-id="bf2af-128">RequirePrivateStoreOnly</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf2af-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf2af-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf2af-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bf2af-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf2af-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf2af-131">Requirements</span></span>



| <span data-ttu-id="bf2af-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf2af-132">Requirement</span></span> | <span data-ttu-id="bf2af-133">Valore</span><span class="sxs-lookup"><span data-stu-id="bf2af-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2af-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf2af-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2af-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bf2af-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf2af-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf2af-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2af-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bf2af-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bf2af-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bf2af-138">Namespace</span></span><br/>                | <span data-ttu-id="bf2af-139">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="bf2af-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bf2af-140">MOF</span><span class="sxs-lookup"><span data-stu-id="bf2af-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf2af-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf2af-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf2af-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bf2af-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf2af-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf2af-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2af-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf2af-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2af-145">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="bf2af-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

