---
description: Informazioni sull'internazionalizzazione
ms.assetid: 9147cd20-eeae-4ad4-8d51-ac1d68a4b2c5
title: Informazioni sull'internazionalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed47364da56e2c5ab5e13001b1b49360b23caa39997484e5058022516f437b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638791"
---
# <a name="understanding-internationalization"></a>Informazioni sull'internazionalizzazione

Lo sviluppo di prodotti software internazionalizzati richiede non solo la produzione di codice corretto, ma anche una progettazione che consenta al prodotto di supportare molte impostazioni locali. Gli sviluppatori e i responsabili devono essere consapevoli del livello di impegno e dell'attenzione ai dettagli necessari per creare applicazioni pronte per il mondo, indipendentemente dal fatto che siano distribuite come singoli file binari pronti per l'uso in molti mercati diversi o come più file binari specifici di un'unica impostazione locale. Gli sviluppatori si assicurano che la gestione comprendi che l'internazionalizzazione non riguarda solo lo sviluppo di codice. La progettazione per l'internazionalizzazione all'inizio del ciclo di prodotti consente di risparmiare tempo, denaro e fatica.

**L'internazionalizzazione** è la creazione di software che si adatta alle impostazioni locali in tutto il mondo. Le **impostazioni locali** sono una raccolta di preferenze utente correlate alla lingua. Le impostazioni locali vengono specificate dall'associazione di una lingua e di un'area geografica. Ad esempio, l'inglese (Stati Uniti) e l'inglese (Regno Unito) sono due impostazioni locali diverse, come l'inglese (Canada) e il francese (Canada).

Il software internazionalizzato ha questi attributi:

-   **L'idoneità al** mondo riguarda la progettazione e l'implementazione che separano il codice indipendente dalle impostazioni locali dalle risorse dipendenti dalle impostazioni locali e comprende due aree principali:
    -   **La globalizzazione** è il processo di sviluppo di un core programma con funzionalità e progettazione del codice indipendenti dalla lingua o dalle impostazioni locali. Al contrario, la progettazione supporta l'input, la visualizzazione e l'output degli script della lingua supportati da Unicode, nonché i dati correlati a impostazioni locali specifiche.
    -   **La localizzabilità** è la progettazione della codebase software e delle risorse in modo che un programma possa essere localizzato, come definito di seguito, in edizioni in lingue diverse senza modifiche al codice sorgente. Ad esempio, i buffer di stringa nel codice e le caselle di testo nell'interfaccia utente devono essere sufficientemente grandi da contenere stringhe di testo più lunghe in lingue come il tedesco o l'olandese.
-   **Localizzazione** Ciò comporta la traduzione e la personalizzazione di un prodotto per un mercato specifico e riguarda principalmente la creazione di file di risorse anziché la scrittura di codice sorgente.

Ad esempio, l'uso del supporto NLS (National Language Support) fornito dall'API Microsoft Win32 è un processo di sviluppo software che supporta l'idoneità al mondo, mentre la modifica degli elementi dell'interfaccia utente, la traduzione del testo e la standardizzazione della terminologia sono passaggi di localizzazione in genere eseguiti da un esperto di lingue, ad esempio un traduttore. Anche quando lo sviluppo del codice enfatizza l'idoneità al mondo, è necessario comprendere la localizzazione perché le decisioni di progettazione influiscono sul lavoro del traduttore.

 

 



