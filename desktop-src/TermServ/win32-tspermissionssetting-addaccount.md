---
title: Metodo AddAccount della classe Win32_TSPermissionsSetting (Faxcomex. h)
description: Il metodo AddAccount prepara l'aggiunta di un account al terminale con il set di autorizzazioni specificato. È possibile aggiungere utenti, gruppi o computer.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddAccount
- Metodo AddAccount Servizi Desktop remoto, classe Win32_TSPermissionsSetting
- Classe Win32_TSPermissionsSetting Servizi Desktop remoto, metodo AddAccount
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477698"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="0f738-107">Metodo AddAccount della \_ classe TSPermissionsSetting Win32</span><span class="sxs-lookup"><span data-stu-id="0f738-107">AddAccount method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="0f738-108">Il metodo **AddAccount** prepara l'aggiunta di un account al terminale con il set di autorizzazioni specificato.</span><span class="sxs-lookup"><span data-stu-id="0f738-108">The **AddAccount** method prepares to add an account to the terminal with the specified permission set.</span></span> <span data-ttu-id="0f738-109">È possibile aggiungere utenti, gruppi o computer.</span><span class="sxs-lookup"><span data-stu-id="0f738-109">You can add users, groups, or computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f738-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f738-110">Syntax</span></span>


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a><span data-ttu-id="0f738-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f738-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f738-112">*AccountName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f738-112">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f738-113">Nome dell'account da aggiungere al terminale.</span><span class="sxs-lookup"><span data-stu-id="0f738-113">The name of the account to add to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="0f738-114">*PermissionPreSet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f738-114">*PermissionPreSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f738-115">Set di autorizzazioni da associare all'account specificato.</span><span class="sxs-lookup"><span data-stu-id="0f738-115">The set of permissions to associate with the specified account.</span></span> <span data-ttu-id="0f738-116">Questo parametro può essere uno o tutti i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0f738-116">This parameter can be any or all of the following values.</span></span> <span data-ttu-id="0f738-117">Per ulteriori informazioni, vedere [Servizi Desktop remoto autorizzazioni](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="0f738-117">For more information, see [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span data-ttu-id="0f738-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_ \_Accesso Guest** (0)</span><span class="sxs-lookup"><span data-stu-id="0f738-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION\_GUEST\_ACCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0f738-119">L'account dispone di autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="0f738-119">The account has Logon permission.</span></span>

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span data-ttu-id="0f738-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_ \_Accesso utente** (1)</span><span class="sxs-lookup"><span data-stu-id="0f738-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION\_USER\_ACCESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0f738-121">L'account dispone delle autorizzazioni seguenti: accesso, informazioni sulle query, invio del messaggio e connessione.</span><span class="sxs-lookup"><span data-stu-id="0f738-121">The account has the following permissions: Logon, Query Information, Send Message, and Connect.</span></span>

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span data-ttu-id="0f738-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_ Tutti gli \_ accessi** (2)</span><span class="sxs-lookup"><span data-stu-id="0f738-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION\_ALL\_ACCESS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0f738-123">L'account dispone di tutte le autorizzazioni Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0f738-123">The account has all Remote Desktop Services Permissions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f738-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f738-124">Return value</span></span>

<span data-ttu-id="0f738-125">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="0f738-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0f738-126">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0f738-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f738-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f738-127">Remarks</span></span>

<span data-ttu-id="0f738-128">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0f738-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0f738-129">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0f738-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0f738-130">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0f738-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0f738-131">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0f738-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f738-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f738-132">Requirements</span></span>



| <span data-ttu-id="0f738-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f738-133">Requirement</span></span> | <span data-ttu-id="0f738-134">Valore</span><span class="sxs-lookup"><span data-stu-id="0f738-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f738-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f738-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0f738-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f738-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f738-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f738-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0f738-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f738-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f738-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0f738-139">Namespace</span></span><br/>                | <span data-ttu-id="0f738-140">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0f738-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0f738-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f738-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f738-142"><dt>Faxcomex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f738-142"><dt>Faxcomex.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f738-143">MOF</span><span class="sxs-lookup"><span data-stu-id="0f738-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f738-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f738-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f738-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0f738-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f738-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f738-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f738-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f738-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f738-148">**\_TSPermissionsSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="0f738-148">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

