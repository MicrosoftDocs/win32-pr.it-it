---
title: App di avvio
description: App di avvio
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- app di avvio
- attività in background
- Chiave di esecuzione
- RunOnce
- cartella di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc2dc2a73a08c3aebd265c209b407646e50a6cb1b7cba630884cf719330b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815051"
---
# <a name="startup-apps"></a>App di avvio

## <a name="platform"></a>Piattaforma

**Client** Windows 8     


## <a name="description"></a>Descrizione

Una delle principali possibilità di Windows è la possibilità di accendere vari fattori di forma, dai tradizionali desktop e portatili ai tablet a basso consumo. Per garantire ai clienti reciproci un'esperienza ottimale in qualsiasi fattore di forma scelto con Windows, due metriche di successo chiave da risolvere sono una maggiore durata della batteria e un'eccellente velocità di risposta del PC. Per ottenere questi risultati, sono stati apportati miglioramenti in più aree di Windows tra cui il ciclo di vita del processo, gli stati di sospensione e le app di avvio (app con avvio automatico dopo l'avvio del computer). Questo argomento evidenzia alcuni degli effetti delle app di avvio su un dispositivo Windows e fornisce indicazioni agli sviluppatori (ISV/IHV) e agli OEM per ridefinire i modelli di utilizzo delle app di avvio per migliorare la durata della batteria e la velocità di risposta per i clienti reciproci. Descrive anche le modifiche apportate al Windows che consentono agli utenti di determinare quali app di avvio devono effettivamente essere eseguite.

Windows Le app dello Store sono progettate per rispettare i nuovi standard di consumo e velocità di risposta della batteria e Windows gestisce il ciclo di vita sospendendole e/o terminandole. Tuttavia, le app desktop progettate per le versioni precedenti di Windows non sono state necessariamente progettate per mantenere la durata della batteria o essere sensibili alle attività dell'utente e possono influire sulla velocità di risposta del sistema(ad esempio, quando un'app invia un normale heartbeat di 1 secondo per verificare la disponibilità di aggiornamenti o prealloca la memoria in anticipo nel caso in cui ne abbia bisogno in un secondo). Ciò può creare un'esperienza non ottimale per l'utente che acquista un tablet PC Windows con una lunga aspettativa di durata della batteria e settimane di standby, ma rileva che la durata della batteria del tablet non raggiunge questi obiettivi. Inoltre, poiché le app di avvio vengono eseguite in background, il numero di app in esecuzione nel sistema può essere notevolmente superiore a quello di cui l'utente è a conoscenza e influire sulla velocità di risposta del sistema. Le app di avvio sono classificate in modo da includere quelle che si sfruttando questi meccanismi per iniziare:

-   Eseguire le chiavi del Registro di sistema (inclusi i nodi HKLM, HKCU, wow64)
-   Chiavi del Registro di sistema RunOnce
-   Cartelle di avvio nel menu Start per ogni utente e percorsi pubblici

È stata aggiunta una nuova funzionalità Windows per garantire che gli utenti finali controllino sempre le app in esecuzione nei propri sistemi. La scheda Avvio in Gestione attività un elenco di app di avvio, insieme ai controlli che consentono agli utenti di disabilitare le app di avvio. Per aiutare gli utenti a determinare cosa disabilitare, Gestione attività visualizza una misura dell'impatto di ogni app di avvio. L'impatto viene valutato in base all'utilizzo della CPU e del disco di un'app all'avvio. I valori di impatto vengono determinati applicando questi criteri:

-   **Impatto elevato**   App che usano più di 1 secondo di tempo della CPU o più di 3 MB di I/O su disco all'avvio
-   **Impatto medio**   App che usano 300 ms - 1000 ms di tempo di CPU o 300 KB - 3 MB di I/O su disco
-   **Impatto basso**   App che usano meno di 300 ms di tempo della CPU e meno di 300 KB di I/O su disco

Microsoft offre strumenti che consentono agli sviluppatori di app di valutare, analizzare e adottare misure per ridurre l'impatto di avvio e migliorare l'esperienza utente. Assessment and Deployment Kit consente di eseguire una valutazione delle prestazioni di avvio e di misurare l'impatto delle app eseguite all'avvio. I risultati della valutazione contengono informazioni dettagliate sull'analisi e la correzione, se applicabile, per i componenti con il maggiore impatto Windows avvio. Usando il Windows analizzatore prestazioni, gli sviluppatori di app possono eseguire analisi approfondite per individuare la causa radice dell'impatto sulle prestazioni e migliorare le Windows di avvio. Installare il Windows ADK da [qui](/previous-versions/windows/hh825494(v=win.10)).

## <a name="guidance"></a>Indicazioni

Le app di avvio si estendono su più categorie, come descritto nella tabella seguente. Viene eseguito il mapping di un set di raccomandazioni per gli sviluppatori alle categorie di app di avvio per allinearsi alle Windows funzionali descritte in precedenza.



Categorie di app di avvio

Descrizione

Recommendation

**Aggiornamenti**

Monitorare e aggiornare gli utenti per gli aggiornamenti online

**Attività di manutenzione**

> [!Note]  
> Tutti gli aggiornamenti devono essere attività di manutenzione, senza requisiti di interazione con l'interfaccia utente. Le app devono semplicemente aggiornarsi in modo silenzioso ed eseguire il rollback in caso di errore

<br/>

${ROWSPAN2}$**Assistenza hardware**${REMOVE}$  

Punti di accesso alternativi

Fornire l'accesso Windows funzionalità e app accessibili tramite altri punti di accesso Windows

**Rimuovi**

> [!Note]  
> La chiave è ridurre le funzionalità duplicate esistenti in Windows

<br/>

Notificanti

Fornire agli utenti notifiche relative ai propri dispositivi

**Rimuovi**

> [!Note]  
> Windows notifiche agli utenti sui propri dispositivi

<br/>

**Pre-utilità di avvio**

Alcune delle attività preliminari necessarie per le app vengono scaricate in un'app di avvio durante l'accesso dell'utente

**Rimuovi**

> [!Note]  
> Windows 8 è ottimizzato per un'esperienza rapida per l'avvio dell'app.

<br/>

${ROWSPAN4}$**Utilità**${REMOVE}$  

Sincronizzazione PC

Fornire la funzionalità di sincronizzazione tra più sistemi

**Avvio** (potenziali aggiornamenti nella versione beta)

Ripristino & backup

Punto di ingresso per salvare e ripristinare lo stato di file, impostazioni o interi sistemi

**Windows App dello Store per l'interfaccia con gli utenti**

Telemetria

Raccogliere e inviare informazioni sull'esperienza utente e sull'ambiente

**Attività di manutenzione**

Monitoraggio dei PC

Fornire il monitoraggio dello stato del sistema non richiesto e le notifiche che duplicano la funzionalità posta in arrivo esistente

**Rimuovi**

> [!Note]  
> La chiave è ridurre le funzionalità duplicate esistenti in Windows

<br/>

${ROWSPAN2}$**Sicurezza**${REMOVE}$  

Controllo genitori & filtri

Applicare regole e restrizioni stabilite per l'accesso a Internet e l'utilizzo

**Avvio**

Configurazione e gestione

Consentire agli utenti di controllare le opzioni di diagnostica e correzione per il monitoraggio della sicurezza del sistema Notificare agli utenti risultati e azioni di sicurezza

**Windows App dello Store per l'interfaccia con gli utenti**

**Comunicazione & Internet** (IM & VoIP)

Inviare e ricevere messaggi e chiamate

**Windows App dello Store**

**Musica & MP3**

Riprodurre, archiviare e gestire musica

**Windows App dello Store**

**Video & foto**

Rilevare, registrare, eseguire il rendering, archiviare e gestire foto e video

**Windows App dello Store**

**Giochi per PC**

Avviare giochi in vari domini

**Windows App dello Store**

**Upsell & Advertisement**

Attirare l'attenzione su beni e servizi disponibili per l'acquisto

**Rimuovi**



 

> [!Note]  
> Le linee guida per le app per l'accessibilità sono coperte da engagement diretti separati con gli ISV. Per [*informazioni dettagliate, Accessibilità*](../winauto/ease-of-access---assistive-technology-registration.md) programmazione.

 

**App di Windows Store**

Windows Le app dello Store migliorano l'esperienza utente introducendo uno spazio Windows con nuove coordinate: un nuovo modello di app, una nuova interfaccia utente e un Windows Store. Queste opzioni relative al linguaggio e al framework di presentazione sono disponibili per lo sviluppo di Windows Store:

-   HTML/JavaScript/CSS
-   XAML/C #
-   XAML/C++

Le informazioni aggregate per lo sviluppo Windows app dello Store sono disponibili [nel](https://msdn.microsoft.com/windows/apps/)Windows Dev Center .

Esempi:

-   [Sviluppo di giochi Windows Store](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Sviluppo di Windows Store che usano contenuti multimediali](/previous-versions/windows/apps/hh465132(v=win.10))

**Attività di manutenzione automatica**

L'attività in background periodica deve essere progettata Manutenzione automatica attività. Questi vengono pianificati in un tempo di inattività del sistema per aumentare la velocità di risposta e l'efficienza energetica Windows PC. Le attività di manutenzione possono essere create e configurate da un'app desktop in fase di installazione, usando Desktop SDK. Per informazioni dettagliate, Manutenzione automatica'argomento seguente.

## <a name="resources"></a>Risorse

-   [Linee guida sull'accessibilità](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Windows Dev Center](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

