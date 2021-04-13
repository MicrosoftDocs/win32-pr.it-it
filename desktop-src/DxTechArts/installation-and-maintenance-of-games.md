---
title: Installazione e manutenzione dei giochi
description: Questo articolo descrive un set di procedure consigliate che consentono di ridurre la frustrazione degli utenti sul tempo necessario per installare un gioco, impedire chiamate di supporto non necessarie e consentire agli utenti di iniziare a giocare il gioco nel modo più rapido e indolore possibile.
ms.assetid: c953165d-2318-ca06-a895-abedcbcb594c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de171fd76654eb3b6edb8818ec073c4ef5ba8ca4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339127"
---
# <a name="installation-and-maintenance-of-games"></a>Installazione e manutenzione dei giochi

Questo articolo descrive un set di procedure consigliate che consentono di ridurre la frustrazione degli utenti sul tempo necessario per installare un gioco, impedire chiamate di supporto non necessarie e consentire agli utenti di iniziare a giocare il gioco nel modo più rapido e indolore possibile.

-   [Installazione iniziale](#initial-installation)
    -   [Semplificazione dell'interfaccia utente di installazione](#streamlining-the-installation-ui)
    -   [Riduzione del tempo necessario per l'installazione](#reducing-the-time-required-for-installation)
    -   [Installazione minima](#minimal-installation)
    -   [Installare su richiesta](#install-on-demand)
-   [Gioco di post-installazione](#post-installation-game-play)
    -   [AutoRun](#autorun)
    -   [Conversione di un'installazione di installazione su richiesta in un'installazione completa](#converting-an-install-on-demand-installation-to-a-full-installation)
    -   [Manutenzione del software e del contenuto del gioco](#maintenance-of-game-software-and-content)
    -   [Verifica automatica degli aggiornamenti](#checking-for-updates-automatically)
    -   [Download automatico delle patch](#downloading-patches-automatically)
-   [Altre risorse](#other-resources)
-   [Argomenti correlati](#related-topics)

## <a name="initial-installation"></a>Installazione iniziale

Gli utenti acquistano giochi in quanto godono di una loro riproduzione, non perché la loro installazione. L'installazione di un gioco deve essere rapida, semplice e indolore possibile per l'utente finale. Idealmente, gli utenti finali non dovrebbero neanche visualizzare un'interfaccia utente di installazione; dovrebbero essere in grado di rilasciare il disco del gioco nel vassoio e iniziare la riproduzione.

### <a name="streamlining-the-installation-ui"></a>Semplificazione dell'interfaccia utente di installazione

Gli aspetti comuni delle interfacce utente di installazione dei giochi esistenti interferiscono con l'esperienza utente finale desiderata:

-   Chiedere all'utente le domande superflue.

    Ad esempio, molti giochi chiedono se l'utente desidera installare DirectX. Se il gioco richiede l'esecuzione di Microsoft DirectX e la versione corretta di DirectX non è già installata, il gioco dovrebbe semplicemente installare DirectX.

-   Chiedere alle domande degli utenti che la maggior parte degli utenti risponderà nello stesso modo.

    Per gli utenti tipici, le impostazioni predefinite per percorso di installazione, percorso del menu Start e così via sono tutte ottimali. Offrire opzioni avanzate per gli utenti che desiderano modificare queste impostazioni.

L'interfaccia utente di installazione deve essere progettata per consentire all'utente comune di iniziare a eseguire il gioco il prima possibile. Se l'esecuzione automatica è abilitata nel computer dell'utente, ovvero l'impostazione predefinita, il programma di installazione presuppone che l'utente voglia giocare il gioco il prima possibile, ignorando eventuali domande superflue. L'installazione di PROGRA[su richiesta](#install-on-demand)m dovrebbe iniziare a installare il gioco nel percorso di installazione predefinito, preferibilmente usando un programma di installazione simile a quello descritto in. È opportuno offrire agli utenti la possibilità di modificare le impostazioni di installazione prima di avviare automaticamente l'installazione. Tuttavia, questa operazione deve essere eseguita richiedendo all'utente di premere un tasto per le opzioni di installazione avanzate e quindi procedendo automaticamente con le opzioni predefinite se l'utente non raggiunge tale chiave entro cinque o dieci secondi.

Se l'esecuzione automatica non è abilitata nel computer dell'utente, il programma di installazione presuppone che l'utente non desideri che il programma di installazione avvii automaticamente l'installazione del gioco. Se il programma di installazione viene avviato con un mezzo diverso dall'AutoRun, deve avviare l'interfaccia utente di installazione avanzata.

### <a name="reducing-the-time-required-for-installation"></a>Riduzione del tempo necessario per l'installazione

Per completare il processo di installazione, la maggior parte dei giochi di Microsoft Windows è attualmente necessaria da cinque minuti a mezz'ora. Al contrario, la maggior parte dei giochi console non ha più di 30 secondi dal momento in cui l'utente inserisce il CD del gioco nel momento in cui l'utente è in grado di riprodurre il gioco. Questa differenza è dovuta al fatto che la maggior parte dei giochi Windows è progettata per eseguire la maggior parte dei contenuti del computer dal disco rigido del computer; le console, che non dispongono di un posto per archiviare in modo permanente grandi quantità di contenuto, richiedono che il contenuto venga eseguito dal supporto di origine. Quando si carica il contenuto dal disco rigido locale, i tempi di caricamento del gioco sono più veloci, il lato negativo è che tutto il contenuto deve essere copiato dal supporto di origine al disco rigido in un determinato momento. La maggior parte dei giochi di Windows sceglie di copiare tutto il contenuto nel disco rigido in una sola volta, come parte di un processo di installazione. Questo tratto dall'esperienza iniziale dell'utente con il gioco fa in modo che l'utente osservi un indicatore di stato per alcuni minuti prima di poter riprodurre il gioco.

Esistono due approcci che è possibile usare per ridurre al minimo il tempo dedicato all'installazione iniziale del gioco: [installazione minima](#minimal-installation) e installazione [su richiesta](#install-on-demand).

### <a name="minimal-installation"></a>Installazione minima

In uno scenario di installazione minima, il gioco installa solo un set minimo di contenuti sul disco rigido. In genere, è costituito solo da file eseguibili del gioco e dll. È possibile accedere al resto del contenuto direttamente dal supporto di origine. Questo riduce drasticamente il tempo necessario per l'installazione, poiché un eseguibile del gioco è raramente più grande di 10-20 MB. Lo svantaggio è che il gioco impiega più tempo per caricare il contenuto durante il gioco, poiché deve caricarlo dal supporto di origine più lento.

Per creare una configurazione di installazione minima in una configurazione basata su Windows Installer:

-   Raggruppare tutti i componenti da installare sul disco rigido in una funzionalità contrassegnata per l'installazione locale.

    Questa funzionalità verrà denominata funzionalità "bootstrap".

-   Raggruppare tutti i componenti che devono essere eseguiti dal supporto di origine in una funzionalità contrassegnata come "Esegui da origine".
-   Quando si apre un file che potrebbe trovarsi sul supporto di origine, usare la funzione [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) per determinare il percorso del file, anziché impostare come hardcoded il percorso.

    In questo modo si garantisce che il file possa essere trovato anche se la lettera di unità dell'unità CD/DVD dell'utente cambia.

-   Comprimere il contenuto che rimane sul CD/DVD.

    La quantità di tempo di CPU impiegato per la decompressione del contenuto viene in genere nascosta dalla velocità di trasferimento lenta dei dati dall'unità CD/DVD.

-   Raggruppare il contenuto in file contigui di grandi dimensioni e accedervi in ordine sequenziale.

    I tempi di ricerca delle unità CD/DVD sono abissati rispetto a quelli dei dischi rigidi e la maggior parte delle unità CD/DVD non raggiunge le velocità di trasferimento massime a meno che non leggano un file esteso e contiguo.

-   Disposizione del contenuto sul CD/DVD nell'ordine in cui è probabile che si acceda.

    I tempi di ricerca vengono notevolmente ridotti quando si accede ai file nello stesso ordine del layout su disco.

### <a name="install-on-demand"></a>Installare su richiesta

In uno scenario di installazione su richiesta, come per l'installazione minima, il gioco viene inizialmente installato nel disco rigido solo per i file necessari per avviare il gioco. Tuttavia, anziché accedere al contenuto rimanente dal supporto di origine ogni volta che è necessario, il gioco installa ogni parte del contenuto sul disco rigido perché è necessario per la prima volta e quindi accede dal disco rigido locale a ogni uso successivo. Il tempo necessario per l'installazione iniziale è ridotto a quello di un'installazione minima, ma, dopo la prima volta che si accede a ogni contenuto, i tempi di caricamento migliorano.

Per creare una configurazione di installazione su richiesta in una configurazione basata su Windows Installer:

-   Raggruppare tutti i componenti da installare inizialmente sul disco rigido in una funzionalità contrassegnata per l'installazione locale.

    Si noti che questo è identico alla funzionalità bootstrap per un'installazione minima.

-   Raggruppare il contenuto rimanente in più funzionalità in base ai componenti che possono essere usati insieme.

    Ad esempio, in un gioco basato sul livello, raggruppare tutto il contenuto usato in un determinato livello in un'unica funzionalità. Si noti che Windows Installer consente la condivisione di un componente da parte di più funzionalità, pertanto se si dispone di contenuto utilizzato su più livelli, è possibile aggiungere tale contenuto alle funzionalità per tutti i livelli necessari senza replicare il contenuto. Tutte queste funzionalità devono essere contrassegnate come "annunciate", il che significa che non verranno installate inizialmente, ma possono essere installate in un secondo momento, se necessario.

-   Quando è necessario un file, verificare prima di tutto se il file è già installato utilizzando la funzione [**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea).

    Se non è ancora installato (ovvero lo stato è INSTALLSTATE \_ annunciato), chiamare la funzione [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) per installare la funzionalità localmente. Quando si apre il file dopo l'installazione, chiamare [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) per determinare il percorso del file. Sebbene non sia strettamente necessario per questo scenario (poiché il contenuto verrà sempre installato sul disco rigido prima di usarlo), questo rende più semplice supportare l'installazione minima oltre all'installazione su richiesta.

-   Se possibile, prevedere il contenuto che probabilmente sarà presto necessario e installarlo in background durante il tempo di inattività.

    L'installazione in background è più appropriata quando il gioco si trova in un punto che non necessita di tutte le ultime once di prestazioni del computer; ad esempio, durante la visualizzazione di un filmato introduttivo, una taglia, un menu e così via.

-   Creare un'opzione nel menu opzioni del gioco per forzare l'installazione di tutti i contenuti rimanenti.

    Per implementare questa funzionalità, creare una funzionalità che è un elemento padre di tutte le funzionalità di installazione su richiesta e quindi chiamare [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) per installare la funzionalità master in locale. In questo modo, anche le sottofunzionalità verranno installate localmente.

-   Il layout del contenuto dovrebbe essere simile a quello per un'installazione minima, ad eccezione del fatto che il contenuto deve essere in cluster solo con altri contenuti che potrebbero essere necessari nello stesso momento (ad esempio, tutto il contenuto di un livello deve essere insieme).

## <a name="post-installation-game-play"></a>Game-Play post-installazione

### <a name="autorun"></a>AutoRun

Per riprodurre un gioco già installato, è necessario che l'utente debba solo eliminare il disco di installazione nella barra delle applicazioni. La prima cosa da fare per eseguire l'eseguibile di AutoRun sul disco consiste nel verificare se il gioco è già stato installato e, in caso affermativo, avviare il gioco. Supponendo che il gioco sia stato installato usando un programma di installazione basato su Windows Installer, il controllo per determinare se il gioco è installato può essere eseguito con una singola chiamata alla funzione [**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea).

### <a name="converting-an-install-on-demand-installation-to-a-full-installation"></a>Conversione di un'installazione di installazione su richiesta in un'installazione completa

Sebbene un'installazione su richiesta consenta all'utente di iniziare a riprodurre il gioco molto prima di un'installazione completa, è possibile che l'utente voglia installare in modo esplicito il resto del contenuto del gioco sul disco rigido locale. È possibile che l'utente voglia essere in grado di riprodurre il gioco senza richiedere il supporto di origine oppure può semplicemente evitare i tempi di caricamento più lunghi del gioco derivanti dall'installazione del contenuto su richiesta. Se l'installazione del gioco usa Windows Installer, il gioco può fornire un'opzione nell'interfaccia utente delle opzioni di gioco per completare l'installazione del contenuto rimanente. Quando l'utente seleziona questa opzione, il gioco può chiamare [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) per forzare l'installazione locale delle funzionalità rimanenti. non è necessario generare un'applicazione di installazione separata a tale scopo.

### <a name="maintenance-of-game-software-and-content"></a>Manutenzione del software e del contenuto del gioco

Uno dei vantaggi offerti da Windows Games rispetto ai giochi console è la facilità relativa con cui l'editore può rilasciare gli aggiornamenti al gioco dopo la versione iniziale. Se questi aggiornamenti introducono nuovi contenuti o si limitano a correggere i bug, è importante rendere il processo di aggiornamento più semplice possibile per l'utente finale. Il processo di aggiornamento è ancora più importante per i giochi online, che in genere richiedono che tutti gli utenti eseguano la versione più recente del gioco per potersi connettere.

### <a name="checking-for-updates-automatically"></a>Verifica automatica degli aggiornamenti

È necessario che gli utenti non debbano ricordare di andare alla ricerca di patch. Se è disponibile un aggiornamento per il gioco, l'utente deve almeno ricevere una notifica e, idealmente, la patch deve essere già scaricata.

Un modo semplice per verificare la disponibilità di aggiornamenti consiste nel connettersi a un server Web ospitato dal server di pubblicazione usando un URL specifico e scaricare un file di testo che specifichi il numero di versione della versione disponibile più recente del gioco, insieme a un URL da cui scaricare un pacchetto che aggiornerà il gioco alla versione più recente.

La verifica della disponibilità di aggiornamenti ogni volta che l'utente riproduce il gioco è sufficiente per assicurarsi che l'utente esegua la versione più recente. Tuttavia, se l'esistenza di un nuovo aggiornamento viene individuata immediatamente prima che l'utente tenti di riprodurre il gioco, l'utente potrebbe essere costretto a ritardare la riproduzione del gioco fino al termine del download dell'aggiornamento. Per gli aggiornamenti di grandi dimensioni o per le connessioni lente, questo ritardo può essere nell'ordine di ore. Per evitare che l'utente debba attendere prima di giocare, il gioco può usare Utilità di pianificazione per pianificare verifiche periodiche dei nuovi aggiornamenti. Se viene rilevato un aggiornamento, il gioco può iniziare immediatamente a scaricare l'aggiornamento, in modo che sia probabilmente completamente scaricato e pronto per l'installazione entro la successiva riproduzione del gioco da parte dell'utente.

### <a name="downloading-patches-automatically"></a>Download automatico delle patch

Quando il gioco ha rilevato che è disponibile un nuovo aggiornamento, dovrebbe iniziare subito a scaricare l'aggiornamento. Poiché l'attività che controlla la presenza di aggiornamenti viene in genere eseguita automaticamente in background, il download deve essere il più possibile non intrusivo. Il Servizio trasferimento intelligente in background (BITS) è una funzionalità del sistema operativo che consente alle applicazioni di scaricare file da Internet anche se l'applicazione stessa non è in esecuzione. I processi di download BITS vengono eseguiti solo quando l'utente è connesso e solo quando il computer è già connesso alla rete. BITS non tenterà di forzare il computer a connettersi alla rete autonomamente. Se l'utente si disconnette dalla rete o si disconnette, il processo BITS viene sospeso e riprenderà il download al successivo accesso dell'utente e si connette alla rete. L'applicazione può configurare i processi BITS in modo da usare solo la larghezza di banda di rete che altrimenti rimarrebbe inutilizzata, per evitare che il processo influisca sulle prestazioni di altre applicazioni che potrebbero usare la rete (ad esempio, un gioco online). BITS è disponibile in Windows XP e Windows 2000 Service Pack 3.

## <a name="other-resources"></a>Risorse aggiuntive

Per ulteriori informazioni sulle tecnologie a cui viene fatto riferimento in questo articolo, vedere le sezioni pertinenti di MSDN Library:

-   [Windows Installer](/windows/desktop/Msi/windows-installer-portal)
-   [Utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page)
-   [Servizio trasferimento intelligente in background](/windows/desktop/Bits/background-intelligent-transfer-service-portal) (BITS)

Per ulteriori informazioni sull'utilizzo di Windows Installer per i giochi, è possibile sintonizzare il prossimo mese per la rubrica DirectX "Introduzione a Windows Installer per sviluppatori di giochi".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea)
</dt> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea)
</dt> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 