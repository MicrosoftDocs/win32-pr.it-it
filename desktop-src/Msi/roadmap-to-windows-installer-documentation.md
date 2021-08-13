---
description: Questa documentazione è la fonte principale di materiale di riferimento per Windows programma di installazione.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Roadmap per la documentazione Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad76621cf26e72bf277964609846c32e514b9cb73296bf27593111f84b92d037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625911"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Roadmap per la documentazione Windows Installer

Questa documentazione è la fonte principale di materiale di riferimento per Windows programma di installazione. Fornisce informazioni sui pacchetti di installazione e sul servizio di installazione. Fornisce inoltre descrizioni complete dell'API (Application Programming Interface) e degli elementi del database del programma di installazione. Questa documentazione contiene anche una descrizione di esempi di base di pacchetti di installazione e aggiornamento in [Windows Installer Examples](windows-installer-examples.md).

La Guida basata sui ruoli per Windows [Installer è](role-based-guide-to-windows-installer-documentation.md) un'alternativa fornita come guida ai lettori che preferiscono visualizzare collegamenti ad argomenti organizzati in base a ruoli professionali e scenari di attività comuni.

Per informazioni sui newsgroup Windows Installer, vedere anche l'argomento Altre origini Windows [informazioni sul programma di installazione](other-sources-of-windows-installer-information.md).

Per un elenco di suggerimenti sull'uso del programma di Windows, vedere Windows Procedure consigliate per il [programma di installazione](windows-installer-best-practices.md)di .

L'elenco seguente descrive ogni sezione della documentazione del programma di installazione.

-   [Informazioni Windows Installer](about-windows-installer.md) offre una panoramica delle funzionalità e dei vantaggi del programma di installazione, ad esempio annunci, installazione su richiesta, resilienza, personalizzazione e gestione dei componenti. Questa sezione presenta i concetti relativi ai componenti e alle funzionalità del programma di installazione, essenziali per comprendere come il programma di installazione organizza un'installazione. Vengono inoltre illustrati diversi argomenti generali sull'installazione, ad esempio Criteri di sistema, Regole di controllo delle versioni dei file e Installazione con rollback.
-   [L Windows installer](using-windows-installer.md) illustra diversi argomenti, ad esempio un metodo standard per organizzare un'applicazione in componenti che il programma di installazione può installare o rimuovere dal computer di un utente. come scaricare un pacchetto di installazione dal World Wide Web; e usando immagini di origine compresse.
-   Le informazioni contenute [nelle sezioni Novità di Windows Installer](what-s-new-in-windows-installer.md) possono essere usate per identificare le nuove funzionalità non supportate dalle versioni precedenti Windows Installer.
-   [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) descrive come usare le firme digitali con pacchetti, trasformazioni, patch, moduli unione e file CAB esterni.
-   [Gli assembly](assemblies.md) illustrano come usare il programma Windows per installare e gestire common language runtime e assembly Win32.
-   [Interfaccia utente](user-interface.md) informazioni sulle funzionalità dell'interfaccia utente del programma di installazione. Anche se il programma di installazione non fornisce un'interfaccia utente, l'autore di un pacchetto può mantenere tutti i dati e la logica necessari per eseguire un'interfaccia utente interna o esterna completamente interattiva nel database di installazione. La sezione Riferimento descrive gli elementi dell'interfaccia utente specificabili nelle tabelle di database, tra cui finestre di dialogo, controlli ed eventi di controllo.
-   [Azioni standard](standard-actions.md) illustra le azioni standard usate dal programma di installazione nelle tabelle di sequenza per eseguire un'installazione. Queste informazioni sono destinate principalmente agli sviluppatori di pacchetti.
-   [Azioni personalizzate](custom-actions.md) descrive come creare funzionalità aggiuntive nel programma di installazione. Le azioni personalizzate consentono a un autore di un pacchetto di installazione di estendere le funzionalità delle azioni standard includendo file eseguibili, librerie a collegamento dinamico e script. Queste informazioni sono destinate agli sviluppatori di pacchetti che devono eseguire funzioni di installazione non disponibili altrove nel programma di installazione.
-   [Proprietà](properties.md) fornisce informazioni sulle proprietà utilizzate dal programma di installazione durante un'installazione. Le sezioni About e Using forniscono una panoramica di queste variabili globali e ogni proprietà è descritta nella sezione Riferimento.
-   [Summary Information Stream documenta](summary-information-stream.md) le proprietà delle informazioni di riepilogo usate dal programma di installazione. Queste informazioni sono di interesse per tutti gli sviluppatori.
-   [Patching and Upgrades (Applicazione](patching-and-upgrades.md) di patch e aggiornamenti) illustra l'uso del programma di installazione per eseguire aggiornamenti di file, QFE, aggiornamenti secondari, aggiornamenti del prodotto e applicazione di patch.
-   [Le trasformazioni](transforms.md) illustrano come modificare o personalizzare un database di installazione usando una trasformazione del database e come generare, proteggere e applicare trasformazioni.
-   [La convalida](package-validation.md) dei pacchetti illustra l'uso degli analizzatori di coerenza interna (ICE) per testare la coerenza interna dei pacchetti di installazione in fase di sviluppo.
-   [I moduli](merge-modules.md) unione presentano uno standard per la progettazione di moduli unione. Questo standard deve essere seguito dagli sviluppatori che creano i propri moduli unione, nonché dagli sviluppatori che pianificano di usare il programma di installazione per distribuire il codice condiviso alle proprie applicazioni.
-   Windows installer nei sistemi operativi a [64 bit](windows-installer-on-64-bit-operating-systems.md) illustra come usare il programma di installazione di Windows per installare e gestire i componenti del programma di installazione progettati per l'esecuzione in sistemi operativi a 64 bit.
-   [Windows esempi di programma di](windows-installer-examples.md) installazione include un esempio passo per passo della creazione di un pacchetto di installazione con un'interfaccia utente interna in Un esempio di [installazione](an-installation-example.md). Per un esempio di creazione di un aggiornamento principale per un pacchetto esistente, vedere [An Upgrade Example](an-upgrade-example.md). Per informazioni su come una trasformazione di personalizzazione disabilita le funzionalità e aggiunge nuove risorse, vedere [a Customization Transform Example](a-customization-transform-example.md). Per un esempio di creazione di un pacchetto di patch che applica un piccolo aggiornamento a un pacchetto di installazione esistente, vedere [A Small Update Patching Example](a-small-update-patching-example.md). Per informazioni su come localizzare un pacchetto di installazione esistente, vedere [Un esempio di localizzazione.](a-localization-example.md)
-   [L'interfaccia di](automation-interface.md) automazione fornisce informazioni agli sviluppatori che vogliono usare l'interfaccia di automazione di Windows Programma di installazione.
-   [Funzioni del programma di](installer-functions.md) installazione descrive le chiamate di funzione all'API del programma di installazione. Si tratta delle funzioni chiamate da altre applicazioni per accedere ai servizi del programma di installazione per installare, gestire o rimuovere applicazioni. Le sezioni Using includono discussioni su come richiedere funzionalità, avviare installazioni e reinstallare i componenti mancanti a livello di codice. La sezione Reference è il materiale di riferimento principale per le funzioni del servizio di installazione.
-   [Database del programma di](installer-database.md) installazione illustra il database di installazione. Il programma di installazione mantiene tutta la logica e i dati necessari per un'installazione in un database relazionale che si trova in un file .msi. La sezione Informazioni su offre una panoramica dei diagrammi dello schema per i principali gruppi funzionali di tabelle del database. La sezione Using illustra l'uso delle tabelle più importanti. Queste sezioni contengono informazioni essenziali per gli sviluppatori che stanno scrivendo pacchetti di installazione o strumenti di creazione di pacchetti. La sezione Riferimento contiene materiale di riferimento completo per ogni tabella di database. Questa sezione contiene anche il riferimento principale per ognuna delle funzioni di database. Le funzioni di database vengono usate internamente dal programma di installazione per accedere al database e sono principalmente di interesse per gli sviluppatori di strumenti di creazione di pacchetti del programma di installazione.

 

 



