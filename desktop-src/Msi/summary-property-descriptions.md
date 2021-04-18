---
description: Le proprietà di riepilogo per i pacchetti di installazione, le trasformazioni e le patch sono descritte nelle tabelle seguenti.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descrizioni delle proprietà di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318276"
---
# <a name="summary-property-descriptions"></a>Descrizioni delle proprietà di riepilogo

Le proprietà di riepilogo per i pacchetti di installazione, le trasformazioni e le patch sono descritte nelle tabelle seguenti. Si noti che il significato di una particolare proprietà di riepilogo può variare a seconda che il database appartenga a un pacchetto di installazione, una trasformazione o un pacchetto di patch. Per ulteriori informazioni sugli ID, i PID e i tipi di proprietà, vedere [set di proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md).

## <a name="installation-packages"></a>Pacchetti di installazione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà Summary</th>
<th>Significato di questa proprietà in un database di installazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Titolo</strong></a></td>
<td>Descrizione del file come pacchetto di installazione. La descrizione deve includere la frase &quot; <a href="about-the-installer-database.md">database di installazione</a>.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Oggetto</strong></a></td>
<td>Nome del prodotto installato da questo pacchetto. Deve corrispondere al nome della proprietà <a href="productname.md"><strong>ProductName</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autore</strong></a></td>
<td>Nome del produttore di questo prodotto. Deve corrispondere al nome della proprietà del <a href="manufacturer.md"><strong>produttore</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Parole chiave</strong></a></td>
<td>Un elenco di parole chiave che possono essere usate dai browser di file per cercare un file. Le parole chiave devono includere il &quot; programma &quot; di installazione e le parole chiave specifiche del prodotto.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Commenti</strong></a></td>
<td>Contiene la frase: il &quot; database del programma di installazione contiene la logica e i dati necessari per installare <<em>nome del prodotto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Modello</strong></a> (obbligatorio)</td>
<td>Piattaforma e linguaggi compatibili con questo pacchetto di installazione. Per la sintassi, vedere il <a href="template-summary.md"><strong>modello</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Autore ultimo salvataggio</strong></a></td>
<td>Gli sviluppatori di strumenti di modifica del database possono utilizzare questa proprietà durante il processo di sviluppo per tenere traccia dell'ultima persona che ha modificato il database di installazione. Questa proprietà deve essere impostata su null in un database di spedizione finale. Il programma di installazione imposta questa proprietà sul valore della proprietà <a href="logonuser.md"><strong>LogonUser</strong></a> durante un' <a href="administrative-installation.md"><strong>installazione amministrativa</strong></a>. Il programma di installazione non usa mai questa proprietà e un utente non deve mai modificarla.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Numero revisione</strong></a> (obbligatorio)</td>
<td>Contiene il <a href="package-codes.md">codice del pacchetto</a> del programma di installazione.</td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Ultima stampa</strong></a></td>
<td>Può essere impostato sulla data e sull'ora durante un' <a href="administrative-installation.md">installazione amministrativa</a> per registrare il momento in cui è stata creata l'immagine amministrativa.</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Data/ora creazione</strong></a></td>
<td>Data e ora in cui è stato creato il database del programma di installazione.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Data/ora ultimo salvataggio</strong></a></td>
<td>Data e ora di sistema correnti al momento dell'ultimo salvataggio del database del programma di installazione. Inizialmente null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Conteggio pagine</strong></a> (obbligatorio)</td>
<td>Contiene un valore utilizzato per identificare la versione minima del programma di installazione richiesta dal pacchetto di installazione. Se, ad esempio, il pacchetto richiede almeno la versione 2,0 del programma di installazione, questa proprietà deve essere impostata su un numero intero pari a 200.
<blockquote>
[!Note]<br />
Il valore di questa proprietà deve essere 200 o superiore con i <a href="64-bit-windows-installer-packages.md">pacchetti Windows Installer a 64 bit</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Conteggio parole</strong></a> (obbligatorio)</td>
<td>Tipo di immagine del file di origine. Archiviato al posto della proprietà Count standard. Questa proprietà è un campo di bit. Vedere l'argomento relativo al <a href="word-count-summary.md"><strong>conteggio delle parole</strong></a> per i valori.<br/> A partire da Windows Installer versione 4,0 in Windows Vista, questa proprietà include BITS per specificare se sono necessari privilegi elevati.<br/></td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Numero di caratteri</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Creazione dell'applicazione</strong></a></td>
<td>Contiene il nome del software utilizzato per creare il database di installazione.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Sicurezza</strong></a></td>
<td>Il valore di questa proprietà deve essere di sola lettura consigliato.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>CodePage</strong></a></td>
<td>Valore numerico della tabella codici ANSI utilizzata per visualizzare le informazioni di riepilogo. Questa proprietà deve essere impostata prima di impostare le proprietà di stringa nelle informazioni di riepilogo.</td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a>Trasformazioni



| Proprietà Summary                                              | Significato di questa proprietà in una trasformazione                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Titolo**](title-summary.md)                                | Descrizione del file come trasformazione. La descrizione deve includere la frase: "[Transform](database-transforms.md)".                                                                                                                                                                     |
| [**Oggetto**](subject-summary.md)                            | Nome del prodotto installato dal pacchetto di installazione originale. Deve corrispondere al valore della proprietà di [**Riepilogo dell'oggetto**](subject-summary.md) nel pacchetto di installazione originale.                                                                                            |
| [**Autore**](author-summary.md)                              | Nome del produttore di questa trasformazione.                                                                                                                                                                                                                                                   |
| [**Parole chiave**](keywords-summary.md)                          | Un elenco di parole chiave che possono essere usate dai browser di file per cercare un file. Le parole chiave devono includere "Installer", nonché parole chiave specifiche del prodotto.                                                                                                                             |
| [**Commenti**](comments-summary.md)                          | Contiene la frase: "questa trasformazione contiene la logica e i dati necessari per installare <*nome prodotto*>".                                                                                                                                                                                     |
| [**Modello**](template-summary.md) (obbligatorio)               | Versioni della piattaforma e della lingua compatibili con questa trasformazione. Questo valore può essere lasciato vuoto se non sono presenti restrizioni. È possibile specificare una sola lingua per una trasformazione. Per ulteriori informazioni sulla sintassi, vedere [**template**](template-summary.md).                                |
| [**Autore ultimo salvataggio**](last-saved-by-summary.md)                | ID della piattaforma e della lingua del database dopo che è stato trasformato. È necessario impostare la proprietà di [**Riepilogo del modello**](template-summary.md) nel nuovo database sugli stessi valori.                                                                                              |
| [**Numero revisione**](revision-number-summary.md) (obbligatorio) | Elenco dei GUID e della versione del codice prodotto dei prodotti nuovi e originali e del GUID del codice di aggiornamento. L'elenco è separato da punti e virgola come indicato di seguito. *Originale-prodotto-codice originale-versione prodotto*; *New-Product Code New-Product-Version*; *Aggiornamento-codice*<br/>                       |
| [**Ultima stampa**](last-printed-summary.md)                  | Null                                                                                                                                                                                                                                                                                              |
| [**Data/ora creazione**](create-time-date-summary.md)          | Data e ora di creazione della trasformazione.                                                                                                                                                                                                                                                 |
| [**Data/ora ultimo salvataggio**](last-saved-time-date-summary.md)  | Data e ora di sistema correnti nel momento in cui la trasformazione è stata salvata. Inizialmente null.                                                                                                                                                                                                             |
| [**Conteggio pagine**](page-count-summary.md) (obbligatorio)           | Valore utilizzato per indicare la versione minima del programma di installazione necessaria per elaborare la trasformazione. Il valore deve essere impostato sul valore maggiore dei due valori della proprietà [**conteggio pagine**](page-count-summary.md) che appartengono ai database utilizzati per generare la trasformazione.                                 |
| [**Conteggio parole**](word-count-summary.md) (obbligatorio)           | Null                                                                                                                                                                                                                                                                                              |
| [**Numero di caratteri**](character-count-summary.md)            | Questa parte del flusso di informazioni di riepilogo è divisa in parole a 2 16 bit. Il termine superiore contiene i [*flag di convalida della trasformazione*](t-gly.md). La parola più bassa contiene [*flag di condizione di errore di trasformazione*](t-gly.md). |
| [**Creazione dell'applicazione**](creating-application-summary.md)  | Contiene il nome del software utilizzato per creare questa trasformazione.                                                                                                                                                                                                                                  |
| [**Sicurezza**](security-summary.md)                          | Il valore di questa proprietà deve essere di sola lettura.                                                                                                                                                                                                                                      |
| [**CodePage**](codepage-summary.md)                          | Valore numerico della tabella codici ANSI utilizzata per visualizzare le informazioni di riepilogo. Questa proprietà deve essere impostata prima di poter impostare le proprietà di stringa nelle informazioni di riepilogo.                                                                                                                    |



 

## <a name="patch-packages"></a>Pacchetti patch



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà Summary</th>
<th>Significato di questa proprietà in un pacchetto di patch</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Titolo</strong></a></td>
<td>Descrizione del file come pacchetto di patch. La descrizione deve includere la frase: &quot; <a href="patch-packages.md">patch</a>.&quot;</td>
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
<td>Elenco delimitato da punti e virgola delle origini della patch.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Commenti</strong></a></td>
<td>Contiene la frase: &quot; questa patch contiene la logica e i dati necessari per installare <<em>nome del prodotto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Modello</strong></a> (obbligatorio)</td>
<td>Elenco delimitato da punti e virgola dei codici prodotto che possono accettare questa patch.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Autore ultimo salvataggio</strong></a></td>
<td>Elenco delimitato da punti e virgola di nomi di sottoarchivi di trasformazione nell'ordine in cui sono applicati da questa patch.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Numero revisione</strong></a> (obbligatorio)</td>
<td>Contiene il codice della patch GUID per la patch. Questo può essere seguito da un elenco di GUID di codice patch per le patch che vengono rimosse quando viene applicata questa patch. I codici patch sono concatenati senza delimitatori che separano i GUID nell'elenco.
<blockquote>
[!Note]<br />
Se il pacchetto di patch contiene una tabella <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> , la patch non rimuove le patch elencate dopo il GUID della patch corrente.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Ultima stampa</strong></a></td>
<td>Null</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Data/ora creazione</strong></a></td>
<td>Data e ora in cui è stato creato il file di patch.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Data/ora ultimo salvataggio</strong></a></td>
<td>Data e ora di sistema correnti nel momento in cui è stato salvato il pacchetto di patch. Questo valore è inizialmente null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Conteggio pagine</strong></a> (obbligatorio)</td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Conteggio parole</strong></a> (obbligatorio)</td>
<td>Contiene un valore che indica la versione minima di Windows Installer necessaria per installare la patch. Per applicare una patch con un valore di conteggio delle parole pari a 4, è necessario Windows Installer versione 3,0 o successiva. Il valore 3 indica che è necessario Windows Installer versione 2,0 o successiva. Il valore 2 indica che è necessario Windows Installer versione 1,2 o successiva. Il valore predefinito è 1.</td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Numero di caratteri</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Creazione dell'applicazione</strong></a></td>
<td>Nome del software utilizzato per creare la patch.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Sicurezza</strong></a></td>
<td>Il valore di questa proprietà deve essere di sola lettura.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>CodePage</strong></a></td>
<td>Valore numerico della tabella codici ANSI utilizzata per visualizzare le informazioni di riepilogo. Questa proprietà deve essere impostata prima di impostare le proprietà di stringa nelle informazioni di riepilogo.</td>
</tr>
</tbody>
</table>



 

 

 




