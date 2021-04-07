---
description: Le linee guida riportate in questo argomento consentono di scrivere messaggi di errore chiari facili da localizzare e utili per i clienti.
ms.assetid: 361833e4-b94f-4ef9-a8f5-adf543534a67
title: Linee guida per i messaggi di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1787eabd43d660322577ac766880d76854c574e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747735"
---
# <a name="error-message-guidelines"></a>Linee guida per i messaggi di errore

Un messaggio di errore è il testo visualizzato per descrivere un problema che si è verificato che impedisce all'utente o al sistema di completare un'attività. Il problema potrebbe causare il danneggiamento o la perdita dei dati. Altri tipi di messaggio includono conferme, avvisi e notifiche. Le linee guida riportate in questo argomento consentono di scrivere messaggi di errore chiari facili da localizzare e utili per i clienti.

I messaggi di errore scritti correttamente possono costituire un'origine di frustrazione per gli utenti e possono aumentare i costi di supporto tecnico. Un messaggio di errore ben scritto fornisce all'utente le informazioni seguenti:

-   Che cosa è successo e perché?
-   Qual è il risultato finale per l'utente?
-   Cosa può fare l'utente per impedire che si verifichi di nuovo?

La lunghezza del testo non è un problema, purché lo sviluppatore gestisca correttamente le dimensioni del buffer. È importante che l'utente disponga di tutte le informazioni necessarie per risolvere il problema. Se un messaggio include più destinatari, potrebbe essere necessario fornire testo separato per gli amministratori, gli utenti finali e gli sviluppatori.

## <a name="best-practices"></a>Procedure consigliate

Di seguito sono riportati alcuni modi per migliorare i messaggi di errore:

-   Evitare le condizioni di errore. Se è possibile stimare che si verificherà un errore quando un utente esegue un'azione specifica, riscrivere il codice in modo che l'utente non possa causare l'errore.
-   Scrivere un messaggio di errore separato per ogni origine nota dell'errore. Non usare un singolo messaggio generico per spiegare ogni possibile motivo dell'errore, a meno che non sia possibile determinare la causa dell'errore quando si verifica.
-   Indicare chiaramente il problema e, se è utile per l'utente, spiegare la causa del problema. Quando possibile, sostituire i messaggi generici dalle risorse della tabella dei messaggi di sistema con un messaggio dettagliato specifico del problema.
-   Fornire all'utente una soluzione al problema. Se la soluzione contiene più di un passaggio, fare riferimento a un argomento della guida che illustra in dettaglio l'attività.
-   Consente di visualizzare solo il nome prodotto, componente o procedura guidata nella barra del titolo del messaggio. Ciò consente all'utente di determinare dove si è verificata la causa del problema. Non riepilogare il problema nella barra del titolo o includere la parola "errore".
-   Non usare il gergo tecnico, usare la terminologia riconosciuta dai destinatari. Non usare slang o abbreviazioni.
-   Usare i pulsanti di comando appropriati, ad esempio OK, Annulla, sì, no e riprova. È possibile utilizzare combinazioni di questi pulsanti. I pulsanti Sì e no devono essere sempre usati insieme e devono essere sempre preceduti da una domanda.
    -   Per arrestare un'operazione e chiudere la finestra di messaggio, utilizzare il pulsante **Annulla** .
    -   Per chiudere una finestra di messaggio, utilizzare il pulsante **Chiudi** .
    -   Per fornire ulteriori informazioni sulla cause dell'errore, utilizzare il pulsante **Dettagli** .
    -   Per fornire ulteriori informazioni sulla soluzione al problema, utilizzare **il pulsante?** .
    -   Se un'azione utente viene inclusa nel messaggio, utilizzare il pulsante **OK** per chiudere la finestra di messaggio.
    -   È necessario utilizzare in combinazione i pulsanti **Sì** e **No** e deve essere sempre preceduto da una domanda.
-   Se l'errore è un errore critico, scriverlo nel [registro eventi](../eventlog/event-logging.md).

## <a name="style-considerations"></a>Considerazioni sullo stile

-   Utilizzare frasi complete ma semplici.
-   Usare il tempo presente per descrivere le condizioni che hanno causato il problema o uno stato ancora esistente. È possibile utilizzare il tempo passato per descrivere un evento distinto che si è verificato nel passato.
-   Usare la voce attiva quando possibile. È possibile utilizzare la voce passiva per descrivere la condizione di errore.
-   Evitare il testo maiuscolo e i punti esclamativi.
-   Non fare in modo che l'utente si trovi in errore anche se il problema è causato da un errore dell'utente.
-   Non antropomorfizzare. Non implica che i programmi o l'hardware possano pensare o meno.
-   Non usare parole o frasi familiari. Non usare termini che potrebbero essere offensivi in determinate impostazioni cultura.
-   Non compostano più sostantivi senza aggiungere una preposizione o una sottoclausola per chiarire il significato. Ad esempio, "il server di directory del servizio LDAP del server di sito" deve essere modificato in "server di directory per il servizio LDAP del server del sito".
-   Inserire i descrittori prima di un termine per chiarire il significato della frase. Ad esempio, "specifica InfID quando il rilevamento è impostato su No". deve essere modificato in "specificare il parametro InfID quando l'opzione rileva è impostata su No".
-   Evitare la parola "Bad". Usare termini più descrittivi per indicare all'utente il problema. Ad esempio, evitare messaggi quali "dimensioni errate". Al contrario, indicare all'utente quali criteri usare quando si specifica una dimensione.
-   Evitare la parola "Please". Può essere interpretato per indicare che un'azione obbligatoria è facoltativa.
-   Inserire parole che sono entrambe nell'indice e rilevanti per il significato centrale all'inizio della stringa del messaggio.

 

 
