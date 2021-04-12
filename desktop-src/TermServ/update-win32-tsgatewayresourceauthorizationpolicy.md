---
title: Metodo Update della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Aggiorna i criteri di autorizzazione delle risorse di Desktop remoto correnti (RD \ 160; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Metodo di aggiornamento Servizi Desktop remoto
- Metodo Update Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120171"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="b6091-106">Metodo Update della classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="b6091-106">Update method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="b6091-107">Aggiorna i criteri di autorizzazione delle risorse di Desktop remoto correnti.</span><span class="sxs-lookup"><span data-stu-id="b6091-107">Updates the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6091-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6091-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="b6091-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6091-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6091-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6091-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6091-111">Nome dei criteri di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b6091-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="b6091-112">*Descrizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b6091-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6091-113">Descrizione del criterio di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b6091-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="b6091-114">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6091-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6091-115">Indica se è necessario abilitare RD RAP.</span><span class="sxs-lookup"><span data-stu-id="b6091-115">Indicates whether the RD RAP should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b6091-116">*ResourceGroupName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6091-116">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6091-117">Nome del gruppo di risorse associato a questo criterio di autorizzazione risorse Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b6091-117">Resource group name associated with this RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="b6091-118">*ResourceGroupType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6091-118">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6091-119">Tipo di gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6091-119">Resource group type.</span></span>

<dt>

<span data-ttu-id="b6091-120">RG</span><span class="sxs-lookup"><span data-stu-id="b6091-120">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="b6091-121">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6091-121">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="b6091-122">CG</span><span class="sxs-lookup"><span data-stu-id="b6091-122">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="b6091-123">Gruppo di computer, come Archiviato in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b6091-123">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="b6091-124">TUTTI</span><span class="sxs-lookup"><span data-stu-id="b6091-124">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="b6091-125">Tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="b6091-125">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b6091-126">*UserGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6091-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6091-127">Elenco delimitato da punti e virgola di nomi di gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="b6091-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="b6091-128">I nomi sono nel formato *dominio \\ nomegruppoutenti*.</span><span class="sxs-lookup"><span data-stu-id="b6091-128">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="b6091-129">Se l'utente appartiene a uno di questi gruppi di utenti, sarà consentito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="b6091-129">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> <dt>

<span data-ttu-id="b6091-130">*ProtocolNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6091-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6091-131">Elenco delimitato da punti e virgola di nomi di protocollo abilitati per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="b6091-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="b6091-132">I nomi devono corrispondere alla restituzione del metodo [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) della [**classe \_ Win32 TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="b6091-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b6091-133">*PortNumbers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6091-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6091-134">Elenco delimitato da punti e virgola di numeri di porta abilitati per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="b6091-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="b6091-135">Per consentire qualsiasi numero di porta, impostare " \* ".</span><span class="sxs-lookup"><span data-stu-id="b6091-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6091-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6091-136">Return value</span></span>

<span data-ttu-id="b6091-137">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="b6091-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b6091-138">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="b6091-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b6091-139">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b6091-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6091-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6091-140">Remarks</span></span>

<span data-ttu-id="b6091-141">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="b6091-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b6091-142">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b6091-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b6091-143">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b6091-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b6091-144">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b6091-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b6091-145">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b6091-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6091-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6091-146">Requirements</span></span>



| <span data-ttu-id="b6091-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6091-147">Requirement</span></span> | <span data-ttu-id="b6091-148">Valore</span><span class="sxs-lookup"><span data-stu-id="b6091-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6091-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6091-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b6091-150">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b6091-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b6091-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6091-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b6091-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6091-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b6091-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6091-153">Namespace</span></span><br/>                | <span data-ttu-id="b6091-154">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b6091-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b6091-155">MOF</span><span class="sxs-lookup"><span data-stu-id="b6091-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6091-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6091-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6091-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b6091-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6091-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6091-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b6091-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6091-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6091-160">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="b6091-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

