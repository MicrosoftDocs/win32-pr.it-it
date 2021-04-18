---
description: Per migliorare la sicurezza del processo host del provider condiviso Strumentazione gestione Windows (WMI) (wmiprvse.exe), sono state apportate modifiche alle piattaforme Windows che proteggono il processo host del provider con un ID di sicurezza (SID) del servizio.
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Chiavi e valori del registro di sistema per il controllo della sicurezza del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c7dd990c1a9ebbc1242af5ce4601ce6eb22a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318538"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a><span data-ttu-id="5bf0b-103">Chiavi e valori del registro di sistema per il controllo della sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="5bf0b-103">Registry Keys and Values for Controlling Provider Security</span></span>

<span data-ttu-id="5bf0b-104">Per migliorare la sicurezza del processo host del provider condiviso Strumentazione gestione Windows (WMI) (wmiprvse.exe), sono state apportate modifiche alle piattaforme Windows che proteggono il processo host del provider con un [*ID di sicurezza (SID) del servizio*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-104">To enhance the security of the Windows Management Instrumentation (WMI) shared provider host process (wmiprvse.exe), changes were made to Windows platforms that secure the provider host process with a [*service security identifier (SID)*](gloss-s.md).</span></span> <span data-ttu-id="5bf0b-105">Queste modifiche introducono le seguenti modalità di esecuzione per l'host condiviso WMI: protetto e compatibile.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-105">These changes introduce the following running modes for the WMI shared host: secure and compatible.</span></span>

<span data-ttu-id="5bf0b-106">In questo argomento vengono descritte le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5bf0b-106">The following sections are covered in this topic:</span></span>

-   [<span data-ttu-id="5bf0b-107">Modalità sicure e compatibili</span><span class="sxs-lookup"><span data-stu-id="5bf0b-107">Secure and Compatible Modes</span></span>](#secure-and-compatible-modes)
-   [<span data-ttu-id="5bf0b-108">Chiavi e valori del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="5bf0b-108">Registry Keys and Values</span></span>](#registry-keys-and-values)
-   [<span data-ttu-id="5bf0b-109">Configurazione di un provider per l'esecuzione in modalità protetta o compatibile</span><span class="sxs-lookup"><span data-stu-id="5bf0b-109">Configuring a Provider to Run in Secure or Compatible Mode</span></span>](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a><span data-ttu-id="5bf0b-110">Modalità sicure e compatibili</span><span class="sxs-lookup"><span data-stu-id="5bf0b-110">Secure and Compatible Modes</span></span>

<span data-ttu-id="5bf0b-111">A partire da Windows 7, sono state aggiunte le due modalità di esecuzione seguenti per il processo host condiviso WMI:</span><span class="sxs-lookup"><span data-stu-id="5bf0b-111">Starting in Windows 7, the following two running modes for the WMI shared host process were added:</span></span>

<dl> <dt>

<span data-ttu-id="5bf0b-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Modalità protetta</span><span class="sxs-lookup"><span data-stu-id="5bf0b-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Secure mode</span></span>
</dt> <dd>

<span data-ttu-id="5bf0b-113">Le risorse del processo host del provider WMI sono protette con un [*SID del servizio*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-113">WMI provider host process resources are secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="5bf0b-114">Solo il *SID del servizio* dispone delle autorizzazioni per queste risorse.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-114">Only the *service SID* has permissions for these resources.</span></span>

</dd> <dt>

<span data-ttu-id="5bf0b-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Modalità compatibile</span><span class="sxs-lookup"><span data-stu-id="5bf0b-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Compatible mode</span></span>
</dt> <dd>

<span data-ttu-id="5bf0b-116">Il processo host del provider condiviso WMI non è protetto con un [*SID del servizio*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-116">The WMI shared provider host process is not secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="5bf0b-117">Il processo host del provider consente l'accesso agli account NetworkService o LocalService, a seconda del modello di hosting.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-117">The provider host process allows access to the NetworkService or LocalService accounts depending on the hosting model.</span></span> <span data-ttu-id="5bf0b-118">Per ulteriori informazioni sui modelli di hosting, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-118">For more information about hosting models, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

<span data-ttu-id="5bf0b-119">**Windows Vista e Windows Server 2008:** Per accedere alle chiavi e ai valori del registro di sistema per il controllo di modalità sicure e compatibili per il processo host del provider, è necessario installare l'aggiornamento della sicurezza in [KB 959454](https://support.microsoft.com/kb/959454).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-119">**Windows Vista and Windows Server 2008:** To access the registry keys and values for controlling secure and compatible modes for the provider host process, you must install the security update in [KB 959454](https://support.microsoft.com/kb/959454).</span></span> <span data-ttu-id="5bf0b-120">Per ulteriori informazioni, vedere [Microsoft Security Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-120">For more information, see the [Microsoft Security Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span></span>

## <a name="registry-keys-and-values"></a><span data-ttu-id="5bf0b-121">Chiavi e valori del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="5bf0b-121">Registry Keys and Values</span></span>

<span data-ttu-id="5bf0b-122">Le impostazioni della modalità protetta e compatibile vengono specificate tramite le chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-122">The secure and compatible mode settings are specified through registry keys.</span></span> <span data-ttu-id="5bf0b-123">Le chiavi del registro di sistema per WMI si trovano nel registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="5bf0b-123">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<span data-ttu-id="5bf0b-124">Le seguenti chiavi del registro di sistema e il valore **DWORD** descritti nell'elenco seguente sono stati aggiunti per controllare il comportamento dei provider WMI.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-124">The following registry keys and **DWORD** value described in the following list were added to control the behavior of WMI providers.</span></span>

<dl> <dt>

<span data-ttu-id="5bf0b-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="5bf0b-126">Questa chiave controlla il comportamento dei singoli provider.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-126">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="5bf0b-127">Tutti i provider elencati in questa chiave vengono sempre eseguiti in modalità protetta.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-127">All of the providers that are listed in this key always run in secure mode.</span></span> <span data-ttu-id="5bf0b-128">Tutti i provider della posta in arrivo forniti con Windows sono elencati sotto questa chiave e vengono eseguiti in modalità protetta per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-128">All inbox providers that are shipped with Windows are listed under this key, and are run in secure mode by default.</span></span>

<span data-ttu-id="5bf0b-129">Questa chiave ha la precedenza sui provider elencati nella chiave **CompatibleHostProviders** .</span><span class="sxs-lookup"><span data-stu-id="5bf0b-129">This key takes precedence over providers listed in the **CompatibleHostProviders** key.</span></span>

</dd> <dt>

<span data-ttu-id="5bf0b-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="5bf0b-131">Questa chiave controlla il comportamento dei singoli provider.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-131">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="5bf0b-132">Tutti i provider elencati in questa chiave vengono sempre eseguiti in modalità compatibile.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-132">All providers that are listed in this key always run in compatible mode.</span></span> <span data-ttu-id="5bf0b-133">Questa chiave è vuota per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-133">This key is empty by default.</span></span>

<span data-ttu-id="5bf0b-134">Se un provider è elencato sia nella chiave **SecuredHostProviders** che nella chiave **CompatibleHostProviders** , il provider viene eseguito in modalità protetta.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-134">If a provider is listed both in the **SecuredHostProviders** key and in the **CompatibleHostProviders** key, the provider is run in secure mode.</span></span>

> [!Note]  
> <span data-ttu-id="5bf0b-135">La chiave **CompatibleHostProviders** fornisce la compatibilità delle applicazioni di terze parti se la chiave **DefaultSecuredHost** è impostata su 1 e il provider non funziona in modalità protetta.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-135">The **CompatibleHostProviders** key provides application compatibility for third-party applications if the **DefaultSecuredHost** key is set to 1 and the provider is known to not function in secure mode.</span></span>

 

</dd> <dt>

<span data-ttu-id="5bf0b-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span></span>
</dt> <dd>

<span data-ttu-id="5bf0b-137">Valore **DWORD** del registro di sistema globale che determina se tutti i provider, che non sono elencati nelle chiavi **SecuredHostProviders** o **CompatibleHostProviders** , vengono eseguiti in modalità protetta o compatibile.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-137">A global registry **DWORD** value that determines whether all of the providers, which are not listed in the **SecuredHostProviders** or **CompatibleHostProviders** keys, are run in the secure or compatible mode.</span></span> <span data-ttu-id="5bf0b-138">Questo valore **DWORD** consente all'amministratore di decidere in quale modalità deve essere eseguito un provider di terze parti.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-138">This **DWORD** value lets the administrator decide under which mode a third-party provider must run.</span></span> <span data-ttu-id="5bf0b-139">Per impostazione predefinita, questo valore è impostato su zero e tutti i provider di terze parti vengono eseguiti in modalità compatibile.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-139">By default, this value is set to zero and all third-party providers are run in compatible mode.</span></span> <span data-ttu-id="5bf0b-140">Per impostazione predefinita, gli amministratori possono rendere il computer più sicuro impostando il valore **DefaultSecuredHost** su 1.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-140">Administrators can make their computer more secure by default by setting the **DefaultSecuredHost** value to 1.</span></span>

> [!Note]  
> <span data-ttu-id="5bf0b-141">Il valore **DefaultSecuredHost** non influisce sulle altre chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-141">The **DefaultSecuredHost** value does not affect the other registry keys.</span></span> <span data-ttu-id="5bf0b-142">I provider elencati nella chiave **SecuredHostProviders** rimangono in modalità protetta e quelli elencati nella chiave **CompatibleHostProviders** rimangono in modalità compatibile.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-142">The providers that are listed in the **SecuredHostProviders** key remain in secure mode, and the ones that are listed in the **CompatibleHostProviders** key remain in compatible mode.</span></span>

 

<span data-ttu-id="5bf0b-143">Sono possibili le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5bf0b-143">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="5bf0b-144"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="5bf0b-144"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="5bf0b-145">Specifica che i provider vengono eseguiti in modalità compatibile.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-145">Specifies that providers run in compatible mode.</span></span>

</dd> <dt>

<span data-ttu-id="5bf0b-146"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="5bf0b-146"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="5bf0b-147">Specifica che i provider vengono eseguiti in modalità protetta.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-147">Specifies that providers run in secure mode.</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="5bf0b-148">Nell'elenco seguente sono elencate le possibili impostazioni del registro di sistema e le modalità di esecuzione associate per un provider.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-148">The following list lists the possible registry settings and the associated running modes for a provider.</span></span>



| <span data-ttu-id="5bf0b-149">Elencato in SecuredHostProviders</span><span class="sxs-lookup"><span data-stu-id="5bf0b-149">Listed under SecuredHostProviders</span></span> | <span data-ttu-id="5bf0b-150">Elencato in CompatibleHostProviders</span><span class="sxs-lookup"><span data-stu-id="5bf0b-150">Listed under CompatibleHostProviders</span></span> | <span data-ttu-id="5bf0b-151">Impostazione DefaultSecuredHost</span><span class="sxs-lookup"><span data-stu-id="5bf0b-151">DefaultSecuredHost Setting</span></span> | <span data-ttu-id="5bf0b-152">Modalità</span><span class="sxs-lookup"><span data-stu-id="5bf0b-152">Mode</span></span>       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| <span data-ttu-id="5bf0b-153">No</span><span class="sxs-lookup"><span data-stu-id="5bf0b-153">No</span></span>                                | <span data-ttu-id="5bf0b-154">No</span><span class="sxs-lookup"><span data-stu-id="5bf0b-154">No</span></span>                                   | <span data-ttu-id="5bf0b-155">0</span><span class="sxs-lookup"><span data-stu-id="5bf0b-155">0</span></span>                          | <span data-ttu-id="5bf0b-156">Compatibile</span><span class="sxs-lookup"><span data-stu-id="5bf0b-156">Compatible</span></span> |
| <span data-ttu-id="5bf0b-157">No</span><span class="sxs-lookup"><span data-stu-id="5bf0b-157">No</span></span>                                | <span data-ttu-id="5bf0b-158">Sì</span><span class="sxs-lookup"><span data-stu-id="5bf0b-158">Yes</span></span>                                  | <span data-ttu-id="5bf0b-159">0</span><span class="sxs-lookup"><span data-stu-id="5bf0b-159">0</span></span>                          | <span data-ttu-id="5bf0b-160">Compatibile</span><span class="sxs-lookup"><span data-stu-id="5bf0b-160">Compatible</span></span> |
| <span data-ttu-id="5bf0b-161">Sì</span><span class="sxs-lookup"><span data-stu-id="5bf0b-161">Yes</span></span>                               | <span data-ttu-id="5bf0b-162">No</span><span class="sxs-lookup"><span data-stu-id="5bf0b-162">No</span></span>                                   | <span data-ttu-id="5bf0b-163">0</span><span class="sxs-lookup"><span data-stu-id="5bf0b-163">0</span></span>                          | <span data-ttu-id="5bf0b-164">Protezione</span><span class="sxs-lookup"><span data-stu-id="5bf0b-164">Secure</span></span>     |
| <span data-ttu-id="5bf0b-165">Sì</span><span class="sxs-lookup"><span data-stu-id="5bf0b-165">Yes</span></span>                               | <span data-ttu-id="5bf0b-166">Sì</span><span class="sxs-lookup"><span data-stu-id="5bf0b-166">Yes</span></span>                                  | <span data-ttu-id="5bf0b-167">0</span><span class="sxs-lookup"><span data-stu-id="5bf0b-167">0</span></span>                          | <span data-ttu-id="5bf0b-168">Protezione</span><span class="sxs-lookup"><span data-stu-id="5bf0b-168">Secure</span></span>     |
| <span data-ttu-id="5bf0b-169">No</span><span class="sxs-lookup"><span data-stu-id="5bf0b-169">No</span></span>                                | <span data-ttu-id="5bf0b-170">No</span><span class="sxs-lookup"><span data-stu-id="5bf0b-170">No</span></span>                                   | <span data-ttu-id="5bf0b-171">1</span><span class="sxs-lookup"><span data-stu-id="5bf0b-171">1</span></span>                          | <span data-ttu-id="5bf0b-172">Protezione</span><span class="sxs-lookup"><span data-stu-id="5bf0b-172">Secure</span></span>     |
| <span data-ttu-id="5bf0b-173">No</span><span class="sxs-lookup"><span data-stu-id="5bf0b-173">No</span></span>                                | <span data-ttu-id="5bf0b-174">Sì</span><span class="sxs-lookup"><span data-stu-id="5bf0b-174">Yes</span></span>                                  | <span data-ttu-id="5bf0b-175">1</span><span class="sxs-lookup"><span data-stu-id="5bf0b-175">1</span></span>                          | <span data-ttu-id="5bf0b-176">Compatibile</span><span class="sxs-lookup"><span data-stu-id="5bf0b-176">Compatible</span></span> |
| <span data-ttu-id="5bf0b-177">Sì</span><span class="sxs-lookup"><span data-stu-id="5bf0b-177">Yes</span></span>                               | <span data-ttu-id="5bf0b-178">No</span><span class="sxs-lookup"><span data-stu-id="5bf0b-178">No</span></span>                                   | <span data-ttu-id="5bf0b-179">1</span><span class="sxs-lookup"><span data-stu-id="5bf0b-179">1</span></span>                          | <span data-ttu-id="5bf0b-180">Protezione</span><span class="sxs-lookup"><span data-stu-id="5bf0b-180">Secure</span></span>     |
| <span data-ttu-id="5bf0b-181">Sì</span><span class="sxs-lookup"><span data-stu-id="5bf0b-181">Yes</span></span>                               | <span data-ttu-id="5bf0b-182">Sì</span><span class="sxs-lookup"><span data-stu-id="5bf0b-182">Yes</span></span>                                  | <span data-ttu-id="5bf0b-183">1</span><span class="sxs-lookup"><span data-stu-id="5bf0b-183">1</span></span>                          | <span data-ttu-id="5bf0b-184">Protezione</span><span class="sxs-lookup"><span data-stu-id="5bf0b-184">Secure</span></span>     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a><span data-ttu-id="5bf0b-185">Configurazione di un provider per l'esecuzione in modalità protetta o compatibile</span><span class="sxs-lookup"><span data-stu-id="5bf0b-185">Configuring a Provider to Run in Secure or Compatible Mode</span></span>

<span data-ttu-id="5bf0b-186">Le chiavi del registro di sistema possono essere modificate utilizzando la Console Gestione Criteri di gruppo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-186">The registry keys can be modified using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="5bf0b-187">Per ulteriori informazioni, vedere [console Gestione criteri di gruppo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-187">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="5bf0b-188">Nelle procedure riportate di seguito viene illustrato come gestire le impostazioni della modalità protetta e compatibile utilizzando le preferenze di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-188">The following procedures illustrate how to manage secure and compatible mode settings by using group policy preferences.</span></span> <span data-ttu-id="5bf0b-189">Per ulteriori informazioni sulle preferenze di criteri di gruppo, vedere la [Panoramica sulle preferenze di criteri di gruppo](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-189">For more information about group policy preferences, see the [Group Policy Preferences Overview](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span></span>

<span data-ttu-id="5bf0b-190">**Per aggiungere un provider alla modalità protetta o compatibile utilizzando Criteri di gruppo**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-190">**To add a provider to either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="5bf0b-191">Aprire Console Gestione Criteri di gruppo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-191">Open the GPMC.</span></span>
2.  <span data-ttu-id="5bf0b-192">Creare un oggetto Criteri di gruppo (GPO).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-192">Create a Group Policy Object (GPO).</span></span>
3.  <span data-ttu-id="5bf0b-193">Modificare l'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-193">Edit the GPO.</span></span>
4.  <span data-ttu-id="5bf0b-194">Passare a Preferenze/impostazioni di Windows/Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-194">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="5bf0b-195">Fare clic con il pulsante destro del mouse e scegliere **nuovo... Registro di sistema**.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-195">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="5bf0b-196">Questa azione presenta un'interfaccia utente in cui è possibile immettere le informazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-196">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="5bf0b-197">Selezionare il comando **Crea** .</span><span class="sxs-lookup"><span data-stu-id="5bf0b-197">Select the **Create** command.</span></span>
7.  <span data-ttu-id="5bf0b-198">Selezionare il percorso della chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="5bf0b-198">Select the following registry key path:</span></span>

    <span data-ttu-id="5bf0b-199">**Modalità protetta: HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-199">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="5bf0b-200">**Modalità compatibile: HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-200">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="5bf0b-201">Nel campo **nome** immettere il nome del provider che si desidera aggiungere a questa chiave.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-201">In the **name** field, enter the name of the provider you want to add to this key.</span></span> <span data-ttu-id="5bf0b-202">Il nome del provider deve essere nel formato seguente: <namespace> : <\_ \_ RelPath>.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-202">The provider name must be in the following format: <namespace>:<\_\_RELPATH>.</span></span> <span data-ttu-id="5bf0b-203">Ad esempio, root \\ CIMV2: \_ \_ Win32Provider. Name = "fornisco".</span><span class="sxs-lookup"><span data-stu-id="5bf0b-203">For example, root\\cimv2:\_\_win32provider.name="MyProvider".</span></span>
9.  <span data-ttu-id="5bf0b-204">Nel campo **dati** immettere 0.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-204">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="5bf0b-205">Fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-205">Click OK.</span></span>

<span data-ttu-id="5bf0b-206">**Per rimuovere un provider dalla modalità protetta o compatibile utilizzando Criteri di gruppo**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-206">**To remove a provider from either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="5bf0b-207">Aprire Console Gestione Criteri di gruppo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-207">Open the GPMC.</span></span>
2.  <span data-ttu-id="5bf0b-208">Creare un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-208">Create a GPO.</span></span>
3.  <span data-ttu-id="5bf0b-209">Modificare l'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-209">Edit the GPO.</span></span>
4.  <span data-ttu-id="5bf0b-210">Passare a Preferenze/impostazioni di Windows/Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-210">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="5bf0b-211">Fare clic con il pulsante destro del mouse e scegliere **nuovo... Registro di sistema**.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-211">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="5bf0b-212">Questa azione presenta un'interfaccia utente in cui è possibile immettere le informazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-212">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="5bf0b-213">Selezionare il comando **Rimuovi** .</span><span class="sxs-lookup"><span data-stu-id="5bf0b-213">Select the **Remove** command.</span></span>
7.  <span data-ttu-id="5bf0b-214">Selezionare il percorso della chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="5bf0b-214">Select the following registry key path:</span></span>

    <span data-ttu-id="5bf0b-215">**Modalità protetta: HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-215">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="5bf0b-216">**Modalità compatibile: HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-216">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="5bf0b-217">Nel campo **nome** immettere il nome del provider che si desidera rimuovere da questa chiave.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-217">In the **name** field, enter the name of the provider you want to remove from this key.</span></span>
9.  <span data-ttu-id="5bf0b-218">Nel campo **dati** immettere 0.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-218">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="5bf0b-219">Fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-219">Click OK.</span></span>

<span data-ttu-id="5bf0b-220">Nella procedura riportata di seguito vengono fornite informazioni dettagliate su come modificare il comportamento dei provider non elencati nelle chiavi **SecuredHostProviders** o **CompatibleHostProviders** .</span><span class="sxs-lookup"><span data-stu-id="5bf0b-220">The following procedure provides details about how to modify the behavior of providers that are not listed in either the **SecuredHostProviders** or **CompatibleHostProviders** keys.</span></span>

<span data-ttu-id="5bf0b-221">**Per modificare il valore predefinito della chiave DefaultSecuredHost usando Criteri di gruppo**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-221">**To change the default value of the DefaultSecuredHost key by using Group Policy**</span></span>

1.  <span data-ttu-id="5bf0b-222">Aprire Console Gestione Criteri di gruppo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-222">Open the GPMC.</span></span>
2.  <span data-ttu-id="5bf0b-223">Creare un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-223">Create a GPO.</span></span>
3.  <span data-ttu-id="5bf0b-224">Modificare l'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-224">Edit the GPO.</span></span>
4.  <span data-ttu-id="5bf0b-225">Passare a Preferenze/impostazioni di Windows/Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-225">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="5bf0b-226">Fare clic con il pulsante destro del mouse e scegliere **nuovo... Registro di sistema**.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-226">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="5bf0b-227">Questa azione presenta un'interfaccia utente in cui è possibile immettere le informazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-227">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="5bf0b-228">Selezionare il comando **Aggiorna** .</span><span class="sxs-lookup"><span data-stu-id="5bf0b-228">Select the **Update** command.</span></span>
7.  <span data-ttu-id="5bf0b-229">Selezionare il percorso della chiave del registro di sistema seguente: **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-229">Select the following registry key path: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**.</span></span>
8.  <span data-ttu-id="5bf0b-230">Nel campo **nome** immettere **DefaultSecuredHost**.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-230">In the **name** field, enter **DefaultSecuredHost**.</span></span>
9.  <span data-ttu-id="5bf0b-231">Nel campo **dati** immettere 0 per modalità compatibile o 1 per modalità protetta.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-231">In the **data** field, enter 0 for compatible mode or 1 for secure mode.</span></span>
10. <span data-ttu-id="5bf0b-232">Fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-232">Click OK.</span></span>

 

 
