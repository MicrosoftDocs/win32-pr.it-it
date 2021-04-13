---
title: Windows Installer per sviluppatori di giochi
description: Questo articolo fornisce una panoramica di Windows Installer, specificamente destinata agli sviluppatori di giochi. Per la documentazione dettagliata sulle funzionalità e sulle API menzionate in questo articolo, fare riferimento a Windows Platform SDK.
ms.assetid: 07401792-b34b-71c9-18f8-a11c916c7d81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e44227b633f7f9491b8a69bc06aa7945941a154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399277"
---
# <a name="windows-installer-for-game-developers"></a>Windows Installer per sviluppatori di giochi

Mostra in che modo è possibile usare Windows Installer per installare giochi nei computer degli utenti finali. Windows Installer offre supporto completo per un'interfaccia utente personalizzata, nonché per l'applicazione di patch.

Microsoft Windows Installer è l'API preferita per l'installazione di software in computer basati su Windows. Sebbene molte delle funzionalità di Windows Installer siano progettate per supportare la distribuzione di applicazioni aziendali in un ambiente aziendale, Windows Installer è anche completamente adatta per l'installazione di giochi nei computer degli utenti finali. I principali vantaggi dell'uso di Windows Installer per l'installazione del gioco sono:

-   Disinstallazione affidabile
-   Possibilità di installare il contenuto su richiesta
-   Supporto per l'interfaccia utente completamente personalizzata
-   Applicazione di patch efficiente

Questo articolo fornisce una panoramica di Windows Installer, specificamente destinata agli sviluppatori di giochi. Per la documentazione dettagliata sulle funzionalità e sulle API menzionate in questo articolo, fare riferimento a Windows Platform SDK.

-   [Overview](#overview)
-   [Concetti chiave Windows Installer](#key-windows-installer-concepts)
    -   [Componenti](#components)
    -   [Funzionalità](#features)
-   [Stati di installazione](#install-states)
-   [Installare su richiesta](#install-on-demand)
-   [Interfaccia utente personalizzata](#custom-user-interface)
-   [Patch](#patching)
-   [Altre risorse](#other-resources)

## <a name="overview"></a>Panoramica

Tutte le configurazioni basate su Windows Installer utilizzano un file di database di installazione denominato file MSI per descrivere la modalità di installazione dell'applicazione. Il file MSI contiene informazioni sui file, le chiavi del registro di sistema, i collegamenti al desktop, le associazioni di file e altri elementi dell'applicazione da installare. È possibile comprimere i file effettivi da installare all'interno del file con estensione MSI, in bundle e compressi in file CAB distinti oppure archiviati in un'altra posizione nel supporto di installazione come singoli file non compressi. Il file MSI può inoltre fare riferimento a azioni personalizzate implementate esternamente, in modo da consentire azioni per le quali il file MSI non consente in modo nativo.

Un file MSI può facoltativamente contenere un'interfaccia utente per guidare l'utente durante il processo di installazione. Questa interfaccia utente è adeguata per la maggior parte delle applicazioni. Tuttavia, ha l'aspetto di una normale applicazione Windows e molti sviluppatori di giochi preferiscono che l'applicazione di installazione mantenga l'aspetto del gioco, per offrire un'esperienza utente finale più coerente. Per supportare questo scenario di interfaccia utente completamente personalizzato, un'applicazione di installazione può disabilitare l'interfaccia utente incorporata Windows Installer e gestire l'intera interfaccia utente. L'API Windows Installer espone un meccanismo di callback per consentire a un'interfaccia utente di installazione personalizzata di ricevere notifiche sullo stato di avanzamento dell'installazione, nonché eventi importanti come le richieste di modifica del disco.

Windows Installer non è una soluzione end-to-end per la creazione di configurazioni. Si tratta solo di un'API che può essere utilizzata da un programma di installazione per eseguire l'installazione effettiva di file, chiavi del registro di sistema, collegamenti desktop e altri elementi dell'applicazione. Le versioni recenti di tutti gli strumenti principali per la configurazione commerciale, ad esempio InstallShield, WISE e Microsoft Visual Studio, supportano Windows Installer. Questi strumenti offrono pratici interfacce utente per la creazione della configurazione per un gioco, ma si basano sull'API Windows Installer per eseguire gran parte dell'installazione effettiva. Questi strumenti possono essere usati anche solo per compilare un database MSI contenente il pacchetto di installazione, che può quindi essere installato da un'interfaccia utente di installazione personalizzata. In alternativa agli strumenti di terze parti, l'API Windows Installer fornisce tutte le funzioni necessarie per la creazione e la modifica di un database MSI a livello di codice e Windows Platform SDK include uno strumento di modifica del database MSI Bare Bones chiamato Orca.

## <a name="key-windows-installer-concepts"></a>Concetti chiave Windows Installer

Di seguito sono riportati i componenti e le funzionalità Windows Installer.

### <a name="components"></a>Componenti

Un'applicazione è costituita da uno o più componenti, identificati da un ID componente GUID. Un componente è un'unità atomica. è installato completamente o non è installato. Un componente può essere costituito da un singolo file, più file, chiavi del registro di sistema, collegamenti desktop o una combinazione di questi elementi. Le risorse (file e così via) all'interno di un componente devono essere univoche per quel componente. due componenti non possono contenere la stessa risorsa. Un componente non viene mai installato in modo esplicito; viene installato solo come parte di una funzionalità (vedere di seguito).

### <a name="features"></a>Funzionalità

Una funzionalità è un gruppo di componenti, identificato da un ID di funzionalità GUID. Diversamente dai componenti, più funzionalità possono contenere lo stesso componente. Un componente condiviso tra più funzionalità verrà installato se una di queste funzionalità viene installata e rimossa solo quando tutte le funzionalità che fanno riferimento al componente sono state disinstallate. L'installazione di una funzionalità può essere eseguita automaticamente come parte dell'installazione di un prodotto oppure può essere eseguita manualmente tramite l'API [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) .

Sebbene pochi giochi abbiano più "funzionalità" che possono essere installate in modo indipendente, il concetto Windows Installer di una funzionalità è ancora utile. Poiché una funzionalità Windows Installer non è nient'altro che una raccolta di componenti che possono essere installati insieme, i giochi possono usare le funzionalità per raggruppare tutti i contenuti necessari per una fase specifica del gioco. Ad esempio, un gioco orientato ai livelli può definire una funzionalità per ogni livello, costituito da tutto il contenuto necessario per tale livello. Questo consentirebbe al gioco di installare il contenuto un livello alla volta dall'interno del gioco, anziché installare tutto il contenuto per tutti i livelli durante l'installazione iniziale.

## <a name="install-states"></a>Stati di installazione

A ogni componente o funzionalità è associato uno stato di installazione, che determina se il componente o la funzionalità è disponibile e, in tal caso, dove sono installati i file per il componente o la funzionalità. Gli Stati di installazione possibili per una funzionalità sono i seguenti:

<dl> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>Assente
</dt> <dd>

La funzionalità non è installata e pertanto non è accessibile.

</dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>Locale
</dt> <dd>

La funzionalità è disponibile e viene installata per l'esecuzione dal disco rigido locale.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Origine
</dt> <dd>

La funzionalità è disponibile e viene installata per l'esecuzione dal supporto di origine originale, in genere un CD o un DVD.

</dd> <dt>

<span id="Advertised"></span><span id="advertised"></span><span id="ADVERTISED"></span>Annunciati
</dt> <dd>

La funzionalità non è installata, ma può essere installata su richiesta con l'API [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) . Quando la funzionalità è effettivamente installata, può essere installata nello stato locale o di origine.

</dd> </dl>

Un componente può avere uno degli stati precedenti ad eccezione di "annunciato". Se un componente fa parte di una funzionalità annunciata, il componente viene visualizzato come "assente" fino a quando non viene installata la funzionalità.

## <a name="install-on-demand"></a>Installare su richiesta

Windows Installer consente a un'applicazione di contrassegnare le funzionalità come pubblicizzate, vale a dire che la funzionalità non è ancora installata, ma è disponibile per l'installazione in fase di esecuzione, se necessario. L'installazione di funzionalità in fase di esecuzione è nota come "installa su richiesta". I giochi possono usare l'installazione su richiesta per ridurre drasticamente il tempo necessario per la configurazione iniziale del gioco rinviando l'installazione del contenuto del gioco fino a quando non è necessario in fase di esecuzione. Il ritardo necessario per installare il contenuto in fase di esecuzione può spesso essere parzialmente o completamente nascosto eseguendo l'installazione su richiesta in un thread in background, mentre l'utente è altrimenti occupato con il gioco.

## <a name="custom-user-interface"></a>Interfaccia utente personalizzata

Sebbene Windows Installer fornisca un'interfaccia utente predefinita che guida l'utente durante l'installazione dell'applicazione, questa interfaccia è simile a quella di un'applicazione Windows standard. Molti sviluppatori di giochi preferiscono che la loro interfaccia utente di installazione abbia lo stesso aspetto del gioco, per offrire all'utente un'idea dell'ambiente del gioco. Per supportare questa operazione, Windows Installer consente la disabilitazione completa dell'interfaccia utente incorporata, consentendo allo sviluppatore di fornire un'interfaccia utente completamente personalizzata.

Il programma di installazione personalizzato Disabilita prima di tutto l'interfaccia utente predefinita di Windows Installer usando l'API [**MsiSetInternalUI**](/windows/desktop/api/msi/nf-msi-msisetinternalui) per impostare il livello di interfaccia utente su INSTALLUILEVEL \_ None. Viene quindi chiamata l'API [**MsiSetExternalUI**](/windows/desktop/api/msi/nf-msi-msisetexternaluia) per specificare una funzione di callback che verrà chiamata durante il processo di installazione per notificare al programma di installazione gli eventi chiave durante l'installazione.

Il processo di installazione effettivo viene quindi avviato chiamando l'API [**MsiInstallProduct**](/windows/desktop/api/msi/nf-msi-msiinstallproducta) . Questa API accetta una stringa di parametro che consente al chiamante di specificare i valori per le proprietà denominate. Queste proprietà possono essere utilizzate all'interno del database di installazione per personalizzare la modalità di installazione dell'applicazione. Queste proprietà possono essere usate per specificare:

-   Directory in cui deve essere installata l'applicazione
-   Quali funzionalità devono essere installate localmente e che devono essere installate per l'esecuzione dal CD/DVD, ad esempio per consentire la scelta tra un'installazione minima e un'installazione completa.
-   Indica se l'applicazione deve essere installata per tutti gli utenti del computer o solo per l'utente corrente

Nel corso dell'installazione, il programma di installazione utilizza i messaggi di notifica inviati alla relativa funzione di callback per determinare quando aggiornare l'interfaccia utente dell'indicatore di stato, quando richiedere all'utente di inserire il CD successivo o quando inviare una notifica all'utente in merito a un errore nel processo di installazione.

## <a name="patching"></a>Applicazione di patch

Windows Installer consente la correzione delle applicazioni installate applicando un file di patch. Un file di patch contiene i nuovi file che verranno aggiunti dalla patch, i file modificati dalla patch e un elenco di modifiche da apportare al database di installazione. Per conservare spazio, anziché archiviare il contenuto completo di un file modificato dalla patch, il file di correzione contiene effettivamente solo le differenze tra la versione originale del file e la nuova versione del file.

Per creare una patch, è necessaria l'immagine di installazione per ogni versione dell'applicazione da cui si vuole eseguire l'aggiornamento della patch, oltre all'immagine di installazione per la nuova versione aggiornata dell'applicazione. Un'immagine di installazione è costituita dal database MSI e da tutti i file di dati effettivi per l'applicazione. Il modo migliore per creare un'immagine di installazione per una nuova versione dell'applicazione consiste nel copiare l'immagine di installazione dalla versione precedente dell'applicazione, quindi apportare le modifiche necessarie per aggiornare la copia alla versione con patch.

Dopo aver creato tutte le immagini di installazione necessarie, è possibile creare le patch usando Msimsp.exe, ovvero uno strumento per la creazione di patch disponibile come parte di Platform SDK. Lo strumento richiederà le posizioni di ogni immagine di installazione e quindi determinerà come rappresentare in modo efficiente le differenze tra le versioni successive. L'output dello strumento è il file patch finale (identificato dall'estensione MSP). Per installare la patch a livello di codice, chiamare l'API [**MsiApplyPatch**](/windows/desktop/api/msi/nf-msi-msiapplypatcha) . L'utente può anche installare manualmente la patch facendo doppio clic sul file MSP in Esplora.

## <a name="other-resources"></a>Risorse aggiuntive

-   Per informazioni dettagliate sull'API Windows Installer, vedere [Windows Installer](/windows/desktop/Msi/windows-installer-portal).
-   Per informazioni sulle procedure consigliate per l'installazione del gioco, vedere [installazione e manutenzione dei giochi](/windows/desktop/DxTechArts/installation-and-maintenance-of-games).

 

 