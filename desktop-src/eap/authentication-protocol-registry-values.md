---
title: Valori del registro di sistema del protocollo di autenticazione
description: Il software di installazione per la DLL EAP può creare i seguenti valori del registro di sistema eaptypeid.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8091197c7b0d5c5a208bf3658bbc15284a29ac9e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104046154"
---
# <a name="authentication-protocol-registry-values"></a><span data-ttu-id="3c941-119">Valori del registro di sistema del protocollo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="3c941-119">Authentication Protocol Registry Values</span></span>

<span data-ttu-id="3c941-120">Il software di installazione per la DLL EAP può creare i seguenti valori del registro di sistema **&lt; eaptypeid &gt;**.</span><span class="sxs-lookup"><span data-stu-id="3c941-120">The setup software for the EAP DLL may create the following registry values below **&lt;eaptypeid&gt;**.</span></span> <span data-ttu-id="3c941-121">Questi valori del registro di sistema sono definiti nel file di intestazione Raseapif. h.</span><span class="sxs-lookup"><span data-stu-id="3c941-121">These registry values are defined in the Raseapif.h header file.</span></span> <span data-ttu-id="3c941-122">I valori **RAS_EAP_VALUENAME_PATH** e **RAS_EAP_VALUENAME_FRIENDLY_NAME** sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="3c941-122">The **RAS_EAP_VALUENAME_PATH** and **RAS_EAP_VALUENAME_FRIENDLY_NAME** values are required.</span></span> <span data-ttu-id="3c941-123">Il software di installazione può anche creare altre chiavi e valori.</span><span class="sxs-lookup"><span data-stu-id="3c941-123">The setup software may create other keys and values as well.</span></span> <span data-ttu-id="3c941-124">Questi possono essere usati dal protocollo di autenticazione stesso.</span><span class="sxs-lookup"><span data-stu-id="3c941-124">These could be used by the authentication protocol itself.</span></span> <span data-ttu-id="3c941-125">Per ulteriori informazioni e un esempio di configurazione del registro di sistema, vedere [esempio di valori del registro di sistema](registry-values-example.md).</span><span class="sxs-lookup"><span data-stu-id="3c941-125">For more information and an example of registry configuration, see [Registry Values Example](registry-values-example.md).</span></span>

[<span data-ttu-id="3c941-126">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="3c941-126">RAS_EAP_VALUENAME_PATH</span></span>](#ras_eap_valuename_path)

[<span data-ttu-id="3c941-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="3c941-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>](#ras_eap_valuename_friendly_name)

[<span data-ttu-id="3c941-128">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="3c941-128">RAS_EAP_VALUENAME_CONFIGUI</span></span>](#ras_eap_valuename_configui)

[<span data-ttu-id="3c941-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="3c941-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>](#ras_eap_valuename_default_data)

[<span data-ttu-id="3c941-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="3c941-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>](#ras_eap_valuename_require_configui)

[<span data-ttu-id="3c941-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="3c941-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>](#ras_eap_valuename_config_clsid)

[<span data-ttu-id="3c941-132">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="3c941-132">RAS_EAP_VALUENAME_IDENTITY</span></span>](#ras_eap_valuename_identity)

<span data-ttu-id="3c941-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) I</span><span class="sxs-lookup"><span data-stu-id="3c941-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui)I</span></span>

[<span data-ttu-id="3c941-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="3c941-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>](#ras_eap_valuename_invoke_namedlg)

[<span data-ttu-id="3c941-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="3c941-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>](#ras_eap_valuename_invoke_pwddlg)

[<span data-ttu-id="3c941-136">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="3c941-136">RAS_EAP_VALUENAME_ENCRYPTION</span></span>](#ras_eap_valuename_encryption)

[<span data-ttu-id="3c941-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="3c941-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>](#ras_eap_valuename_standalone_supported)

[<span data-ttu-id="3c941-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="3c941-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>](#ras_eap_valuename_roles_supported)

[<span data-ttu-id="3c941-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="3c941-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>](#ras_eap_valuename_per_policy_config)

[<span data-ttu-id="3c941-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="3c941-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>](#ras_eap_valuename_istunnel_method)

[<span data-ttu-id="3c941-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="3c941-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a><span data-ttu-id="3c941-142">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="3c941-142">RAS_EAP_VALUENAME_PATH</span></span>

| <span data-ttu-id="3c941-143">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-143">Constant value</span></span> | <span data-ttu-id="3c941-144">Percorso</span><span class="sxs-lookup"><span data-stu-id="3c941-144">Path</span></span>                               |
|----------------|------------------------------------|
| <span data-ttu-id="3c941-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-145">Type</span></span>           | <span data-ttu-id="3c941-146">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="3c941-146">REG_EXPAND_SZ</span></span>                    |
| <span data-ttu-id="3c941-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-147">Description</span></span>    | <span data-ttu-id="3c941-148">Specifica il percorso della DLL EAP.</span><span class="sxs-lookup"><span data-stu-id="3c941-148">Specifies the path to the EAP DLL.</span></span> |

## <a name="ras_eap_valuename_friendly_name"></a><span data-ttu-id="3c941-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="3c941-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>

| <span data-ttu-id="3c941-150">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-150">Constant value</span></span> | <span data-ttu-id="3c941-151">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3c941-151">FriendlyName</span></span>                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-152">Type</span></span>           | <span data-ttu-id="3c941-153">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="3c941-153">REG_SZ</span></span>                                                                                                                                                           |
| <span data-ttu-id="3c941-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-154">Description</span></span>    | <span data-ttu-id="3c941-155">Specifica un nome descrittivo per il protocollo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3c941-155">Specifies a friendly name for the authentication protocol.</span></span> <span data-ttu-id="3c941-156">Questo nome viene visualizzato nell'interfaccia utente dell'applicazione EAP per le implementazioni remote e wireless.</span><span class="sxs-lookup"><span data-stu-id="3c941-156">This name appears in the EAP application user interface for both dial-up and wireless implementations.</span></span> |

## <a name="ras_eap_valuename_configui"></a><span data-ttu-id="3c941-157">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="3c941-157">RAS_EAP_VALUENAME_CONFIGUI</span></span>

| <span data-ttu-id="3c941-158">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-158">Constant value</span></span> | <span data-ttu-id="3c941-159">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="3c941-159">ConfigUIPath</span></span>                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-160">Type</span></span>           | <span data-ttu-id="3c941-161">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="3c941-161">REG_EXPAND_SZ</span></span>                                                                                                                   |
| <span data-ttu-id="3c941-162">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-162">Description</span></span>    | <span data-ttu-id="3c941-163">Specifica il percorso della DLL che implementa l'interfaccia utente di configurazione nel client, perché questa interfaccia utente è solo per il client.</span><span class="sxs-lookup"><span data-stu-id="3c941-163">Specifies the path to the DLL that implements the configuration user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_default_data"></a><span data-ttu-id="3c941-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="3c941-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>

| <span data-ttu-id="3c941-165">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-165">Constant value</span></span> | <span data-ttu-id="3c941-166">ConfigData</span><span class="sxs-lookup"><span data-stu-id="3c941-166">ConfigData</span></span>                                                            |
|----------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3c941-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-167">Type</span></span>           | <span data-ttu-id="3c941-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="3c941-168">REG_BINARY</span></span>                                                           |
| <span data-ttu-id="3c941-169">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-169">Description</span></span>    | <span data-ttu-id="3c941-170">Specifica i dati di configurazione predefiniti per il protocollo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3c941-170">Specifies default configuration data for the authentication protocol.</span></span> |

## <a name="ras_eap_valuename_require_configui"></a><span data-ttu-id="3c941-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="3c941-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>

| <span data-ttu-id="3c941-172">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-172">Constant value</span></span> | <span data-ttu-id="3c941-173">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="3c941-173">RequireConfigUI</span></span>                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-174">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-174">Type</span></span>           | <span data-ttu-id="3c941-175">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="3c941-175">REG_DWORD</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="3c941-176">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-176">Description</span></span>    | <span data-ttu-id="3c941-177">Specifica se l'utente deve fornire i dati di configurazione nell'interfaccia utente dell'applicazione client EAP.</span><span class="sxs-lookup"><span data-stu-id="3c941-177">Specifies whether the user must provide configuration data in the EAP client application user interface.</span></span> <span data-ttu-id="3c941-178">Se questo valore è 1, l'utente non è autorizzato a uscire dall'interfaccia utente dell'applicazione client EAP senza fornire i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="3c941-178">If this value is 1, the user is not allowed to exit the EAP client application UI without providing configuration data.</span></span> <span data-ttu-id="3c941-179">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="3c941-179">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_config_clsid"></a><span data-ttu-id="3c941-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="3c941-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>

| <span data-ttu-id="3c941-181">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-181">Constant value</span></span> | <span data-ttu-id="3c941-182">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="3c941-182">ConfigCLSID</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="3c941-183">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-183">Type</span></span>           | <span data-ttu-id="3c941-184">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="3c941-184">REG_SZ</span></span>                                                       |
| <span data-ttu-id="3c941-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-185">Description</span></span>    | <span data-ttu-id="3c941-186">Specifica l'ID classe dell'interfaccia utente di configurazione nel server.</span><span class="sxs-lookup"><span data-stu-id="3c941-186">Specifies the class ID of the configuration UI on the server.</span></span> |

## <a name="ras_eap_valuename_identity"></a><span data-ttu-id="3c941-187">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="3c941-187">RAS_EAP_VALUENAME_IDENTITY</span></span>

| <span data-ttu-id="3c941-188">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-188">Constant value</span></span> | <span data-ttu-id="3c941-189">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="3c941-189">IdentityPath</span></span>                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-190">Type</span></span>           | <span data-ttu-id="3c941-191">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="3c941-191">REG_EXPAND_SZ</span></span>                                                                                                                        |
| <span data-ttu-id="3c941-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-192">Description</span></span>    | <span data-ttu-id="3c941-193">Specifica il percorso della DLL che implementa le funzioni per ottenere l'identità utente nel client, perché questa interfaccia utente è destinata solo ai client.</span><span class="sxs-lookup"><span data-stu-id="3c941-193">Specifies the path to the DLL that implements functions to obtain the user identity on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_interactiveui"></a><span data-ttu-id="3c941-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span><span class="sxs-lookup"><span data-stu-id="3c941-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span></span>

| <span data-ttu-id="3c941-195">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-195">Constant value</span></span> | <span data-ttu-id="3c941-196">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="3c941-196">InteractiveUIPath</span></span>                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-197">Type</span></span>           | <span data-ttu-id="3c941-198">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="3c941-198">REG_EXPAND_SZ</span></span>                                                                                                                 |
| <span data-ttu-id="3c941-199">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-199">Description</span></span>    | <span data-ttu-id="3c941-200">Specifica il percorso della DLL che implementa l'interfaccia utente interattiva sul client perché questa interfaccia utente è solo per il client.</span><span class="sxs-lookup"><span data-stu-id="3c941-200">Specifies the path to the DLL that implements the interactive user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_invoke_namedlg"></a><span data-ttu-id="3c941-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="3c941-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>

| <span data-ttu-id="3c941-202">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-202">Constant value</span></span> | <span data-ttu-id="3c941-203">InvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="3c941-203">InvokeUsernameDialog</span></span>                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-204">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-204">Type</span></span>           | <span data-ttu-id="3c941-205">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="3c941-205">REG_DWORD</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="3c941-206">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-206">Description</span></span>    | <span data-ttu-id="3c941-207">Specifica se RAS deve visualizzare la finestra di dialogo del nome utente standard di Windows NT/Windows 2000 (valore 1) o richiamare [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (valore 0).</span><span class="sxs-lookup"><span data-stu-id="3c941-207">Specifies whether RAS should display the standard Windows NT/Windows 2000 user name dialog (value of 1) or invoke [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (value of 0).</span></span> <span data-ttu-id="3c941-208">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="3c941-208">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_invoke_pwddlg"></a><span data-ttu-id="3c941-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="3c941-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>

| <span data-ttu-id="3c941-210">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-210">Constant value</span></span> | <span data-ttu-id="3c941-211">InvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="3c941-211">InvokePasswordDialog</span></span>                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-212">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-212">Type</span></span>           | <span data-ttu-id="3c941-213">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="3c941-213">REG_DWORD</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="3c941-214">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-214">Description</span></span>    | <span data-ttu-id="3c941-215">Specifica se RAS deve visualizzare la finestra di dialogo della password standard di Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3c941-215">Specifies whether RAS should display the standard Windows NT/Windows 2000 password dialog.</span></span> <span data-ttu-id="3c941-216">Se questo valore esiste e è 0, RAS non visualizzerà la finestra di dialogo password.</span><span class="sxs-lookup"><span data-stu-id="3c941-216">If this value exists and is 0, RAS will not display the password dialog.</span></span> <span data-ttu-id="3c941-217">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="3c941-217">The default value is 1.</span></span> |


## <a name="ras_eap_valuename_encryption"></a><span data-ttu-id="3c941-218">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="3c941-218">RAS_EAP_VALUENAME_ENCRYPTION</span></span>

| <span data-ttu-id="3c941-219">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-219">Constant value</span></span> | <span data-ttu-id="3c941-220">MPPEEncryptionSupported</span><span class="sxs-lookup"><span data-stu-id="3c941-220">MPPEEncryptionSupported</span></span>                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-221">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-221">Type</span></span>           | <span data-ttu-id="3c941-222">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="3c941-222">REG_DWORD</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="3c941-223">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-223">Description</span></span>    | <span data-ttu-id="3c941-224">Se questo valore è 1, il protocollo di autenticazione può generare chiavi per lo stile di crittografia Point-to-Point Encryption (MPPE) di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3c941-224">If this value is 1, the authentication protocol can generate keys for the Microsoft Point-to-Point Encryption (MPPE) style of encryption.</span></span> <span data-ttu-id="3c941-225">I valori possibili sono 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="3c941-225">Possible values are 0 or 1.</span></span> <span data-ttu-id="3c941-226">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="3c941-226">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_standalone_supported"></a><span data-ttu-id="3c941-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="3c941-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>

| <span data-ttu-id="3c941-228">Valore costante</span><span class="sxs-lookup"><span data-stu-id="3c941-228">Constant value</span></span> | <span data-ttu-id="3c941-229">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="3c941-229">StandaloneSupported</span></span>                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-230">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-230">Type</span></span>           | <span data-ttu-id="3c941-231">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="3c941-231">REG_DWORD</span></span>                                                                                                                                                                     |
| <span data-ttu-id="3c941-232">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-232">Description</span></span>    | <span data-ttu-id="3c941-233">Specifica se il protocollo di autenticazione è supportato in un server Windows 2000 autonomo.</span><span class="sxs-lookup"><span data-stu-id="3c941-233">Specifies whether this authentication protocol is supported on a standalone Windows 2000 Server.</span></span> <span data-ttu-id="3c941-234">Il valore 0 indica che il protocollo EAP non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3c941-234">A value of 0 indicates that the EAP is not supported.</span></span> <span data-ttu-id="3c941-235">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="3c941-235">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_roles_supported"></a><span data-ttu-id="3c941-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="3c941-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>

| <span data-ttu-id="3c941-237">Constant Value</span><span class="sxs-lookup"><span data-stu-id="3c941-237">Constant Value</span></span> | <span data-ttu-id="3c941-238">RolesSupported</span><span class="sxs-lookup"><span data-stu-id="3c941-238">RolesSupported</span></span>                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-239">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-239">Type</span></span>           | <span data-ttu-id="3c941-240">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="3c941-240">REG_DWORD</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="3c941-241">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-241">Description</span></span>    | <span data-ttu-id="3c941-242">Specifica i vari ruoli supportati da EAP.</span><span class="sxs-lookup"><span data-stu-id="3c941-242">Specifies the various roles the EAP supports.</span></span> <span data-ttu-id="3c941-243">Indica se può essere utilizzato in un server o in un client, se è supportato per le connessioni RAS (VPN) o PEAP.</span><span class="sxs-lookup"><span data-stu-id="3c941-243">This indicates whether it can be used on a server or a client, whether it is supported for RAS connections (VPN) or PEAP.</span></span> <span data-ttu-id="3c941-244">Il comportamento predefinito prevede la visualizzazione del metodo EAP in PEAP e in EAP.</span><span class="sxs-lookup"><span data-stu-id="3c941-244">The default behavior is to show the EAP method in PEAP and in EAP.</span></span> |

## <a name="ras_eap_valuename_per_policy_config"></a><span data-ttu-id="3c941-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="3c941-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>

| <span data-ttu-id="3c941-246">Constant Value</span><span class="sxs-lookup"><span data-stu-id="3c941-246">Constant Value</span></span> | <span data-ttu-id="3c941-247">PerPolicyConfig</span><span class="sxs-lookup"><span data-stu-id="3c941-247">PerPolicyConfig</span></span> |
|----------------|-----------------|
| <span data-ttu-id="3c941-248">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c941-248">Type</span></span>           | <span data-ttu-id="3c941-249">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="3c941-249">REG_DWORD</span></span>      |
| <span data-ttu-id="3c941-250">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c941-250">Description</span></span>    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a><span data-ttu-id="3c941-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="3c941-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>

<span data-ttu-id="3c941-252">Il valore del registro di sistema non è in uso.</span><span class="sxs-lookup"><span data-stu-id="3c941-252">This registry value is not in use.</span></span>

## <a name="ras_eap_valuename_filter_innermethods"></a><span data-ttu-id="3c941-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="3c941-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>

<span data-ttu-id="3c941-254">Il valore del registro di sistema non è in uso.</span><span class="sxs-lookup"><span data-stu-id="3c941-254">This registry value is not in use.</span></span>

