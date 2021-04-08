---
title: Classe MDM_Policy_User_Result01_Notifications02
description: La \_ classe del criterio MDM \_ utente \_ Result01 \_ Notifications02 rappresenta i criteri di notifica disponibili.
ms.assetid: a2da74f3-2585-4c8c-abab-751ba4c708a1
keywords:
- Classe MDM_Policy_User_Result01_Notifications02
- Classe MDM_Policy_User_Result01_Notifications02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Notifications02
- MDM_Policy_User_Result01_Notifications02.InstanceID
- MDM_Policy_User_Result01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c917e42ef568783b1c804ce17d52474a86359e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047904"
---
# <a name="mdm_policy_user_result01_notifications02-class"></a><span data-ttu-id="1d1c2-105">\_Utente criteri \_ MDM \_ Result01 \_ classe Notifications02</span><span class="sxs-lookup"><span data-stu-id="1d1c2-105">MDM\_Policy\_User\_Result01\_Notifications02 class</span></span>

<span data-ttu-id="1d1c2-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="1d1c2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1d1c2-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="1d1c2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1d1c2-108">La classe del **\_ criterio MDM \_ utente \_ Result01 \_ Notifications02** rappresenta i criteri di notifica disponibili.</span><span class="sxs-lookup"><span data-stu-id="1d1c2-108">The **MDM\_Policy\_User\_Result01\_Notifications02** class represents the notification policies available.</span></span>

<span data-ttu-id="1d1c2-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1d1c2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d1c2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d1c2-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a><span data-ttu-id="1d1c2-111">Members</span><span class="sxs-lookup"><span data-stu-id="1d1c2-111">Members</span></span>

<span data-ttu-id="1d1c2-112">La **classe \_ \_ \_ Result01 \_ Notifications02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1d1c2-112">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these types of members:</span></span>

-   [<span data-ttu-id="1d1c2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d1c2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d1c2-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d1c2-114">Properties</span></span>

<span data-ttu-id="1d1c2-115">La **classe \_ \_ \_ Result01 \_ Notifications02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d1c2-115">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1d1c2-116">DisallowNotificationMirroring</span><span class="sxs-lookup"><span data-stu-id="1d1c2-116">DisallowNotificationMirroring</span></span>](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1c2-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1d1c2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d1c2-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1d1c2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d1c2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1d1c2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1c2-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d1c2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1c2-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d1c2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d1c2-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d1c2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1d1c2-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="1d1c2-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="1d1c2-124">Per questa classe la stringa è "Notifications".</span><span class="sxs-lookup"><span data-stu-id="1d1c2-124">For this class, the string is "Notifications".</span></span>

</dd> <dt>

<span data-ttu-id="1d1c2-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1d1c2-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1c2-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d1c2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1c2-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d1c2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d1c2-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d1c2-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1d1c2-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="1d1c2-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="1d1c2-130">Per questa classe la stringa è "./User/Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="1d1c2-130">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d1c2-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d1c2-131">Requirements</span></span>



| <span data-ttu-id="1d1c2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d1c2-132">Requirement</span></span> | <span data-ttu-id="1d1c2-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1d1c2-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d1c2-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d1c2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1d1c2-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1d1c2-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1d1c2-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d1c2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1d1c2-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1d1c2-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="1d1c2-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d1c2-138">Namespace</span></span><br/>                | <span data-ttu-id="1d1c2-139">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="1d1c2-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="1d1c2-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1d1c2-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d1c2-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d1c2-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="1d1c2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1d1c2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d1c2-143"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1d1c2-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

