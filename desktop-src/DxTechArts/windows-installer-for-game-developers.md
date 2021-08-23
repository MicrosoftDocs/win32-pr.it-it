---
title: Windows Programma di installazione per sviluppatori di giochi
description: Questo articolo offre una panoramica del programma di Windows, destinato in modo specifico agli sviluppatori di giochi. Per la documentazione dettagliata sulle funzionalità e sulle API citate in questo articolo, fare riferimento a Windows Platform SDK.
ms.assetid: 07401792-b34b-71c9-18f8-a11c916c7d81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc587725ce2a2a675c9db835fabb503bc44ffa62c07ee1ce80578aef9432cf9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290391"
---
# <a name="windows-installer-for-game-developers"></a>Windows Programma di installazione per sviluppatori di giochi

Illustra come Windows Installer può essere usato per installare giochi nei computer degli utenti finali. Windows Il programma di installazione offre supporto completo per un'interfaccia utente personalizzata e per l'applicazione di patch.

Microsoft Windows Installer è l'API preferita per l'installazione di software Windows computer basati su computer. Anche se molte delle funzionalità del programma di installazione di Windows sono progettate per supportare la distribuzione di applicazioni aziendali in un ambiente aziendale, il programma di installazione di Windows è completamente adatto anche per l'installazione di giochi nei computer degli utenti finali. I vantaggi principali dell'uso di Windows programma di installazione per l'installazione del gioco sono:

-   Disinstallazione affidabile
-   Possibilità di installare contenuto su richiesta
-   Supporto per l'interfaccia utente completamente personalizzata
-   Applicazione efficiente delle patch

Questo articolo offre una panoramica del programma di Windows, destinato in modo specifico agli sviluppatori di giochi. Per la documentazione dettagliata sulle funzionalità e sulle API citate in questo articolo, fare riferimento a Windows Platform SDK.

-   [Overview](#overview)
-   [Concetti chiave Windows programma di installazione](#key-windows-installer-concepts)
    -   [Componenti](#components)
    -   [Funzionalità](#features)
-   [Stati di installazione](#install-states)
-   [Installare su richiesta](#install-on-demand)
-   [Interfaccia utente personalizzata](#custom-user-interface)
-   [Applicazione di patch](#patching)
-   [Altre risorse](#other-resources)

## <a name="overview"></a>Panoramica

Tutte Windows di installazione basate sul programma di installazione usano un file di database di installazione denominato file MSI per descrivere la modalità di installazione dell'applicazione. Il file MSI contiene informazioni su quali file, chiavi del Registro di sistema, collegamenti al desktop, associazioni di file e altri elementi dell'applicazione devono essere installati. I file effettivi da installare possono essere compressi all'interno del file MSI stesso, aggregati e compressi in "file CAB" separati o archiviati altrove nel supporto di installazione come singoli file non compressi. Il file MSI può anche fare riferimento ad azioni personalizzate implementate esternamente, per consentire azioni per cui il file MSI non consente in modo nativo.

Un file MSI può facoltativamente contenere un'interfaccia utente per guidare l'utente nel processo di installazione. Questa interfaccia utente è adeguata per la maggior parte delle applicazioni. Tuttavia, ha l'aspetto di una normale applicazione Windows e molti sviluppatori di giochi preferiscono che l'applicazione di configurazione mantenga l'aspetto del gioco stesso, per offrire un'esperienza utente finale più coerente. Per supportare questo scenario di interfaccia utente completamente personalizzato, un'applicazione di installazione può disattivare l'interfaccia utente predefinita del programma di installazione di Windows e gestire l'intera interfaccia utente. L'API Windows Installer di Windows espone un meccanismo di callback per consentire a un'interfaccia utente di installazione personalizzata di ricevere una notifica dello stato di avanzamento dell'installazione, nonché eventi importanti, ad esempio le richieste di modifica del disco.

Windows Il programma di installazione non è una soluzione end-to-end per la creazione di configurazioni. È solo un'API che può essere usata da un programma di installazione per eseguire l'installazione effettiva di file, chiavi del Registro di sistema, collegamenti al desktop e altri elementi dell'applicazione. Le versioni recenti di tutti i principali strumenti di installazione commerciale (ad esempio InstallShield, WISE e Microsoft Visual Studio) supportano Windows programma di installazione. Questi strumenti offrono interfacce utente utili per la creazione della configurazione per un gioco, ma si basano sull'API del programma di installazione di Windows per eseguire gran parte dell'installazione effettiva. Questi strumenti possono anche essere usati solo per compilare un database MSI contenente il pacchetto di installazione, che può quindi essere installato da un'interfaccia utente di installazione personalizzata. In alternativa agli strumenti di terze parti, l'API del programma di installazione di Windows fornisce tutte le funzioni necessarie per la creazione e la modifica di un database MSI a livello di codice e Windows Platform SDK include uno strumento di modifica del database MSI di base denominato Orca.

## <a name="key-windows-installer-concepts"></a>Concetti chiave Windows programma di installazione

Ecco i componenti Windows e le funzionalità del programma di installazione.

### <a name="components"></a>Componenti

Un'applicazione è costituito da uno o più componenti, identificati da un ID componente GUID. Un componente è un'unità atomica. è completamente installato o non è installato affatto. Un componente può essere costituito da un singolo file, più file, chiavi del Registro di sistema, collegamenti al desktop o una combinazione di questi. Le risorse (file e così via) all'interno di un componente devono essere univoche per tale componente. Due componenti non possono contenere la stessa risorsa. Un componente non viene mai installato in modo esplicito. viene installato solo come parte di una funzionalità (vedere di seguito).

### <a name="features"></a>Funzionalità

Una funzionalità è un gruppo di componenti, identificato da un ID di funzionalità GUID. A differenza dei componenti, più funzionalità possono contenere lo stesso componente. Un componente condiviso tra più funzionalità verrà installato se una di queste funzionalità è installata e rimossa solo quando tutte le funzionalità che fanno riferimento al componente sono state disinstallate. L'installazione di una funzionalità può essere eseguita automaticamente durante l'installazione di un prodotto oppure manualmente tramite l'API [**MsiConfigureFeature.**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea)

Anche se alcuni giochi hanno più "funzionalità" che possono essere installate in modo indipendente, il concetto Windows installer di una funzionalità è comunque utile. Poiché una funzionalità del programma di installazione di Windows non è altro che una raccolta di componenti che possono essere installati insieme, i giochi possono usare le funzionalità per raggruppare tutto il contenuto necessario per una determinata fase del gioco. Ad esempio, un gioco orientato ai livelli può definire una funzionalità per ogni livello, costituita da tutto il contenuto necessario per tale livello. In questo modo il gioco può installare il contenuto un livello alla volta dall'interno del gioco stesso, anziché installare tutto il contenuto per tutti i livelli durante l'installazione iniziale.

## <a name="install-states"></a>Stati di installazione

A ogni componente o funzionalità è associato uno stato di installazione, che determina se il componente o la funzionalità è disponibile e, in tal caso, dove sono installati i file per il componente o la funzionalità. I possibili stati di installazione per una funzionalità sono:

<dl> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>Assente
</dt> <dd>

La funzionalità non è installata e pertanto non è accessibile.

</dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>Locale
</dt> <dd>

La funzionalità è disponibile e viene installata per l'esecuzione dal disco rigido locale.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>fonte
</dt> <dd>

La funzionalità è disponibile e viene installata per l'esecuzione dal supporto di origine (in genere un CD o DVD).

</dd> <dt>

<span id="Advertised"></span><span id="advertised"></span><span id="ADVERTISED"></span>Pubblicizzato
</dt> <dd>

La funzionalità non è installata, ma può essere installata su richiesta usando l'API [**MsiConfigureFeature.**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) Quando la funzionalità viene effettivamente installata, può essere installata nello stato Locale o Origine.

</dd> </dl>

Un componente può avere uno qualsiasi degli stati precedenti, ad eccezione di "Annunciato". Se un componente fa parte di una funzionalità annunciata, verrà visualizzato come "Absent" fino a quando la funzionalità non viene installata.

## <a name="install-on-demand"></a>Installare su richiesta

Windows Il programma di installazione consente a un'applicazione di contrassegnare le funzionalità come annunciate, vale a dire che la funzionalità non è ancora installata, ma è disponibile per l'installazione in fase di esecuzione, se necessario. L'installazione delle funzionalità in fase di esecuzione è nota come "installazione su richiesta". I giochi possono usare Installa su richiesta per ridurre drasticamente il tempo necessario per la configurazione iniziale del gioco rinviando l'installazione del contenuto del gioco fino a quando non è necessario in fase di esecuzione. Il ritardo necessario per installare il contenuto in fase di esecuzione può spesso essere parzialmente o completamente nascosto eseguendo l'installazione su richiesta in un thread in background, mentre l'utente è altrimenti occupato con il gioco.

## <a name="custom-user-interface"></a>Interfaccia utente personalizzata

Anche Windows Installer fornisce un'interfaccia utente predefinita che guida l'utente nell'installazione dell'applicazione, questa interfaccia è simile a quella di un'applicazione Windows standard. Molti sviluppatori di giochi preferiscono che l'interfaccia utente di installazione abbia lo stesso aspetto del gioco stesso, per offrire all'utente un assaggio dell'ambiente del gioco. A tale scopo, Windows installer consente di disabilitarne completamente l'interfaccia utente predefinita, consentendo allo sviluppatore di fornire un'interfaccia utente completamente personalizzata.

Il programma di installazione personalizzato disabilita Windows'interfaccia utente predefinita del programma di installazione usando l'API [**MsiSetInternalUI**](/windows/desktop/api/msi/nf-msi-msisetinternalui) per impostare il livello dell'interfaccia utente su INSTALLUILEVEL \_ NONE. Chiama quindi l'API [**MsiSetExternalUI**](/windows/desktop/api/msi/nf-msi-msisetexternaluia) per specificare una funzione di callback che verrà chiamata durante il processo di installazione per notificare al programma di installazione gli eventi chiave durante l'installazione.

Il processo di installazione effettivo viene quindi avviato chiamando l'API [**MsiInstallProduct.**](/windows/desktop/api/msi/nf-msi-msiinstallproducta) Questa API accetta una stringa di parametro che consente al chiamante di specificare i valori per le proprietà denominate. Queste proprietà possono essere usate all'interno del database di installazione stesso per personalizzare la modalità di installazione dell'applicazione. Queste proprietà possono essere usate per specificare:

-   Directory in cui deve essere installata l'applicazione
-   Quali funzionalità devono essere installate in locale e quali devono essere installate per l'esecuzione da CD/DVD (ad esempio, per consentire la scelta tra un'installazione minima e un'installazione completa)
-   Indica se l'applicazione deve essere installata per tutti gli utenti del computer o solo per l'utente corrente

Durante l'installazione, il programma di installazione usa i messaggi di notifica inviati alla relativa funzione di callback per determinare quando aggiornare l'interfaccia utente dell'indicatore di stato, quando richiedere all'utente di inserire il CD successivo o quando notificare all'utente un errore nel processo di installazione.

## <a name="patching"></a>Applicazione di patch

Windows Il programma di installazione consente di applicare patch alle applicazioni installate applicando un file di patch. Un file di patch contiene i nuovi file che devono essere aggiunti dalla patch, i file modificati dalla patch e un elenco di modifiche da apportare al database di installazione. Per risparmiare spazio, invece di archiviare il contenuto completo di un file modificato dalla patch, il file di patch contiene effettivamente solo le differenze tra la versione originale del file e la nuova versione del file.

Per creare una patch, è necessaria l'immagine di installazione per ognuna delle versioni dell'applicazione da cui si vuole eseguire l'aggiornamento della patch, nonché l'immagine di installazione per la nuova versione aggiornata dell'applicazione. Un'immagine di installazione è costituita dal database MSI e da tutti i file di dati effettivi per l'applicazione. Il modo migliore per creare un'immagine di installazione per una nuova versione dell'applicazione è copiare l'immagine di installazione dalla versione precedente dell'applicazione e quindi apportare le modifiche necessarie per aggiornare tale copia alla versione con patch.

Dopo aver creato tutte le immagini di installazione necessarie, è possibile creare le patch usando Msimsp.exe, uno strumento di creazione di patch disponibile come parte di Platform SDK. Lo strumento richiederà le posizioni di ognuna delle immagini di installazione e quindi determinerà come rappresentare in modo efficiente le differenze tra le versioni successive. L'output dello strumento è il file di patch finale (identificato dall'estensione MSP). Per installare la patch a livello di codice, chiamare l'API [**MsiApplyPatch.**](/windows/desktop/api/msi/nf-msi-msiapplypatcha) L'utente può anche installare la patch manualmente facendo doppio clic sul file MSP in Esplora risorse.

## <a name="other-resources"></a>Risorse aggiuntive

-   Per informazioni dettagliate sull'API Windows Installer, vedere [Windows Installer](/windows/desktop/Msi/windows-installer-portal).
-   Per informazioni sulle procedure consigliate per l'installazione dei giochi, vedere [Installazione e manutenzione dei giochi.](/windows/desktop/DxTechArts/installation-and-maintenance-of-games)

 

 