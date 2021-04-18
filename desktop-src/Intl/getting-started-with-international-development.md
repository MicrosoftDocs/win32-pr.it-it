---
description: Questo argomento consente di iniziare a creare applicazioni internazionali, specificando prerequisiti, Riepilogando le tecnologie e introducendo un'esercitazione introduttiva.
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: Introduzione con sviluppo Windows internazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cc77a86b652f1b713b29517b513cddc26ed801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314817"
---
# <a name="getting-started-with-international-windows-development"></a>Introduzione con sviluppo Windows internazionale

Questo argomento consente di iniziare a creare applicazioni internazionali, specificando prerequisiti, Riepilogando le tecnologie e introducendo un'esercitazione introduttiva.

## <a name="getting-started"></a>Introduzione

Se si scrivono applicazioni per gli utenti in un'unica impostazione locale, tali applicazioni possono essere eseguite correttamente anche se vengono progettate con presupposti specifici delle impostazioni locali, ad esempio la presentazione di date in un particolare formato o l'ordinamento di stringhe in una determinata sequenza. A questo punto è necessario assicurarsi che le applicazioni possano essere usate in più paesi, da utenti con lingue diverse e impostazioni cultura diverse. Per avere esito positivo in più impostazioni locali, è necessario adattare le applicazioni alle impostazioni locali in cui vengono eseguite. Questa flessibilità è importante se viene aggiunta a un'applicazione esistente o se viene progettata in una nuova applicazione.

Questa sezione consente di iniziare a usare lo sviluppo internazionale. Vengono presentati collegamenti ad argomenti che forniscono panoramiche sui prerequisiti di internazionalizzazione. Riepiloga le tecnologie offerte dall'SDK per il supporto dei clienti in tutto il mondo. Infine, in questa sezione viene fornita un'applicazione di esempio che consente di risolvere un problema che spesso si verifica durante la scrittura di software globale.

## <a name="prerequisites"></a>Prerequisiti

È necessario acquisire familiarità con i problemi che si verificano nello sviluppo di software internazionale per Windows. Inizia con queste panoramiche.

-   La [comprensione dell'internazionalizzazione](understanding-internationalization.md) spiega la difficoltà aggiunta allo sviluppo di applicazioni predisposte per l'internazionalizzazione e definisce i termini chiave.
-   L'argomento relativo all'internazionalizzazione consente di [ottenere](https://msdn.microsoft.com/goglobal/bb895995.aspx) linee guida e procedure consigliate che è possibile scorrere o approfondire in base alle esigenze.
-   L' [elenco di controllo di internazionalizzazione](internationalization-checklist.md) riepiloga le azioni che è necessario intraprendere per creare un'applicazione predisposta per l'internazionalizzazione.
-   La sicurezza è sempre un problema nello sviluppo del software, ma è necessario considerare altri problemi durante lo sviluppo di software internazionali. Esaminare le considerazioni sulla [sicurezza: funzionalità internazionali](security-considerations--international-features.md).

Tenere anche presente gli articoli più estesi che si trovano nella sezione [go Global Developer Center](https://msdn.microsoft.com/globalization/mt613165) nella sezione [Step-by-step della globalizzazione](https://msdn.microsoft.com/globalization/mt642951) . Durante lo sviluppo di software internazionale, sarà possibile consultare le panoramiche aggiuntive e gli articoli dettagliati disponibili.

## <a name="learning-paths"></a>Percorsi di apprendimento

Il percorso da seguire per la creazione di software internazionale dipende dagli scenari che si affrontano. Gli scenari seguenti sono basati su quelli introdotti nella sezione principale argomento, [internazionalizzazione per le applicazioni Windows](international-support.md).

-   **Creare applicazioni che possono essere distribuite in più aree in più lingue.**

    Il problema è quello di sviluppare un'applicazione che non deve essere riscritta per ogni lingua o cultura.

    -   Vedere l'articolo [informazioni sull'interfaccia utente multilingue (MUI)](./about-multilingual-user-interface.md).
    -   Esplorare la documentazione per l' [interfaccia utente multilingue](multilingual-user-interface.md).
    -   Iniziare a usare l'applicazione [Hello MUI](#the-hello-mui-application) .

-   **Supportare l'input e la visualizzazione di lingue, set di caratteri e tipi di carattere diversi.**

    È possibile che l'applicazione debba supportare più set di caratteri, supportare alfabeti non latini, ad esempio quelli usati per rappresentare lingue ebraiche, arabe, tailandesi e indiane, consentire all'utente di effettuare una selezione da caratteri internazionali o consentire all'utente di immettere caratteri e simboli, ad esempio il Kanji giapponese, per altre lingue usando una tastiera standard.

    -   Leggere gli articoli:

        -   [Supporto di script e tipi di carattere in Windows](https://msdn.microsoft.com/globalization/mt791278)
        -   [Lingua di input: tastiere e IME](https://msdn.microsoft.com/globalization/mt662332)

    -   Esplora la documentazione per:

        -   [Unicode e set di caratteri](unicode-and-character-sets.md)
        -   [Caratteri internazionali e visualizzazione del testo](international-fonts-and-text-display.md)
        -   [Gestione metodo di input](input-method-manager.md)

-   **Visualizza gli oggetti dipendenti dalle impostazioni cultura nei formati appropriati.**

    Le applicazioni internazionali devono utilizzare le impostazioni locali per ordinare correttamente le stringhe e visualizzare informazioni dipendenti dalle impostazioni cultura, ad esempio ora, date e valuta.

    -   Esplora il [Knowledge Center per il supporto nazionale](./national-language-support-reference.md).
    -   Esaminare la documentazione relativa a [NLS (National Language Support)](national-language-support.md).

-   **Individuare il linguaggio o lo script utilizzato dall'utente e applicarlo agli altri servizi dell'applicazione.**

    Se l'applicazione è in grado di determinare la lingua in cui viene scritto il testo e l'input dell'utente, può visualizzare contenuto come le richieste o la Guida in una lingua comprensibile.

    -   Leggi l'articolo [scrittura di applicazioni internazionali in Windows: Servizi linguistici estesi di Windows](./using-extended-linguistic-services.md).
    -   Esplora la documentazione per [servizi linguistici estesi (ELS)](extended-linguistic-services.md).

## <a name="internationalization-technologies-in-the-sdk"></a>Tecnologie di internazionalizzazione nell'SDK

La sezione supporto per lo sviluppo internazionale dell'SDK fornisce tecnologie che consentono all'applicazione di enumerare lingue, impostazioni locali e formati specifici delle impostazioni locali. È possibile usarli nelle applicazioni Microsoft Win32 scritte in C o C++.

I [servizi linguistici estesi](extended-linguistic-services.md) offrono tecnologia brevettata da Microsoft per l'identificazione di linguaggi e script in formato testo. L'applicazione può determinare i servizi disponibili in base alla categoria, nonché al linguaggio di input e di output, allo script e al tipo di contenuto.

I [tipi di carattere internazionali e la visualizzazione del testo](international-fonts-and-text-display.md) forniscono informazioni sui tipi di carattere internazionali, gli alfabeti e i glifi complessi e il rendering accurato della tipografia sulla piattaforma Windows.

[Input Method Manager (IMM)](input-method-manager.md) è una tecnologia che consente all'applicazione di ricevere input dal software IME (Input Method Editor), che a sua volta consente l'immissione di caratteri e simboli, ad esempio il Kanji giapponese, per altre lingue utilizzando una tastiera standard.

## <a name="the-hello-mui-application"></a>Applicazione Hello MUI

Un'attività comune nello sviluppo internazionale inizia con un'applicazione monolingua che deve essere preparata per l'internazionalizzazione. È necessario aggiungere il supporto per altre lingue, ma in un modo che non richiede la riscrittura del codice per ogni nuova lingua o cultura.

Questa attività consente di presentare un'esercitazione che illustra in modo dettagliato la creazione di un'applicazione Hello MUI, usando il modello di risorse [MUI (Multilingual User Interface)](multilingual-user-interface.md) e il supporto associato disponibile in Windows.

L'esercitazione adotta il concetto di Hello World applicazione familiare, dimostrando l'uso di MUI per creare un'applicazione multilingue di base.

È possibile iniziare l'esercitazione Hello MUI in [aggiunta del supporto dell'interfaccia utente multilingue a un'applicazione](creating-a-multilingual-user-interface-application.md).

 

 
