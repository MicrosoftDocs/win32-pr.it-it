---
title: App di avvio
description: App di avvio
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- app di avvio
- attività in background
- Esegui chiave
- RunOnce
- cartella di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734631"
---
# <a name="startup-apps"></a>App di avvio

## <a name="platform"></a>Piattaforma

**Client**   di   Windows 8  


## <a name="description"></a>Descrizione

Una delle principali scommesse con Windows è la possibilità di creare diversi fattori di forma, da desktop e portatili tradizionali a tablet a basso consumo. Per garantire che i nostri clienti reciproci abbiano un'esperienza eccezionale su qualsiasi fattore di forma che scelgono con Windows, due metriche di successo chiave che devono essere risolte sono una maggiore durata della batteria e una velocità di risposta del PC eccellente. Per ottenere questi risultati, sono stati apportati miglioramenti in più aree di Windows, tra cui il ciclo di vita del processo, gli Stati di sospensione e le app di avvio (app con avvio automatico dopo l'avvio del computer). In questo argomento vengono illustrati alcuni degli effetti sulle app di avvio in un dispositivo Windows e vengono fornite indicazioni per sviluppatori (ISV/IHV) e OEM per ripensare ai modelli di utilizzo delle app di avvio per migliorare la durata e la velocità di risposta della batteria per i clienti reciproci. Vengono inoltre descritte le modifiche apportate in Windows che consentono agli utenti di controllare la determinazione delle app di avvio effettivamente da eseguire.

Le app di Windows Store sono progettate per essere conformi ai nuovi standard di consumo e velocità di risposta della batteria e Windows gestisce il proprio ciclo di vita sospendendo e/o terminando tali app. Tuttavia, le applicazioni desktop progettate per le versioni precedenti di Windows non sono necessariamente state progettate per preservare la durata della batteria o essere sensibili alle attività degli utenti e possono influenzare la velocità di risposta del sistema, ad esempio quando un'app invia un normale heartbeat di 1 secondo per verificare la disponibilità di aggiornamenti o pre-alloca la memoria in anticipo, se necessario in un secondo momento. Questo può creare un'esperienza insufficiente per l'utente che acquista un Tablet PC Windows con una lunga permanenza della batteria e settimane di standby, ma rileva che la durata della batteria della tavoletta non raggiunge questi obiettivi. Inoltre, poiché le app di avvio vengono eseguite in background, il numero di app in esecuzione nel sistema può essere significativamente superiore rispetto a quello che l'utente è a conoscenza e influisce sulla velocità di risposta del sistema. Le app di avvio sono classificate in modo da includere quelle che sfruttano questi meccanismi per iniziare:

-   Eseguire le chiavi del registro di sistema (i nodi HKLM, HKCU, WOW64 sono inclusi)
-   Chiavi del registro di sistema RunOnce
-   Cartelle di avvio nel menu Start per ogni utente e località pubbliche

Nuove funzionalità sono state aggiunte a Windows per garantire che gli utenti finali siano sempre in grado di controllare le app eseguite nei sistemi. La scheda Startup in Gestione attività Mostra un elenco di app di avvio, insieme ai controlli che consentono agli utenti di disabilitare le app di avvio. Per consentire agli utenti di determinare gli elementi da disabilitare, gestione attività Visualizza una misura di ogni effetto dell'app di avvio. L'effetto viene valutato in base all'utilizzo della CPU e del disco dell'app all'avvio. I valori di effetto vengono determinati applicando questi criteri:

-   **Effetto elevato**   App che usano più di un secondo di tempo di CPU o più di 3 MB di I/O su disco all'avvio
-   **Effetto medio**   App che usano 300 ms-1000 ms di tempo di CPU o 300 KB-3 MB di I/O su disco
-   **Basso effetto**   App che usano meno di 300 ms di tempo di CPU e inferiori a 300 KB di I/O su disco

Microsoft offre strumenti che consentono agli sviluppatori di app di valutare, analizzare e intraprendere le misure per ridurre l'effetto di avvio e migliorare l'esperienza utente. Il kit Assessment and Deployment fornisce la possibilità di eseguire una valutazione delle prestazioni di avvio e di misurare l'impatto delle app eseguite all'avvio. I risultati della valutazione contengono informazioni dettagliate su analisi e monitoraggio e aggiornamento, ove applicabile, per i componenti che hanno un impatto superiore all'avvio di Windows. Con Windows Performance Analyzer, gli sviluppatori di app possono eseguire analisi approfondite per trovare la causa radice dell'effetto sulle prestazioni e migliorare le prestazioni di avvio di Windows. Installare Windows ADK da [qui](/previous-versions/windows/hh825494(v=win.10)).

## <a name="guidance"></a>Indicazioni

Le app di avvio si estendono su più categorie, come descritto nella tabella seguente. Un set di raccomandazioni per gli sviluppatori viene mappato alle categorie di app di avvio per allinearsi alle modifiche funzionali di Windows descritte in precedenza.



Categorie di app di avvio

Descrizione

Recommendation

**Quelli**

Monitorare e aggiornare gli utenti per gli aggiornamenti online

**Attività di manutenzione**

> [!Note]  
> Tutti gli aggiornamenti devono essere attività di manutenzione, senza alcun requisito di interazione dell'interfaccia utente. Le app dovrebbero semplicemente aggiornarsi tranquillamente ed eseguire il rollback in caso di errore

<br/>

$ {ROWSPAN2} $**assistenza hardware**$ {Remove} $  

Punti di accesso alternativi

Fornire l'accesso alle funzionalità e alle app di Windows accessibili tramite altri punti di accesso in Windows

**Rimuovi**

> [!Note]  
> La chiave consiste nel ridurre le funzionalità duplicate presenti in Windows

<br/>

Notificanti

Fornire agli utenti le notifiche relative ai dispositivi

**Rimuovi**

> [!Note]  
> Windows fornisce notifiche agli utenti sui dispositivi

<br/>

**Pre-avviatori**

Alcune attività preliminari richieste dalle app vengono scaricate in un'app di avvio durante l'accesso dell'utente

**Rimuovi**

> [!Note]  
> Windows 8 è ottimizzato per un'esperienza rapida per i lanci di app.

<br/>

$ {ROWSPAN4} $**Utility**$ {Remove} $  

Sincronizzazione PC

Fornire funzionalità di sincronizzazione tra più sistemi

**Avvio** (potenziali aggiornamenti nella versione beta)

Backup & ripristino

Punto di ingresso per salvare e ripristinare lo stato di file, impostazioni o interi sistemi

**App di Windows Store per l'interazione con gli utenti**

Telemetria

Raccogli e invia informazioni sull'esperienza utente e sull'ambiente

**Attività di manutenzione**

Monitoraggio del PC

Fornire il monitoraggio dello stato del sistema non richiesto e le notifiche che duplicano la funzionalità di posta in arrivo esistente

**Rimuovi**

> [!Note]  
> La chiave consiste nel ridurre le funzionalità duplicate presenti in Windows

<br/>

$ {ROWSPAN2} $**Security**$ {Remove} $  

Filtri & per il controllo parentale

Applicare le regole e le restrizioni stabilite per l'utilizzo e l'accesso a Internet

**Avvio**

Configurazione e gestione

Consenti agli utenti di controllare le opzioni di diagnostica e correzione per il monitoraggio della sicurezza del sistema notificare agli utenti i risultati e le azioni di sicurezza

**App di Windows Store per l'interazione con gli utenti**

**Comunicazione & Internet** (im & VoIP)

Inviare e ricevere messaggi e chiamate

**App di Windows Store**

**Music & MP3**

Riprodurre, archiviare e gestire musica

**App di Windows Store**

**Video & foto**

Rilevare, registrare, eseguire il rendering, archiviare e gestire foto e video

**App di Windows Store**

**Giochi per PC**

Avviare giochi tra diversi domini

**App di Windows Store**

**Annuncio & di vendita**

Attirare l'attenzione sui beni e i servizi disponibili per l'acquisto

**Rimuovi**



 

> [!Note]  
> Le linee guida sulle app di accessibilità sono coperte da Engagement diretti distinti con gli ISV. Per informazioni dettagliate, vedere [*programmazione per semplificare l'accesso*](../winauto/ease-of-access---assistive-technology-registration.md) .

 

**App di Windows Store**

Le app di Windows Store migliorano l'esperienza utente introducendo uno spazio Windows con nuove coordinate: un nuovo modello di app, una nuova interfaccia utente e un Windows Store. Queste opzioni relative al linguaggio e al Framework di presentazione sono disponibili per lo sviluppo di app di Windows Store:

-   HTML/JavaScript/CSS
-   XAML/C #
-   XAML/C++

Le informazioni aggregate per lo sviluppo di app di Windows Store sono disponibili nel [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).

Esempi:

-   [Sviluppo di giochi di Windows Store](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Sviluppo di un'app di Windows Store che usa supporti](/previous-versions/windows/apps/hh465132(v=win.10))

**Attività di manutenzione automatica**

L'attività in background periodica deve essere progettata come attività di manutenzione automatica. Questi sono pianificati al tempo di inattività del sistema per aumentare la velocità di risposta e l'efficienza energetica dei PC Windows. Le attività di manutenzione possono essere create e configurate da un'applicazione desktop al momento dell'installazione usando desktop SDK. Per informazioni dettagliate, vedere l'argomento manutenzione automatica che segue.

## <a name="resources"></a>Risorse

-   [Linee guida sull'accessibilità](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Windows Dev Center](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

