---
title: Latenza di rete e velocità effettiva
description: Latenza di rete e velocità effettiva con RPC (Remote Procedure Call).
ms.assetid: 8285fd73-eb54-4c06-b01a-1bffafb7e675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c51c4db75b904ac5feae8c4a1cc5965fc2b06e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221917"
---
# <a name="network-latency-and-throughput"></a>Latenza di rete e velocità effettiva

Tre problemi principali riguardano l'uso ottimale della rete:

-   Latenza di rete
-   Saturazione della rete
-   Implicazioni di elaborazione dei pacchetti

Questa sezione introduce un'attività di programmazione che richiede l'uso di RPC, quindi progetta due soluzioni: una scritta malamente e una ben scritta. Vengono quindi esaminate entrambe le soluzioni e il relativo impatto sulle prestazioni di rete viene illustrato.

Prima di illustrare le due soluzioni, le sezioni successive discutono e chiariscono i problemi di prestazioni correlati alla rete.

## <a name="network-latency"></a>Latenza di rete

La larghezza di banda di rete e la latenza di rete sono termini distinti. Le reti con larghezza di banda elevata non garantiscono bassa latenza. Ad esempio, un percorso di rete che attraversa un collegamento satellite spesso presenta una latenza elevata, anche se la velocità effettiva è molto elevata. Non è insolito per un round trip di rete attraversare un collegamento satellite per avere cinque o più secondi di latenza. L'implicazione di tale ritardo è il seguente: un'applicazione progettata per inviare una richiesta, attendere una risposta, inviare un'altra richiesta, attendere un'altra risposta e così via, attenderà almeno cinque secondi per ogni scambio di pacchetti, indipendentemente dalla velocità con cui si trova il server. Nonostante la maggiore velocità dei computer, le trasmissioni satellite e i supporti di rete sono basati sulla velocità della luce, che in genere rimane costante. Di conseguenza, è improbabile che si verifichino miglioramenti della latenza per le reti satellite esistenti.

## <a name="network-saturation"></a>Saturazione della rete

Una saturazione si verifica in molte reti. Le reti più semplici da saturare sono collegamenti modem lenti, ad esempio modem analoghi 56K standard. Tuttavia, i collegamenti Ethernet con molti computer in un singolo segmento possono anche diventare saturi. Lo stesso vale per le reti WAN con una larghezza di banda ridotta o un collegamento altrimenti sovraccaricato, ad esempio un router o un commutere che può gestire una quantità limitata di traffico. In questi casi, se la rete invia più pacchetti di quelli che possono essere gestiti dal collegamento più debole, i pacchetti vengono eliminati. Per evitare la congestione lo stack TCP di Windows viene ridimensionato quando vengono rilevati pacchetti eliminati che possono causare ritardi significativi.

## <a name="packet-processing-implications"></a>Implicazioni di elaborazione dei pacchetti

Quando si sviluppano programmi per ambienti di livello superiore come RPC, COM e persino Windows Sockets, gli sviluppatori tendono a dimenticare quanto lavoro si svolge in background per ogni pacchetto inviato o ricevuto. Quando arriva un pacchetto dalla rete, un interrupt dalla scheda di rete viene gestito dal computer. Una chiamata di procedura posticipata viene quindi accodata e deve essere configurata attraverso i driver. Se viene utilizzata una forma di sicurezza, è possibile che sia necessario decrittografare il pacchetto oppure che sia stato verificato l'hash crittografico. È necessario eseguire anche un numero di controlli di validità a ogni stato. Solo a questo punto il pacchetto arriva alla destinazione finale: il codice server. L'invio di molti piccoli blocchi di dati comporta un sovraccarico di elaborazione dei pacchetti per ogni piccolo blocco di dati. L'invio di un grande blocco di dati tende a consumare un tempo di CPU significativamente inferiore nel sistema, anche se il costo di esecuzione per molti blocchi piccoli rispetto a un blocco di grandi dimensioni può essere lo stesso per l'applicazione server.

## <a name="example-1-a-poorly-designed-rpc-server"></a>Esempio 1: un server RPC progettato in modo non corretto

Si supponga che un'applicazione debba accedere ai file remoti e che l'attività sia quella di progettare un'interfaccia RPC per la manipolazione del file remoto. La soluzione più semplice consiste nel rispecchiare le routine dei file di studio per i file locali. Questa operazione può comportare un'interfaccia apparentemente pulita e familiare. Ecco un file. idl abbreviato:

``` syntax
typedef [context_handle] void *remote_file;
... .
interface remote_file
{
    remote_file remote_fopen(file_name);
    void remote_fclose(remote_file ...);
    size_t remote_fread(void *, size_t, size_t, remote_file ...);
    size_t remote_fwrite(const void *, size_t, size_t, remote_file ...);
    size_t remote_fseek(remote_file ..., long, int);
}
```

Questa operazione sembra abbastanza elegante, ma in realtà si tratta di una ricetta del tempo rispettata per l'emergenza delle prestazioni. Contrariamente al parere comune, la chiamata di procedura remota non è semplicemente una chiamata di procedura locale con una rete tra il chiamante e il chiamato.

Per vedere in che modo questa ricetta brucia le prestazioni, prendere in considerazione un file 2K, in cui 20 byte vengono letti dall'inizio e poi 20 byte dalla fine e vedere come viene eseguita questa operazione. Sul lato client vengono effettuate le chiamate seguenti (molti percorsi di codice vengono omessi per brevità):

``` syntax
rfp = remote_fopen("c:\\sample.txt");
remote_read(...);
remote_fseek(...);
remote_read(...);
remote_fclose(rfp);
```

Si supponga ora che il server sia separato dal client tramite un collegamento satellite con un tempo di round trip di cinque secondi. Ognuna di queste chiamate deve attendere una risposta prima di procedere, il che significa un valore minimo assoluto per l'esecuzione di questa sequenza di 25 secondi. Considerato che si sta recuperando solo 40 byte, si tratta di un rallentamento delle prestazioni. I clienti di questa applicazione sarebbero furiosi.

Si supponga ora che la rete sia satura, perché la capacità di un router in un percorso di rete è sovraccarica. Questa progettazione impone al router di gestire almeno 10 pacchetti se non si ha la sicurezza (uno per ogni richiesta e uno per ogni risposta). Anche questo non è un aspetto positivo.

Questa progettazione impone inoltre al server di ricevere cinque pacchetti e inviare cinque pacchetti. Anche in questo caso non è un'implementazione molto corretta.

## <a name="example-2-a-better-designed-rpc-server"></a>Esempio 2: un server RPC progettato meglio

Riprogettare l'interfaccia illustrata nell'esempio 1 e verificare se è possibile migliorare. È importante sottolineare che rendere questo server molto valido richiede la conoscenza del modello di utilizzo per i file specificati: tali informazioni non vengono considerate per questo esempio. Pertanto, si tratta di un server RPC progettato meglio, ma non di un server RPC progettato in modo ottimale.

L'idea in questo esempio consiste nel comprimere il numero di operazioni remote in un'unica operazione possibile. Il primo tentativo è il seguente:

``` syntax
typedef [context_handle] void *remote_file;
typedef struct
{
    long position;
    int origin;
} remote_seek_instruction;
... .
interface remote_file
{
    remote_fread(file_name, void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
    size_t remote_fwrite(file_name, const void *, size_t, size_t, [in, out] remote_file ..., BOOL CloseWhenDone, remote_seek_instruction *...);
}
```

Questo esempio Mostra come comprimere tutte le operazioni in lettura e scrittura, che consente l'apertura facoltativa nella stessa operazione, nonché una chiusura e una ricerca facoltative.

Questa stessa sequenza di operazione, se scritta in formato abbreviato, ha un aspetto simile al seguente:

``` syntax
remote_read("c:\\sample.txt", ..., &rfp, FALSE, NULL);
remote_read(NULL, ..., &rfp, TRUE, seek_to_20_bytes_before_end);
```

Quando si considera il server RPC migliore progettato, nella seconda chiamata il server verifica che il *\_ nome del file* sia **null** e usa il file aperto archiviato in RDP. Vengono quindi visualizzate le istruzioni di ricerca e il puntatore del file verrà posizionato 20 byte prima della fine prima della lettura. Al termine, riconoscerà che il flag **CloseWhenDone** è impostato su **true** e chiuderà il file e chiuderà RDP.

Nella rete ad alta latenza, questa versione migliore richiede 10 secondi per il completamento (2,5 volte più velocemente) e richiede l'elaborazione di soli quattro pacchetti; due ricevute dal server e due invii dal server. Le prestazioni *IFS* e unmarshaling aggiuntive eseguite dal server sono irrilevanti rispetto a tutti gli altri elementi.

Se l'ordinamento causale è specificato in modo corretto, l'interfaccia può anche essere eseguita in modo asincrono e le due chiamate possono essere inviate in parallelo. Quando l'ordinamento causale viene usato, le chiamate vengono comunque inviate in ordine, ovvero nella rete a latenza elevata viene sopportato solo un ritardo di cinque secondi, anche se il numero di pacchetti inviati e ricevuti è lo stesso.

È possibile comprimere ulteriormente questo problema creando un metodo che accetta una matrice di strutture, ogni membro della matrice che descrive un'operazione di file particolare. variazione remota di I/O a dispersione/raccolta. L'approccio si paga fino a quando il risultato di ogni operazione non richiede un'ulteriore elaborazione nel client. in altre parole, l'applicazione leggerà i 20 byte alla fine, indipendentemente dai primi 20 byte letti.

Tuttavia, se è necessario eseguire alcune elaborazioni sui primi 20 byte dopo la lettura per determinare l'operazione successiva, il collasso di tutto in un'unica operazione non funziona (almeno non in tutti i casi). L'eleganza di RPC è che un'applicazione può avere entrambi i metodi nell'interfaccia e chiamare uno dei metodi in base alle esigenze.

In generale, quando è presente la rete è preferibile combinare il maggior numero possibile di chiamate a una singola chiamata. Se un'applicazione ha due attività indipendenti, usare le operazioni asincrone e consentirne l'esecuzione in parallelo. In pratica, la pipeline viene mantenuta piena.

 

 




