---
description: Questo argomento consente di iniziare a creare applicazioni pronte per il mondo, specificando i prerequisiti, riepilogando le tecnologie e introducendo un'esercitazione introduttiva.
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: Attività iniziali con lo sviluppo Windows internazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c346f03717b5f50c27911891daaea8aa4ed55ce199e7ca807690d2f3185d8114
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949430"
---
# <a name="getting-started-with-international-windows-development"></a>Attività iniziali con lo sviluppo Windows internazionale

Questo argomento consente di iniziare a creare applicazioni pronte per il mondo, specificando i prerequisiti, riepilogando le tecnologie e introducendo un'esercitazione introduttiva.

## <a name="getting-started"></a>Introduzione

Se si scrivono applicazioni per gli utenti in un'unica impostazione locale, tali applicazioni possono avere esito positivo anche se si progettano con presupposti specifici delle impostazioni locali, ad esempio la presentazione di date in un formato specifico o l'ordinamento delle stringhe in una sequenza specifica. Ma ora è necessario assicurarsi che le applicazioni possano essere usate in più paesi, da utenti con lingue e impostazioni cultura diverse. Per avere esito positivo in più impostazioni locali, le applicazioni devono adattarsi alle impostazioni locali in cui vengono eseguite. Questa flessibilità è importante se la si aggiunge a un'applicazione esistente o la si progetta in una nuova applicazione.

Questa sezione consente di iniziare a usare lo sviluppo internazionale. Vengono forniti collegamenti ad argomenti che forniscono panoramiche sui prerequisiti per l'internazionalizzazione. Riepiloga le tecnologie offerte dall'SDK per il supporto di clienti in tutto il mondo. Infine, questa sezione fornisce un'applicazione di esempio che risolve un problema che si verifica spesso durante la scrittura di software globale.

## <a name="prerequisites"></a>Prerequisiti

È consigliabile acquisire familiarità con i problemi che si verificano nello sviluppo di software internazionale per Windows. Iniziare con queste panoramiche.

-   [Understanding Internationalization](understanding-internationalization.md) (Informazioni sull'internazionalizzazione) spiega le difficoltà aggiunte nello sviluppo di applicazioni internazionali e definisce i termini chiave.
-   [L'argomento Get World-Ready](https://msdn.microsoft.com/goglobal/bb895995.aspx) contiene linee guida e procedure consigliate che è possibile scorrere o approfondire in base alle esigenze.
-   [L'elenco di controllo](internationalization-checklist.md) per l'internazionalizzazione riepiloga le azioni da eseguire per creare un'applicazione pronta all'mondo.
-   La sicurezza è sempre un problema nello sviluppo di software, ma è necessario prendere in considerazione altri problemi durante lo sviluppo di software internazionale. Vedere Security Considerations: International Features ( Considerazioni sulla [sicurezza: funzionalità internazionali).](security-considerations--international-features.md)

Tenere presenti anche gli articoli più dettagliati disponibili in [Go Global Developer Center](https://msdn.microsoft.com/globalization/mt613165) nella sezione [Step-by-Step della](https://msdn.microsoft.com/globalization/mt642951) globalizzazione. Durante lo sviluppo di software internazionale, è necessario consultare le panoramiche aggiuntive e gli articoli dettagliati disponibili qui.

## <a name="learning-paths"></a>Percorsi di apprendimento

Il percorso seguito per imparare a creare software internazionale dipende dagli scenari che si affrontano. Gli scenari seguenti sono basati su quelli introdotti nell'argomento della sezione [principale, Internationalization for Windows Applications](international-support.md).

-   **Creare applicazioni che possono essere distribuite in più aree in più lingue.**

    La sfida consiste nel sviluppare un'applicazione che non deve essere riscritta per ogni lingua o cultura.

    -   Leggere [l'articolo Informazioni interfaccia utente multilingue (MUI).](./about-multilingual-user-interface.md)
    -   Esplorare la documentazione [per](multilingual-user-interface.md)interfaccia utente multilingue .
    -   Introduzione [all'applicazione Hello MUI.](#the-hello-mui-application)

-   **Supportare l'input e la visualizzazione di lingue, set di caratteri e tipi di carattere diversi.**

    L'applicazione potrebbe dover supportare più set di caratteri, supportare script complessi (ad esempio quelli usati per rappresentare lingue ebraiche, arabe, thai e indic), consentire all'utente di selezionare tra tipi di carattere internazionali o consentire all'utente di immettere caratteri e simboli, ad esempio kanji giapponese, per altre lingue usando una tastiera standard.

    -   Leggere gli articoli:

        -   [Supporto di script e tipi di carattere in Windows](https://msdn.microsoft.com/globalization/mt791278)
        -   [Lingua di input: tastiere e IME](https://msdn.microsoft.com/globalization/mt662332)

    -   Esplorare la documentazione per:

        -   [Unicode e set di caratteri](unicode-and-character-sets.md)
        -   [Tipi di carattere internazionali e visualizzazione del testo](international-fonts-and-text-display.md)
        -   [Gestione metodi di input](input-method-manager.md)

-   **Visualizzare gli oggetti dipendenti dalle impostazioni cultura nei formati appropriati.**

    Le applicazioni internazionali devono usare le impostazioni locali per ordinare correttamente le stringhe e visualizzare informazioni con distinzione delle impostazioni cultura, ad esempio ora, date e valuta.

    -   Esplorare il [National Language Support Knowledge Center.](./national-language-support-reference.md)
    -   Esaminare la documentazione per [national language support (NLS).](national-language-support.md)

-   **Individuare la lingua o lo script usato dall'utente e applicarlo agli altri servizi dell'applicazione.**

    Se l'applicazione è in grado di determinare la lingua in cui viene scritto il testo e l'input dell'utente, può visualizzare contenuto come richieste o guida in una lingua comprensibile.

    -   Leggere [l'articolo Writing World-Ready Applications in Windows: Extended Linguistic Services in Windows](./using-extended-linguistic-services.md).
    -   Esplorare la documentazione di [Extended Linguistic Services (ELS).](extended-linguistic-services.md)

## <a name="internationalization-technologies-in-the-sdk"></a>Tecnologie di internazionalizzazione nell'SDK

La sezione Supporto per lo sviluppo internazionale dell'SDK fornisce tecnologie che consentono all'applicazione di enumerare lingue, impostazioni locali e formati specifici delle impostazioni locali. È possibile usarli nelle applicazioni Microsoft Win32 che si scrivono in C o C++.

I [Servizi linguistici estesi offrono](extended-linguistic-services.md) una tecnologia microsoft-patentata per l'identificazione di lingue e script nel testo. L'applicazione può determinare i servizi disponibili in base alla categoria, nonché alla lingua di input e output, allo script e al tipo di contenuto.

[Caratteri internazionali e visualizzazione testo](international-fonts-and-text-display.md) fornisce informazioni sui tipi di carattere internazionali, su script e glifi complessi e sul rendering fine della tipografia Windows piattaforma.

[Input Method Manager (IMM)](input-method-manager.md) è una tecnologia che consente all'applicazione di ricevere input dal software Input Method Editor (IME), che a sua volta consente l'immissione di caratteri e simboli, ad esempio kanji giapponese, per altre lingue usando una tastiera standard.

## <a name="the-hello-mui-application"></a>Applicazione Hello MUI

Un'attività comune nello sviluppo internazionale inizia con un'applicazione monolingue che è necessario rendere internazionali. È necessario aggiungere il supporto per altre lingue, ma in un modo che non richiede la riscrittura del codice per ogni nuova lingua o lingua.

Questa attività offre la possibilità di presentare un'esercitazione che illustra dettagliatamente la creazione di un'applicazione Hello MUI, usando il modello di risorse [interfaccia utente multilingue (MUI)](multilingual-user-interface.md) e il supporto associato fornito in Windows.

L'esercitazione adotta il concetto di applicazione Hello World, dimostrando l'uso di MUI per creare un'applicazione multilingue di base.

È possibile iniziare l'esercitazione Hello MUI in Adding interfaccia utente multilingue Support to an Application (Aggiunta [del supporto interfaccia utente multilingue a un'applicazione).](creating-a-multilingual-user-interface-application.md)

 

 
