---
description: Lo strumento Windows di traccia dei servizi HTTP (WinHTTP), WinHttpTraceCfg.exe, viene usato per configurare le funzionalità di traccia a scopo di debug e analisi dei pacchetti.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, uno strumento di configurazione della traccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7747e0b2fe023ab3c2c86d19a722059482aed19062cf2a450b8d0f237a8b3a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562415"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, uno strumento di configurazione della traccia

Lo strumento Windows di traccia dei servizi [HTTP (WinHTTP),](about-winhttp.md) WinHttpTraceCfg.exe, viene usato per configurare le funzionalità di traccia a scopo di debug e analisi dei pacchetti. La possibilità di monitorare le funzioni WinHTTP e il traffico di rete corrispondente è importante. Il debug di applicazioni che utilizzano protocolli di rete crittografati, ad esempio Secure Sockets Layer (SSL), preclude lo sniffing dei pacchetti a livello di trasporto di rete e richiede la possibilità di intercettare il traffico tra il client e il server dopo che è stato decrittografato. Microsoft Windows servizi HTTP (WinHTTP) offre una funzionalità di traccia con una gamma di funzionalità per intercettare il flusso di traffico tra il client e il server.

Questa funzionalità di traccia può essere uno strumento utile per il debug. Può essere usato, ad esempio, per visualizzare i parametri passati a varie chiamate di funzione, nonché per visualizzare i dati effettivi inviati e ricevuti da un'applicazione WinHTTP.

-   [Uso della funzionalità di traccia](#using-the-trace-facility)
-   [Interpretazione dei dati di traccia](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Uso della funzionalità di traccia

WinHTTP ottiene i parametri di controllo di traccia dal Registro di sistema. Questi parametri di controllo influiscono sul modo in cui WinHTTP produce l'output di traccia e sulla formattazione dell'output. Tutte le applicazioni che usano WinHTTP condividono le stesse impostazioni.

Uno strumento di configurazione della funzionalità di traccia, WinHttpTraceCfg.exe, è disponibile come download nel sito Web degli strumenti [di Windows Server 2003 Resource Kit.](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) Lo strumento di configurazione imposta o recupera le impostazioni del Registro di sistema della funzionalità di traccia in base ai parametri della riga di comando specificati.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

Nella tabella seguente sono elencati i possibili parametri per lo strumento di configurazione.



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
<td>Visualizza i dati della sintassi.<br/></td>
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
<p><<em></em> > prefisso -< <em>nome dell'applicazione</em> > . <<em>ora .log</em> ></p>
<p>Se non viene specificato un prefisso, viene utilizzata una stringa vuota. Specificare &quot; * &quot; per eliminare un prefisso esistente.</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>Specifica se l'output di traccia viene visualizzato in un debugger o scritto in un file.</p>

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
<td><p>Specifica la modalità di visualizzazione del traffico di rete (richieste e risposte).</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Visualizza solo le intestazioni HTTP.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Impostazione predefinita. Mostra il traffico di rete in American National Standards Institute (ANSI).</td>
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
<td><p>Specifica le dimensioni massime, in byte, di un file di log generato dalla funzionalità di traccia. Se questa opzione viene specificata senza dimensioni, il valore minimo è 65.535 byte. Se un file di log raggiunge le dimensioni massime, il contenuto del file viene cancellato. I dati di traccia continuano a essere scritti nel file di log.</p></td>
</tr>
</tbody>
</table>



 

Se si esegue lo strumento di configurazione della funzionalità di traccia e non si specifica alcun parametro, vengono recuperate e visualizzate le impostazioni correnti del Registro di sistema.

> [!Note]  
> I file di log aumentano rapidamente e riducono le prestazioni dell'applicazione. Assicurarsi che lo spazio su disco rigido richiesto sia disponibile prima di abilitare la funzionalità di traccia.

 

## <a name="interpreting-trace-data"></a>Interpretazione dei dati di traccia

Il flusso di dati della struttura di traccia riflette le funzioni WinHTTP chiamate nell'applicazione e tutti i dati HTTP inviati o ricevuti. In alcuni casi, vengono visualizzate anche le funzioni chiamate internamente da WinHTTP.

L'immagine seguente mostra una parte di un file di log generato dalla funzionalità di traccia. Diversi elementi sono evidenziati ed etichettati.

![traccia di esempio](images/ss-tracer-wco.png)

Ogni riga di output di traccia contiene informazioni in tre colonne. La prima colonna mostra la data e l'ora in cui è stata registrata la voce. La seconda colonna mostra un identificatore di richiesta (ID) che può essere usato per distinguere tra più richieste. Se la voce di log non corrisponde a una richiesta specifica, in questa colonna viene \* \* visualizzato " Sessione ". Può essere utile ordinare il file di log in base a questo ID per visualizzare solo gli eventi che si verificano per una singola richiesta. Nell'esempio seguente viene illustrato un comando che è possibile usare per ordinare il file di log.

**findstr 00000001 LogFile.log**

La terza colonna mostra una chiamata di funzione, il traffico HTTP o un messaggio di stato incluso per interpretare la traccia.

Quando una voce di log corrisponde a una chiamata di funzione, vengono registrati anche i parametri della funzione. Gli indirizzi di memoria vengono visualizzati in formato esadecimale, mentre tutti gli altri valori vengono visualizzati come stringa ASCII. La funzionalità di traccia registra anche l'ora e il valore restituiti per ogni funzione.

Il formato dei dati HTTP dipende dalle impostazioni del Registro di sistema specificate con lo strumento di configurazione della funzionalità di traccia. Quando i dati HTTP vengono crittografati, i dati decrittografati vengono visualizzati anche nell'output di traccia.

 

 




