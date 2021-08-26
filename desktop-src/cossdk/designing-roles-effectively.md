---
description: In molti scenari la sicurezza basata sui ruoli è un meccanismo molto efficace, ma in alcune situazioni è meno efficace.
ms.assetid: 6a1e6cf3-7a8c-4249-926d-675a54061adf
title: Progettazione efficace dei ruoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134b1caa68c06aef14a21963bb01ee4dfd12f43153ea917487598d76b0e36d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991121"
---
# <a name="designing-roles-effectively"></a>Progettazione efficace dei ruoli

In molti scenari la sicurezza basata sui ruoli è un meccanismo molto efficace, ma in alcune situazioni è meno efficace. Quando si decide dove e come applicare la sicurezza basata sui ruoli a una determinata applicazione, è necessario prendere in considerazione diversi fattori.

## <a name="user-and-data-characteristics-and-the-suitability-of-roles"></a>Caratteristiche degli utenti e dei dati e idoneità dei ruoli

I ruoli funzionano molto bene per caratterizzare i gruppi di utenti e, su tale base, filtrare le azioni che gli utenti possono eseguire. Spesso questa operazione viene eseguita creando ruoli che riflettono la posizione di un utente all'interno di un'organizzazione, ad esempio i ruoli "Manager" e "Teller", "Amministratori" e "Lettori", "Project One Employees" e "Project Two Employees". In questi casi, in cui i dati a cui si accede sono piuttosto generici rispetto agli utenti, i ruoli possono essere usati in modo efficiente per applicare regole business come le seguenti:

-   "I manager possono trasferire qualsiasi importo di denaro. Gli utenti possono trasferire solo fino a $ 10.000."

-   "Gli amministratori possono modificare qualsiasi elemento. Tutti gli altri possono solo leggere".

-   "Project un dipendente può accedere a un determinato database. Nessun altro può".

Gli utenti possono naturalmente rientrare in più ruoli, a seconda del modo in cui i ruoli modellano la struttura organizzativa di un'azienda.

Tuttavia, i ruoli non funzionano molto bene quando una decisione di accesso alla sicurezza dipende sulle caratteristiche di un particolare dato. Ad esempio, sarebbe difficile usare i ruoli per riflettere relazioni utente-dati complesse come le seguenti:

-   "Un manager specifico può accedere ai dati del personale solo per i report personali".

-   "Joe Consumer can look up his account balance."

In questi casi, il controllo di sicurezza deve spesso essere eseguito nel database stesso, in cui è più facile prendere in considerazione le caratteristiche innate dei dati a cui si accede. Ciò significa che è necessario utilizzare la *rappresentazione* per passare l'identità client al database e consentire al database di convalidare la richiesta. Ciò può influire sulle prestazioni e influire sulla progettazione dell'applicazione. Ad esempio, il pool di connessioni potrebbe non funzionare quando viene aperta una connessione con una determinata identità utente. Per una descrizione dei problemi, vedere Sicurezza delle applicazioni [multilivello](multi-tier-application-security.md) e [Rappresentazione e delega del client.](client-impersonation-and-delegation.md)

## <a name="complexity-and-scalability-of-a-role-based-authorization-policy"></a>Complessità e scalabilità di un Role-Based di autorizzazione

Qualsiasi criterio di sicurezza inserito sarà efficace solo quanto l'implementazione da parte degli amministratori di sistema che distribuiscono l'applicazione. Se gli amministratori commettono errori nell'assegnazione degli utenti ai ruoli corretti in base ai criteri di sicurezza, i criteri non funzioneranno come previsto. È molto probabile che si verifichino problemi nelle circostanze seguenti:

-   Sono stati emersi criteri basati sui ruoli molto complessi, con molti ruoli e utenti che eservitino il mapping a numerosi ruoli.
-   È possibile creare ruoli con criteri ambigui per gli utenti che devono appartenere a essi.
-   Nel sito in cui è installata l'applicazione sono presenti molti utenti e gli utenti si spostano spesso all'interno dell'organizzazione, modificando i ruoli creati.
-   Nel sito in cui è installata l'applicazione sono presenti molti amministratori, con una suddivisione di responsabilità, in modo che un amministratore che abbia familiarità con i requisiti di sicurezza dell'applicazione non abbia familiarità con i gruppi di utenti di grandi dimensioni che devono usarla. Questo è un problema particolare quando gli utenti si spostano all'interno dell'organizzazione. Tali informazioni devono essere comunicate in modo ben noto.

Inoltre, con l'aumentare del numero di ruoli assegnati a un'applicazione, aumenta anche la quantità di tempo che COM+ deve dedicare alla ricerca dell'appartenenza del chiamante a tali ruoli, con una probabile riduzione delle prestazioni.

Per gestire la complessità e attenuare questi problemi, è possibile usare le linee guida seguenti:

-   Scegliere nomi di ruolo auto descrittivi. Rendere più ovvio possibile quali utenti devono appartenere a quali ruoli.
-   Rendere i criteri basati sui ruoli il più semplici possibile (e non più semplici). Scegliere il numero di ruoli possibile, mantenendo al tempo stesso un criterio efficace.
-   Documentare chiaramente i criteri basati sui ruoli che si costruiscono per gli amministratori, indipendentemente dal fatto che l'appartenenza ai ruoli sia ovvia (per l'utente). In particolare, usare il campo della descrizione disponibile per ogni ruolo per descrivere la finalità del ruolo. Se non è possibile descrivere in genere chi deve appartenere al ruolo in un paio di frasi, è probabilmente troppo complicato.
-   È consigliabile che gli amministratori dell'applicazione popolino i ruoli con gruppi di utenti anziché con singoli utenti. Si tratta di una soluzione molto più scalabile. Rende più semplice riassegnare o rimuovere gli utenti quando si spostano all'interno dell'organizzazione e isola gli amministratori da una certa quantità di supervisione e problemi di comunicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limiti di sicurezza](security-boundaries.md)
</dt> <dt>

[Informazioni sul contesto di chiamata di sicurezza](security-call-context-information.md)
</dt> <dt>

[Proprietà del contesto di sicurezza](security-context-property.md)
</dt> <dt>

[Uso dei ruoli per l'autorizzazione client](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



