---
title: Metodo ModifyPermissions della classe Win32_TSAccount
description: Imposta un'autorizzazione per l'account specificato.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ModifyPermissions
- Metodo ModifyPermissions Servizi Desktop remoto, classe Win32_TSAccount
- Classe Win32_TSAccount Servizi Desktop remoto, metodo ModifyPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bf6147c215475314f65bb8fa426442884bc82e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301509"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="35a89-106">Metodo ModifyPermissions della \_ classe TSAccount Win32</span><span class="sxs-lookup"><span data-stu-id="35a89-106">ModifyPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="35a89-107">Imposta un'autorizzazione per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="35a89-107">Sets a permission for the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a89-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35a89-108">Syntax</span></span>


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a><span data-ttu-id="35a89-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="35a89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a89-110">*PermissionMask* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a89-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a89-111">[Autorizzazione host sessione Desktop remoto](terminal-services-permissions.md) da impostare.</span><span class="sxs-lookup"><span data-stu-id="35a89-111">The [Remote Desktop Session Host Permission](terminal-services-permissions.md) to set.</span></span>

<span data-ttu-id="35a89-112">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="35a89-112">The possible values are:</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="35a89-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_ QUERY** (0)</span><span class="sxs-lookup"><span data-stu-id="35a89-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-114">Autorizzazione per eseguire query sulle informazioni relative a una sessione.</span><span class="sxs-lookup"><span data-stu-id="35a89-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="35a89-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ IMPOSTA** (1)</span><span class="sxs-lookup"><span data-stu-id="35a89-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-116">Autorizzazione per la modifica dei parametri di connessione.</span><span class="sxs-lookup"><span data-stu-id="35a89-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="35a89-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ Reimposta** (6)</span><span class="sxs-lookup"><span data-stu-id="35a89-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-118">Autorizzazione per reimpostare o terminare una sessione o una connessione.</span><span class="sxs-lookup"><span data-stu-id="35a89-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="35a89-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ \| Diritti standard \_ virtuali \_ richiesti** (3)</span><span class="sxs-lookup"><span data-stu-id="35a89-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-120">Autorizzazione per l'utilizzo di canali virtuali.</span><span class="sxs-lookup"><span data-stu-id="35a89-120">Permission to use virtual channels.</span></span> <span data-ttu-id="35a89-121">I canali virtuali forniscono l'accesso da un programma server ai dispositivi client.</span><span class="sxs-lookup"><span data-stu-id="35a89-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="35a89-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ OMBREGGIAtura** (4)</span><span class="sxs-lookup"><span data-stu-id="35a89-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-123">Autorizzazione per nascondere o controllare in modalità remota la sessione di un altro utente.</span><span class="sxs-lookup"><span data-stu-id="35a89-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="35a89-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ ACCESSO** (5)</span><span class="sxs-lookup"><span data-stu-id="35a89-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-125">Autorizzazione per accedere a una sessione nel server.</span><span class="sxs-lookup"><span data-stu-id="35a89-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="35a89-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ Disconnessione** (2)</span><span class="sxs-lookup"><span data-stu-id="35a89-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-127">Autorizzazione per disconnettere un utente da una sessione.</span><span class="sxs-lookup"><span data-stu-id="35a89-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="35a89-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MESSAGGIO** (7)</span><span class="sxs-lookup"><span data-stu-id="35a89-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-129">Autorizzazione per l'invio di un messaggio alla sessione di un altro utente.</span><span class="sxs-lookup"><span data-stu-id="35a89-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="35a89-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ Connetti** (8)</span><span class="sxs-lookup"><span data-stu-id="35a89-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-131">Autorizzazione per la connessione a un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="35a89-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="35a89-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ Disconnetti** (9)</span><span class="sxs-lookup"><span data-stu-id="35a89-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="35a89-133">Autorizzazione per disconnettere una sessione.</span><span class="sxs-lookup"><span data-stu-id="35a89-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="35a89-134">*Consenti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a89-134">*Allow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a89-135">Specifica se l'autorizzazione nel parametro *PermissionMask* è consentita o negata.</span><span class="sxs-lookup"><span data-stu-id="35a89-135">Specifies whether the permission in the *PermissionMask* parameter is allowed or denied.</span></span>

<span data-ttu-id="35a89-136">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="35a89-136">The possible values are:</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="35a89-137"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="35a89-137"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="35a89-138">Il set di autorizzazioni specificato è consentito.</span><span class="sxs-lookup"><span data-stu-id="35a89-138">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="35a89-139"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="35a89-139"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="35a89-140">Il set di autorizzazioni specificato è stato negato.</span><span class="sxs-lookup"><span data-stu-id="35a89-140">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a89-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35a89-141">Return value</span></span>

<span data-ttu-id="35a89-142">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="35a89-142">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="35a89-143">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="35a89-143">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a89-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="35a89-144">Remarks</span></span>

<span data-ttu-id="35a89-145">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="35a89-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="35a89-146">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="35a89-146">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="35a89-147">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="35a89-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="35a89-148">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="35a89-148">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="35a89-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35a89-149">Requirements</span></span>



| <span data-ttu-id="35a89-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a89-150">Requirement</span></span> | <span data-ttu-id="35a89-151">Valore</span><span class="sxs-lookup"><span data-stu-id="35a89-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35a89-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a89-152">Minimum supported client</span></span><br/> | <span data-ttu-id="35a89-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35a89-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35a89-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a89-154">Minimum supported server</span></span><br/> | <span data-ttu-id="35a89-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35a89-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35a89-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35a89-156">Namespace</span></span><br/>                | <span data-ttu-id="35a89-157">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="35a89-157">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="35a89-158">MOF</span><span class="sxs-lookup"><span data-stu-id="35a89-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35a89-159"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35a89-159"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="35a89-160">DLL</span><span class="sxs-lookup"><span data-stu-id="35a89-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a89-161"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a89-161"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a89-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35a89-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a89-163">**\_TSAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="35a89-163">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

