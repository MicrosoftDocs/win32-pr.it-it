---
description: In molti scenari la protezione basata sui ruoli è un meccanismo molto efficace, ma in alcuni casi è meno efficace.
ms.assetid: 6a1e6cf3-7a8c-4249-926d-675a54061adf
title: Progettazione efficace dei ruoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a340cb2fc643a414ebf784a14e7b61a45bccd3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523249"
---
# <a name="designing-roles-effectively"></a>Progettazione efficace dei ruoli

In molti scenari la protezione basata sui ruoli è un meccanismo molto efficace, ma in alcuni casi è meno efficace. È necessario prendere in considerazione alcuni fattori quando si decide dove e come applicare la sicurezza basata sui ruoli a una particolare applicazione.

## <a name="user-and-data-characteristics-and-the-suitability-of-roles"></a>Caratteristiche di utenti e dati e idoneità dei ruoli

I ruoli funzionano molto bene per caratterizzare i gruppi di utenti e, su tale base, filtrare le azioni che gli utenti possono eseguire. Spesso questa operazione viene eseguita in pratica creando ruoli che riflettono la posizione di un utente all'interno di un'organizzazione, ad esempio i ruoli "Manager" e "Tellers", "Administrators" e "Readers", "Project One Employees" e "Project Two Employees". In questi casi, in cui i dati a cui si accede sono piuttosto generici rispetto agli utenti, i ruoli possono essere utilizzati in modo efficiente per applicare regole business come le seguenti:

-   "I responsabili possono trasferire qualsiasi quantità di denaro. I reteller possono trasferire solo fino a $10.000 ".

-   "Gli amministratori possono modificare qualsiasi elemento. Tutti gli altri utenti possono solo leggere ".

-   "Il progetto One Employees può accedere a un determinato database. Nessun altro possibile. "

È possibile che gli utenti rientrino naturalmente in più ruoli, a seconda del modo in cui i ruoli modellano la struttura organizzativa di un'azienda.

Tuttavia, i ruoli non funzionano molto bene quando una decisione di accesso alla sicurezza si basa sulle caratteristiche di un determinato dato. Ad esempio, sarebbe difficile usare i ruoli per riflettere le complesse relazioni utente-dati come le seguenti:

-   "Un particolare responsabile può accedere ai dati del personale solo per i propri report."

-   "Joe consumer può cercare il suo saldo conto".

In questi casi, il controllo della sicurezza deve essere spesso eseguito nel database stesso, in cui è più semplice prendere in considerazione le caratteristiche innate dei dati a cui si accede. Ciò significa che è necessario utilizzare la *rappresentazione* per passare l'identità del client insieme al database e consentire al database di convalidare la richiesta. Questo può influire sulle prestazioni e può influire sulla progettazione dell'applicazione, ad esempio il pool di connessioni potrebbe non funzionare quando viene aperta una connessione con una determinata identità utente. Per informazioni sui problemi correlati, vedere [protezione delle applicazioni](multi-tier-application-security.md) a più livelli e [rappresentazione e delega del client](client-impersonation-and-delegation.md).

## <a name="complexity-and-scalability-of-a-role-based-authorization-policy"></a>Complessità e scalabilità di un criterio di autorizzazione Role-Based

Tutti i criteri di sicurezza applicati saranno efficaci solo come la relativa implementazione da parte degli amministratori di sistema che distribuiscono l'applicazione. Se gli amministratori hanno commesso errori nell'assegnazione di utenti ai ruoli corretti in base ai criteri di sicurezza, i criteri non funzioneranno come previsto. I problemi si verificano con maggiore probabilità nei casi seguenti:

-   Sono stati creati criteri molto complessi basati sui ruoli, con molti ruoli e utenti che hanno eseguito il mapping a numerosi ruoli.
-   È possibile creare ruoli con criteri ambigui per chi deve appartenere ad essi.
-   Sono presenti molti utenti nel sito in cui è installata l'applicazione e gli utenti vengono spesso spostati all'interno dell'organizzazione, cambiando rispetto ai ruoli creati.
-   Ci sono molti amministratori nel sito in cui è installata l'applicazione, con la divisione delle responsabilità, in modo che un amministratore che abbia familiarità con i requisiti di sicurezza dell'applicazione non abbia familiarità con gli ampi gruppi di utenti che devono utilizzarlo. Si tratta di un problema particolare, perché gli utenti si spostano all'interno dell'organizzazione. tali informazioni devono essere comunicate correttamente.

Inoltre, man mano che aumenta il numero di ruoli assegnati a un'applicazione, l'intervallo di tempo COM+ deve dedicare alla ricerca dell'appartenenza del chiamante a tali ruoli, con una probabile riduzione delle prestazioni.

Per gestire la complessità e attenuare queste problematiche, è possibile usare le linee guida seguenti:

-   Scegliere i nomi dei ruoli che sono autodescrittivi. Renderlo più ovvio possibile quali utenti devono appartenere a quali ruoli.
-   Rendere i criteri basati sui ruoli il più semplice possibile (e senza più semplice). Scegliere il minor numero di ruoli possibile, mantenendo al tempo stesso un criterio effettivo.
-   Documentare chiaramente i criteri basati sui ruoli che si costruiscono per gli amministratori, se l'appartenenza al ruolo è ovvia (all'utente). In particolare, utilizzare il campo Description disponibile per ogni ruolo per descrivere lo scopo del ruolo. Se non è possibile descrivere in genere chi deve appartenere al ruolo in un paio di frasi, probabilmente è troppo complicato.
-   È consigliabile che gli amministratori dell'applicazione popolano i ruoli con gruppi di utenti anziché con singoli utenti. Si tratta di una soluzione molto più scalabile. Semplifica la riassegnazione o la rimozione degli utenti mentre si spostano all'interno dell'organizzazione e isola gli amministratori da una certa quantità di supervisione e problemi di comunicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limiti di sicurezza](security-boundaries.md)
</dt> <dt>

[Informazioni sul contesto delle chiamate di sicurezza](security-call-context-information.md)
</dt> <dt>

[Proprietà del contesto di sicurezza](security-context-property.md)
</dt> <dt>

[Utilizzo dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



