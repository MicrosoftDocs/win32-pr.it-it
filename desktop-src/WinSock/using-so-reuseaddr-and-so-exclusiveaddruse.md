---
description: Lo sviluppo di un'infrastruttura di rete sicura di alto livello è una priorità per la maggior parte degli sviluppatori di applicazioni di rete. Tuttavia, la sicurezza dei socket viene spesso trascurata nonostante sia molto critica quando si considera una soluzione completamente sicura.
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: Uso SO_REUSEADDR e SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d58b0249ab19b4c7a1655a1c65130d545d328ef4fba3fd56ae9b05a911cb3fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121147"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a>Uso di SO \_ REUSEADDR e SO \_ EXCLUSIVEADDRUSE

Lo sviluppo di un'infrastruttura di rete sicura di alto livello è una priorità per la maggior parte degli sviluppatori di applicazioni di rete. Tuttavia, la sicurezza dei socket viene spesso trascurata nonostante sia molto critica quando si considera una soluzione completamente sicura. La sicurezza dei socket, in particolare, riguarda i processi associati alla stessa porta precedentemente associata da un altro processo dell'applicazione. In passato un'applicazione di rete poteva "dirottare" la porta di un'altra applicazione, che poteva facilmente causare un attacco "Denial of Service" o un furto di dati.

In generale, la sicurezza dei socket si applica ai processi sul lato server. In particolare, la sicurezza dei socket si applica a qualsiasi applicazione di rete che accetta connessioni e riceve traffico di datagrammi IP. Queste applicazioni in genere si associano a una porta nota e sono destinazioni comuni per codice di rete dannoso.

È meno probabile che le applicazioni client siano le destinazioni di tali attacchi, non perché sono meno sensibili, ma perché la maggior parte dei client si associa a porte locali "effimeri" anziché a porte di "servizio" statiche. Le applicazioni di rete client devono sempre eseguire il binding a porte effimere (specificando la porta 0 nella struttura [**SOCKADDR**](sockaddr-2.md) a cui punta il parametro *name* quando si chiama la funzione [**bind),**](/windows/win32/api/winsock/nf-winsock-bind) a meno che non vi sia un motivo architetturale interessante per non farlo. Le porte locali effimeri sono costituite da porte maggiori della porta 49151. La maggior parte delle applicazioni server per i servizi dedicati esegue il binding a una porta riservata nota minore o uguale alla porta 49151. Pertanto, per la maggior parte delle applicazioni, in genere non si verifica un conflitto per le richieste di associazione tra applicazioni client e server.

Questa sezione descrive il livello predefinito di sicurezza in varie piattaforme Microsoft Windows e il modo in cui le opzioni di socket **so \_ REUSEADDR** e [SO \_ EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) influiscono sulla sicurezza delle applicazioni di rete. In Windows Server 2003 e versioni successive è disponibile una funzionalità aggiuntiva denominata sicurezza avanzata dei socket. La disponibilità di queste opzioni socket e la sicurezza avanzata dei socket variano a seconda delle versioni dei sistemi operativi Microsoft, come illustrato nella tabella seguente.

| Piattaforma            | QUINDI \_ REUSEADDR | SO \_ EXCLUSIVEADDRUSE                  | Sicurezza avanzata dei socket |
|---------------------|---------------|---------------------------------------|--------------------------|
| Windows 95          | Disponibile     | Non disponibile                         | Non disponibile            |
| Windows 98          | Disponibile     | Non disponibile                         | Non disponibile            |
| Windows Me          | Disponibile     | Non disponibile                         | Non disponibile            |
| Windows NT 4.0      | Disponibile     | Disponibile nel Service Pack 4 e versioni successive | Non disponibile            |
| Windows 2000        | Disponibile     | Disponibile                             | Non disponibile            |
| Windows XP          | Disponibile     | Disponibile                             | Non disponibile            |
| Windows Server 2003 | Disponibile     | Disponibile                             | Disponibile                |
| Windows Vista       | Disponibile     | Disponibile                             | Disponibile                |
| Windows Server 2008 | Disponibile     | Disponibile                             | Disponibile                |
| Windows 7 e versione più recente  | Disponibile     | Disponibile                             | Disponibile                |

## <a name="using-so_reuseaddr"></a>Uso di SO \_ REUSEADDR

**L'opzione SO \_ REUSEADDR** socket consente a un socket di eseguire l'associazione forzata a una porta in uso da un altro socket. Il secondo socket chiama [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) con il parametro *optname* impostato su **SO \_ REUSEADDR** e il parametro *optval* impostato su un valore booleano **TRUE** prima di chiamare [**bind**](/windows/win32/api/winsock/nf-winsock-bind) sulla stessa porta del socket originale. Dopo che il secondo socket è stato associato correttamente, il comportamento per tutti i socket associati a tale porta è indeterminato. Ad esempio, se tutti i socket sulla stessa porta forniscono il servizio TCP, non è possibile garantire che tutte le richieste di connessione TCP in ingresso sulla porta siano gestite dal socket corretto. Il comportamento è non deterministico. Un programma dannoso può usare **SO \_ REUSEADDR** per associare forzatamente i socket già in uso per i servizi del protocollo di rete standard per negare l'accesso a tali servizi. Per usare questa opzione non sono necessari privilegi speciali.

Se un'applicazione client esegue il binding a una porta prima che un'applicazione server sia in grado di eseguire il binding alla stessa porta, potrebbero verificarsi problemi. Se l'applicazione server esegue il binding forzato usando l'opzione socket **SO \_ REUSEADDR** alla stessa porta, il comportamento per tutti i socket associati a tale porta è indeterminato.

L'eccezione a questo comportamento non deterministico è i socket multicast. Se due socket sono associati alla stessa interfaccia e alla stessa porta e sono membri dello stesso gruppo multicast, i dati verranno recapitati a entrambi i socket, anziché a uno scelto arbitrariamente.

## <a name="using-so_exclusiveaddruse"></a>Uso di SO \_ EXCLUSIVEADDRUSE

Prima dell'introduzione dell'opzione socket **SO \_ EXCLUSIVEADDRUSE,** uno sviluppatore di applicazioni di rete poteva fare molto poco per impedire a un programma dannoso di eseguire il binding alla porta a cui l'applicazione di rete aveva i propri socket associati. Per risolvere questo problema di sicurezza, Windows Sockets ha introdotto l'opzione socket **SO \_ EXCLUSIVEADDRUSE,** disponibile in Windows NT 4.0 con Service Pack 4 (SP4) e versioni successive.

L'opzione socket **SO \_ EXCLUSIVEADDRUSE** può essere usata solo dai membri del gruppo di sicurezza Administrators Windows XP e versioni precedenti. I motivi per cui questo requisito è stato modificato Windows Server 2003 e versioni successive sono descritti più avanti nell'articolo.

L'opzione **SO \_ EXCLUSIVEADDRUSE** viene impostata chiamando la funzione [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) con il parametro *optname* impostato su **SO \_ EXCLUSIVEADDRUSE** e il parametro *optval* impostato su un valore booleano **TRUE** prima che il socket venga associato. Dopo aver impostato l'opzione , il comportamento delle chiamate [**di associazione**](/windows/win32/api/winsock/nf-winsock-bind) successive varia a seconda dell'indirizzo di rete specificato in ogni **chiamata di** associazione.

La tabella seguente descrive il comportamento che si verifica in Windows XP e versioni precedenti quando un secondo socket tenta di eseguire l'associazione a un indirizzo associato in precedenza da un primo socket usando opzioni socket specifiche.

> [!NOTE]  
> Nella tabella seguente il carattere jolly indica l'indirizzo con caratteri jolly per il protocollo specificato, ad esempio "0.0.0.0" per IPv4 e "::" per IPv6. "Specifico" indica un indirizzo IP specifico assegnato a un'interfaccia. Le celle della tabella indicano se l'associazione ha esito positivo ("Operazione riuscita") o se viene restituito un errore ("INUSE" per [l'errore WSAEADDRINUSE;](windows-sockets-error-codes-2.md) "ACCESS" per [l'errore WSAEACCES).](windows-sockets-error-codes-2.md)

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Prima <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>chiamata di</strong></a> associazione</td>
        <td bgcolor="#C0C0C0" colspan="6">Seconda <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>chiamata di</strong></a> associazione</td>
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

Quando due socket sono associati allo stesso numero di porta ma in interfacce esplicite diverse, non si verifica alcun conflitto. Ad esempio, nel caso in cui un computer abbia due interfacce IP, 10.0.0.1 e 10.99.99.99, se la prima chiamata a [**bind**](/windows/win32/api/winsock/nf-winsock-bind) è su 10.0.0.1  con la porta impostata su 5150 e **SO \_ EXCLUSIVEADDRUSE** specificata, una seconda chiamata per eseguire il binding su 10.99.99.99.99 con la porta impostata anche su 5150 e nessuna opzione specificata avrà esito positivo. Tuttavia, se il primo socket è associato all'indirizzo con caratteri jolly e alla porta 5150, qualsiasi chiamata di associazione successiva alla porta 5150 con l'impostazione **SO \_ EXCLUSIVEADDRUSE** avrà esito negativo con [WSAEADDRINUSE](windows-sockets-error-codes-2.md) o [WSAEACCES](windows-sockets-error-codes-2.md) restituito dall'operazione **di** associazione.

Nel caso in cui la prima chiamata a [**bind**](/windows/win32/api/winsock/nf-winsock-bind) imposta **SO \_ REUSEADDR** o nessuna opzione socket, la seconda chiamata di binding "hijack" la porta e l'applicazione non sarà in grado di determinare quale dei due socket ha ricevuto pacchetti specifici inviati alla porta "condivisa". 

Un'applicazione tipica [](/windows/win32/api/winsock/nf-winsock-bind) che chiama la funzione di associazione non alloca il socket associato per l'uso esclusivo, a meno che l'opzione del socket **SO \_ EXCLUSIVEADDRUSE** non venga chiamata sul socket prima della chiamata alla **funzione di** associazione. Se un'applicazione client esegue l'associazione a una porta effimera o a una porta specifica prima che un'applicazione server venga associata alla stessa porta, possono verificarsi problemi. L'applicazione server può eseguire l'associazione forzata alla stessa porta usando l'opzione socket **SO \_ REUSEADDR** sul socket prima di chiamare la funzione di associazione, ma il comportamento per tutti i socket associati a tale porta è quindi indeterminato.  Se l'applicazione server tenta di usare l'opzione **socket SO \_ EXCLUSIVEADDRUSE** per l'uso esclusivo della porta, la richiesta avrà esito negativo.

Al contrario, un socket con il set **SO \_ EXCLUSIVEADDRUSE** non può essere necessariamente riutilizzato immediatamente dopo la chiusura del socket. Ad esempio, se un socket in ascolto con il set **SO \_ EXCLUSIVEADDRUSE** accetta una connessione e successivamente viene chiuso, un altro socket (anche con **SO \_ EXCLUSIVEADDRUSE**) non può essere associato alla stessa porta del primo socket fino a quando la connessione originale non diventa inattiva.

Questo problema può diventare complicato perché il protocollo di trasporto sottostante potrebbe non terminare la connessione anche se il socket è stato chiuso. Anche dopo che il socket è stato chiuso dall'applicazione, il sistema deve trasmettere tutti i dati memorizzati nel buffer, inviare un messaggio di disconnessione normalmente al peer e attendere un messaggio di disconnessione normalmente corrispondente dal peer. È possibile che il protocollo di trasporto sottostante non rilasci mai la connessione. Ad esempio, il peer che partecipa alla connessione originale potrebbe annunciare una finestra di dimensioni pari a zero o un'altra forma di configurazione di "attacco". In tal caso, la connessione client rimane in uno stato attivo nonostante la richiesta di chiusura, poiché i dati non confermati rimangono nel buffer.

Per evitare questa situazione, le applicazioni di rete devono garantire un arresto normale chiamando [**shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) con il flag SD SEND impostato e quindi attendere in un ciclo \_ [**recv**](/windows/win32/api/winsock/nf-winsock-recv) fino a quando non vengono restituiti zero byte sulla connessione. Ciò garantisce che tutti i dati vengono ricevuti dal peer e allo stesso modo conferma con il peer che ha ricevuto tutti i dati trasmessi, evitando il problema di riutilizzo delle porte mittente.

L'opzione socket SO LINGER può essere impostata su un socket per impedire la transizione della porta a uno stato di attesa "attivo". Tuttavia, questo comportamento è sconsigliato perché può causare effetti desiderati, ad esempio la reimpostazione delle \_ connessioni. Ad esempio, se i dati vengono ricevuti dal peer ma non vengono ancora ricevuti e il computer locale chiude il socket con SO LINGER impostato, la connessione tra i due computer viene reimpostata e i dati non contrassegnati vengono eliminati dal \_ peer. La scelta di un tempo di attesa appropriato è difficile perché un valore di timeout più piccolo spesso causa l'interruzione improvvisamente delle connessioni, mentre valori di timeout più grandi lasciano il sistema vulnerabile agli attacchi Denial of Service (stabilendo molte connessioni e potenzialmente bloccando/bloccando i thread dell'applicazione). La chiusura di un socket con un valore di timeout residuo diverso da zero può anche causare il blocco della chiamata [**closesocket.**](/windows/win32/api/winsock/nf-winsock-closesocket)

## <a name="enhanced-socket-security"></a>Sicurezza socket avanzata

È stata aggiunta la sicurezza avanzata dei socket con il rilascio Windows Server 2003. Nelle versioni precedenti del sistema operativo server Microsoft, la sicurezza socket predefinita consentiva facilmente ai processi di hijack delle porte da applicazioni ignare. In Windows Server 2003, i socket non sono in uno stato di condivisione per impostazione predefinita. Pertanto, se un'applicazione vuole consentire ad altri processi di riutilizzare una porta a cui è già associato un socket, deve abilitarla in modo specifico. In questo caso, per il primo socket da chiamare [**bind**](/windows/win32/api/winsock/nf-winsock-bind) sulla porta deve essere impostato **SO \_ REUSEADDR** sul socket. L'unica eccezione a questo caso si verifica quando la seconda chiamata **di** associazione viene eseguita dallo stesso account utente che ha effettuato la chiamata originale per **associare**. Questa eccezione esiste esclusivamente per garantire la compatibilità con le versioni precedenti.

La tabella seguente descrive il comportamento che si verifica nei sistemi operativi Windows Server 2003 e versioni successive quando un secondo socket tenta di eseguire l'associazione a un indirizzo associato in precedenza da un primo socket usando opzioni socket specifiche.

> [!NOTE]
> Nella tabella seguente il carattere jolly indica l'indirizzo con caratteri jolly per il protocollo specificato, ad esempio "0.0.0.0" per IPv4 e "::" per IPv6. "Specifico" indica un indirizzo IP specifico assegnato a un'interfaccia. Le celle della tabella indicano se l'associazione ha esito positivo ("Success") o l'errore restituito ("INUSE" per [l'errore WSAEADDRINUSE;](windows-sockets-error-codes-2.md) "ACCESS" per [l'errore WSAEACCES).](windows-sockets-error-codes-2.md)
>
> Si noti anche che in questa tabella specifica entrambe [**le chiamate di**](/windows/win32/api/winsock/nf-winsock-bind) associazione vengono effettuate con lo stesso account utente.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Prima <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>chiamata di</strong></a> binding</td>
        <td bgcolor="#C0C0C0" colspan="6">Seconda <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>chiamata di</strong></a> binding</td>
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

Alcune voci nella tabella precedente spiegano i vantaggi.

Ad esempio, se il primo chiamante imposta **SO \_ EXCLUSIVEADDRUSE** su un indirizzo specifico e il secondo  chiamante tenta di chiamare [**bind**](/windows/win32/api/winsock/nf-winsock-bind) con un indirizzo con caratteri jolly sulla stessa porta, la seconda chiamata di binding avrà esito positivo. In questo caso specifico, il secondo chiamante è associato a tutte le interfacce ad eccezione dell'indirizzo specifico a cui è associato il primo chiamante. Si noti che il contrario di questo caso non è vero:  se il primo chiamante imposta **SO \_ EXCLUSIVEADDRUSE** e chiama bind con il flag con caratteri jolly, il secondo chiamante non è in grado di chiamare **bind** con la stessa porta.

Il comportamento dell'associazione socket cambia quando le chiamate di associazione socket vengono effettuate con account utente diversi. La tabella seguente specifica il comportamento che si verifica nei sistemi operativi Windows Server 2003 e versioni successive quando un secondo socket tenta di eseguire l'associazione a un indirizzo associato in precedenza da un primo socket usando opzioni socket specifiche e un account utente diverso.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Prima <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>chiamata di</strong></a> binding</td>
        <td bgcolor="#C0C0C0" colspan="6">Seconda <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>chiamata di</strong></a> binding</td>
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

Si noti che il comportamento predefinito è diverso quando le [**chiamate di**](/windows/win32/api/winsock/nf-winsock-bind) associazione vengono effettuate con account utente diversi. Se il primo chiamante non imposta alcuna opzione nel socket ed esegue l'associazione all'indirizzo con caratteri jolly, il secondo chiamante non può impostare l'opzione **SO \_ REUSEADDR** ed eseguire correttamente l'associazione alla stessa porta. Anche il comportamento predefinito senza opzioni impostate restituisce un errore.

In Windows Vista e versioni successive è possibile creare un socket dual stack che opera sia su IPv6 che su IPv4. Quando un socket dual stack è associato all'indirizzo con caratteri jolly, la porta specificata viene riservata sia nello stack di rete IPv4 che in quello IPv6 e nei controlli associati a **SO \_ REUSEADDR** e **SO \_ EXCLUSIVEADDRUSE** (se impostato). Questi controlli devono avere esito positivo in entrambi gli stack di rete. Ad esempio, se un socket TCP dual stack imposta **SO \_ EXCLUSIVEADDRUSE** e quindi tenta di eseguire l'associazione alla porta 5000, nessun altro socket TCP può essere associato in precedenza alla porta 5000 (carattere jolly o specifico). In questo caso, se un socket TCP IPv4 è stato associato in [](/windows/win32/api/winsock/nf-winsock-bind) precedenza all'indirizzo di loopback sulla porta 5000, la chiamata di associazione per il socket dual stack avrà esito negativo con [WSAEACCES](windows-sockets-error-codes-2.md).

## <a name="application-strategies"></a>Strategie delle applicazioni

Quando si sviluppa un'applicazione di rete che opera a livello di socket, è importante considerare il tipo di sicurezza del socket necessario. Le applicazioni client, ovvero le applicazioni che si connettono o inviano dati a un servizio, raramente richiedono passaggi aggiuntivi perché vengono associati a una porta locale casuale (effimera). Se il client richiede un'associazione di porta locale specifica per funzionare correttamente, è necessario considerare la sicurezza del socket.

**L'opzione SO \_ REUSEADDR** ha pochissimi usi nelle applicazioni normali, a parte i socket multicast in cui i dati vengono recapitati a tutti i socket associati sulla stessa porta. In caso contrario, qualsiasi applicazione che imposta questa opzione socket deve essere riprogettata per rimuovere la dipendenza perché è estremamente vulnerabile al "hijack del socket". Se **l'opzione SOCKET \_ REUSEADDR** può essere usata per eseguire potenzialmente il hijack di una porta in un'applicazione server, l'applicazione deve essere considerata non sicura.

Tutte le applicazioni server devono impostare **SO \_ EXCLUSIVEADDRUSE** per un livello elevato di sicurezza dei socket. Non solo impedisce a software dannoso di hijack della porta, ma indica anche se un'altra applicazione è associata o meno alla porta richiesta. Ad esempio, una [](/windows/win32/api/winsock/nf-winsock-bind) chiamata per l'associazione all'indirizzo con caratteri jolly da parte di un processo con l'opzione socket **SO \_ EXCLUSIVEADDRUSE** impostata avrà esito negativo se un altro processo è attualmente associato alla stessa porta su un'interfaccia specifica.

Infine, anche se la sicurezza dei socket è stata migliorata in Windows Server 2003, un'applicazione deve sempre impostare l'opzione socket **SO \_ EXCLUSIVEADDRUSE** per assicurarsi che sia associata a tutte le interfacce specifiche richieste dal processo. La sicurezza dei socket in Windows Server 2003 aggiunge un maggiore livello di sicurezza per le applicazioni legacy, ma gli sviluppatori di applicazioni devono comunque progettare i propri prodotti in base a tutti gli aspetti della sicurezza.
