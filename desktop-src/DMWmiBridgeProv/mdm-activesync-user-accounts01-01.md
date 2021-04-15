---
title: Classe MDM_ActiveSync_User_Accounts01_01
description: La \_ classe MDM ActiveSync \_ User \_ Accounts01 \_ 01 definisce tutti gli account ActiveSync disponibili.
ms.assetid: bcd1fdcb-675a-4833-9d3c-0509e68f7b00
keywords:
- Classe MDM_ActiveSync_User_Accounts01_01
- Classe MDM_ActiveSync_User_Accounts01_01, descritta
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01.InstanceID
- MDM_ActiveSync_User_Accounts01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a065fb3f33e69b636a35fc848e5d717898f1fa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476288"
---
# <a name="mdm_activesync_user_accounts01_01-class"></a><span data-ttu-id="417d6-105">\_Classe MDM ActiveSync \_ User \_ Accounts01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="417d6-105">MDM\_ActiveSync\_User\_Accounts01\_01 class</span></span>

<span data-ttu-id="417d6-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="417d6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="417d6-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="417d6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="417d6-108">La classe **MDM \_ ActiveSync \_ User \_ Accounts01 \_ 01** definisce tutti gli account ActiveSync disponibili.</span><span class="sxs-lookup"><span data-stu-id="417d6-108">The **MDM\_ActiveSync\_User\_Accounts01\_01** class defines all available ActiveSync accounts.</span></span>

<span data-ttu-id="417d6-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="417d6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="417d6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="417d6-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Accounts01_01
{
  string InstanceID;
  string ParentID;
  string EmailAddress;
  string Domain;
  string AccountIcon;
  string AccountType;
  string AccountName;
  string Password;
  string ServerName;
  string UserName;
};
```

## <a name="members"></a><span data-ttu-id="417d6-111">Members</span><span class="sxs-lookup"><span data-stu-id="417d6-111">Members</span></span>

<span data-ttu-id="417d6-112">La classe **MDM \_ ActiveSync \_ User \_ Accounts01 \_ 01** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="417d6-112">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="417d6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="417d6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="417d6-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="417d6-114">Properties</span></span>

<span data-ttu-id="417d6-115">La classe **MDM \_ ActiveSync \_ User \_ Accounts01 \_ 01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="417d6-115">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="417d6-116">AccountIcon</span><span class="sxs-lookup"><span data-stu-id="417d6-116">AccountIcon</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounticon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="417d6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="417d6-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="417d6-119">AccountName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accountname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="417d6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="417d6-122">AccountType</span><span class="sxs-lookup"><span data-stu-id="417d6-122">AccountType</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounttype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="417d6-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="417d6-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="417d6-125">Domain</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-domain)
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="417d6-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="417d6-128">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="417d6-128">EmailAddress</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-emailaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="417d6-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="417d6-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="417d6-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="417d6-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417d6-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="417d6-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="417d6-135">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="417d6-135">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="417d6-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="417d6-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="417d6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="417d6-139">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="417d6-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="417d6-140">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="417d6-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="417d6-141">Per questa classe la stringa è "./Vendor/MSFT/ActiveSync/"</span><span class="sxs-lookup"><span data-stu-id="417d6-141">For this class, the string is "./Vendor/MSFT/ActiveSync/"</span></span>

</dd> <dt>

[<span data-ttu-id="417d6-142">Password</span><span class="sxs-lookup"><span data-stu-id="417d6-142">Password</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="417d6-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="417d6-145">ServerName</span><span class="sxs-lookup"><span data-stu-id="417d6-145">ServerName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-servername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="417d6-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="417d6-148">UserName</span><span class="sxs-lookup"><span data-stu-id="417d6-148">UserName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="417d6-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="417d6-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="417d6-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="417d6-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="417d6-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="417d6-151">Requirements</span></span>



| <span data-ttu-id="417d6-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="417d6-152">Requirement</span></span> | <span data-ttu-id="417d6-153">Valore</span><span class="sxs-lookup"><span data-stu-id="417d6-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="417d6-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="417d6-154">Minimum supported client</span></span><br/> | <span data-ttu-id="417d6-155">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="417d6-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="417d6-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="417d6-156">Minimum supported server</span></span><br/> | <span data-ttu-id="417d6-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="417d6-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="417d6-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="417d6-158">Namespace</span></span><br/>                | <span data-ttu-id="417d6-159">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="417d6-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="417d6-160">MOF</span><span class="sxs-lookup"><span data-stu-id="417d6-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="417d6-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="417d6-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="417d6-162">DLL</span><span class="sxs-lookup"><span data-stu-id="417d6-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="417d6-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="417d6-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="417d6-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="417d6-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="417d6-165">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="417d6-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

