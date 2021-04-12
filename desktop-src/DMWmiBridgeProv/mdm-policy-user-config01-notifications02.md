---
title: Classe MDM_Policy_User_Config01_Notifications02
description: La \_ classe del criterio MDM \_ utente \_ Config01 \_ Notifications02 rappresenta i criteri di notifica disponibili.
ms.assetid: da70b3b4-e8ed-4784-ad6b-52e152a8b78f
keywords:
- Classe MDM_Policy_User_Config01_Notifications02
- Classe MDM_Policy_User_Config01_Notifications02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Notifications02
- MDM_Policy_User_Config01_Notifications02.InstanceID
- MDM_Policy_User_Config01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c85dcd9a622d29baf6d7c8f28d9e72b68998ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119899"
---
# <a name="mdm_policy_user_config01_notifications02-class"></a><span data-ttu-id="a6e99-105">\_Utente criteri \_ MDM \_ Config01 \_ classe Notifications02</span><span class="sxs-lookup"><span data-stu-id="a6e99-105">MDM\_Policy\_User\_Config01\_Notifications02 class</span></span>

<span data-ttu-id="a6e99-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="a6e99-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a6e99-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="a6e99-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a6e99-108">La classe del **\_ criterio MDM \_ utente \_ Config01 \_ Notifications02** rappresenta i criteri di notifica disponibili.</span><span class="sxs-lookup"><span data-stu-id="a6e99-108">The **MDM\_Policy\_User\_Config01\_Notifications02** class represents the notification policies available.</span></span>

<span data-ttu-id="a6e99-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a6e99-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e99-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6e99-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a><span data-ttu-id="a6e99-111">Members</span><span class="sxs-lookup"><span data-stu-id="a6e99-111">Members</span></span>

<span data-ttu-id="a6e99-112">La **classe \_ \_ \_ Config01 \_ Notifications02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a6e99-112">The **MDM\_Policy\_User\_Config01\_Notifications02** class has these types of members:</span></span>

-   [<span data-ttu-id="a6e99-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6e99-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6e99-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6e99-114">Properties</span></span>

<span data-ttu-id="a6e99-115">La **classe \_ \_ \_ Config01 \_ Notifications02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a6e99-115">The **MDM\_Policy\_User\_Config01\_Notifications02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a6e99-116">DisallowNotificationMirroring</span><span class="sxs-lookup"><span data-stu-id="a6e99-116">DisallowNotificationMirroring</span></span>](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e99-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a6e99-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6e99-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a6e99-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a6e99-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a6e99-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e99-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6e99-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e99-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6e99-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e99-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a6e99-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a6e99-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="a6e99-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="a6e99-124">Per questa classe la stringa è "Notifications".</span><span class="sxs-lookup"><span data-stu-id="a6e99-124">For this class, the string is "Notifications".</span></span>

</dd> <dt>

<span data-ttu-id="a6e99-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a6e99-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6e99-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6e99-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6e99-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6e99-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6e99-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a6e99-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a6e99-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="a6e99-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="a6e99-130">Per questa classe la stringa è "./User/Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="a6e99-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6e99-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6e99-131">Requirements</span></span>



| <span data-ttu-id="a6e99-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6e99-132">Requirement</span></span> | <span data-ttu-id="a6e99-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a6e99-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e99-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6e99-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a6e99-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a6e99-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a6e99-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6e99-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a6e99-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a6e99-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="a6e99-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6e99-138">Namespace</span></span><br/>                | <span data-ttu-id="a6e99-139">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="a6e99-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="a6e99-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a6e99-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6e99-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6e99-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="a6e99-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a6e99-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6e99-143"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a6e99-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

