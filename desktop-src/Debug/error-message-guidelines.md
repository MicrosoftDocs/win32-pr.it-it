---
description: Le linee guida in questo argomento consentono di scrivere messaggi di errore chiari, facili da localizzare e utili per i clienti.
ms.assetid: 361833e4-b94f-4ef9-a8f5-adf543534a67
title: Linee guida per i messaggi di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ceb2c89826ce45f39fdce2d0102e847c00245ba62ec3522e83725944b7f421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343491"
---
# <a name="error-message-guidelines"></a>Linee guida per i messaggi di errore

Un messaggio di errore è un testo visualizzato per descrivere un problema che impedisce all'utente o al sistema di completare un'attività. Il problema potrebbe causare il danneggiamento o la perdita dei dati. Altri tipi di messaggio includono conferme, avvisi e notifiche. Le linee guida in questo argomento consentono di scrivere messaggi di errore chiari, facili da localizzare e utili per i clienti.

I messaggi di errore scritti in modo non significativo possono essere fonte di frustrazione per gli utenti e possono aumentare i costi del supporto tecnico. Un messaggio di errore ben scritto fornisce all'utente le informazioni seguenti:

-   Che cosa è successo e perché?
-   Qual è il risultato finale per l'utente?
-   Cosa può fare l'utente per evitare che si verifichi di nuovo?

La lunghezza del testo non rappresenta un problema, purché lo sviluppatore gestisca correttamente le dimensioni del buffer. È importante che l'utente abbia tutte le informazioni necessarie per risolvere il problema. Se un messaggio ha più destinatari, potrebbe essere necessario fornire testo separato per amministratori, utenti finali e sviluppatori.

## <a name="best-practices"></a>Procedure consigliate

Di seguito sono riportati i modi per migliorare i messaggi di errore:

-   Evitare condizioni di errore. Se è possibile prevedere che si verificherà un errore quando un utente esegue un'azione specifica, riscrivere il codice in modo che l'utente non possa causare l'errore.
-   Scrivere un messaggio di errore separato per ogni causa nota dell'errore. Non usare un singolo messaggio generico per spiegare ogni possibile motivo dell'errore, a meno che non sia possibile determinare la causa dell'errore quando si verifica.
-   Indica chiaramente il problema e, se sarà utile per l'utente, spiega cosa ha causato il problema. Quando possibile, sostituire i messaggi generici dalle risorse della tabella dei messaggi di sistema con un messaggio dettagliato specifico del problema.
-   Fornire all'utente una soluzione al problema. Se la soluzione include più passaggi, fare riferimento a un argomento della Guida in cui viene illustrata in dettaglio l'attività.
-   Visualizzare solo il nome del prodotto, del componente o della procedura guidata nella barra del titolo del messaggio. Ciò consente all'utente di determinare dove si trova il problema. Non riepilogare il problema nella barra del titolo o includere la parola "errore".
-   Non usare il gergo tecnico, usare la terminologia che il pubblico comprende. Non usare slang o abbreviazioni.
-   Usare i pulsanti di comando appropriati, ad esempio OK, Annulla, Sì, No e Riprova. È possibile usare combinazioni di questi pulsanti. I pulsanti Sì e No devono essere sempre usati in combinazione e devono essere sempre preceduti da una domanda.
    -   Per arrestare un'operazione e chiudere la finestra di messaggio, usare il **pulsante** Annulla.
    -   Per chiudere una finestra di messaggio, usare il **pulsante** Chiudi.
    -   Per fornire altre informazioni sulla causa dell'errore, usare il **pulsante** Dettagli.
    -   Per fornire altre informazioni sulla soluzione al problema, usare il **pulsante ?** .
    -   Se nel messaggio è inclusa un'azione utente, usare il **pulsante OK** per chiudere la finestra di messaggio.
    -   **I** pulsanti **Sì e No** devono essere usati in combinazione e devono essere sempre preceduti da una domanda.
-   Se l'errore è un errore critico, scriverlo nel [registro eventi](../eventlog/event-logging.md).

## <a name="style-considerations"></a>Considerazioni sullo stile

-   Usare frasi complete ma semplici.
-   Usare il tempo presente per descrivere le condizioni che hanno causato il problema o uno stato ancora esistente. È possibile usare il tempo passato per descrivere un evento distinto che si è verificato in passato.
-   Usare la voce attiva quando possibile. È possibile usare la voce passiva per descrivere la condizione di errore.
-   Evitare il testo maiuscolo e i punti esclamativi.
-   Non fare in modo che l'utente si senta in errore anche se il problema è il risultato di un errore dell'utente.
-   Non eseguire la tropizzazione. Non implica che i programmi o l'hardware possano pensare o sentire.
-   Non usare parole o frasi colloquiali. Non usare termini che possono essere offensivi in determinate impostazioni cultura.
-   Non composto più sostantivi senza aggiungere una preposizione o una sottoclause per chiarire il significato. Ad esempio, "Server di directory del servizio LDAP del server del sito" deve essere modificato in "Server di directory per il servizio LDAP del server del sito".
-   Inserire descrittori prima di un termine per chiarire il significato della frase. Ad esempio, "Specificare InfID quando Detect è impostato su No". deve essere modificato in "Specificare il parametro InfID quando l'opzione Rileva è impostata su No".
-   Evitare la parola "bad". Usare termini più descrittivi per indicare all'utente cosa non va. Ad esempio, evitare messaggi come "Dimensioni non consentite". Indicare invece all'utente quali criteri usare quando si specifica una dimensione.
-   Evitare la parola "please". Può essere interpretato per indicare che un'azione richiesta è facoltativa.
-   Inserire parole sia nell'indice che rilevanti per il significato centrale all'inizio della stringa di messaggio.

 

 
