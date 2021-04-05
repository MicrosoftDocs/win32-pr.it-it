---
description: Lo sviluppo di un'infrastruttura di rete di alto livello protetta è una priorità per la maggior parte degli sviluppatori di applicazioni di rete. Tuttavia, la sicurezza del socket viene spesso trascurata anche se è molto importante quando si considera una soluzione completamente sicura.
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: Utilizzo di SO_REUSEADDR e SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa4024f031102cbd634c235bb39f4c7860e6c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756998"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a>Con \_ REUSEADDR e \_ EXCLUSIVEADDRUSE

Lo sviluppo di un'infrastruttura di rete di alto livello protetta è una priorità per la maggior parte degli sviluppatori di applicazioni di rete. Tuttavia, la sicurezza del socket viene spesso trascurata anche se è molto importante quando si considera una soluzione completamente sicura. La sicurezza dei socket, in particolare, gestisce i processi che si associano alla stessa porta precedentemente associata da un altro processo dell'applicazione. In passato era possibile che un'applicazione di rete "Hijack" la porta di un'altra applicazione, causando un attacco di tipo Denial of Service o un furto di dati.

In generale, la sicurezza del socket si applica ai processi sul lato server. In particolare, la sicurezza del socket si applica a qualsiasi applicazione di rete che accetta connessioni e riceve il traffico del datagramma IP. Queste applicazioni in genere si associano a una porta nota e sono destinazioni comuni per il codice di rete dannoso.

È meno probabile che le applicazioni client siano le destinazioni di tali attacchi, non perché sono meno vulnerabili, ma poiché la maggior parte dei client si associa a porte locali "effimere" invece che a porte "Service" statiche. Le applicazioni di rete client devono sempre essere associate a porte temporanee (specificando la porta 0 nella struttura [**sockaddr**](sockaddr-2.md) a cui punta il parametro *Name* quando si chiama la funzione di [**Binding**](/windows/win32/api/winsock/nf-winsock-bind) ) a meno che non esista un motivo architetturale interessante per non farlo. Le porte locali effimere sono costituite da porte di dimensioni maggiori della porta 49151. La maggior parte delle applicazioni server per i servizi dedicati è associata a una porta riservata nota che è minore o uguale alla porta 49151. Per la maggior parte delle applicazioni, pertanto, non esiste in genere un conflitto per le richieste di binding tra applicazioni client e server.

In questa sezione viene descritto il livello di sicurezza predefinito per le varie piattaforme Microsoft Windows e il modo in cui le opzioni socket specifiche **\_ REUSEADDR** e [così \_ EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) influiscono sulla sicurezza delle applicazioni di rete. Una funzionalità aggiuntiva denominata sicurezza avanzata del socket è disponibile in Windows Server 2003 e versioni successive. La disponibilità di queste opzioni di socket e la protezione avanzata dei socket variano in base alle versioni dei sistemi operativi Microsoft, come illustrato nella tabella seguente.

| Piattaforma            | \_REUSEADDR | \_EXCLUSIVEADDRUSE                  | Sicurezza avanzata del socket |
|---------------------|---------------|---------------------------------------|--------------------------|
| Windows 95          | Disponibile     | Non disponibile                         | Non disponibile            |
| Windows 98          | Disponibile     | Non disponibile                         | Non disponibile            |
| Windows me          | Disponibile     | Non disponibile                         | Non disponibile            |
| Windows NT 4.0      | Disponibile     | Disponibile in Service Pack 4 e versioni successive | Non disponibile            |
| Windows 2000        | Disponibile     | Disponibile                             | Non disponibile            |
| Windows XP          | Disponibile     | Disponibile                             | Non disponibile            |
| Windows Server 2003 | Disponibile     | Disponibile                             | Disponibile                |
| Windows Vista       | Disponibile     | Disponibile                             | Disponibile                |
| Windows Server 2008 | Disponibile     | Disponibile                             | Disponibile                |
| Windows 7and più recente  | Disponibile     | Disponibile                             | Disponibile                |

## <a name="using-so_reuseaddr"></a>Uso di \_ REUSEADDR

L' **opzione \_ REUSEADDR** socket consente a un socket di associarsi forzatamente a una porta usata da un altro socket. Il secondo socket chiama [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) con il parametro *optname* impostato su **\_ REUSEADDR** e il parametro *optVal* impostato su un valore booleano **true** prima di chiamare [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) sulla stessa porta del socket originale. Una volta che il secondo socket è stato associato correttamente, il comportamento per tutti i socket associati a tale porta è indeterminato. Se, ad esempio, tutti i socket sulla stessa porta forniscono il servizio TCP, non è possibile garantire che le richieste di connessione TCP in ingresso sulla porta siano gestite dal socket corretto. il comportamento è non deterministico. Un programma dannoso può utilizzare **così \_ REUSEADDR** per associare in modo forzato i socket già in uso per i servizi del protocollo di rete standard per negare l'accesso a tali servizi. Per usare questa opzione non sono necessari privilegi speciali.

Se un'applicazione client è associata a una porta prima che un'applicazione server sia in grado di eseguire il binding alla stessa porta, potrebbero verificarsi dei problemi. Se l'applicazione server si associa forzatamente utilizzando l'opzione **\_ REUSEADDR** socket, alla stessa porta, il comportamento per tutti i socket associati a tale porta è indeterminato.

L'eccezione a questo comportamento non deterministico è socket multicast. Se due socket sono associati alla stessa interfaccia e alla stessa porta e sono membri dello stesso gruppo multicast, i dati verranno recapitati a entrambi i socket, anziché a una scelta arbitraria.

## <a name="using-so_exclusiveaddruse"></a>Uso di \_ EXCLUSIVEADDRUSE

Prima che venisse introdotta l'opzione di socket **\_ EXCLUSIVEADDRUSE** , era possibile che uno sviluppatore di applicazioni di rete potesse impedire a un programma dannoso di associarsi alla porta in cui l'applicazione di rete aveva i propri socket associati. Per risolvere questo problema di sicurezza, Windows Sockets ha introdotto l'opzione **\_ EXCLUSIVEADDRUSE** socket, che è stata resa disponibile in Windows NT 4,0 con Service Pack 4 (SP4) e versioni successive.

L'opzione di socket **\_ EXCLUSIVEADDRUSE** può essere utilizzata solo dai membri del gruppo di sicurezza Administrators in Windows XP e versioni precedenti. I motivi per cui questo requisito è stato modificato in Windows Server 2003 e versioni successive sono descritti più avanti in questo articolo.

L' **opzione so \_ EXCLUSIVEADDRUSE** viene impostata chiamando la funzione [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) con il parametro *optname* impostato su **\_ EXCLUSIVEADDRUSE** e il parametro *optVal* impostato su **true** prima che il socket venga associato. Una volta impostata l'opzione, il comportamento delle chiamate di [**Binding**](/windows/win32/api/winsock/nf-winsock-bind) successive differisce a seconda dell'indirizzo di rete specificato in ogni chiamata di **Binding** .

La tabella seguente descrive il comportamento che si verifica in Windows XP e versioni precedenti quando un secondo socket tenta di eseguire l'associazione a un indirizzo precedentemente associato da un primo socket usando opzioni socket specifiche.

> [!NOTE]  
> Nella tabella seguente, "wildcard" indica l'indirizzo jolly per il protocollo specificato (ad esempio "0.0.0.0" per IPv4 e "::" per IPv6). "Specific" indica che a un indirizzo IP specifico è stata assegnata un'interfaccia. Le celle della tabella indicano se l'associazione ha avuto esito positivo ("operazione riuscita") o se viene restituito un errore ("INUSE" per l'errore [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ; "Accesso" per l'errore [WSAEACCES](windows-sockets-error-codes-2.md) .

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Prima chiamata di <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Binding</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Seconda chiamata di <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Binding</strong></a></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Predefinito</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td bgcolor="#C0C0C0">Specifica</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Predefinito</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Operazione completata</td>
        <td>Operazione completata</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Operazione completata</td>
        <td>Operazione completata</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Operazione completata</td>
        <td>Operazione completata</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Operazione completata</td>
        <td>Operazione completata</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Quando due socket sono associati allo stesso numero di porta ma su interfacce esplicite diverse, non si verifica alcun conflitto. Ad esempio, nel caso in cui un computer disponga di due interfacce IP, 10.0.0.1 e 10.99.99.99, se la prima chiamata a [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) si trova in 10.0.0.1 con la porta impostata su 5150 e **quindi \_ EXCLUSIVEADDRUSE** specificato, una seconda chiamata a **Bind** su 10.99.99.99 con la porta è impostata anche su 5150 e nessuna opzione specificata avrà esito positivo. Tuttavia, se il primo socket è associato all'indirizzo con caratteri jolly e alla porta 5150, eventuali chiamate di binding successive alla porta 5150 con tale set di **\_ EXCLUSIVEADDRUSE** avranno esito negativo con [WSAEADDRINUSE](windows-sockets-error-codes-2.md) o [WSAEACCES](windows-sockets-error-codes-2.md) restituito dall'operazione di **associazione** .

Nel caso in cui la prima chiamata a [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) imposta in **modo che \_ REUSEADDR** o nessuna opzione di socket, la seconda chiamata di **Binding** "dirotta" la porta e l'applicazione non sarà in grado di determinare quale dei due socket ha ricevuto pacchetti specifici inviati alla porta "condivisa".

Un'applicazione tipica che chiama la funzione [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) non alloca il socket associato per l'utilizzo esclusivo, a meno che l'opzione **\_ EXCLUSIVEADDRUSE** socket non venga chiamata sul socket prima della chiamata alla funzione di **Binding** . Se un'applicazione client si associa a una porta temporanea o a una porta specifica prima che un'applicazione server venga associata alla stessa porta, potrebbero verificarsi problemi. L'applicazione server è in grado di eseguire il binding forzato alla stessa porta utilizzando l'opzione **\_ REUSEADDR** socket sul socket prima di chiamare la funzione **Bind** , ma il comportamento per tutti i socket associati a tale porta è quindi indeterminato. Se l'applicazione server tenta di utilizzare l'opzione socket **\_ EXCLUSIVEADDRUSE** per l'utilizzo esclusivo della porta, la richiesta avrà esito negativo.

Viceversa, non è possibile riutilizzare un socket con il set **\_ EXCLUSIVEADDRUSE** , immediatamente dopo la chiusura del socket. Se, ad esempio, un socket di ascolto con **\_ EXCLUSIVEADDRUSE** impostato accetta una connessione e viene successivamente chiuso, un altro socket (anche **con \_ EXCLUSIVEADDRUSE**) non può essere associato alla stessa porta del primo socket fino a quando la connessione originale non diventa inattiva.

Questo problema può diventare complicato perché il protocollo di trasporto sottostante potrebbe non terminare la connessione anche se il socket è stato chiuso. Anche dopo la chiusura del socket da parte dell'applicazione, il sistema deve trasmettere tutti i dati memorizzati nel buffer, inviare un messaggio di disconnessione normale al peer e attendere un messaggio di disconnessione normale corrispondente dal peer. È possibile che il protocollo di trasporto sottostante possa non rilasciare mai la connessione; ad esempio, il peer che partecipa alla connessione originale potrebbe annunciare una finestra di dimensioni pari a zero o un'altra forma di configurazione di "attacco". In tal caso, la connessione client rimane in uno stato attivo nonostante la richiesta di chiusura, poiché i dati non riconosciuti rimangono nel buffer.

Per evitare questa situazione, le applicazioni di rete devono garantire un arresto normale chiamando [**Shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) con il \_ flag di invio SD impostato e quindi attendere il completamento di un ciclo [**ricezione**](/windows/win32/api/winsock/nf-winsock-recv) fino a quando non vengono restituiti zero byte sulla connessione. In questo modo si garantisce che tutti i dati vengano ricevuti dal peer e che confermino con il peer che ha ricevuto tutti i dati trasmessi, oltre a evitare il problema di riutilizzo delle porte menzionato.

\_Per impedire che la porta passi a uno stato di attesa "attivo", è possibile impostare l'opzione per il socket Linger, in modo che possa causare effetti desiderati, ad esempio la reimpostazione delle connessioni. Se, ad esempio, i dati vengono ricevuti dal peer ma non vengono riconosciuti da tale peer e il computer locale chiude il socket con l' \_ impostazione Linger, la connessione tra i due computer viene reimpostata e i dati non riconosciuti vengono rimossi dal peer. La scelta di un intervallo di tempo appropriato è difficile perché un valore di timeout più basso comporta spesso connessioni interrotte improvvisamente, mentre i valori di timeout maggiori lasciano il sistema vulnerabile agli attacchi Denial of Service (stabilendo molte connessioni e bloccando potenzialmente i thread dell'applicazione). La chiusura di un socket con un valore di timeout di attesa diverso da zero può causare il blocco della chiamata [**chiamata closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) .

## <a name="enhanced-socket-security"></a>Sicurezza avanzata del socket

È stata aggiunta la protezione avanzata dei socket con la versione di Windows Server 2003. Nelle versioni precedenti del sistema operativo di Microsoft Server la sicurezza del socket predefinita consentiva facilmente ai processi di eseguire il Hijack delle porte da applicazioni non sospette. Per impostazione predefinita, in Windows Server 2003 i socket non sono in uno stato condivisibile. Se quindi un'applicazione vuole consentire ad altri processi di riutilizzare una porta a cui è già associato un socket, deve abilitarla in modo specifico. In tal caso, il primo socket per chiamare [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) sulla porta deve avere **\_ REUSEADDR** impostato sul socket. L'unica eccezione a questo caso si verifica quando la seconda chiamata di **Binding** viene eseguita dallo stesso account utente che ha eseguito la chiamata originale per l' **associazione**. Questa eccezione esiste esclusivamente per garantire la compatibilità con le versioni precedenti.

La tabella seguente descrive il comportamento che si verifica in Windows Server 2003 e nei sistemi operativi successivi quando un secondo socket tenta di eseguire l'associazione a un indirizzo precedentemente associato da un primo socket usando opzioni socket specifiche.

> [!NOTE]
> Nella tabella seguente, "wildcard" indica l'indirizzo jolly per il protocollo specificato (ad esempio "0.0.0.0" per IPv4 e "::" per IPv6). "Specific" indica che a un indirizzo IP specifico è stata assegnata un'interfaccia. Le celle della tabella indicano se l'associazione ha avuto esito positivo ("operazione riuscita") o se è stato restituito l'errore ("INUSE" per l'errore [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ; "Accesso" per l'errore [WSAEACCES](windows-sockets-error-codes-2.md) .
>
> Si noti inoltre che in questa tabella specifica entrambe le chiamate di [**Binding**](/windows/win32/api/winsock/nf-winsock-bind) vengono eseguite con lo stesso account utente.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Prima chiamata di <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Binding</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Seconda chiamata di <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Binding</strong></a></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Predefinito</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td bgcolor="#C0C0C0">Specifica</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Predefinito</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td>INUSE</td>
        <td>Operazione riuscita</td>
        <td>ACCESS</td>
        <td>Operazione riuscita</td>
        <td>INUSE</td>
        <td>Operazione riuscita</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td>Operazione riuscita</td>
        <td>INUSE</td>
        <td>Operazione riuscita</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td>INUSE</td>
        <td>Operazione completata</td>
        <td>Operazione completata</td>
        <td>Operazione completata</td>
        <td>INUSE</td>
        <td>Operazione riuscita</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td>Operazione riuscita</td>
        <td>INUSE</td>
        <td>Operazione completata</td>
        <td>Operazione completata</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td>Operazione riuscita</td>
        <td>INUSE</td>
        <td>Operazione riuscita</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Alcune voci della tabella sopra la spiegazione Merit.

Se, ad esempio, il primo chiamante **imposta \_ EXCLUSIVEADDRUSE** su un indirizzo specifico e il secondo chiamante tenta di chiamare [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) con un indirizzo jolly sulla stessa porta, la seconda chiamata di **Binding** avrà esito positivo. In questo caso particolare, il secondo chiamante è associato a tutte le interfacce ad eccezione dell'indirizzo specifico a cui è associato il primo chiamante. Si noti che il contrario di questo caso non è vero: se il primo chiamante **imposta \_ EXCLUSIVEADDRUSE** e chiama **Bind** con il flag jolly, il secondo chiamante non è in grado di chiamare **Bind** con la stessa porta.

Il comportamento di associazione del socket cambia quando le chiamate di binding del socket vengono effettuate con account utente diversi. La tabella seguente specifica il comportamento che si verifica in Windows Server 2003 e nei sistemi operativi successivi quando un secondo socket tenta di eseguire l'associazione a un indirizzo precedentemente associato da un primo socket usando opzioni socket specifiche e un account utente diverso.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Prima chiamata di <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Binding</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Seconda chiamata di <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>Binding</strong></a></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Predefinito</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td bgcolor="#C0C0C0">Specifica</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Predefinito</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td>Operazione riuscita</td>
        <td>INUSE</td>
        <td>Operazione riuscita</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>Operazione completata</td>
        <td>Operazione completata</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td>Operazione riuscita</td>
        <td>INUSE</td>
        <td>Operazione completata</td>
        <td>Operazione completata</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Wildcard (Carattere jolly)</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Specifica</td>
        <td>Operazione riuscita</td>
        <td>INUSE</td>
        <td>Operazione riuscita</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Si noti che il comportamento predefinito è diverso quando le chiamate di [**Binding**](/windows/win32/api/winsock/nf-winsock-bind) vengono eseguite con account utente diversi. Se il primo chiamante non imposta alcuna opzione sul socket e si associa all'indirizzo con caratteri jolly, il secondo chiamante non può impostare l'opzione **\_ REUSEADDR** e associare correttamente la stessa porta. Il comportamento predefinito senza set di opzioni restituisce anche un errore.

In Windows Vista e versioni successive è possibile creare un socket a doppio stack che opera su IPv6 e IPv4. Quando un socket dello stack doppio è associato all'indirizzo con caratteri jolly, la porta specificata è riservata sia negli stack di rete IPv4 che IPv6 e i controlli associati a **tale \_ REUSEADDR** , **quindi \_ EXCLUSIVEADDRUSE** (se impostati). Questi controlli devono avere esito positivo in entrambi gli stack di rete. Se, ad esempio, un socket TCP a doppio stack imposta **\_ EXCLUSIVEADDRUSE** e tenta di eseguire l'associazione alla porta 5000, nessun altro socket TCP può essere associato in precedenza alla porta 5000 (carattere jolly o specifico). In questo caso, se un socket TCP IPv4 è stato precedentemente associato all'indirizzo di loopback sulla porta 5000, la chiamata di [**Binding**](/windows/win32/api/winsock/nf-winsock-bind) per il socket dello stack doppio avrebbe esito negativo con [WSAEACCES](windows-sockets-error-codes-2.md).

## <a name="application-strategies"></a>Strategie delle applicazioni

Quando si sviluppa un'applicazione di rete che opera a livello di socket, è importante considerare il tipo di sicurezza del socket necessario. Le applicazioni client, ovvero le applicazioni che si connettono o inviano dati a un servizio, richiedono raramente passaggi aggiuntivi poiché si associano a una porta casuale locale (temporanea). Se il client richiede un binding della porta locale specifico per funzionare correttamente, è necessario prendere in considerazione la sicurezza del socket.

L'opzione **so \_ REUSEADDR** ha pochissimi usi nelle applicazioni normali, a parte i socket multicast in cui i dati vengono recapitati a tutti i socket associati sulla stessa porta. In caso contrario, qualsiasi applicazione che imposta questa opzione socket deve essere riprogettata per rimuovere la dipendenza perché è particolarmente vulnerabile al "hijack del socket". Fino a quando l'opzione socket **\_ REUSEADDR** può essere usata per eseguire potenzialmente il Hijack di una porta in un'applicazione server, l'applicazione deve essere considerata non sicura.

Tutte le applicazioni server devono impostare in **modo che \_ EXCLUSIVEADDRUSE** per un livello elevato di sicurezza del socket. Non solo impedisce al software dannoso di eseguire il Hijack della porta, ma indica anche se un'altra applicazione è associata alla porta richiesta. Ad esempio, una chiamata per [**associare**](/windows/win32/api/winsock/nf-winsock-bind) l'indirizzo con carattere jolly da un processo con il set di opzioni di **\_ EXCLUSIVEADDRUSE** socket non riuscirà se un altro processo è attualmente associato alla stessa porta su un'interfaccia specifica.

Infine, anche se la sicurezza del socket è stata migliorata in Windows Server 2003, un'applicazione deve sempre impostare l'opzione **\_ EXCLUSIVEADDRUSE** socket per assicurarsi che venga associata a tutte le interfacce specifiche richieste dal processo. La protezione dei socket in Windows Server 2003 aggiunge un livello di sicurezza maggiore per le applicazioni legacy, ma gli sviluppatori di applicazioni devono comunque progettare i prodotti con tutti gli aspetti della sicurezza.
