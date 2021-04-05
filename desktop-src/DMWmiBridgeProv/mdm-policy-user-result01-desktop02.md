---
title: Classe MDM_Policy_User_Result01_Desktop02
description: La \_ \_ classe Result01 Desktop02 utente dei criteri MDM \_ \_ rappresenta i criteri del profilo di cartella disponibili.
ms.assetid: dab89ac4-b857-474e-8fe5-6822fe06ac91
keywords:
- Classe MDM_Policy_User_Result01_Desktop02
- Classe MDM_Policy_User_Result01_Desktop02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Desktop02
- MDM_Policy_User_Result01_Desktop02.InstanceID
- MDM_Policy_User_Result01_Desktop02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da6504176140b9e775c7b7f83e0f9835ce25b42c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048408"
---
# <a name="mdm_policy_user_result01_desktop02-class"></a><span data-ttu-id="455c8-105">\_Utente criteri \_ MDM \_ Result01 \_ classe Desktop02</span><span class="sxs-lookup"><span data-stu-id="455c8-105">MDM\_Policy\_User\_Result01\_Desktop02 class</span></span>

<span data-ttu-id="455c8-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="455c8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="455c8-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="455c8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="455c8-108">La \_ \_ classe Result01 Desktop02 utente dei criteri MDM \_ \_ rappresenta i criteri del profilo di cartella disponibili.</span><span class="sxs-lookup"><span data-stu-id="455c8-108">The MDM\_Policy\_User\_Result01\_Desktop02 class represents the available folder profile policies.</span></span>

<span data-ttu-id="455c8-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="455c8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="455c8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="455c8-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Desktop02
{
  string InstanceID;
  string ParentID;
  string PreventUserRedirectionOfProfileFolders;
};
```

## <a name="members"></a><span data-ttu-id="455c8-111">Members</span><span class="sxs-lookup"><span data-stu-id="455c8-111">Members</span></span>

<span data-ttu-id="455c8-112">La **classe \_ \_ \_ Result01 \_ Desktop02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="455c8-112">The **MDM\_Policy\_User\_Result01\_Desktop02** class has these types of members:</span></span>

-   [<span data-ttu-id="455c8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="455c8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="455c8-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="455c8-114">Properties</span></span>

<span data-ttu-id="455c8-115">La **classe \_ \_ \_ Result01 \_ Desktop02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="455c8-115">The **MDM\_Policy\_User\_Result01\_Desktop02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="455c8-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="455c8-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="455c8-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="455c8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="455c8-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="455c8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="455c8-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="455c8-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="455c8-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="455c8-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="455c8-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="455c8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="455c8-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="455c8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="455c8-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="455c8-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="455c8-124">PreventUserRedirectionOfProfileFolders</span><span class="sxs-lookup"><span data-stu-id="455c8-124">PreventUserRedirectionOfProfileFolders</span></span>](/windows/client-management/mdm/policy-csp-desktop#desktop-preventuserredirectionofprofilefolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="455c8-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="455c8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="455c8-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="455c8-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="455c8-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="455c8-127">Requirements</span></span>



| <span data-ttu-id="455c8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="455c8-128">Requirement</span></span> | <span data-ttu-id="455c8-129">Valore</span><span class="sxs-lookup"><span data-stu-id="455c8-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="455c8-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="455c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="455c8-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="455c8-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="455c8-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="455c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="455c8-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="455c8-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="455c8-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="455c8-134">Namespace</span></span><br/>                | <span data-ttu-id="455c8-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="455c8-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="455c8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="455c8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="455c8-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="455c8-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="455c8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="455c8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="455c8-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="455c8-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

