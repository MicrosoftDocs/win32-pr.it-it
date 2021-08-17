---
description: Questa documentazione è l'origine principale del materiale di riferimento per Windows Installer.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Guida di orientamento Windows del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad76621cf26e72bf277964609846c32e514b9cb73296bf27593111f84b92d037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625911"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Guida di orientamento Windows del programma di installazione

Questa documentazione è l'origine principale del materiale di riferimento per Windows Installer. Fornisce informazioni sui pacchetti di installazione e sul servizio di installazione. Fornisce inoltre descrizioni complete dell'API (Application Programming Interface) e degli elementi del database del programma di installazione. Questa documentazione contiene anche una descrizione di esempi di base di pacchetti di installazione e aggiornamento in [Windows del programma di installazione](windows-installer-examples.md).

La [Guida basata sui ruoli](role-based-guide-to-windows-installer-documentation.md) per Windows installer è un'alternativa fornita come guida ai lettori che preferiscono visualizzare collegamenti ad argomenti organizzati in base al ruolo professionale e agli scenari di attività comuni.

Per informazioni sui Windows del programma di installazione, vedere anche l'argomento Altre origini Windows [informazioni sul programma di installazione.](other-sources-of-windows-installer-information.md)

Per un elenco di suggerimenti sull'uso del Windows, vedere Windows procedure consigliate per il [programma di installazione.](windows-installer-best-practices.md)

L'elenco seguente descrive ogni sezione della documentazione del programma di installazione.

-   [Informazioni Windows installer](about-windows-installer.md) offre una panoramica delle funzionalità e dei vantaggi del programma di installazione, ad esempio annunci, installazione su richiesta, resilienza, personalizzazione e gestione dei componenti. In questa sezione vengono presentati i concetti relativi ai componenti e alle funzionalità del programma di installazione, essenziali per comprendere come il programma di installazione organizza un'installazione. Vengono inoltre illustrati diversi argomenti generali relativi all'installazione, ad esempio Criteri di sistema, Regole di controllo delle versioni dei file e Rollback dell'installazione.
-   [L Windows Installer](using-windows-installer.md) illustra un'ampia gamma di argomenti, ad esempio un metodo standard per organizzare un'applicazione in componenti che il programma di installazione può installare o rimuovere dal computer di un utente; come scaricare un pacchetto di installazione dal World Wide Web; e usando immagini di origine compresse.
-   Le informazioni nelle sezioni Novità del programma di Windows [Installer](what-s-new-in-windows-installer.md) possono essere usate per identificare le nuove funzionalità non supportate dalle versioni precedenti Windows Installer.
-   [Firme digitali e Windows installer](digital-signatures-and-windows-installer.md) descrive come usare le firme digitali con pacchetti, trasformazioni, patch, moduli unione e file CAB esterni.
-   [Gli assembly](assemblies.md) illustrano come usare il Windows installer per installare e gestire la fase di esecuzione del linguaggio comune e gli assembly Win32.
-   [Interfaccia utente](user-interface.md) informazioni sulle funzionalità dell'interfaccia utente del programma di installazione. Anche se il programma di installazione non fornisce un'interfaccia utente, l'autore di un pacchetto può mantenere tutti i dati e la logica necessari per eseguire un'interfaccia utente interna o esterna completamente interattiva nel database di installazione. La sezione Riferimento descrive gli elementi dell'interfaccia utente specificabili nelle tabelle di database, tra cui finestre di dialogo, controlli ed eventi di controllo.
-   [Azioni standard](standard-actions.md) illustra le azioni standard usate dal programma di installazione nelle tabelle di sequenza per eseguire un'installazione. Queste informazioni sono destinate principalmente agli sviluppatori di pacchetti.
-   [Azioni personalizzate](custom-actions.md) descrive come creare funzionalità aggiuntive nel programma di installazione. Le azioni personalizzate consentono a un autore di un pacchetto di installazione di estendere le funzionalità delle azioni standard includendo eseguibili, librerie a collegamento dinamico e script. Queste informazioni sono destinate agli sviluppatori di pacchetti che devono eseguire funzioni di installazione non trovate altrove nel programma di installazione.
-   [Proprietà](properties.md) fornisce informazioni sulle proprietà utilizzate dal programma di installazione durante un'installazione. Le sezioni About e Using forniscono una panoramica di queste variabili globali e ogni proprietà è descritta nella sezione Riferimento.
-   [Summary Information Stream documenta](summary-information-stream.md) le proprietà delle informazioni di riepilogo usate dal programma di installazione. Queste informazioni sono di interesse per tutti gli sviluppatori.
-   [Patch e aggiornamenti illustra l'uso](patching-and-upgrades.md) del programma di installazione per eseguire aggiornamenti di file, QFE, aggiornamenti secondari, aggiornamenti del prodotto e applicazione di patch.
-   [Le trasformazioni](transforms.md) illustrano come modificare o personalizzare un database di installazione usando una trasformazione del database e come generare, proteggere e applicare trasformazioni.
-   [La convalida](package-validation.md) dei pacchetti illustra l'uso degli analizzatori di coerenza interna per testare la coerenza interna dei pacchetti di installazione in fase di sviluppo.
-   [I moduli unione](merge-modules.md) presentano uno standard per la progettazione dei moduli unione. Questo standard deve essere seguito dagli sviluppatori che creano i propri moduli unione, nonché dagli sviluppatori che pianificano di usare il programma di installazione per distribuire codice condiviso alle applicazioni.
-   Windows Installer nei sistemi operativi a [64 bit](windows-installer-on-64-bit-operating-systems.md) illustra come usare il programma di installazione di Windows per installare e gestire i componenti del programma di installazione progettati per l'esecuzione in sistemi operativi a 64 bit.
-   [Windows esempi di programma di](windows-installer-examples.md) installazione include un esempio di procedura dettagliata per la creazione di un pacchetto di installazione con un'interfaccia utente interna in An Installation [Example](an-installation-example.md). Per un esempio di creazione di un aggiornamento principale per un pacchetto esistente, vedere [Un esempio di aggiornamento](an-upgrade-example.md). Per informazioni su come una trasformazione di personalizzazione disabilita le funzionalità e aggiunge nuove risorse, vedere [Un esempio di trasformazione personalizzazione](a-customization-transform-example.md). Per un esempio di creazione di un pacchetto patch che applica un piccolo aggiornamento a un pacchetto di installazione esistente, vedere [A Small Update Patching Example](a-small-update-patching-example.md). Per informazioni su come localizzare un pacchetto del programma di installazione esistente, vedere [Esempio di localizzazione](a-localization-example.md).
-   [L'interfaccia](automation-interface.md) di automazione fornisce informazioni agli sviluppatori che vogliono usare l'interfaccia di automazione di Windows Installer.
-   [Funzioni del programma di](installer-functions.md) installazione descrive le chiamate di funzione all'API del programma di installazione. Queste sono le funzioni chiamate da altre applicazioni per accedere ai servizi del programma di installazione per installare, gestire o rimuovere applicazioni. Le sezioni Using includono discussioni su come richiedere funzionalità, avviare installazioni e reinstallare i componenti mancanti a livello di codice. La sezione Riferimento è il materiale di riferimento principale per le funzioni del servizio di installazione.
-   [Database del programma di](installer-database.md) installazione illustra il database di installazione. Il programma di installazione mantiene tutta la logica e i dati necessari per un'installazione in un database relazionale che si trova in un file .msi file. La sezione Informazioni su offre una panoramica dei diagrammi dello schema per i principali gruppi funzionali di tabelle del database. La sezione Uso illustra l'uso delle tabelle più importanti. Queste sezioni contengono informazioni essenziali per gli sviluppatori che stanno scrivendo pacchetti di installazione o strumenti di creazione di pacchetti. La sezione Riferimento contiene materiale di riferimento completo per ogni tabella di database. Questa sezione contiene anche il riferimento principale per ognuna delle funzioni di database. Le funzioni di database vengono usate internamente dal programma di installazione per accedere al database e sono principalmente di interesse per gli sviluppatori di strumenti di creazione di pacchetti del programma di installazione.

 

 



