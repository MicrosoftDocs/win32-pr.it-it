---
description: Le proprietà di riepilogo per i pacchetti di installazione, le trasformazioni e le patch sono descritte nelle tabelle seguenti.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descrizioni delle proprietà di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb93e5881a25b6b79eef0fb0711acc1fec1b6666
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629544"
---
# <a name="summary-property-descriptions"></a>Descrizioni delle proprietà di riepilogo

Le proprietà di riepilogo per i pacchetti di installazione, le trasformazioni e le patch sono descritte nelle tabelle seguenti. Si noti che il significato di una particolare proprietà di riepilogo può essere diverso a seconda che il database appartenga a un pacchetto di installazione, una trasformazione o un pacchetto patch. Per altre informazioni su ID proprietà, PIN e tipi, vedere [Summary Information Stream Property Set](summary-information-stream-property-set.md).

## <a name="installation-packages"></a>Pacchetti di installazione



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Summary - proprietà</th>
<th>Significato di questa proprietà in un database di installazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Titolo</strong></a></td>
<td>Descrizione di questo file come pacchetto di installazione. La descrizione deve includere la frase &quot; <a href="about-the-installer-database.md">Database di installazione</a>.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Oggetto</strong></a></td>
<td>Nome del prodotto installato da questo pacchetto. Deve essere lo stesso nome della <a href="productname.md"><strong>proprietà ProductName.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autore</strong></a></td>
<td>Nome del produttore del prodotto. Deve essere lo stesso nome della <a href="manufacturer.md"><strong>proprietà Manufacturer.</strong></a></td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Parole chiave</strong></a></td>
<td>Elenco di parole chiave che possono essere usate dai browser di file per eseguire ricerche di parole chiave per un file. Le parole chiave devono includere &quot; il programma di installazione e parole chiave specifiche del &quot; prodotto.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Commenti</strong></a></td>
<td>Contiene la frase: Questo database del programma di installazione contiene la logica e i dati necessari per &quot; installare <nome del <em>prodotto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Modello</strong></a> (OBBLIGATORIO)</td>
<td>Piattaforma e lingue compatibili con questo pacchetto di installazione. Per la <a href="template-summary.md"><strong>sintassi,</strong></a> vedere Modello.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Autore ultimo salvataggio</strong></a></td>
<td>Gli sviluppatori di strumenti di modifica del database possono usare questa proprietà durante il processo di sviluppo per tenere traccia dell'ultima persona che ha modificato il database di installazione. Questa proprietà deve essere impostata su Null in un database di spedizione finale. Il programma di installazione imposta questa proprietà sul valore della <a href="logonuser.md"><strong>proprietà LogonUser</strong></a> durante un'installazione <a href="administrative-installation.md"><strong>amministrativa</strong></a>di . Il programma di installazione non usa mai questa proprietà e un utente non deve mai modificarla.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Numero revisione</strong></a> (OBBLIGATORIO)</td>
<td>Contiene il codice <a href="package-codes.md">del pacchetto del</a> programma di installazione.</td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Ultima stampa</strong></a></td>
<td>Può essere impostato sulla data e sull'ora durante un'installazione <a href="administrative-installation.md">amministrativa</a> per registrare quando è stata creata l'immagine amministrativa.</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Crea ora/data</strong></a></td>
<td>Data e ora di creazione del database del programma di installazione.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Data/ora ultimo salvataggio</strong></a></td>
<td>Data e ora di sistema correnti dell'ultimo salvataggio del database del programma di installazione. Inizialmente Null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Conteggio pagine</strong></a> (OBBLIGATORIO)</td>
<td>Contiene un valore utilizzato per identificare la versione minima del programma di installazione richiesta dal pacchetto di installazione. Ad esempio, se il pacchetto richiede almeno la versione 2.0 del programma di installazione, questa proprietà deve essere impostata su un numero intero di 200.
<blockquote>
[!Note]<br />
Il valore di questa proprietà deve essere maggiore o uguale a 200 con i pacchetti Windows <a href="64-bit-windows-installer-packages.md">programma di installazione a 64 bit.</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Conteggio parole</strong></a> (OBBLIGATORIO)</td>
<td>Tipo dell'immagine del file di origine. Archiviato al posto della proprietà Count standard. Questa proprietà è un campo di bit. Per i <a href="word-count-summary.md"><strong>valori, vedere</strong></a> l'argomento Conteggio parole.<br/> A partire Windows Installer versione 4.0 in Windows Vista, questa proprietà include bit per specificare se sono necessari privilegi elevati.<br/></td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Numero di caratteri</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Creazione di un'applicazione</strong></a></td>
<td>Contiene il nome del software usato per creare il database di installazione.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Sicurezza</strong></a></td>
<td>Il valore di questa proprietà deve essere 2 - Consigliato in sola lettura.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Codepage</strong></a></td>
<td>Valore numerico della tabella codici ANSI utilizzata per visualizzare le informazioni di riepilogo. Questa proprietà deve essere impostata prima che le proprietà della stringa siano impostate nelle informazioni di riepilogo.</td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a>Trasformazioni



| Summary - proprietà                                              | Significato di questa proprietà in una trasformazione                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Titolo**](title-summary.md)                                | Descrizione di questo file come trasformazione. La descrizione deve includere la frase: "[Transform](database-transforms.md)".                                                                                                                                                                     |
| [**Oggetto**](subject-summary.md)                            | Nome del prodotto installato dal pacchetto di installazione originale. Deve essere lo stesso valore della proprietà [**Riepilogo**](subject-summary.md) oggetto nel pacchetto di installazione originale.                                                                                            |
| [**Autore**](author-summary.md)                              | Nome del produttore della trasformazione.                                                                                                                                                                                                                                                   |
| [**Parole chiave**](keywords-summary.md)                          | Elenco di parole chiave che possono essere usate dai browser di file per eseguire ricerche di parole chiave per un file. Le parole chiave devono includere "Installer" e parole chiave specifiche del prodotto.                                                                                                                             |
| [**Commenti**](comments-summary.md)                          | Contiene la frase: "Questa trasformazione contiene la logica e i dati necessari per installare <*nome del* prodotto>".                                                                                                                                                                                     |
| [**Modello**](template-summary.md) (OBBLIGATORIO)               | Le versioni della piattaforma e del linguaggio compatibili con questa trasformazione. Questo valore può essere lasciato vuoto se non sono presenti restrizioni. È possibile specificare un solo linguaggio per una trasformazione. Per altre informazioni sulla sintassi, vedere [**Modello**](template-summary.md).                                |
| [**Autore ultimo salvataggio**](last-saved-by-summary.md)                | ID piattaforma e lingua del database dopo che è stato trasformato. La [**proprietà Riepilogo**](template-summary.md) modello nel nuovo database deve essere impostata sullo stesso valore.                                                                                              |
| [**Numero revisione**](revision-number-summary.md) (OBBLIGATORIO) | Elenco dei GUID del codice prodotto e della versione dei prodotti nuovi e originali e del GUID del codice di aggiornamento. L'elenco è separato da punti e virgola come indicato di seguito. *Original-Product-Code Original-Product-Version*; *New-Product Code New-Product-Version*; *Codice di aggiornamento*<br/>                       |
| [**Ultima stampa**](last-printed-summary.md)                  | Null                                                                                                                                                                                                                                                                                              |
| [**Crea ora/data**](create-time-date-summary.md)          | Data e ora di creazione della trasformazione.                                                                                                                                                                                                                                                 |
| [**Data/ora ultimo salvataggio**](last-saved-time-date-summary.md)  | Data e ora di sistema correnti al momento del salvataggio della trasformazione. Inizialmente Null.                                                                                                                                                                                                             |
| [**Conteggio pagine**](page-count-summary.md) (OBBLIGATORIO)           | Valore utilizzato per indicare la versione minima del programma di installazione necessaria per elaborare la trasformazione. Il valore deve essere impostato sul maggiore dei due valori della proprietà [**Conteggio**](page-count-summary.md) pagine che appartengono ai database usati per generare la trasformazione.                                 |
| [**Conteggio parole**](word-count-summary.md) (OBBLIGATORIO)           | Null                                                                                                                                                                                                                                                                                              |
| [**Numero di caratteri**](character-count-summary.md)            | Questa parte del flusso di informazioni di riepilogo è suddivisa in due parole a 16 bit. La parola superiore contiene i [*flag di convalida della trasformazione*](t-gly.md). La parola inferiore contiene [*flag di condizione di errore di trasformazione*](t-gly.md). |
| [**Creazione di un'applicazione**](creating-application-summary.md)  | Contiene il nome del software usato per creare questa trasformazione.                                                                                                                                                                                                                                  |
| [**Sicurezza**](security-summary.md)                          | Il valore di questa proprietà deve essere 4 - Applicato in sola lettura.                                                                                                                                                                                                                                      |
| [**Codepage**](codepage-summary.md)                          | Valore numerico della tabella codici ANSI utilizzata per visualizzare le informazioni di riepilogo. Questa proprietà deve essere impostata prima di poter impostare le proprietà della stringa nelle informazioni di riepilogo.                                                                                                                    |



 

## <a name="patch-packages"></a>Pacchetti di patch



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà Summary</th>
<th>Significato di questa proprietà in un pacchetto patch</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Titolo</strong></a></td>
<td>Descrizione di questo file come pacchetto di patch. La descrizione deve includere la frase: &quot; <a href="patch-packages.md">Patch</a>.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Oggetto</strong></a></td>
<td>Descrizione della patch che include il nome del prodotto.</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autore</strong></a></td>
<td>Nome del produttore del pacchetto di patch.</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Parole chiave</strong></a></td>
<td>Elenco delimitato da punto e virgola di origini della patch.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Commenti</strong></a></td>
<td>Contiene la frase: Questa patch contiene la logica e i dati necessari per installare <&quot; <em>nome del prodotto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Modello</strong></a> (OBBLIGATORIO)</td>
<td>Elenco delimitato da punto e virgola dei codici prodotto che possono accettare questa patch.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Autore ultimo salvataggio</strong></a></td>
<td>Elenco delimitato da punto e virgola di nomi di archiviazione secondari di trasformazione nell'ordine in cui vengono applicati da questa patch.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Numero di revisione</strong></a> (OBBLIGATORIO)</td>
<td>Contiene il codice di patch GUID per la patch. Questa operazione può essere seguita da un elenco di GUID del codice patch per le patch che vengono rimosse quando viene applicata questa patch. I codici patch vengono concatenati senza delimitatori che separano i GUID nell'elenco.
<blockquote>
[!Note]<br />
Se il pacchetto di patch contiene una tabella <a href="msipatchsequence-table.md"><strong>MsiPatchSequence,</strong></a> la patch non rimuove le patch elencate dopo il GUID della patch corrente.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Ultima stampa</strong></a></td>
<td>Null</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Crea ora/data</strong></a></td>
<td>Ora e data di creazione del file di patch.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Data/ora ultimo salvataggio</strong></a></td>
<td>Ora e data di sistema correnti al momento del salvataggio del pacchetto di patch. Questo valore è inizialmente Null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Conteggio pagine</strong></a> (OBBLIGATORIO)</td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Conteggio parole</strong></a> (OBBLIGATORIO)</td>
<td>Contiene un valore che indica la versione minima Windows del programma di installazione necessaria per installare la patch. Una patch con un valore di conteggio parole pari a 4 richiede Windows Installer versione 3.0 o successiva per applicare la patch. Il valore 3 indica che è necessario Windows installer versione 2.0 o successiva. Il valore 2 indica che è necessario Windows Installer versione 1.2 o successiva. Il valore predefinito è 1.</td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Conteggio caratteri</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Creazione di un'applicazione</strong></a></td>
<td>Nome del software usato per creare la patch.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Sicurezza</strong></a></td>
<td>Il valore di questa proprietà deve essere 4 - Applicato in sola lettura.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Codepage</strong></a></td>
<td>Valore numerico della tabella codici ANSI utilizzata per visualizzare le informazioni di riepilogo. Questa proprietà deve essere impostata prima che le proprietà della stringa siano impostate nelle informazioni di riepilogo.</td>
</tr>
</tbody>
</table>



 

 

 




