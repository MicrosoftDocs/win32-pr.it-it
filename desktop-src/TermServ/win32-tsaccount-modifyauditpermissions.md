---
title: Metodo ModifyAuditPermissions della classe Win32_TSAccount
description: Prepara l'impostazione di un set di autorizzazioni di controllo più granulare per l'account specificato.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ModifyAuditPermissions
- Metodo ModifyAuditPermissions Servizi Desktop remoto, classe Win32_TSAccount
- Classe Win32_TSAccount Servizi Desktop remoto, metodo ModifyAuditPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874441"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="ede00-106">Metodo ModifyAuditPermissions della \_ classe TSAccount Win32</span><span class="sxs-lookup"><span data-stu-id="ede00-106">ModifyAuditPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="ede00-107">Il metodo **ModifyAuditPermissions** prepara a impostare un set di autorizzazioni di controllo più granulare per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="ede00-107">The **ModifyAuditPermissions** method prepares to set a more granular set of audit permissions to the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede00-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ede00-108">Syntax</span></span>


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a><span data-ttu-id="ede00-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ede00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede00-110">*PermissionMask* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ede00-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede00-111">Set di [host sessione Desktop remoto autorizzazioni](terminal-services-permissions.md) da associare all'account specificato.</span><span class="sxs-lookup"><span data-stu-id="ede00-111">The set of [Remote Desktop Session Host Permissions](terminal-services-permissions.md) to associate with the specified account.</span></span> <span data-ttu-id="ede00-112">Il valore di questo parametro è una bitmap ed è possibile selezionare uno o tutti i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ede00-112">The value of this parameter is a bitmap, and any or all of the following values may be selected.</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="ede00-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_ QUERY** (0)</span><span class="sxs-lookup"><span data-stu-id="ede00-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-114">Autorizzazione per eseguire query sulle informazioni relative a una sessione.</span><span class="sxs-lookup"><span data-stu-id="ede00-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="ede00-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ IMPOSTA** (1)</span><span class="sxs-lookup"><span data-stu-id="ede00-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-116">Autorizzazione per la modifica dei parametri di connessione.</span><span class="sxs-lookup"><span data-stu-id="ede00-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="ede00-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ Reimposta** (6)</span><span class="sxs-lookup"><span data-stu-id="ede00-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-118">Autorizzazione per reimpostare o terminare una sessione o una connessione.</span><span class="sxs-lookup"><span data-stu-id="ede00-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="ede00-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ \| Diritti standard \_ virtuali \_ richiesti** (3)</span><span class="sxs-lookup"><span data-stu-id="ede00-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-120">Autorizzazione per l'utilizzo di canali virtuali.</span><span class="sxs-lookup"><span data-stu-id="ede00-120">Permission to use virtual channels.</span></span> <span data-ttu-id="ede00-121">I canali virtuali forniscono l'accesso da un programma server ai dispositivi client.</span><span class="sxs-lookup"><span data-stu-id="ede00-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="ede00-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ OMBREGGIAtura** (4)</span><span class="sxs-lookup"><span data-stu-id="ede00-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-123">Autorizzazione per nascondere o controllare in modalità remota la sessione di un altro utente.</span><span class="sxs-lookup"><span data-stu-id="ede00-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="ede00-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ ACCESSO** (5)</span><span class="sxs-lookup"><span data-stu-id="ede00-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-125">Autorizzazione per accedere a una sessione nel server.</span><span class="sxs-lookup"><span data-stu-id="ede00-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="ede00-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ Disconnessione** (2)</span><span class="sxs-lookup"><span data-stu-id="ede00-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-127">Autorizzazione per disconnettere un utente da una sessione.</span><span class="sxs-lookup"><span data-stu-id="ede00-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="ede00-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MESSAGGIO** (7)</span><span class="sxs-lookup"><span data-stu-id="ede00-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-129">Autorizzazione per l'invio di un messaggio alla sessione di un altro utente.</span><span class="sxs-lookup"><span data-stu-id="ede00-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="ede00-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ Connetti** (8)</span><span class="sxs-lookup"><span data-stu-id="ede00-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-131">Autorizzazione per la connessione a un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="ede00-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="ede00-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ Disconnetti** (9)</span><span class="sxs-lookup"><span data-stu-id="ede00-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="ede00-133">Autorizzazione per disconnettere una sessione.</span><span class="sxs-lookup"><span data-stu-id="ede00-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ede00-134">*Operazione riuscita* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ede00-134">*Success* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede00-135">Specifica se il set di autorizzazioni specificato dal valore del parametro *PermissionMask* è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="ede00-135">Specifies if the permission set specified by the value of the *PermissionMask* parameter is allowed or denied.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="ede00-136"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="ede00-136"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="ede00-137">Il set di autorizzazioni specificato è consentito.</span><span class="sxs-lookup"><span data-stu-id="ede00-137">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="ede00-138"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="ede00-138"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="ede00-139">Il set di autorizzazioni specificato è stato negato.</span><span class="sxs-lookup"><span data-stu-id="ede00-139">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede00-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ede00-140">Return value</span></span>

<span data-ttu-id="ede00-141">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="ede00-141">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ede00-142">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ede00-142">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ede00-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="ede00-143">Remarks</span></span>

<span data-ttu-id="ede00-144">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ede00-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ede00-145">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="ede00-145">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ede00-146">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ede00-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ede00-147">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ede00-147">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ede00-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ede00-148">Requirements</span></span>



| <span data-ttu-id="ede00-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="ede00-149">Requirement</span></span> | <span data-ttu-id="ede00-150">Valore</span><span class="sxs-lookup"><span data-stu-id="ede00-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ede00-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ede00-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ede00-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ede00-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ede00-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ede00-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ede00-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ede00-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ede00-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ede00-155">Namespace</span></span><br/>                | <span data-ttu-id="ede00-156">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ede00-156">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ede00-157">MOF</span><span class="sxs-lookup"><span data-stu-id="ede00-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ede00-158"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ede00-158"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ede00-159">DLL</span><span class="sxs-lookup"><span data-stu-id="ede00-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ede00-160"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ede00-160"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ede00-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ede00-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede00-162">**\_TSAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="ede00-162">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

