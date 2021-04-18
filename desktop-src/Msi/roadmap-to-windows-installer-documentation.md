---
description: Questa documentazione è la fonte principale del materiale di riferimento per Windows Installer.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Guida di orientamento alla documentazione di Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 324d626eb5dd201a47c16613c5de598fcd13052d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309454"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Guida di orientamento alla documentazione di Windows Installer

Questa documentazione è la fonte principale del materiale di riferimento per Windows Installer. Fornisce informazioni sui pacchetti di installazione e il servizio del programma di installazione. Fornisce inoltre descrizioni complete del Application Programming Interface (API) e degli elementi del database del programma di installazione. Questa documentazione contiene inoltre una descrizione degli esempi di base dei pacchetti di installazione e aggiornamento in [Windows Installer esempi](windows-installer-examples.md).

La [Guida basata sui ruoli per Windows Installer documentazione](role-based-guide-to-windows-installer-documentation.md) è un'alternativa fornita come guida ai lettori che preferiscono visualizzare collegamenti ad argomenti organizzati in base al ruolo professionale e agli scenari di attività comuni.

Per informazioni sui newsgroup Windows Installer, vedere anche l'argomento relativo ad [altre fonti di informazioni di Windows Installer](other-sources-of-windows-installer-information.md).

Per un elenco di suggerimenti sull'uso del Windows Installer, vedere [Windows Installer procedure](windows-installer-best-practices.md)consigliate.

Nell'elenco seguente viene descritta ogni sezione della documentazione del programma di installazione.

-   [Informazioni su Windows Installer](about-windows-installer.md) offre una panoramica delle funzionalità e dei vantaggi del programma di installazione, ad esempio annuncio, installazione su richiesta, resilienza, personalizzazione e gestione dei componenti. In questa sezione vengono introdotti i concetti relativi ai componenti e alle funzionalità del programma di installazione, essenziali per comprendere il modo in cui il programma di installazione organizza un'installazione. Vengono inoltre illustrati alcuni argomenti generali sull'installazione, ad esempio i criteri di sistema, le regole di controllo delle versioni dei file e l'installazione di rollback.
-   L' [uso di Windows Installer](using-windows-installer.md) illustra una serie di argomenti, ad esempio un metodo standard per organizzare un'applicazione in componenti che il programma di installazione può installare o rimuovere dal computer di un utente. come scaricare un pacchetto di installazione dal World Wide Web; e usando immagini di origine compresse.
-   Le informazioni contenute nelle sezioni [novità delle Windows Installer](what-s-new-in-windows-installer.md) possono essere utilizzate per identificare nuove funzionalità non supportate dalle versioni precedenti di Windows Installer.
-   [Firme digitali e Windows Installer](digital-signatures-and-windows-installer.md) descrive in che modo è possibile usare le firme digitali con pacchetti, trasformazioni, patch, moduli unione e file CAB esterni.
-   Gli [assembly](assemblies.md) spiegano come usare Windows Installer per installare e gestire i Common Language Runtime e gli assembly Win32.
-   L' [interfaccia utente](user-interface.md) fornisce informazioni sulle funzionalità dell'interfaccia utente del programma di installazione. Sebbene il programma di installazione non fornisca un'interfaccia utente, l'autore di un pacchetto può contenere tutti i dati e la logica necessari per eseguire un'interfaccia utente interna o esterna completamente interattiva nel database di installazione. Nella sezione di riferimento vengono descritti gli elementi dell'interfaccia utente che sono specificabili nelle tabelle di database, incluse le finestre di dialogo, i controlli e gli eventi di controllo.
-   [Azioni standard](standard-actions.md) illustra le azioni standard usate dal programma di installazione nelle tabelle di sequenza per eseguire un'installazione. Queste informazioni sono destinate principalmente agli sviluppatori di pacchetti.
-   [Azioni personalizzate](custom-actions.md) descrive come creare funzionalità aggiuntive nel programma di installazione. Le azioni personalizzate consentono a un autore di un pacchetto di installazione di estendere le funzionalità delle azioni standard includendo file eseguibili, librerie a collegamento dinamico e script. Queste informazioni sono destinate agli sviluppatori di pacchetti che devono eseguire funzioni di installazione non trovate altrove nel programma di installazione.
-   [Properties](properties.md) fornisce informazioni sulle proprietà utilizzate dal programma di installazione durante un'installazione. Le sezioni about e using forniscono una panoramica di queste variabili globali e ogni proprietà viene descritta nella sezione di riferimento.
-   Il [flusso di informazioni di riepilogo](summary-information-stream.md) documenta le proprietà delle informazioni di riepilogo utilizzate dal programma di installazione. Queste informazioni sono di particolare interesse per tutti gli sviluppatori.
-   L'applicazione di [patch e gli aggiornamenti](patching-and-upgrades.md) illustra l'uso del programma di installazione per eseguire aggiornamenti di file, QFE, aggiornamenti secondari, aggiornamenti del prodotto e applicazione di patch.
-   [Transformations](transforms.md) spiega come modificare o personalizzare un database di installazione usando una trasformazione del database e come generare, proteggere e applicare le trasformazioni.
-   La [convalida dei pacchetti](package-validation.md) illustra l'uso degli analizzatori di coerenza interni (CIEM) per testare la coerenza interna dei pacchetti di installazione in fase di sviluppo.
-   I [moduli unione](merge-modules.md) presentano uno standard per la progettazione di modelli unione. Questo standard deve essere seguito dagli sviluppatori che creano i propri moduli unione e dagli sviluppatori che pianificano di utilizzare il programma di installazione per fornire codice condiviso alle proprie applicazioni.
-   [Windows Installer nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md) viene illustrato come utilizzare Windows Installer per installare e gestire i componenti del programma di installazione progettati per l'esecuzione in sistemi operativi a 64 bit.
-   In [Windows Installer esempi](windows-installer-examples.md) è incluso un esempio dettagliato di creazione di un pacchetto di installazione con un'interfaccia utente interna in [un esempio di installazione](an-installation-example.md). Per un esempio di creazione di un aggiornamento principale per un pacchetto esistente, vedere [un esempio di aggiornamento](an-upgrade-example.md). Per informazioni sul modo in cui una trasformazione di personalizzazione Disabilita le funzionalità e aggiunge nuove risorse, vedere [un esempio di trasformazione della personalizzazione](a-customization-transform-example.md). Per un esempio di creazione di un pacchetto di patch che applica un piccolo aggiornamento a un pacchetto di installazione esistente, vedere [un piccolo esempio di patch](a-small-update-patching-example.md)per l'aggiornamento. Per informazioni su come localizzare un pacchetto di installazione esistente, vedere [un esempio di localizzazione](a-localization-example.md).
-   L' [interfaccia di automazione](automation-interface.md) fornisce informazioni agli sviluppatori che desiderano utilizzare l'interfaccia di automazione di Windows Installer.
-   [Funzioni del programma di installazione](installer-functions.md) descrive le chiamate di funzione all'API del programma di installazione. Queste sono le funzioni chiamate da altre applicazioni per accedere ai servizi del programma di installazione per installare, gestire o rimuovere le applicazioni. Le sezioni using includono discussioni su come richiedere funzionalità, avviare installazioni e reinstallare i componenti mancanti a livello di codice. La sezione di riferimento è il materiale di riferimento principale per le funzioni del servizio di installazione.
-   Il [database del programma](installer-database.md) di installazione illustra il database di installazione. Il programma di installazione mantiene tutta la logica e i dati necessari per un'installazione in un database relazionale che si trova in un file con estensione msi. La sezione about fornisce una panoramica dei diagrammi schema per i principali gruppi funzionali di tabelle del database. Nella sezione using viene illustrato l'utilizzo del più importante di queste tabelle. Queste sezioni contengono informazioni essenziali per gli sviluppatori che creano pacchetti di installazione o scrivono strumenti per la creazione di pacchetti. La sezione di riferimento contiene il materiale di riferimento completo per ogni tabella di database. Questa sezione contiene anche il riferimento principale per ogni funzione di database. Le funzioni di database vengono utilizzate internamente dal programma di installazione di per accedere al database e sono principalmente di interesse per gli sviluppatori di strumenti di creazione dei pacchetti del programma di installazione.

 

 



