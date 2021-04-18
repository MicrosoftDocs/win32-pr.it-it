---
description: Informazioni sull'internazionalizzazione
ms.assetid: 9147cd20-eeae-4ad4-8d51-ac1d68a4b2c5
title: Informazioni sull'internazionalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df3fc38ab844ec991c0e87f286ffb48c3d48ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316274"
---
# <a name="understanding-internationalization"></a>Informazioni sull'internazionalizzazione

Lo sviluppo di prodotti software internazionali richiede non solo la produzione di codice corretto, ma anche una progettazione che consenta al prodotto di supportare molte impostazioni locali. Gli sviluppatori e i rispettivi responsabili devono essere a conoscenza del livello di sforzo e dell'attenzione ai dettagli necessari per creare applicazioni internazionali, se vengono recapitate come singoli file binari pronti per l'uso in diversi mercati o come più file binari specifici per un'unica impostazione locale. Gli sviluppatori assicurano che la gestione riconosca che l'internazionalizzazione implica più del semplice sviluppo di codice. La progettazione per l'internazionalizzazione all'inizio del ciclo del prodotto ti permette di risparmiare tempo, denaro e fatica.

**Internazionalizzazione** è la creazione di software che si adatta alle impostazioni locali in tutto il mondo. Le **impostazioni locali** sono una raccolta di preferenze utente correlate al linguaggio. Le impostazioni locali vengono specificate dall'associazione di una lingua e di un'area geografica. Ad esempio, inglese (Stati Uniti) e inglese (Regno Unito) sono due impostazioni locali diverse, in inglese (Canada) e francese (Canada).

Il software internazionalizzazione presenta questi attributi:

-   La predisposizione per l' **internazionalizzazione** riguarda progettazione e implementazione che separano il codice indipendente dalle impostazioni locali dalle risorse dipendenti dalle impostazioni locali e comprende due aree principali:
    -   La **globalizzazione** è il processo di sviluppo di un programma di base con funzionalità e progettazione di codice indipendenti dalle lingue o dalle impostazioni locali. Il progetto supporta invece l'input, la visualizzazione e l'output di script di linguaggio supportati da Unicode, oltre ai dati correlati a impostazioni locali specifiche.
    -   La **localizzabilità** è la progettazione della base di codice software e delle risorse in modo che un programma possa essere localizzato, come definito di seguito, in diverse edizioni della lingua senza alcuna modifica al codice sorgente. Ad esempio, i buffer di stringa nel codice e le caselle di testo nell'interfaccia utente devono essere sufficientemente grandi da contenere stringhe di testo più lunghe in lingue quali tedesco o olandese.
-   **Localizzazione** Questo implica la traduzione e la personalizzazione di un prodotto per un mercato specifico e principalmente la creazione di file di risorse anziché la scrittura di codice sorgente.

Ad esempio, l'uso del NLS (National Language Support) fornito dall'API Microsoft Win32 è un processo di sviluppo software che supporta la predisposizione per l'internazionalizzazione, mentre la modifica degli elementi dell'interfaccia utente, la traduzione del testo e la standardizzazione della terminologia sono passaggi di localizzazione eseguiti in genere da un utente che è uno specialista del linguaggio, ad esempio un traduttore. Anche quando lo sviluppo del codice enfatizza la predisposizione per l'internazionalizzazione, è necessario comprendere la localizzazione poiché le decisioni di progettazione influiscono sul lavoro del traduttore.

 

 



