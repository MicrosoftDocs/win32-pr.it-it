---
title: Controllo di accesso (piattaforma filtro Windows)
description: In Windows Filtering Platform (WFP), il servizio BFE (Base Filtering Engine) implementa il modello di controllo di accesso di Windows standard basato sui token di accesso e i descrittori di sicurezza.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350986"
---
# <a name="access-control-windows-filtering-platform"></a><span data-ttu-id="88fb1-103">Controllo di accesso (piattaforma filtro Windows)</span><span class="sxs-lookup"><span data-stu-id="88fb1-103">Access Control (Windows Filtering Platform)</span></span>

<span data-ttu-id="88fb1-104">In Windows Filtering Platform (WFP), il servizio BFE (Base Filtering Engine) implementa il [modello di controllo di accesso di Windows](/windows/desktop/SecAuthZ/access-control-model) standard basato sui token di accesso e i descrittori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="88fb1-104">In Windows Filtering Platform (WFP), the Base Filtering Engine (BFE) service implements the standard [Windows access control model](/windows/desktop/SecAuthZ/access-control-model) based on access tokens and security descriptors.</span></span>

## <a name="access-control-model"></a><span data-ttu-id="88fb1-105">Modello di controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="88fb1-105">Access Control Model</span></span>

<span data-ttu-id="88fb1-106">I descrittori di sicurezza possono essere specificati quando si aggiungono nuovi oggetti WFP, ad esempio filtri e sottolivelli.</span><span class="sxs-lookup"><span data-stu-id="88fb1-106">Security descriptors can be specified when adding new WFP objects, such as filters and sub-layers.</span></span> <span data-ttu-id="88fb1-107">I descrittori di sicurezza vengono gestiti tramite le funzioni di gestione PAM **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0**, dove \* *\** _ sta per il nome dell'oggetto WFP.</span><span class="sxs-lookup"><span data-stu-id="88fb1-107">Security descriptors are managed using the WFP management functions **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0**, where \**\** _ stands for the WFP object's name.</span></span> <span data-ttu-id="88fb1-108">Queste funzioni sono semanticamente identiche alle funzioni Windows [_ *GetSecurityInfo* \*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="88fb1-108">These functions are semantically identical to the Windows [_ *GetSecurityInfo*\*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

> [!Note]  
> <span data-ttu-id="88fb1-109">Non è possibile chiamare le funzioni **\* SetSecurityInfo0 di Fwpm** dall'interno di una transazione esplicita.</span><span class="sxs-lookup"><span data-stu-id="88fb1-109">The **Fwpm\*SetSecurityInfo0** functions cannot be called from within an explicit transaction.</span></span>

 

> [!Note]  
> <span data-ttu-id="88fb1-110">Le funzioni **Fwpm \* SetSecurityInfo0** possono essere chiamate solo dall'interno di una sessione dinamica se vengono usate per gestire un oggetto dinamico creato all'interno della stessa sessione.</span><span class="sxs-lookup"><span data-stu-id="88fb1-110">The **Fwpm\*SetSecurityInfo0** functions can only be called from within a dynamic session if they are being used to manage a dynamic object created within the same session.</span></span>

 

<span data-ttu-id="88fb1-111">Il descrittore di sicurezza predefinito per il motore di filtro (l'oggetto motore radice nel diagramma seguente) è il seguente.</span><span class="sxs-lookup"><span data-stu-id="88fb1-111">The default security descriptor for the filter engine (the root Engine object in the diagram below) is as follows.</span></span>

-   <span data-ttu-id="88fb1-112">Concedere i diritti di accesso **generici \_ All** (GA) al gruppo Administrators predefinito.</span><span class="sxs-lookup"><span data-stu-id="88fb1-112">Grant **GENERIC\_ALL** (GA) access rights to the built-in Administrators group.</span></span>
-   <span data-ttu-id="88fb1-113">Concedere i diritti di accesso generico di **\_ lettura** (gr) Generic **\_ Write** ( **GW) per \_** gli operatori di configurazione di rete.</span><span class="sxs-lookup"><span data-stu-id="88fb1-113">Grant **GENERIC\_READ** (GR) **GENERIC\_WRITE** (GW) **GENERIC\_EXECUTE** (GX) access rights to network configuration operators.</span></span>
-   <span data-ttu-id="88fb1-114">Concedere i diritti di accesso **GRGWGX** ai seguenti identificatori di sicurezza del servizio (SSID): MpsSvc (Windows Firewall), napagent (agente protezione accesso alla rete), PolicyAgent (agente criteri IPSec), RPCSS (Remote Procedure Call) e WdiServiceHost (host del servizio di diagnostica).</span><span class="sxs-lookup"><span data-stu-id="88fb1-114">Grant **GRGWGX** access rights to the following service security identifiers (SSIDs): MpsSvc (Windows Firewall), NapAgent (Network Access Protection Agent), PolicyAgent (IPsec Policy Agent), RpcSs (Remote Procedure Call), and WdiServiceHost (Diagnostic Service Host).</span></span>
-   <span data-ttu-id="88fb1-115">Concedere a **FWPM \_ ACTRL \_ Open** e **FWPM \_ ACTRL \_ classificate** a tutti.</span><span class="sxs-lookup"><span data-stu-id="88fb1-115">Grant **FWPM\_ACTRL\_OPEN** and **FWPM\_ACTRL\_CLASSIFY** to everyone.</span></span> <span data-ttu-id="88fb1-116">Si tratta di diritti di accesso specifici di WFP, descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="88fb1-116">(These are WFP-specific access rights, described in table below.)</span></span>

<span data-ttu-id="88fb1-117">I rimanenti descrittori di sicurezza predefiniti sono derivati tramite ereditarietà.</span><span class="sxs-lookup"><span data-stu-id="88fb1-117">The remaining default security descriptors are derived through inheritance.</span></span>

<span data-ttu-id="88fb1-118">Sono disponibili alcuni controlli di accesso, ad esempio per le chiamate di funzione **Fwpm \* Add0**, **Fwpm \* CreateEnumHandle0**, **Fwpm \* SubscribeChanges0** , che non possono essere eseguite a livello di singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="88fb1-118">There are some access checks, such as for **Fwpm\*Add0**, **Fwpm\*CreateEnumHandle0**, **Fwpm\*SubscribeChanges0** function calls, that cannot be done at the individual object level.</span></span> <span data-ttu-id="88fb1-119">Per queste funzioni sono disponibili oggetti contenitore per ogni tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="88fb1-119">For these functions, there are container objects for each object type.</span></span> <span data-ttu-id="88fb1-120">Per i tipi di oggetto standard (ad esempio, provider, callout, filtri), le funzioni **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0** esistenti sono in overload, in modo che un parametro **GUID** null identifichi il contenitore associato.</span><span class="sxs-lookup"><span data-stu-id="88fb1-120">For the standard object types (for example, providers, callouts, filters), the existing **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0** functions are overloaded, such that a null **GUID** parameter identifies the associated container.</span></span> <span data-ttu-id="88fb1-121">Per gli altri tipi di oggetto (ad esempio, eventi di rete e associazioni di sicurezza IPsec), sono disponibili funzioni esplicite per la gestione delle informazioni di sicurezza del contenitore.</span><span class="sxs-lookup"><span data-stu-id="88fb1-121">For the other object types (for example, network events and IPsec security associations), there are explicit functions for managing the container's security information.</span></span>

<span data-ttu-id="88fb1-122">BFE supporta l'ereditarietà automatica delle voci di controllo di accesso (DACL) dell'elenco di controllo di accesso discrezionale (DACL).</span><span class="sxs-lookup"><span data-stu-id="88fb1-122">BFE supports automatic inheritance of Discretionary Access Control List (DACL) access control entries (ACEs).</span></span> <span data-ttu-id="88fb1-123">BFE non supporta le voci dell'elenco di controllo di accesso di sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="88fb1-123">BFE does not support System Access Control List (SACL) ACEs.</span></span> <span data-ttu-id="88fb1-124">Gli oggetti ereditano le voci ACE dal relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="88fb1-124">Objects inherit ACEs from their container.</span></span> <span data-ttu-id="88fb1-125">I contenitori ereditano le voci ACE dal motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="88fb1-125">Containers inherit ACEs from the filter engine.</span></span> <span data-ttu-id="88fb1-126">Il diagramma seguente illustra i percorsi di propagazione.</span><span class="sxs-lookup"><span data-stu-id="88fb1-126">The propagation paths are shown in the diagram below.</span></span>

![Diagramma che mostra i percorsi di propagazione ACE, a partire da' Engine '.](images/access-control.jpg)

<span data-ttu-id="88fb1-128">Per i tipi di oggetto standard, BFE impone tutti i diritti di accesso generici e standard.</span><span class="sxs-lookup"><span data-stu-id="88fb1-128">For the standard object types, BFE enforces all the generic and standard access rights.</span></span> <span data-ttu-id="88fb1-129">Inoltre, WFP definisce i seguenti diritti di accesso specifici.</span><span class="sxs-lookup"><span data-stu-id="88fb1-129">In addition, WFP defines the following specific access rights.</span></span>



| <span data-ttu-id="88fb1-130">Diritto di accesso WFP</span><span class="sxs-lookup"><span data-stu-id="88fb1-130">WFP Access Right</span></span>                                                                                                                        | <span data-ttu-id="88fb1-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88fb1-131">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88fb1-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**\_aggiunta FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span><br/>                                       | <span data-ttu-id="88fb1-133">Obbligatorio per aggiungere un oggetto a un contenitore.</span><span class="sxs-lookup"><span data-stu-id="88fb1-133">Required to add an object to a container.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="88fb1-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Aggiungi \_ collegamento**</span><span class="sxs-lookup"><span data-stu-id="88fb1-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>                       | <span data-ttu-id="88fb1-135">Obbligatorio per creare un'associazione a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="88fb1-135">Required to create an association to an object.</span></span> <span data-ttu-id="88fb1-136">Per aggiungere, ad esempio, un filtro che fa riferimento a un callout, il chiamante deve disporre dell' \_ accesso Aggiungi collegamento al callout.</span><span class="sxs-lookup"><span data-stu-id="88fb1-136">For example, to add a filter that references a callout, the caller must have ADD\_LINK access to the callout.</span></span><br/> |
| <span data-ttu-id="88fb1-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="88fb1-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span><br/>    | <span data-ttu-id="88fb1-138">Obbligatorio per iniziare una transazione di lettura esplicita.</span><span class="sxs-lookup"><span data-stu-id="88fb1-138">Required to begin an explicit read transaction.</span></span><br/>                                                                                                               |
| <span data-ttu-id="88fb1-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="88fb1-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span><br/> | <span data-ttu-id="88fb1-140">Obbligatorio per iniziare una transazione di scrittura esplicita.</span><span class="sxs-lookup"><span data-stu-id="88fb1-140">Required to begin an explicit write transaction.</span></span><br/>                                                                                                              |
| <span data-ttu-id="88fb1-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_classificazione FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span><br/>                        | <span data-ttu-id="88fb1-142">Obbligatorio per la classificazione in base a un livello in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="88fb1-142">Required to classify against a user-mode layer.</span></span><br/>                                                                                                               |
| <span data-ttu-id="88fb1-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**\_enumerazione FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span><br/>                                    | <span data-ttu-id="88fb1-144">Obbligatorio per enumerare gli oggetti in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="88fb1-144">Required to enumerate the objects in a container.</span></span> <span data-ttu-id="88fb1-145">Tuttavia, l'enumeratore restituisce solo gli oggetti a cui il chiamante \_ ha \_ accesso in lettura ACTRL FWPM.</span><span class="sxs-lookup"><span data-stu-id="88fb1-145">However, the enumerator only returns objects to which the caller has FWPM\_ACTRL\_READ access.</span></span><br/>              |
| <span data-ttu-id="88fb1-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="88fb1-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span><br/>                                    | <span data-ttu-id="88fb1-147">Obbligatorio per aprire una sessione con BFE.</span><span class="sxs-lookup"><span data-stu-id="88fb1-147">Required to open a session with BFE.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="88fb1-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="88fb1-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span><br/>                                    | <span data-ttu-id="88fb1-149">Obbligatorio per leggere le proprietà di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="88fb1-149">Required to read an object's properties.</span></span><br/>                                                                                                                      |
| <span data-ttu-id="88fb1-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_ \_ statistiche leggere FWPM \_ ACTRL**</span><span class="sxs-lookup"><span data-stu-id="88fb1-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span><br/>                 | <span data-ttu-id="88fb1-151">Obbligatorio per leggere le statistiche.</span><span class="sxs-lookup"><span data-stu-id="88fb1-151">Required to read statistics.</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="88fb1-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**sottoscrizione di FWPM \_ ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span><br/>                     | <span data-ttu-id="88fb1-153">Obbligatorio per sottoscrivere le notifiche.</span><span class="sxs-lookup"><span data-stu-id="88fb1-153">Required to subscribe for notifications.</span></span> <span data-ttu-id="88fb1-154">I sottoscrittori riceveranno solo le notifiche per gli oggetti a cui hanno \_ accesso in lettura ACTRL FWPM \_ .</span><span class="sxs-lookup"><span data-stu-id="88fb1-154">Subscribers will only receive notifications for objects to which they have FWPM\_ACTRL\_READ access.</span></span><br/>                 |
| <span data-ttu-id="88fb1-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**\_scrittura FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span><br/>                                 | <span data-ttu-id="88fb1-156">Obbligatorio per impostare le opzioni del motore.</span><span class="sxs-lookup"><span data-stu-id="88fb1-156">Required to set engine options.</span></span><br/>                                                                                                                               |



 

<span data-ttu-id="88fb1-157">BFE ignora tutti i controlli di accesso per i chiamanti in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="88fb1-157">BFE skips all access checks for kernel-mode callers.</span></span>

<span data-ttu-id="88fb1-158">Per impedire agli amministratori di bloccarsi da BFE, ai membri del gruppo Administrators predefinito viene sempre concesso **FWPM \_ ACTRL \_ aperto** all'oggetto motore.</span><span class="sxs-lookup"><span data-stu-id="88fb1-158">In order to prevent administrators from locking themselves out of BFE, members of the built-in administrators group are always granted **FWPM\_ACTRL\_OPEN** to the engine object.</span></span> <span data-ttu-id="88fb1-159">Pertanto, un amministratore può ottenere nuovamente l'accesso tramite i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="88fb1-159">Thus, an administrator can regain access through the following steps.</span></span>

-   <span data-ttu-id="88fb1-160">Abilitare il **privilegio \_ se \_ accetta \_ nome proprietà** .</span><span class="sxs-lookup"><span data-stu-id="88fb1-160">Enable the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="88fb1-161">Chiamare [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="88fb1-161">Call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span> <span data-ttu-id="88fb1-162">La chiamata ha esito positivo perché il chiamante è un membro degli amministratori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="88fb1-162">The call succeeds because the caller is a member of Built-in Administrators.</span></span>
-   <span data-ttu-id="88fb1-163">Assumere la proprietà dell'oggetto motore.</span><span class="sxs-lookup"><span data-stu-id="88fb1-163">Take ownership of the engine object.</span></span> <span data-ttu-id="88fb1-164">Questa operazione ha esito positivo perché il chiamante ha il privilegio **se \_ accetta il \_ \_ nome di proprietà** .</span><span class="sxs-lookup"><span data-stu-id="88fb1-164">This succeeds because the caller has the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="88fb1-165">Aggiornare l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="88fb1-165">Update the DACL.</span></span> <span data-ttu-id="88fb1-166">Questa operazione ha esito positivo perché il proprietario ha sempre l'accesso a **\_ DAC in scrittura**</span><span class="sxs-lookup"><span data-stu-id="88fb1-166">This succeeds because the owner always has **WRITE\_DAC** access</span></span>

<span data-ttu-id="88fb1-167">Poiché BFE supporta il proprio controllo personalizzato, non genera controlli di accesso agli oggetti generici.</span><span class="sxs-lookup"><span data-stu-id="88fb1-167">Since BFE supports its own custom auditing, it does not generate generic object access audits.</span></span> <span data-ttu-id="88fb1-168">Quindi, il SACL viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="88fb1-168">Thus, the SACL is ignored.</span></span>

## <a name="wfp-required-access-rights"></a><span data-ttu-id="88fb1-169">Diritti di accesso necessari per Pam</span><span class="sxs-lookup"><span data-stu-id="88fb1-169">WFP Required Access Rights</span></span>

<span data-ttu-id="88fb1-170">La tabella seguente illustra i diritti di accesso richiesti dalle funzioni PAM per accedere a vari oggetti della piattaforma di filtro.</span><span class="sxs-lookup"><span data-stu-id="88fb1-170">The table below shows the access rights required by the WFP functions in order to access various filtering platform objects.</span></span> <span data-ttu-id="88fb1-171">Le **\* *funzioni _ FwpmFilter sono elencate come esempio per l'accesso agli oggetti standard. Tutte le altre funzioni che accedono agli oggetti standard seguono il modello di* \*** accesso alle funzioni _ FwpmFilter.</span><span class="sxs-lookup"><span data-stu-id="88fb1-171">The **FwpmFilter\**_ functions are listed as an example for accessing the standard objects. All the other functions that access standard objects follow the _\* FwpmFilter\**\* functions access model.</span></span>



<span data-ttu-id="88fb1-172">Funzione</span><span class="sxs-lookup"><span data-stu-id="88fb1-172">Function</span></span>

<span data-ttu-id="88fb1-173">Oggetto selezionato</span><span class="sxs-lookup"><span data-stu-id="88fb1-173">Object Checked</span></span>

<span data-ttu-id="88fb1-174">Accesso obbligatorio</span><span class="sxs-lookup"><span data-stu-id="88fb1-174">Access Required</span></span>

[<span data-ttu-id="88fb1-175">**FwpmEngineOpen0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-175">**FwpmEngineOpen0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

<span data-ttu-id="88fb1-176">Motore</span><span class="sxs-lookup"><span data-stu-id="88fb1-176">Engine</span></span>

<span data-ttu-id="88fb1-177">**FWPM \_ ACTRL \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="88fb1-177">**FWPM\_ACTRL\_OPEN**</span></span>

[<span data-ttu-id="88fb1-178">**FwpmEngineGetOption0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-178">**FwpmEngineGetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

<span data-ttu-id="88fb1-179">Motore</span><span class="sxs-lookup"><span data-stu-id="88fb1-179">Engine</span></span>

<span data-ttu-id="88fb1-180">**FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="88fb1-180">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="88fb1-181">**FwpmEngineSetOption0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-181">**FwpmEngineSetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

<span data-ttu-id="88fb1-182">Motore</span><span class="sxs-lookup"><span data-stu-id="88fb1-182">Engine</span></span>

<span data-ttu-id="88fb1-183">**\_scrittura FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-183">**FWPM\_ACTRL\_WRITE**</span></span>

[<span data-ttu-id="88fb1-184">**FwpmSessionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-184">**FwpmSessionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

<span data-ttu-id="88fb1-185">Motore</span><span class="sxs-lookup"><span data-stu-id="88fb1-185">Engine</span></span>

<span data-ttu-id="88fb1-186">**\_enumerazione FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-186">**FWPM\_ACTRL\_ENUM**</span></span>

[<span data-ttu-id="88fb1-187">**FwpmTransactionBegin0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-187">**FwpmTransactionBegin0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

<span data-ttu-id="88fb1-188">Motore</span><span class="sxs-lookup"><span data-stu-id="88fb1-188">Engine</span></span>

<span data-ttu-id="88fb1-189">**FWPM \_ ACTRL \_ Begin \_ Read \_ transazione**  &  **FWPM \_ ACTRL \_ Begin \_ Write \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="88fb1-189">**FWPM\_ACTRL\_BEGIN\_READ\_TXN** & **FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>

[<span data-ttu-id="88fb1-190">**FwpmFilterAdd0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-190">**FwpmFilterAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

<span data-ttu-id="88fb1-191">Provider di contenitori</span><span class="sxs-lookup"><span data-stu-id="88fb1-191">Container Provider</span></span><br/> <span data-ttu-id="88fb1-192">Livello</span><span class="sxs-lookup"><span data-stu-id="88fb1-192">Layer</span></span><br/> <span data-ttu-id="88fb1-193">Sub-Layer</span><span class="sxs-lookup"><span data-stu-id="88fb1-193">Sub-Layer</span></span><br/> <span data-ttu-id="88fb1-194">Callout</span><span class="sxs-lookup"><span data-stu-id="88fb1-194">Callout</span></span><br/> <span data-ttu-id="88fb1-195">Contesto del provider</span><span class="sxs-lookup"><span data-stu-id="88fb1-195">Provider Context</span></span><br/>

<span data-ttu-id="88fb1-196">**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ Aggiungi \_ collegamento**</span><span class="sxs-lookup"><span data-stu-id="88fb1-196">**FWPM\_ACTRL\_ADDFWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="88fb1-197">**FWPM \_ ACTRL \_ Aggiungi \_ collegamento**</span><span class="sxs-lookup"><span data-stu-id="88fb1-197">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="88fb1-198">**FWPM \_ ACTRL \_ Aggiungi \_ collegamento**</span><span class="sxs-lookup"><span data-stu-id="88fb1-198">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="88fb1-199">**FWPM \_ ACTRL \_ Aggiungi \_ collegamento**</span><span class="sxs-lookup"><span data-stu-id="88fb1-199">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="88fb1-200">**FWPM \_ ACTRL \_ Aggiungi \_ collegamento**</span><span class="sxs-lookup"><span data-stu-id="88fb1-200">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>

<span data-ttu-id="88fb1-201">[](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0** FwpmFilterDeleteById0](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="88fb1-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span></span><br/>

<span data-ttu-id="88fb1-202">Filtra</span><span class="sxs-lookup"><span data-stu-id="88fb1-202">Filter</span></span>

<span data-ttu-id="88fb1-203">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="88fb1-203">**DELETE**</span></span>

<span data-ttu-id="88fb1-204">[](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0** FwpmFilterGetById0](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span><span class="sxs-lookup"><span data-stu-id="88fb1-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span></span><br/>

<span data-ttu-id="88fb1-205">Filtra</span><span class="sxs-lookup"><span data-stu-id="88fb1-205">Filter</span></span>

<span data-ttu-id="88fb1-206">**FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="88fb1-206">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="88fb1-207">**FwpmFilterCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-207">**FwpmFilterCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

<span data-ttu-id="88fb1-208">Filtro contenitore</span><span class="sxs-lookup"><span data-stu-id="88fb1-208">Container Filter</span></span><br/>

<span data-ttu-id="88fb1-209">**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="88fb1-209">**FWPM\_ACTRL\_ENUMFWPM\_ACTRL\_READ**</span></span><br/>

[<span data-ttu-id="88fb1-210">**FwpmFilterSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-210">**FwpmFilterSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

<span data-ttu-id="88fb1-211">Contenitore</span><span class="sxs-lookup"><span data-stu-id="88fb1-211">Container</span></span>

<span data-ttu-id="88fb1-212">**sottoscrizione di FWPM \_ ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-212">**FWPM\_ACTRL\_SUBSCRIBE**</span></span>

[<span data-ttu-id="88fb1-213">**FwpmFilterSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-213">**FwpmFilterSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

<span data-ttu-id="88fb1-214">Contenitore</span><span class="sxs-lookup"><span data-stu-id="88fb1-214">Container</span></span>

<span data-ttu-id="88fb1-215">**FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="88fb1-215">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="88fb1-216">**IPsecGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-216">**IPsecGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

<span data-ttu-id="88fb1-217">DB SA IPsec</span><span class="sxs-lookup"><span data-stu-id="88fb1-217">IPsec SA DB</span></span>

<span data-ttu-id="88fb1-218">**\_ \_ statistiche leggere FWPM \_ ACTRL**</span><span class="sxs-lookup"><span data-stu-id="88fb1-218">**FWPM\_ACTRL\_READ\_STATS**</span></span>

<span data-ttu-id="88fb1-219">[](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0** IPsecSaContextCreate0](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span><span class="sxs-lookup"><span data-stu-id="88fb1-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span></span><br/> [<span data-ttu-id="88fb1-220">**IPsecSaContextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-220">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [<span data-ttu-id="88fb1-221">**IPsecSaContextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-221">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

<span data-ttu-id="88fb1-222">DB SA IPsec</span><span class="sxs-lookup"><span data-stu-id="88fb1-222">IPsec SA DB</span></span>

<span data-ttu-id="88fb1-223">**\_aggiunta FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-223">**FWPM\_ACTRL\_ADD**</span></span>

<span data-ttu-id="88fb1-224">[](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0** IPsecSaContextDeleteById0](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span><span class="sxs-lookup"><span data-stu-id="88fb1-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span></span><br/>

<span data-ttu-id="88fb1-225">DB SA IPsec</span><span class="sxs-lookup"><span data-stu-id="88fb1-225">IPsec SA DB</span></span>

<span data-ttu-id="88fb1-226">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="88fb1-226">**DELETE**</span></span>

[<span data-ttu-id="88fb1-227">**IPsecSaContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-227">**IPsecSaContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

<span data-ttu-id="88fb1-228">DB SA IPsec</span><span class="sxs-lookup"><span data-stu-id="88fb1-228">IPsec SA DB</span></span>

<span data-ttu-id="88fb1-229">**FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="88fb1-229">**FWPM\_ACTRL\_READ**</span></span>

<span data-ttu-id="88fb1-230">[](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0** IPsecSaContextCreateEnumHandle0](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span><span class="sxs-lookup"><span data-stu-id="88fb1-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span></span><br/>

<span data-ttu-id="88fb1-231">DB SA IPsec</span><span class="sxs-lookup"><span data-stu-id="88fb1-231">IPsec SA DB</span></span>

<span data-ttu-id="88fb1-232">**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="88fb1-232">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="88fb1-233">**IkeextGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-233">**IkeextGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

<span data-ttu-id="88fb1-234">DB SA IKE</span><span class="sxs-lookup"><span data-stu-id="88fb1-234">IKE SA DB</span></span>

<span data-ttu-id="88fb1-235">**\_ \_ statistiche leggere FWPM \_ ACTRL**</span><span class="sxs-lookup"><span data-stu-id="88fb1-235">**FWPM\_ACTRL\_READ\_STATS**</span></span>

[<span data-ttu-id="88fb1-236">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-236">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

<span data-ttu-id="88fb1-237">DB SA IKE</span><span class="sxs-lookup"><span data-stu-id="88fb1-237">IKE SA DB</span></span>

<span data-ttu-id="88fb1-238">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="88fb1-238">**DELETE**</span></span>

[<span data-ttu-id="88fb1-239">**IkeextSaGetById0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-239">**IkeextSaGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

<span data-ttu-id="88fb1-240">DB SA IKE</span><span class="sxs-lookup"><span data-stu-id="88fb1-240">IKE SA DB</span></span>

<span data-ttu-id="88fb1-241">**FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="88fb1-241">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="88fb1-242">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-242">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

<span data-ttu-id="88fb1-243">DB SA IKE</span><span class="sxs-lookup"><span data-stu-id="88fb1-243">IKE SA DB</span></span>

<span data-ttu-id="88fb1-244">**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="88fb1-244">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="88fb1-245">**FwpmNetEventCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="88fb1-245">**FwpmNetEventCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

<span data-ttu-id="88fb1-246">Contenitore</span><span class="sxs-lookup"><span data-stu-id="88fb1-246">Container</span></span>

<span data-ttu-id="88fb1-247">**\_enumerazione FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="88fb1-247">**FWPM\_ACTRL\_ENUM**</span></span>

<span data-ttu-id="88fb1-248">[](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0** FwpmIPsecTunnelAdd0](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="88fb1-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span></span><br/>

<span data-ttu-id="88fb1-249">Nessun controllo di accesso aggiuntivo oltre a quelli per i singoli contesti di filtri e provider</span><span class="sxs-lookup"><span data-stu-id="88fb1-249">No additional access checks beyond those for the individual filters and provider contexts</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="88fb1-250">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88fb1-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88fb1-251">**Diritti di accesso standard**</span><span class="sxs-lookup"><span data-stu-id="88fb1-251">**Standard Access Rights**</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="88fb1-252">Modello di controllo di accesso di Windows</span><span class="sxs-lookup"><span data-stu-id="88fb1-252">Windows access control model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[<span data-ttu-id="88fb1-253">**Identificatori dei diritti di accesso della piattaforma filtro Windows**</span><span class="sxs-lookup"><span data-stu-id="88fb1-253">**Windows Filtering Platform Access Rights Identifiers**</span></span>](access-right-identifiers.md)
</dt> </dl>

 

