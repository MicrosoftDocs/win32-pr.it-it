---
description: Il sistema operativo Windows fornisce meccanismi per facilitare le comunicazioni e la condivisione dei dati tra le applicazioni. Collettivamente, le attività abilitate da questi meccanismi sono dette comunicazione interprocesso (IPC).
ms.assetid: ad3fb0d9-d0ab-479e-b9a6-22a463b6728c
title: Comunicazione interprocesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca9789da756ae5449e77237c1140386a6f5cfd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882233"
---
# <a name="interprocess-communications"></a>Comunicazione interprocesso

Il sistema operativo Windows fornisce meccanismi per facilitare le comunicazioni e la condivisione dei dati tra le applicazioni. Collettivamente, le attività abilitate da questi meccanismi sono dette *comunicazione interprocesso* (IPC). Alcune forme di IPC facilitano la divisione del lavoro tra diversi processi specializzati. Altre forme di IPC facilitano la divisione del lavoro tra computer in una rete.

In genere, le applicazioni possono usare IPC categorizzate come client o server. Un *client* è un'applicazione o un processo che richiede un servizio da un'altra applicazione o processo. Un *Server* è un'applicazione o un processo che risponde a una richiesta del client. Molte applicazioni fungono sia da client che da server, a seconda della situazione. Ad esempio, un'applicazione di elaborazione di testo può fungere da client nella richiesta di una tabella riepilogativa dei costi di produzione da un'applicazione del foglio di calcolo che funge da server. L'applicazione del foglio di calcolo, a sua volta, può fungere da client per richiedere i livelli di inventario più recenti da un'applicazione di controllo inventario automatico.

Dopo aver deciso che l'applicazione potrebbe trarre vantaggio da IPC, è necessario decidere quale dei metodi IPC disponibili usare. È probabile che un'applicazione utilizzerà diversi meccanismi IPC. Le risposte a queste domande determinano se un'applicazione può trarre vantaggio mediante uno o più meccanismi IPC.

-   L'applicazione deve essere in grado di comunicare con altre applicazioni in esecuzione su altri computer in una rete o è sufficiente che l'applicazione comunichi solo con le applicazioni nel computer locale?
-   L'applicazione deve essere in grado di comunicare con le applicazioni in esecuzione in altri computer che possono essere in esecuzione in sistemi operativi diversi, ad esempio Windows o UNIX a 16 bit?
-   Se l'utente dell'applicazione deve scegliere le altre applicazioni con cui l'applicazione comunica o se è in grado di trovare in modo implicito i partner cooperativi.
-   Se l'applicazione comunica con molte applicazioni diverse in modo generale, ad esempio consentendo operazioni Taglia e incolla con qualsiasi altra applicazione, oppure se i requisiti di comunicazione sono limitati a un set limitato di interazioni con altre applicazioni specifiche,
-   Le prestazioni sono un aspetto critico dell'applicazione? Tutti i meccanismi IPC includono una certa quantità di overhead.
-   L'applicazione deve essere un'applicazione GUI o un'applicazione console? Alcuni meccanismi IPC richiedono un'applicazione GUI.

I meccanismi IPC seguenti sono supportati da Windows:

-   [Appunti](#using-the-clipboard-for-ipc)
-   [COM](#using-com-for-ipc)
-   [Copia dei dati](#using-data-copy-for-ipc)
-   [DDE](#using-dde-for-ipc)
-   [Mapping dei file](#using-a-file-mapping-for-ipc)
-   [Mailslot](#using-a-mailslot-for-ipc)
-   [Pipe](#using-pipes-for-ipc)
-   [RPC](#using-rpc-for-ipc)
-   [Windows Sockets](#using-windows-sockets-for-ipc)

## <a name="using-the-clipboard-for-ipc"></a>Uso degli Appunti per IPC

Gli appunti agiscono come depositari centrali per la condivisione dei dati tra le applicazioni. Quando un utente esegue un'operazione di taglia o copia in un'applicazione, l'applicazione inserisce i dati selezionati negli Appunti in uno o più formati standard o definiti dall'applicazione. Qualsiasi altra applicazione può quindi recuperare i dati dagli Appunti, scegliendo tra i formati disponibili che riconosce. Gli Appunti sono un supporto di scambio a regime di controllo libero, in cui le applicazioni devono accettare solo il formato dei dati. Le applicazioni possono risiedere nello stesso computer o in computer diversi in una rete.

**Punto chiave:** Tutte le applicazioni devono supportare gli Appunti per i formati di dati che conoscono. Ad esempio, un editor di testo o un elaboratore di testo deve essere in grado di produrre e accettare i dati degli Appunti in formato testo puro. Per ulteriori informazioni, vedere gli [Appunti](../dataxchg/clipboard.md).

## <a name="using-com-for-ipc"></a>Uso di COM per IPC

Le applicazioni che usano OLE gestiscono *documenti composti*, ovvero documenti costituiti da dati provenienti da un'ampia gamma di applicazioni diverse. OLE fornisce servizi che semplificano la chiamata delle applicazioni su altre applicazioni per la modifica dei dati. Ad esempio, un elaboratore di testo che utilizza OLE potrebbe incorporare un grafo da un foglio di calcolo. L'utente può avviare il foglio di calcolo automaticamente dall'interno del processore di Word scegliendo il grafico incorporato per la modifica. OLE si occupa dell'avvio del foglio di calcolo e della presentazione del grafico per la modifica. Quando l'utente esce dal foglio di calcolo, il grafico viene aggiornato nel documento di Word Processor originale. Il foglio di calcolo sembra essere un'estensione del elaboratore di testo.

La base di OLE è la Component Object Model (COM). Un componente software che usa COM può comunicare con un'ampia gamma di altri componenti, anche quelli che non sono stati ancora scritti. I componenti interagiscono come oggetti e client. Distributed COM estende il modello di programmazione COM in modo che funzioni in una rete.

**Punto chiave:** OLE supporta documenti composti e consente a un'applicazione di includere dati incorporati o collegati che, quando scelti, avvia automaticamente un'altra applicazione per la modifica dei dati. Ciò consente di estendere l'applicazione da qualsiasi altra applicazione che utilizza OLE. Gli oggetti COM forniscono l'accesso ai dati di un oggetto tramite uno o più set di funzioni correlate, noti come *interfacce*. Per ulteriori informazioni, vedere Object Services COM e ActiveX.

## <a name="using-data-copy-for-ipc"></a>Uso della copia dei dati per IPC

La copia dei dati consente a un'applicazione di inviare informazioni a un'altra applicazione usando il messaggio [**WM \_ COPYDATA**](../dataxchg/wm-copydata.md) . Questo metodo richiede la collaborazione tra l'applicazione mittente e l'applicazione ricevente. L'applicazione ricevente deve conoscere il formato delle informazioni ed essere in grado di identificare il mittente. L'applicazione mittente non può modificare la memoria a cui fanno riferimento i puntatori.

**Punto chiave:** La copia dei dati può essere utilizzata per inviare rapidamente informazioni a un'altra applicazione mediante la messaggistica di Windows. Per ulteriori informazioni, vedere la pagina relativa alla [copia dei dati](../dataxchg/data-copy.md).

## <a name="using-dde-for-ipc"></a>Uso di DDE per IPC

DDE è un protocollo che consente alle applicazioni di scambiare dati in una varietà di formati. Le applicazioni possono utilizzare il DDE per gli scambi di dati monouso o per gli scambi in corso in cui le applicazioni si aggiornano una volta che i nuovi dati diventano disponibili.

I formati di dati utilizzati da DDE sono identici a quelli utilizzati dagli Appunti. Il DDE può essere considerato come un'estensione del meccanismo degli Appunti. Gli Appunti vengono quasi sempre usati per una risposta singola a un comando utente, ad esempio la scelta del comando Incolla da un menu. Il DDE viene in genere avviato da un comando utente, ma spesso continua a funzionare senza ulteriore intervento dell'utente. È anche possibile definire formati di dati DDE personalizzati per IPC per scopi specifici tra le applicazioni con requisiti di comunicazione più strettamente collegati.

Possono verificarsi scambi DDE tra le applicazioni in esecuzione nello stesso computer o in computer diversi in una rete.

**Punto chiave:** Il DDE non è efficiente come le tecnologie più recenti. Tuttavia, è comunque possibile utilizzare DDE se altri meccanismi IPC non sono appropriati o se è necessario interfacciarsi con un'applicazione esistente che supporta solo DDE. Per ulteriori informazioni, vedere [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md) e la [libreria di gestione Dynamic Data Exchange](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="using-a-file-mapping-for-ipc"></a>Uso di un mapping di file per IPC

Il *mapping dei file* consente a un processo di trattare il contenuto di un file come se si trattasse di un blocco di memoria nello spazio degli indirizzi del processo. Il processo può usare semplici operazioni di puntatore per esaminare e modificare il contenuto del file. Quando due o più processi accedono allo stesso mapping di file, ogni processo riceve un puntatore alla memoria nello spazio degli indirizzi che può usare per leggere o modificare il contenuto del file. I processi devono usare un oggetto di sincronizzazione, ad esempio un semaforo, per evitare il danneggiamento dei dati in un ambiente multitasking.

È possibile utilizzare un caso speciale di mapping dei file per fornire la *memoria condivisa denominata* tra i processi. Se si specifica il file di swapping del sistema durante la creazione di un oggetto di mapping di file, l'oggetto di mapping dei file viene considerato come un blocco di memoria condivisa. Altri processi possono accedere allo stesso blocco di memoria aprendo lo stesso oggetto mapping di file.

Il mapping dei file è piuttosto efficiente e fornisce anche attributi di sicurezza supportati dal sistema operativo che consentono di evitare il danneggiamento dei dati non autorizzati. Il mapping dei file può essere usato solo tra processi in un computer locale. non può essere usato in una rete.

**Punto chiave:** Il mapping dei file è un modo efficiente per due o più processi nello stesso computer per condividere i dati, ma è necessario fornire la sincronizzazione tra i processi. Per ulteriori informazioni, vedere [mapping di file](/windows/desktop/Memory/file-mapping) e [sincronizzazione](/windows/desktop/Sync/synchronization).

## <a name="using-a-mailslot-for-ipc"></a>Uso di un inserimento/espulsione per IPC

Mailslot forniscono una comunicazione unidirezionale. Qualsiasi processo che crea un inserimento/espulsione è un *Server inserimento/espulsione*. Altri processi, detti *client inserimento/espulsione*, inviano messaggi al server inserimento/espulsione scrivendo un messaggio nel relativo inserimento/espulsione. I messaggi in arrivo vengono sempre aggiunti a inserimento/espulsione. Il inserimento/espulsione Salva i messaggi fino a quando non vengono letti dal server inserimento/espulsione. Un processo può essere sia un server inserimento/espulsione che un client inserimento/espulsione, quindi è possibile usare più mailslot per la comunicazione bidirezionale.

Un client inserimento/espulsione può inviare un messaggio a un inserimento/espulsione nel computer locale, a un inserimento/espulsione in un altro computer o a tutti mailslot con lo stesso nome in tutti i computer di un dominio di rete specificato. I messaggi trasmessi a tutti i mailslot in un dominio non possono essere più lunghi di 400 byte, mentre i messaggi inviati a un singolo inserimento/espulsione sono limitati solo dalla dimensione massima dei messaggi specificata dal server inserimento/espulsione durante la creazione del inserimento/espulsione.

**Punto chiave:** Mailslot offre un modo semplice per l'invio e la ricezione di messaggi brevi da parte delle applicazioni. Offrono inoltre la possibilità di trasmettere messaggi tra tutti i computer di un dominio di rete. Per ulteriori informazioni, vedere [mailslot](mailslots.md).

## <a name="using-pipes-for-ipc"></a>Uso di pipe per IPC

Esistono due tipi di pipe per la comunicazione bidirezionale: le pipe anonime e le named pipe. Le *pipe anonime* consentono ai processi correlati di trasferire le informazioni tra loro. In genere, viene usata una pipe anonima per il reindirizzamento dell'input o dell'output standard di un processo figlio, in modo che possa scambiare dati con il processo padre. Per scambiare dati in entrambe le direzioni (operazione duplex), è necessario creare due pipe anonime. Il processo padre scrive i dati in una pipe usando il relativo handle di scrittura, mentre il processo figlio legge i dati da tale pipe usando il relativo handle di lettura. Analogamente, il processo figlio scrive i dati nell'altra pipe e il processo padre legge da esso. Non è possibile usare le pipe anonime in una rete né utilizzarle tra processi non correlati.

Le *named pipe* vengono utilizzate per trasferire i dati tra processi che non sono processi correlati e tra processi in computer diversi. Un processo server con named pipe crea in genere un named pipe con un nome noto o un nome che deve essere comunicato ai client. Un processo client named pipe che sa il nome della pipe può aprire l'altra estremità, soggetta a restrizioni di accesso specificate dal processo server named pipe. Dopo che il server e il client sono connessi alla pipe, possono scambiare dati eseguendo operazioni di lettura e scrittura sulla pipe.

**Punto chiave:** Le pipe anonime forniscono un modo efficiente per reindirizzare l'input o l'output standard ai processi figlio nello stesso computer. Le named pipe forniscono una semplice interfaccia di programmazione per il trasferimento di dati tra due processi, che risiedono nello stesso computer o in una rete. Per altre informazioni, vedere [Pipes](pipes.md).

## <a name="using-rpc-for-ipc"></a>Uso di RPC per IPC

RPC consente alle applicazioni di chiamare le funzioni in modalità remota. Pertanto, RPC rende IPC semplice come chiamare una funzione. RPC opera tra i processi in un singolo computer o in computer diversi in una rete.

La RPC fornita da Windows è conforme a Open Software Foundation (OSF) Distributed Computing Environment (DCE). Ciò significa che le applicazioni che usano RPC sono in grado di comunicare con le applicazioni in esecuzione con altri sistemi operativi che supportano DCE. RPC supporta automaticamente la conversione dei dati per tenere conto di diverse architetture hardware e per l'ordine dei byte tra ambienti diversi.

I client e i server RPC sono strettamente associati, ma continuano a garantire prestazioni elevate. Il sistema utilizza RPC per facilitare una relazione client/server tra diverse parti del sistema operativo.

**Punto chiave:** RPC è un'interfaccia a livello di funzione, con supporto per la conversione automatica dei dati e per le comunicazioni con altri sistemi operativi. Con RPC è possibile creare applicazioni distribuite a prestazioni elevate e strettamente associate. Per ulteriori informazioni, vedere [Microsoft RPC Components](/windows/desktop/Rpc/microsoft-rpc-components).

## <a name="using-windows-sockets-for-ipc"></a>Uso di Windows Sockets per IPC

Windows Sockets è un'interfaccia indipendente dal protocollo. Sfrutta le funzionalità di comunicazione dei protocolli sottostanti. In Windows Sockets 2 è possibile usare facoltativamente un handle di socket come handle di file con le funzioni di I/O dei file standard.

I socket Windows sono basati sui socket prima diffusi da Berkeley Software Distribution (BSD). Un'applicazione che utilizza Windows Sockets è in grado di comunicare con altre implementazioni di socket su altri tipi di sistemi. Tuttavia, non tutti i provider di servizi di trasporto supportano tutte le opzioni disponibili.

**Punto chiave:** Windows Sockets è un'interfaccia indipendente dal protocollo in grado di supportare le funzionalità di rete attuali ed emergenti. Per ulteriori informazioni, vedere [Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2).

 

 
