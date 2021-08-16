---
description: Lo scopo della regola dei criteri di autorizzazione centrale è fornire una definizione a livello di dominio di un aspetto isolato dei criteri di autorizzazione delle organizzazioni.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Regola dei criteri di autorizzazione centrale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5638633f655794464a9d603e1bb6a0380d2224170b9afe0f6314b1f8fee945b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783205"
---
# <a name="central-authorization-policy-rule"></a>Regola dei criteri di autorizzazione centrale

Lo scopo della regola dei criteri di autorizzazione centrale è fornire una definizione a livello di dominio di un aspetto isolato dei criteri di autorizzazione dell'organizzazione. L'amministratore definisce il CAPR per applicare uno dei requisiti di autorizzazione specifici. Poiché il capr definisce solo un requisito desiderato specifico dei criteri di autorizzazione, può essere definito e compreso più semplicemente che se tutti i requisiti dei criteri di autorizzazione dell'organizzazione vengono compilati in una singola definizione di criteri.

Il capr ha gli attributi seguenti:

-   Nome: identifica il capr agli amministratori.
-   Descrizione: definisce lo scopo del CAPR e tutte le informazioni che possono essere necessarie ai consumer del CAPR.
-   Espressione di applicabilità: definisce le risorse o le situazioni in cui verranno applicati i criteri.
-   ID: identificatore da usare nel controllo delle modifiche apportate al capr.
-   Criteri di controllo di accesso effettivi: Windows descrittore di sicurezza contenente un elenco DACL che definisce i criteri di autorizzazione effettivi.
-   Espressione di eccezione: una o più espressioni che forniscono un mezzo per eseguire l'override dei criteri e concedere l'accesso a un'entità in base alla valutazione dell'espressione.
-   Criteri di gestione temporanea: un descrittore di sicurezza Windows facoltativo contenente un elenco DACL che definisce un criterio di autorizzazione proposto (elenco di voci di controllo di accesso) che verrà testato rispetto ai criteri effettivi ma non applicati. Se esiste una differenza tra i risultati dei criteri effettivi e i criteri di gestione temporanea, la differenza verrà registrata nel registro eventi di controllo.
    -   Poiché la gestione temporanea può avere un effetto imprevedibile sulle prestazioni del sistema, un amministratore Criteri di gruppo deve essere in grado di selezionare computer specifici in cui sarà attivo lo staging. In questo modo i criteri esistenti possono essere posizionati nella maggior parte dei computer di un'unità organizzativa durante la gestione temporanea in un subset dei computer.
    -   P2: un amministratore locale in un computer specifico deve essere in grado di disabilitare la gestione temporanea se lo staging in tale computer causa una riduzione troppo significativa delle prestazioni.
-   Backlink a CAP: elenco di backlink a qualsiasi CAP che può fare riferimento a questo CAPR.

Durante il controllo di accesso, il capr viene valutato per l'applicabilità in base all'espressione di applicabilità. Se è applicabile un CAPR, viene valutato se fornisce all'utente richiedente l'accesso richiesto alla risorsa identificata. I risultati della valutazione CAPE vengono quindi uniti logicamente da **AND** con i risultati dell'elenco DACL sulla risorsa e qualsiasi altro CAPR applicabile in vigore sulla risorsa.

CapR di esempio:

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

## <a name="deny-aces-in-capes"></a>Negare le voci ACE nelle api di controllo di accesso

In Windows 8 le ACE di negazione non saranno supportate in un capr. L'esperienza utente di creazione capr non consentirà la creazione di una ACE di negazione. Inoltre, quando l'LSA recupera il cap da Active Directory, LSA verificherà che nessun capR abbia ACE di negazione. Se viene trovata una voce ACE di negazione in un capr, il cap verrà considerato non valido e non verrà copiato nel Registro di sistema o in SRM.

> [!Note]  
> Il controllo di accesso non impone che non siano presenti ACE di negazione. Verranno applicate le ACE di negazione in un capr. È previsto che gli strumenti di creazione impediranno questa situazione.

 

## <a name="cape-definition"></a>Definizione di CAPE

I capr vengono creati anche se viene fornita una nuova esperienza utente in Centro di amministrazione di Active Directory (ADAC). In ADAC viene fornita una nuova opzione di attività per creare un capr. Quando questa attività è selezionata, ADAC richiede all'utente una finestra di dialogo che richiede all'utente un nome capr e una descrizione. Quando vengono forniti, i controlli per definire uno qualsiasi degli elementi CAPR rimanenti diventano abilitati. Per ogni elemento CAPR rimanente, l'esperienza utente chiamerà l'interfaccia utente ACL per consentire la definizione di espressioni e/o ACL.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[Scenario di controllo dinamico degli accessi (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
