---
description: Lo strumento di configurazione della traccia Microsoft Windows HTTP Services (WinHTTP), WinHttpTraceCfg.exe, viene usato per configurare le funzionalità di traccia per il debug e l'analisi dei pacchetti.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, uno strumento di configurazione della traccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307088"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, uno strumento di configurazione della traccia

Lo strumento di configurazione della traccia [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) , WinHttpTraceCfg.exe, viene usato per configurare le funzionalità di traccia per il debug e l'analisi dei pacchetti. La possibilità di monitorare le funzioni WinHTTP e il traffico di rete corrispondente è importante. Il debug di applicazioni che utilizzano protocolli di Wire crittografati, ad esempio Secure Sockets Layer (SSL), impedisce l'analisi dei pacchetti a livello di trasporto di rete e richiede la possibilità di intercettare il traffico tra il client e il server dopo che è stato decrittografato. I servizi HTTP di Microsoft Windows (WinHTTP) forniscono una funzionalità di traccia con una vasta gamma di funzionalità per intercettare il flusso di traffico tra il client e il server.

Questa funzionalità di traccia può essere uno strumento utile per eseguire il debug. Può essere usato, ad esempio, per visualizzare i parametri passati a diverse chiamate di funzione, nonché per visualizzare i dati effettivi inviati e ricevuti da un'applicazione WinHTTP.

-   [Utilizzo della funzionalità di traccia](#using-the-trace-facility)
-   [Interpretazione dei dati di traccia](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Utilizzo della funzionalità di traccia

WinHTTP ottiene i parametri di controllo della traccia dal registro di sistema. Questi parametri di controllo influiscono sul modo in cui WinHTTP produce l'output di traccia e la formattazione dell'output. Tutte le applicazioni che utilizzano WinHTTP condividono le stesse impostazioni.

Uno strumento di configurazione della funzionalità di traccia, WinHttpTraceCfg.exe, è disponibile come download nel sito Web [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) . Lo strumento di configurazione consente di impostare o recuperare le impostazioni del registro di sistema della funzionalità di traccia basate sui parametri della riga di comando specificati.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

Nella tabella seguente sono elencati i parametri possibili per lo strumento di configurazione di.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parametro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Visualizza i dati di sintassi.<br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Specifica se la funzionalità di traccia è abilitata o disabilitata. <br/> 
<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Impostazione predefinita. Disabilita la traccia.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Abilita la traccia.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-l</td>
<td><p>Specifica un prefisso per il file di log. Il prefisso può includere un percorso. Il file di log viene scritto nella directory corrente o nella directory specificata nel prefisso e ha il formato seguente.</p>
<p><<em></em> > prefisso -< <em>nome dell'applicazione</em> > . <<em>Time</em> > . log</p>
<p>Se non si specifica un prefisso, viene utilizzata una stringa vuota. Specificare &quot; * &quot; per eliminare un prefisso esistente.</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>Specifica se l'output di traccia viene visualizzato in un debugger o viene scritto in un file.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Impostazione predefinita. Scrive nel file di log.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Viene visualizzato in un debugger.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-S</td>
<td><p>Specifica il modo in cui viene visualizzato il traffico di rete (richieste e risposte).</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Visualizza solo le intestazioni HTTP.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Impostazione predefinita. Mostra il traffico di rete in formato American National Standards Institute (ANSI).</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Mostra il traffico di rete in formato esadecimale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>-T</td>
<td><p>Specifica se le chiamate di funzione di primo livello vengono registrate nella traccia.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Impostazione predefinita. Le chiamate di funzione non vengono registrate.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Vengono registrate le chiamate di funzione di primo livello.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-M</td>
<td><p>Specifica la dimensione massima, in byte, di un file di log generato dalla funzionalità di traccia. Se questa opzione viene specificata senza una dimensione, il valore minimo è 65.535 byte. Se un file di log raggiunge la dimensione massima, il contenuto del file verrà cancellato. I dati di traccia continuano a essere scritti nel file di log.</p></td>
</tr>
</tbody>
</table>



 

L'esecuzione dello strumento di configurazione della funzionalità Trace e la specifica di nessun parametro consente di recuperare e visualizzare le impostazioni correnti del registro di sistema

> [!Note]  
> I file di log aumentano rapidamente e peggiorano le prestazioni dell'applicazione. Prima di abilitare la funzionalità di traccia, verificare che lo spazio su disco rigido richiesto sia disponibile.

 

## <a name="interpreting-trace-data"></a>Interpretazione dei dati di traccia

Il flusso di dati della funzionalità di traccia riflette le funzioni WinHTTP chiamate nell'applicazione e qualsiasi dato HTTP inviato o ricevuto. In alcuni casi, vengono visualizzate anche le funzioni chiamate internamente da WinHTTP.

Nell'immagine seguente viene illustrata una parte di un file di log generato dalla funzionalità Trace. Diversi elementi vengono evidenziati e contrassegnati con l'etichetta.

![traccia di esempio](images/ss-tracer-wco.png)

Ogni riga dell'output di traccia contiene informazioni in tre colonne. La prima colonna indica la data e l'ora in cui è stata registrata la voce. La seconda colonna Mostra un identificatore (ID) di richiesta che può essere usato per distinguere più richieste. Se la voce di log non corrisponde a una richiesta specifica, \* \* in questa colonna viene visualizzato "Session". Può essere utile ordinare il file di log in base a questo ID per visualizzare solo gli eventi che si verificano per una singola richiesta. Nell'esempio seguente viene illustrato un comando che è possibile utilizzare per ordinare il file di log.

**findstr 00000001 LogFile. log**

La terza colonna Mostra una chiamata di funzione, il traffico HTTP o un messaggio di stato incluso per facilitare l'interpretazione della traccia.

Quando una voce di log corrisponde a una chiamata di funzione, vengono registrati anche i parametri della funzione. Gli indirizzi di memoria vengono visualizzati in formato esadecimale, mentre tutti gli altri valori vengono visualizzati come stringa ASCII. La funzionalità di traccia registra anche il valore e l'ora di ritorno per ogni funzione.

Il formato dei dati HTTP dipende dalle impostazioni del registro di sistema specificate con lo strumento di configurazione della funzionalità Trace. Quando i dati HTTP vengono crittografati, anche i dati decrittografati vengono visualizzati nell'output di traccia.

 

 




