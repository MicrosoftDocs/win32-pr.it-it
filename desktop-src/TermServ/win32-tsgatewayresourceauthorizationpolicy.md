---
title: Classe Win32_TSGatewayResourceAuthorizationPolicy
description: Descrive i criteri di autorizzazione delle risorse di Desktop remoto (RD \ 160; RAP). RD \ 160; Il RAP viene usato per decidere se un utente è autorizzato a connettersi a una risorsa specificata tramite Desktop remoto Gateway (Gateway Desktop remoto).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048286"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="c65a6-106">Win32 \_ TSGatewayResourceAuthorizationPolicy (classe)</span><span class="sxs-lookup"><span data-stu-id="c65a6-106">Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="c65a6-107">Descrive un criterio di autorizzazione risorse Desktop remoto (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="c65a6-107">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="c65a6-108">Un criterio di autorizzazione risorse Desktop remoto viene usato per decidere se un utente è autorizzato a connettersi a una risorsa specificata tramite Desktop remoto Gateway (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="c65a6-108">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="c65a6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c65a6-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a><span data-ttu-id="c65a6-110">Members</span><span class="sxs-lookup"><span data-stu-id="c65a6-110">Members</span></span>

<span data-ttu-id="c65a6-111">La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c65a6-111">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="c65a6-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c65a6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c65a6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c65a6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c65a6-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="c65a6-114">Methods</span></span>

<span data-ttu-id="c65a6-115">La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c65a6-115">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="c65a6-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="c65a6-116">Method</span></span>                                                                                          | <span data-ttu-id="c65a6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c65a6-117">Description</span></span>                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c65a6-118">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="c65a6-118">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="c65a6-119">Aggiunge i nomi dei gruppi di utenti specificati ai gruppi di utenti esistenti nella proprietà **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="c65a6-119">Adds the specified user group names to the existing user groups in the **UserGroupNames** property.</span></span><br/>      |
| [<span data-ttu-id="c65a6-120">**Creare**</span><span class="sxs-lookup"><span data-stu-id="c65a6-120">**Create**</span></span>](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="c65a6-121">Creazione di un criterio di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c65a6-121">Creates an RD RAP.</span></span><br/>                                                                                       |
| [<span data-ttu-id="c65a6-122">**Delete**</span><span class="sxs-lookup"><span data-stu-id="c65a6-122">**Delete**</span></span>](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="c65a6-123">Elimina il RAP RD corrente.</span><span class="sxs-lookup"><span data-stu-id="c65a6-123">Deletes the current RD RAP.</span></span><br/>                                                                              |
| [<span data-ttu-id="c65a6-124">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="c65a6-124">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | <span data-ttu-id="c65a6-125">Rimuove i nomi dei gruppi di utenti specificati dai gruppi di utenti esistenti nella proprietà **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="c65a6-125">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span><br/> |
| [<span data-ttu-id="c65a6-126">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="c65a6-126">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="c65a6-127">Imposta la proprietà **Description** per il criterio di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c65a6-127">Sets the **Description** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="c65a6-128">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="c65a6-128">**SetEnabled**</span></span>](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | <span data-ttu-id="c65a6-129">Abilita o Disabilita il criterio di autorizzazione connessioni Desktop remoto impostando la proprietà **Enabled** .</span><span class="sxs-lookup"><span data-stu-id="c65a6-129">Enables or disables the RD RAP by setting the **Enabled** property.</span></span><br/>                                      |
| [<span data-ttu-id="c65a6-130">**SetName**</span><span class="sxs-lookup"><span data-stu-id="c65a6-130">**SetName**</span></span>](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | <span data-ttu-id="c65a6-131">Imposta la proprietà **Name** per il criterio di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c65a6-131">Sets the **Name** property for the RD RAP.</span></span><br/>                                                               |
| [<span data-ttu-id="c65a6-132">**SetPortNumbers**</span><span class="sxs-lookup"><span data-stu-id="c65a6-132">**SetPortNumbers**</span></span>](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="c65a6-133">Imposta la proprietà **PortNumbers** per il criterio di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c65a6-133">Sets the **PortNumbers** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="c65a6-134">**SetResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="c65a6-134">**SetResourceGroup**</span></span>](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | <span data-ttu-id="c65a6-135">Imposta le proprietà **ResourceGroupType** e **ResourceGroupName** .</span><span class="sxs-lookup"><span data-stu-id="c65a6-135">Sets the **ResourceGroupType** and **ResourceGroupName** properties.</span></span><br/>                                     |
| [<span data-ttu-id="c65a6-136">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="c65a6-136">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="c65a6-137">Imposta la proprietà **UserGroupNames** per il criterio di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c65a6-137">Sets the **UserGroupNames** property for the RD RAP.</span></span><br/>                                                     |
| [<span data-ttu-id="c65a6-138">**Aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="c65a6-138">**Update**</span></span>](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="c65a6-139">Aggiorna il RAP RD corrente.</span><span class="sxs-lookup"><span data-stu-id="c65a6-139">Updates the current RD RAP.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="c65a6-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c65a6-140">Properties</span></span>

<span data-ttu-id="c65a6-141">La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c65a6-141">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c65a6-142">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c65a6-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65a6-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c65a6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65a6-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c65a6-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65a6-145">Descrizione del criterio di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c65a6-145">Description of the RD RAP.</span></span> <span data-ttu-id="c65a6-146">Questa proprietà viene modificata con il metodo [**sedescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="c65a6-146">This property is changed with the [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c65a6-147">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="c65a6-147">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65a6-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c65a6-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c65a6-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c65a6-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65a6-150">Indica se l'autorizzazione RD è abilitata.</span><span class="sxs-lookup"><span data-stu-id="c65a6-150">Indicates whether this RD RAP is enabled.</span></span> <span data-ttu-id="c65a6-151">Questa proprietà viene modificata con il metodo [**Seenabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="c65a6-151">This property is changed with the [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c65a6-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c65a6-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65a6-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c65a6-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65a6-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c65a6-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c65a6-155">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c65a6-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c65a6-156">Nome dei criteri di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c65a6-156">Name of the RD RAP.</span></span> <span data-ttu-id="c65a6-157">Questa proprietà viene modificata con il metodo [**Sename**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="c65a6-157">This property is changed with the [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c65a6-158">**PortNumbers**</span><span class="sxs-lookup"><span data-stu-id="c65a6-158">**PortNumbers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65a6-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c65a6-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65a6-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c65a6-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65a6-161">Elenco di numeri di porta separati da punti e virgola consentiti per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="c65a6-161">List of semicolon-separated port numbers that are allowed for this policy.</span></span> <span data-ttu-id="c65a6-162">Per consentire qualsiasi numero di porta, impostare " \* ".</span><span class="sxs-lookup"><span data-stu-id="c65a6-162">To allow any port number, set "\*".</span></span>

</dd> <dt>

<span data-ttu-id="c65a6-163">**ProtocolNames**</span><span class="sxs-lookup"><span data-stu-id="c65a6-163">**ProtocolNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65a6-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c65a6-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65a6-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c65a6-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65a6-166">Elenco di nomi di protocollo delimitati da punti e virgola abilitati per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="c65a6-166">List of semicolon-separated protocol names that are enabled for this policy.</span></span> <span data-ttu-id="c65a6-167">I nomi devono corrispondere alla restituzione del metodo [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) della [**classe \_ Win32 TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="c65a6-167">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="c65a6-168">**ResourceGroupName**</span><span class="sxs-lookup"><span data-stu-id="c65a6-168">**ResourceGroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65a6-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c65a6-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65a6-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c65a6-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65a6-171">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c65a6-171">Resource group name.</span></span> <span data-ttu-id="c65a6-172">Questa proprietà viene modificata con il metodo [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="c65a6-172">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c65a6-173">**ResourceGroupType**</span><span class="sxs-lookup"><span data-stu-id="c65a6-173">**ResourceGroupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65a6-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c65a6-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65a6-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c65a6-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65a6-176">Identifica il tipo del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c65a6-176">Identifies the type of the resource group.</span></span> <span data-ttu-id="c65a6-177">Questa proprietà viene modificata con il metodo [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="c65a6-177">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

<dt>

<span data-ttu-id="c65a6-178">RG</span><span class="sxs-lookup"><span data-stu-id="c65a6-178">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="c65a6-179">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c65a6-179">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="c65a6-180">CG</span><span class="sxs-lookup"><span data-stu-id="c65a6-180">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="c65a6-181">Gruppo di computer, come Archiviato in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c65a6-181">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="c65a6-182">TUTTI</span><span class="sxs-lookup"><span data-stu-id="c65a6-182">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="c65a6-183">Tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="c65a6-183">All resources.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c65a6-184">**UserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="c65a6-184">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c65a6-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c65a6-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c65a6-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c65a6-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c65a6-187">Elenco delimitato da punti e virgola di nomi di gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="c65a6-187">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="c65a6-188">Se l'utente appartiene a uno di questi gruppi di utenti, sarà consentito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="c65a6-188">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="c65a6-189">Questa proprietà viene modificata con i metodi [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)e [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="c65a6-189">This property is changed with the [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), and [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c65a6-190">Commenti</span><span class="sxs-lookup"><span data-stu-id="c65a6-190">Remarks</span></span>

<span data-ttu-id="c65a6-191">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="c65a6-191">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="c65a6-192">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c65a6-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c65a6-193">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="c65a6-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c65a6-194">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="c65a6-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c65a6-195">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c65a6-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c65a6-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c65a6-196">Requirements</span></span>



| <span data-ttu-id="c65a6-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="c65a6-197">Requirement</span></span> | <span data-ttu-id="c65a6-198">Valore</span><span class="sxs-lookup"><span data-stu-id="c65a6-198">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c65a6-199">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65a6-199">Minimum supported client</span></span><br/> | <span data-ttu-id="c65a6-200">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c65a6-200">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c65a6-201">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65a6-201">Minimum supported server</span></span><br/> | <span data-ttu-id="c65a6-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c65a6-202">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c65a6-203">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c65a6-203">Namespace</span></span><br/>                | <span data-ttu-id="c65a6-204">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c65a6-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c65a6-205">MOF</span><span class="sxs-lookup"><span data-stu-id="c65a6-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c65a6-206"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c65a6-206"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c65a6-207">DLL</span><span class="sxs-lookup"><span data-stu-id="c65a6-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c65a6-208"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c65a6-208"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c65a6-209">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c65a6-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c65a6-210">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="c65a6-210">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="c65a6-211">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="c65a6-211">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="c65a6-212">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="c65a6-212">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="c65a6-213">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="c65a6-213">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="c65a6-214">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="c65a6-214">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="c65a6-215">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="c65a6-215">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

