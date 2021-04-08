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
# <a name="central-authorization-policy-rule"></a>Regola dei criteri di autorizzazione centrale

Lo scopo della regola dei criteri di autorizzazione centrale (CAPR) è fornire una definizione a livello di dominio di un aspetto isolato dei criteri di autorizzazione dell'organizzazione. L'amministratore definisce CAPR per applicare uno dei requisiti di autorizzazione specifici. Poiché CAPR definisce solo un requisito specifico per i criteri di autorizzazione, può essere definito più semplicemente e compreso se tutti i requisiti dei criteri di autorizzazione dell'organizzazione vengono compilati in una singola definizione di criteri.

Il CAPR ha gli attributi seguenti:

-   Nome: identifica CAPR per gli amministratori.
-   Descrizione: definisce lo scopo di CAPR e tutte le informazioni che potrebbero essere necessarie per i consumer di CAPR.
-   Espressione applicabilità: definisce le risorse o le situazioni in cui verranno applicati i criteri.
-   ID: identificatore da usare nel controllo delle modifiche apportate a CAPR.
-   Criteri di controllo degli accessi validi, un descrittore di sicurezza di Windows contenente un DACL che definisce i criteri di autorizzazione validi.
-   Espressione di eccezione: una o più espressioni che forniscono un metodo per eseguire l'override del criterio e concedere l'accesso a un'entità in base alla valutazione dell'espressione.
-   Criteri di gestione temporanea: un descrittore di sicurezza di Windows facoltativo contenente un DACL che definisce i criteri di autorizzazione proposti (elenco di voci di controllo di accesso) che verranno testati rispetto ai criteri validi ma non applicati. Se esiste una differenza tra i risultati dei criteri effettivi e i criteri di gestione temporanea, la differenza verrà registrata nel registro eventi di controllo.
    -   Poiché la gestione temporanea può avere un effetto imprevedibile sulle prestazioni del sistema, un amministratore di Criteri di gruppo deve essere in grado di selezionare computer specifici in cui verrà applicata la gestione temporanea. In questo modo è possibile applicare i criteri esistenti alla maggior parte dei computer in un'unità organizzativa mentre la gestione temporanea si verifica in un subset di computer.
    -   P2: un amministratore locale su un computer specifico deve essere in grado di disabilitare la gestione temporanea se la gestione temporanea di tale computer causa un calo eccessivo delle prestazioni.
-   Da backlink a CAP: un elenco di collegamenti a eventuali CAPs che possono essere riferiti a questo CAPR.

Durante il controllo dell'accesso, il CAPR viene valutato per l'applicabilità in base all'espressione di applicabilità. Se un CAPR è applicabile, viene valutato se fornisce all'utente richiedente l'accesso richiesto alla risorsa identificata. I risultati della valutazione CAPE vengono quindi Uniti in modo logico da **e** con i risultati dell'elenco DACL sulla risorsa e di eventuali altri CAPRs applicabili sulla risorsa.

CAPRs di esempio:

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

## <a name="deny-aces-in-capes"></a>Nega le voci ACE in CAPES

In Windows 8 Deny ACE non sarà supportato in una CAPR. L'esperienza utente di creazione di CAPR non consente la creazione di una voce ACE Deny. Inoltre, quando l'LSA Recupera il CAP da Active Directory, LSA verificherà che nessun CAPRs abbia ACE di negazione. Se una voce Deny ACE viene trovata in un CAPR, il limite verrà considerato non valido e non verrà copiato nel registro di sistema o SRM.

> [!Note]  
> Il controllo dell'accesso non impone che non siano presenti ACE di negazione. Verranno applicate le voci ACE Deny in un CAPR. Si prevede che gli strumenti di creazione impediscano questa situazione.

 

## <a name="cape-definition"></a>Definizione CAPE

CAPRs vengono creati anche se una nuova esperienza utente è disponibile in Centro di amministrazione di Active Directory (ADAC). Per creare un CAPR, in ADAC è disponibile un'opzione nuova attività. Quando questa attività è selezionata, il centro di ricerca richiede all'utente una finestra di dialogo in cui viene chiesto all'utente un nome CAPR e una descrizione. Quando vengono fornite, i controlli per definire gli elementi CAPR rimanenti diventano abilitati. Per ogni elemento CAPR rimanente, l'esperienza utente richiama l'interfaccia utente ACL per consentire la definizione di espressioni e/o ACL.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[Scenario di controllo dinamico degli accessi (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
