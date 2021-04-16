---
title: Classe MDM_Policy_User_Result01_AttachmentManager02
description: La \_ \_ classe Result01 AttachmentManager02 utente dei criteri MDM \_ \_ rappresenta i criteri di gestione degli allegati disponibili.
ms.assetid: c6cfec0d-24f8-4356-a12b-d9b9944776a7
keywords:
- Classe MDM_Policy_User_Result01_AttachmentManager02
- Classe MDM_Policy_User_Result01_AttachmentManager02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_AttachmentManager02
- MDM_Policy_User_Result01_AttachmentManager02.InstanceID
- MDM_Policy_User_Result01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b78eadb9aa320d35d3a8078359a682536fd7e120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476894"
---
# <a name="mdm_policy_user_result01_attachmentmanager02-class"></a><span data-ttu-id="af3ea-105">\_Utente criteri \_ MDM \_ Result01 \_ classe AttachmentManager02</span><span class="sxs-lookup"><span data-stu-id="af3ea-105">MDM\_Policy\_User\_Result01\_AttachmentManager02 class</span></span>

<span data-ttu-id="af3ea-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="af3ea-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="af3ea-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="af3ea-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="af3ea-108">La \_ \_ classe Result01 AttachmentManager02 utente dei criteri MDM \_ \_ rappresenta i criteri di gestione degli allegati disponibili.</span><span class="sxs-lookup"><span data-stu-id="af3ea-108">The MDM\_Policy\_User\_Result01\_AttachmentManager02 class represents the available attachment manager policies.</span></span>

<span data-ttu-id="af3ea-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="af3ea-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="af3ea-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af3ea-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a><span data-ttu-id="af3ea-111">Members</span><span class="sxs-lookup"><span data-stu-id="af3ea-111">Members</span></span>

<span data-ttu-id="af3ea-112">La **classe \_ \_ \_ Result01 \_ AttachmentManager02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af3ea-112">The **MDM\_Policy\_User\_Result01\_AttachmentManager02** class has these types of members:</span></span>

-   [<span data-ttu-id="af3ea-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af3ea-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af3ea-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af3ea-114">Properties</span></span>

<span data-ttu-id="af3ea-115">La **classe \_ \_ \_ Result01 \_ AttachmentManager02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="af3ea-115">The **MDM\_Policy\_User\_Result01\_AttachmentManager02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="af3ea-116">DoNotPreserveZoneInformation</span><span class="sxs-lookup"><span data-stu-id="af3ea-116">DoNotPreserveZoneInformation</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="af3ea-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af3ea-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af3ea-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="af3ea-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="af3ea-119">HideZoneInfoMechanism</span><span class="sxs-lookup"><span data-stu-id="af3ea-119">HideZoneInfoMechanism</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
</dt> <dd> <dl> <dt>

<span data-ttu-id="af3ea-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af3ea-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af3ea-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="af3ea-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="af3ea-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="af3ea-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af3ea-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af3ea-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af3ea-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af3ea-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af3ea-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="af3ea-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="af3ea-126">NotifyAntivirusPrograms</span><span class="sxs-lookup"><span data-stu-id="af3ea-126">NotifyAntivirusPrograms</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="af3ea-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af3ea-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af3ea-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="af3ea-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="af3ea-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="af3ea-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af3ea-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="af3ea-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af3ea-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af3ea-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af3ea-132">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="af3ea-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af3ea-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af3ea-133">Requirements</span></span>



| <span data-ttu-id="af3ea-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="af3ea-134">Requirement</span></span> | <span data-ttu-id="af3ea-135">Valore</span><span class="sxs-lookup"><span data-stu-id="af3ea-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af3ea-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af3ea-136">Minimum supported client</span></span><br/> | <span data-ttu-id="af3ea-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="af3ea-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af3ea-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af3ea-138">Minimum supported server</span></span><br/> | <span data-ttu-id="af3ea-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af3ea-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="af3ea-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af3ea-140">Namespace</span></span><br/>                | <span data-ttu-id="af3ea-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="af3ea-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="af3ea-142">MOF</span><span class="sxs-lookup"><span data-stu-id="af3ea-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af3ea-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af3ea-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="af3ea-144">DLL</span><span class="sxs-lookup"><span data-stu-id="af3ea-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af3ea-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af3ea-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

