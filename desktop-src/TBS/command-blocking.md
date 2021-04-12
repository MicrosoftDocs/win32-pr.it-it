---
title: Blocco comandi
description: Per mantenere l'integrità delle operazioni, alcuni comandi TPM non possono essere eseguiti dal software sulla piattaforma.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104398807"
---
# <a name="command-blocking"></a><span data-ttu-id="a4e55-103">Blocco comandi</span><span class="sxs-lookup"><span data-stu-id="a4e55-103">Command Blocking</span></span>

<span data-ttu-id="a4e55-104">Per mantenere l'integrità delle operazioni, alcuni comandi TPM non possono essere eseguiti dal software sulla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="a4e55-104">To preserve integrity of operations, certain TPM commands are not allowed to be executed by software on the platform.</span></span> <span data-ttu-id="a4e55-105">Alcuni comandi, ad esempio, vengono eseguiti solo dal software di sistema.</span><span class="sxs-lookup"><span data-stu-id="a4e55-105">For example, some commands are only executed by system software.</span></span> <span data-ttu-id="a4e55-106">Quando TBS blocca un comando, viene restituito un errore nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="a4e55-106">When the TBS blocks a command, an error is returned as appropriate.</span></span> <span data-ttu-id="a4e55-107">Per impostazione predefinita, TBS blocca i comandi che potrebbero influisca sulla privacy, sulla sicurezza e sulla stabilità del sistema.</span><span class="sxs-lookup"><span data-stu-id="a4e55-107">By default, the TBS blocks commands that could impact system privacy, security, and stability.</span></span> <span data-ttu-id="a4e55-108">In TBS si presuppone inoltre che altre parti dello stack software possano limitare l'accesso a determinati comandi a entità autorizzate.</span><span class="sxs-lookup"><span data-stu-id="a4e55-108">The TBS also assumes that other parts of the software stack may restrict access to certain commands to authorized entities.</span></span>

<span data-ttu-id="a4e55-109">Per i comandi TPM versione 1,2 sono disponibili tre elenchi di comandi bloccati: un elenco controllato da criteri di gruppo, un elenco controllato dagli amministratori locali e un elenco predefinito.</span><span class="sxs-lookup"><span data-stu-id="a4e55-109">For TPM version 1.2 commands, there are three lists of blocked commands: a list controlled by group policy, a list controlled by local administrators, and a default list.</span></span> <span data-ttu-id="a4e55-110">Un comando TPM viene bloccato se si trova in uno qualsiasi degli elenchi.</span><span class="sxs-lookup"><span data-stu-id="a4e55-110">A TPM command is blocked if it is on any of the lists.</span></span> <span data-ttu-id="a4e55-111">Esistono tuttavia flag di criteri di gruppo che consentono a TBS di ignorare l'elenco locale e l'elenco predefinito.</span><span class="sxs-lookup"><span data-stu-id="a4e55-111">However, there are group policy flags to allow the TBS to ignore the local list and the default list.</span></span> <span data-ttu-id="a4e55-112">I flag di criteri di gruppo possono essere modificati direttamente o a cui si accede tramite la Editor oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="a4e55-112">The group policy flags can be edited directly or accessed through the Group Policy Object Editor.</span></span>

> [!Note]  
> <span data-ttu-id="a4e55-113">L'elenco dei comandi bloccati localmente non viene mantenuto dopo un aggiornamento al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a4e55-113">The list of locally blocked commands is not preserved after an upgrade to the operating system.</span></span> <span data-ttu-id="a4e55-114">I comandi bloccati nell'elenco Criteri di gruppo vengono conservati.</span><span class="sxs-lookup"><span data-stu-id="a4e55-114">Commands that are blocked on the Group Policy list are preserved.</span></span>

 

<span data-ttu-id="a4e55-115">Per i comandi TPM versione 2,0, la logica per il blocco viene invertita; Usa un elenco di comandi consentiti.</span><span class="sxs-lookup"><span data-stu-id="a4e55-115">For TPM version 2.0 commands, the logic for blocking is inverted; it uses a list of allowed commands.</span></span> <span data-ttu-id="a4e55-116">Questa logica bloccherà automaticamente i comandi che non erano noti quando l'elenco è stato creato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="a4e55-116">This logic will automatically block commands that were not known when the list was first made.</span></span> <span data-ttu-id="a4e55-117">Quando i comandi vengono aggiunti alla specifica TPM dopo che è stata spedita una versione di Windows, questi nuovi comandi vengono bloccati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a4e55-117">When commands are added to the TPM specification after a version of Windows has shipped, these new commands are automatically blocked.</span></span> <span data-ttu-id="a4e55-118">Solo un aggiornamento del registro di sistema aggiungerà questi nuovi comandi all'elenco dei comandi consentiti.</span><span class="sxs-lookup"><span data-stu-id="a4e55-118">Only an update of the registry will add these new commands to the list of allowed commands.</span></span>

<span data-ttu-id="a4e55-119">A partire da Windows 10 1809 (Windows Server 2019), i comandi TPM 2,0 consentiti non possono più essere modificati tramite le impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a4e55-119">Starting with Windows 10 1809 (Windows Server 2019), allowed TPM 2.0 commands can no longer be manipulated through registry settings.</span></span> <span data-ttu-id="a4e55-120">Per queste versioni di Windows 10, i comandi TPM 2,0 consentiti sono corretti nel driver TPM.</span><span class="sxs-lookup"><span data-stu-id="a4e55-120">For these Windows 10 versions, the allowed TPM 2.0 commands are fixed in the TPM driver.</span></span> <span data-ttu-id="a4e55-121">È ancora possibile bloccare e sbloccare i comandi TPM 1,2 tramite modifiche al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a4e55-121">TPM 1.2 commands can still be blocked and unblocked through registry changes.</span></span> 

## <a name="direct-registry-access"></a><span data-ttu-id="a4e55-122">Accesso diretto al registro di sistema</span><span class="sxs-lookup"><span data-stu-id="a4e55-122">Direct Registry Access</span></span>

<span data-ttu-id="a4e55-123">I flag di criteri di gruppo si trovano nella chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **BlockedCommands**.</span><span class="sxs-lookup"><span data-stu-id="a4e55-123">The Group Policy flags are under registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Tpm**\\**BlockedCommands**.</span></span>

<span data-ttu-id="a4e55-124">Per determinare gli elenchi da usare per bloccare i comandi TPM, sono disponibili due valori **DWORD** usati come flag booleani:</span><span class="sxs-lookup"><span data-stu-id="a4e55-124">To determine which lists should be used to block TPM commands, there are two **DWORD** values that are used as Boolean flags:</span></span>

-   <span data-ttu-id="a4e55-125">"IgnoreDefaultList"</span><span class="sxs-lookup"><span data-stu-id="a4e55-125">"IgnoreDefaultList"</span></span>

    <span data-ttu-id="a4e55-126">Se impostato (il valore esiste e è diverso da zero), TBS ignora l'elenco dei comandi bloccati predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a4e55-126">If set (value exists and is nonzero), the TBS ignores the default blocked-commands list.</span></span>

-   <span data-ttu-id="a4e55-127">"IgnoreLocalList"</span><span class="sxs-lookup"><span data-stu-id="a4e55-127">"IgnoreLocalList"</span></span>

    <span data-ttu-id="a4e55-128">Se impostato (il valore esiste e è diverso da zero), TBS ignora l'elenco dei comandi bloccati locali.</span><span class="sxs-lookup"><span data-stu-id="a4e55-128">If set (value exists and is nonzero), the TBS ignores the local blocked-commands list.</span></span>

## <a name="group-policy-object-editor"></a><span data-ttu-id="a4e55-129">Editor oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="a4e55-129">Group Policy Object Editor</span></span>

<span data-ttu-id="a4e55-130">**Per accedere all'Editor oggetti di Criteri di gruppo**</span><span class="sxs-lookup"><span data-stu-id="a4e55-130">**To access the Group Policy object editor**</span></span>

1.  <span data-ttu-id="a4e55-131">Fare clic su **Start** (Avvia).</span><span class="sxs-lookup"><span data-stu-id="a4e55-131">Click **Start**.</span></span>
2.  <span data-ttu-id="a4e55-132">Fare clic su **Esegui**.</span><span class="sxs-lookup"><span data-stu-id="a4e55-132">Click **Run**.</span></span>
3.  <span data-ttu-id="a4e55-133">Nella casella **Apri** digitare **gpedit.msc**.</span><span class="sxs-lookup"><span data-stu-id="a4e55-133">In the **Open** box, type **gpedit.msc**.</span></span> <span data-ttu-id="a4e55-134">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4e55-134">Click **OK**.</span></span> <span data-ttu-id="a4e55-135">Verrà aperto l'Editor oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="a4e55-135">The Group Policy object editor opens.</span></span>
4.  <span data-ttu-id="a4e55-136">Espandere **Configurazione computer**.</span><span class="sxs-lookup"><span data-stu-id="a4e55-136">Expand **Computer Configuration**.</span></span>
5.  <span data-ttu-id="a4e55-137">Espandere **modelli amministrativi**.</span><span class="sxs-lookup"><span data-stu-id="a4e55-137">Expand **Administrative Templates**.</span></span>
6.  <span data-ttu-id="a4e55-138">Espandere **sistema**.</span><span class="sxs-lookup"><span data-stu-id="a4e55-138">Expand **System**.</span></span>
7.  <span data-ttu-id="a4e55-139">Espandere **Trusted Platform Module Services**.</span><span class="sxs-lookup"><span data-stu-id="a4e55-139">Expand **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="a4e55-140">Gli elenchi di comandi TPM 1.2 bloccati specifici possono essere modificati direttamente nei percorsi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a4e55-140">The lists of specific blocked TPM1.2 commands can be edited directly in the following locations.</span></span>

-   <span data-ttu-id="a4e55-141">Elenco criteri di gruppo:</span><span class="sxs-lookup"><span data-stu-id="a4e55-141">Group policy list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   <span data-ttu-id="a4e55-142">Elenco locale:</span><span class="sxs-lookup"><span data-stu-id="a4e55-142">Local list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   <span data-ttu-id="a4e55-143">Elenco predefinito:</span><span class="sxs-lookup"><span data-stu-id="a4e55-143">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

<span data-ttu-id="a4e55-144">In ognuna di queste chiavi del registro di sistema è presente un elenco di valori del registro di sistema di \_ tipo reg SZ.</span><span class="sxs-lookup"><span data-stu-id="a4e55-144">Under each of these registry keys, there is a list of registry values of REG\_SZ type.</span></span> <span data-ttu-id="a4e55-145">Ogni valore rappresenta un comando TPM bloccato.</span><span class="sxs-lookup"><span data-stu-id="a4e55-145">Each value represents a blocked TPM command.</span></span> <span data-ttu-id="a4e55-146">Ogni chiave del registro di sistema ha un campo "nome valore" e un campo "dati valore".</span><span class="sxs-lookup"><span data-stu-id="a4e55-146">Each registry key has a "Value name" field and a "Value data" field.</span></span> <span data-ttu-id="a4e55-147">Sia i campi ("nome valore" che "dati valore") devono corrispondere esattamente al valore decimale dell'ordinale del comando TPM da bloccare.</span><span class="sxs-lookup"><span data-stu-id="a4e55-147">Both fields ("Value Name" and "Value data"), should exactly match the decimal value of the TPM command ordinal to be blocked.</span></span>

<span data-ttu-id="a4e55-148">L'elenco di specifici comandi TPM 2,0 consentiti può essere modificato direttamente nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="a4e55-148">The list of specific allowed TPM 2.0 commands can be edited directly in the following location.</span></span> <span data-ttu-id="a4e55-149">Nella chiave del registro di sistema è presente un elenco dei valori del registro di sistema REG \_ DWORD Type.</span><span class="sxs-lookup"><span data-stu-id="a4e55-149">Under the registry key, there is a list of registry values of REG\_DWORD type.</span></span> <span data-ttu-id="a4e55-150">Ogni valore rappresenta un comando TPM 2,0 consentito.</span><span class="sxs-lookup"><span data-stu-id="a4e55-150">Each value represents an allowed TPM 2.0 command.</span></span> <span data-ttu-id="a4e55-151">Ogni valore del registro di sistema ha un **nome** e un campo **valore** .</span><span class="sxs-lookup"><span data-stu-id="a4e55-151">Each registry value has a **name** and a **value** field.</span></span> <span data-ttu-id="a4e55-152">Il **nome** corrisponde al numero ordinale del comando TPM 2,0 esadecimale che deve essere consentito.</span><span class="sxs-lookup"><span data-stu-id="a4e55-152">The **name** matches the hexadecimal TPM 2.0 command ordinal that should be allowed.</span></span> <span data-ttu-id="a4e55-153">Se **il comando** è consentito, il valore è 1.</span><span class="sxs-lookup"><span data-stu-id="a4e55-153">The **value** has a value of 1 if the command is allowed.</span></span> <span data-ttu-id="a4e55-154">Se un ordinale del comando non è presente o ha un valore pari a 0, il comando verrà bloccato.</span><span class="sxs-lookup"><span data-stu-id="a4e55-154">If a command ordinal is not present or has a value of 0, the command will be blocked.</span></span>

-   <span data-ttu-id="a4e55-155">Elenco predefinito:</span><span class="sxs-lookup"><span data-stu-id="a4e55-155">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

<span data-ttu-id="a4e55-156">Per Windows 8, Windows Server 2012 e versioni successive, le chiavi del registro di sistema **BlockedCommands** e **AllowedW8Commands** stabiliscono rispettivamente i comandi TPM bloccati o consentiti per gli account amministratore.</span><span class="sxs-lookup"><span data-stu-id="a4e55-156">For Windows 8, Windows Server 2012 and later, the **BlockedCommands** and **AllowedW8Commands** registry keys respectively determine the blocked or allowed TPM commands for administrator accounts.</span></span> <span data-ttu-id="a4e55-157">Gli account utente includono rispettivamente un elenco di comandi TPM bloccati o consentiti nelle chiavi del registro di sistema **BlockedUserCommands** e **AllowedW8UserCommands** .</span><span class="sxs-lookup"><span data-stu-id="a4e55-157">User accounts have a list of blocked or allowed TPM commands in the **BlockedUserCommands** and **AllowedW8UserCommands** registry keys respectively.</span></span> <span data-ttu-id="a4e55-158">In Windows 10 versione 1607 sono state introdotte nuove chiavi del registro di sistema per le applicazioni AppContainer: **BlockedAppContainerCommands** e **AllowedW8AppContainerCommands**.</span><span class="sxs-lookup"><span data-stu-id="a4e55-158">In Windows 10, version 1607, new registry keys have been introduces for AppContainer applications: **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands**.</span></span>

 

 




