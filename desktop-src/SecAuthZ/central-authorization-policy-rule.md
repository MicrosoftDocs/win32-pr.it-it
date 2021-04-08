---
description: Lo scopo della regola dei criteri di autorizzazione centrale (CAPR) è fornire una definizione a livello di dominio di un aspetto isolato dei criteri di autorizzazione delle organizzazioni.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Regola dei criteri di autorizzazione centrale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda6279b2bf28f80f99a0e2608b5bf209855a76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058382"
---
# <a name="central-authorization-policy-rule"></a><span data-ttu-id="b5b16-103">Regola dei criteri di autorizzazione centrale</span><span class="sxs-lookup"><span data-stu-id="b5b16-103">Central Authorization Policy Rule</span></span>

<span data-ttu-id="b5b16-104">Lo scopo della regola dei criteri di autorizzazione centrale (CAPR) è fornire una definizione a livello di dominio di un aspetto isolato dei criteri di autorizzazione dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b5b16-104">The purpose of the Central Authorization Policy Rule (CAPR) is to provide a domain-wide definition of an isolated aspect of the organization's authorization policy.</span></span> <span data-ttu-id="b5b16-105">L'amministratore definisce CAPR per applicare uno dei requisiti di autorizzazione specifici.</span><span class="sxs-lookup"><span data-stu-id="b5b16-105">The administrator defines the CAPR to enforce one of the specific authorization requirements.</span></span> <span data-ttu-id="b5b16-106">Poiché CAPR definisce solo un requisito specifico per i criteri di autorizzazione, può essere definito più semplicemente e compreso se tutti i requisiti dei criteri di autorizzazione dell'organizzazione vengono compilati in una singola definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="b5b16-106">Since the CAPR defines only one specific desired requirement of the authorization policy it can be more simply defined and understood than if all the authorization policy requirements of the organization are compiled into a single policy definition.</span></span>

<span data-ttu-id="b5b16-107">Il CAPR ha gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5b16-107">The CAPR has the following attributes:</span></span>

-   <span data-ttu-id="b5b16-108">Nome: identifica CAPR per gli amministratori.</span><span class="sxs-lookup"><span data-stu-id="b5b16-108">Name – identifies the CAPR to the administrators.</span></span>
-   <span data-ttu-id="b5b16-109">Descrizione: definisce lo scopo di CAPR e tutte le informazioni che potrebbero essere necessarie per i consumer di CAPR.</span><span class="sxs-lookup"><span data-stu-id="b5b16-109">Description – defines the purpose of the CAPR and any information that may be needed by consumers of the CAPR.</span></span>
-   <span data-ttu-id="b5b16-110">Espressione applicabilità: definisce le risorse o le situazioni in cui verranno applicati i criteri.</span><span class="sxs-lookup"><span data-stu-id="b5b16-110">Applicability Expression – defines the resources or situations in which the policy will be applied.</span></span>
-   <span data-ttu-id="b5b16-111">ID: identificatore da usare nel controllo delle modifiche apportate a CAPR.</span><span class="sxs-lookup"><span data-stu-id="b5b16-111">ID – identifier for use in auditing of changes to the CAPR.</span></span>
-   <span data-ttu-id="b5b16-112">Criteri di controllo degli accessi validi, un descrittore di sicurezza di Windows contenente un DACL che definisce i criteri di autorizzazione validi.</span><span class="sxs-lookup"><span data-stu-id="b5b16-112">Effective Access Control Policy – a Windows security descriptor containing a DACL that defines the effective authorization policy.</span></span>
-   <span data-ttu-id="b5b16-113">Espressione di eccezione: una o più espressioni che forniscono un metodo per eseguire l'override del criterio e concedere l'accesso a un'entità in base alla valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="b5b16-113">Exception Expression – one or more expressions that provide a means to override the policy and grant access to a principal according to the evaluation of the expression.</span></span>
-   <span data-ttu-id="b5b16-114">Criteri di gestione temporanea: un descrittore di sicurezza di Windows facoltativo contenente un DACL che definisce i criteri di autorizzazione proposti (elenco di voci di controllo di accesso) che verranno testati rispetto ai criteri validi ma non applicati.</span><span class="sxs-lookup"><span data-stu-id="b5b16-114">Staging Policy – an optional Windows security descriptor containing a DACL that defines a proposed authorization policy (list of access control entries) that will be tested against the effective policy but not enforced.</span></span> <span data-ttu-id="b5b16-115">Se esiste una differenza tra i risultati dei criteri effettivi e i criteri di gestione temporanea, la differenza verrà registrata nel registro eventi di controllo.</span><span class="sxs-lookup"><span data-stu-id="b5b16-115">If there is a difference between the results of the effective policy and the staging policy the difference will be recorded in the audit event log.</span></span>
    -   <span data-ttu-id="b5b16-116">Poiché la gestione temporanea può avere un effetto imprevedibile sulle prestazioni del sistema, un amministratore di Criteri di gruppo deve essere in grado di selezionare computer specifici in cui verrà applicata la gestione temporanea.</span><span class="sxs-lookup"><span data-stu-id="b5b16-116">Since staging can have an unpredictable effect on system performance, a Group Policy administrator must be able to select specific machines on which staging will be in effect.</span></span> <span data-ttu-id="b5b16-117">In questo modo è possibile applicare i criteri esistenti alla maggior parte dei computer in un'unità organizzativa mentre la gestione temporanea si verifica in un subset di computer.</span><span class="sxs-lookup"><span data-stu-id="b5b16-117">This allows the existing policy to be in place on most machines in an OU while staging is happening on a subset of the machines.</span></span>
    -   <span data-ttu-id="b5b16-118">P2: un amministratore locale su un computer specifico deve essere in grado di disabilitare la gestione temporanea se la gestione temporanea di tale computer causa un calo eccessivo delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b5b16-118">P2 – A local administrator on a particular machine should be able to disable staging if staging on that machine is causing too much of a performance degradation.</span></span>
-   <span data-ttu-id="b5b16-119">Da backlink a CAP: un elenco di collegamenti a eventuali CAPs che possono essere riferiti a questo CAPR.</span><span class="sxs-lookup"><span data-stu-id="b5b16-119">Backlink to CAP – A list of backlinks to any CAPs that may be referring to this CAPR.</span></span>

<span data-ttu-id="b5b16-120">Durante il controllo dell'accesso, il CAPR viene valutato per l'applicabilità in base all'espressione di applicabilità.</span><span class="sxs-lookup"><span data-stu-id="b5b16-120">During access check, the CAPR is be evaluated for applicability based on the applicability expression.</span></span> <span data-ttu-id="b5b16-121">Se un CAPR è applicabile, viene valutato se fornisce all'utente richiedente l'accesso richiesto alla risorsa identificata.</span><span class="sxs-lookup"><span data-stu-id="b5b16-121">If a CAPR is applicable, it is evaluated for whether it provides the requesting user the requested access to the identified resource.</span></span> <span data-ttu-id="b5b16-122">I risultati della valutazione CAPE vengono quindi Uniti in modo logico da **e** con i risultati dell'elenco DACL sulla risorsa e di eventuali altri CAPRs applicabili sulla risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5b16-122">The results of the CAPE evaluation is then logically joined by **AND** with the results of the DACL on the resource and any other applicable CAPRs in effect on the resource.</span></span>

<span data-ttu-id="b5b16-123">CAPRs di esempio:</span><span class="sxs-lookup"><span data-stu-id="b5b16-123">Example CAPRs:</span></span>

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a><span data-ttu-id="b5b16-124">Nega le voci ACE in CAPES</span><span class="sxs-lookup"><span data-stu-id="b5b16-124">Deny ACEs in CAPEs</span></span>

<span data-ttu-id="b5b16-125">In Windows 8 Deny ACE non sarà supportato in una CAPR.</span><span class="sxs-lookup"><span data-stu-id="b5b16-125">In Windows 8 deny ACEs will not be supported in a CAPR.</span></span> <span data-ttu-id="b5b16-126">L'esperienza utente di creazione di CAPR non consente la creazione di una voce ACE Deny.</span><span class="sxs-lookup"><span data-stu-id="b5b16-126">The CAPR authoring UX will not allow creation of a deny ACE.</span></span> <span data-ttu-id="b5b16-127">Inoltre, quando l'LSA Recupera il CAP da Active Directory, LSA verificherà che nessun CAPRs abbia ACE di negazione.</span><span class="sxs-lookup"><span data-stu-id="b5b16-127">Additionally, when the LSA retrieves the CAP from Active Directory, LSA will verify that no CAPRs have deny ACEs.</span></span> <span data-ttu-id="b5b16-128">Se una voce Deny ACE viene trovata in un CAPR, il limite verrà considerato non valido e non verrà copiato nel registro di sistema o SRM.</span><span class="sxs-lookup"><span data-stu-id="b5b16-128">If a deny ACE is found in a CAPR then the CAP will be treated as invalid and not be copied to the registry or SRM.</span></span>

> [!Note]  
> <span data-ttu-id="b5b16-129">Il controllo dell'accesso non impone che non siano presenti ACE di negazione.</span><span class="sxs-lookup"><span data-stu-id="b5b16-129">The access check will not enforce that no deny ACEs are present.</span></span> <span data-ttu-id="b5b16-130">Verranno applicate le voci ACE Deny in un CAPR.</span><span class="sxs-lookup"><span data-stu-id="b5b16-130">Deny ACEs in a CAPR will be applied.</span></span> <span data-ttu-id="b5b16-131">Si prevede che gli strumenti di creazione impediscano questa situazione.</span><span class="sxs-lookup"><span data-stu-id="b5b16-131">It is expected that authoring tools will prevent this from happening.</span></span>

 

## <a name="cape-definition"></a><span data-ttu-id="b5b16-132">Definizione CAPE</span><span class="sxs-lookup"><span data-stu-id="b5b16-132">CAPE Definition</span></span>

<span data-ttu-id="b5b16-133">CAPRs vengono creati anche se una nuova esperienza utente è disponibile in Centro di amministrazione di Active Directory (ADAC). Per creare un CAPR, in ADAC è disponibile un'opzione nuova attività.</span><span class="sxs-lookup"><span data-stu-id="b5b16-133">CAPRs are created though a new UX provided in Active Directory Administrative Center (ADAC.) In ADAC a new task option is provided to create a CAPR.</span></span> <span data-ttu-id="b5b16-134">Quando questa attività è selezionata, il centro di ricerca richiede all'utente una finestra di dialogo in cui viene chiesto all'utente un nome CAPR e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="b5b16-134">When this task is selected, ADAC will prompt the user with a dialog asking the user for a CAPR name and a description.</span></span> <span data-ttu-id="b5b16-135">Quando vengono fornite, i controlli per definire gli elementi CAPR rimanenti diventano abilitati.</span><span class="sxs-lookup"><span data-stu-id="b5b16-135">When these are provided, the controls to define any of the remaining CAPR elements become enabled.</span></span> <span data-ttu-id="b5b16-136">Per ogni elemento CAPR rimanente, l'esperienza utente richiama l'interfaccia utente ACL per consentire la definizione di espressioni e/o ACL.</span><span class="sxs-lookup"><span data-stu-id="b5b16-136">For each of the remaining CAPR elements, the UX will call out to the ACL-UI to allow definition of expression and/or ACLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5b16-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b5b16-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5b16-138">**AccessCheck**</span><span class="sxs-lookup"><span data-stu-id="b5b16-138">**AccessCheck**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[<span data-ttu-id="b5b16-139">Scenario di controllo dinamico degli accessi (DAC)</span><span class="sxs-lookup"><span data-stu-id="b5b16-139">Dynamic Access Control (DAC) scenario</span></span>](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
