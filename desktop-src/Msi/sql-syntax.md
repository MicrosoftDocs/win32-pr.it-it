---
description: Le stringhe di query SQL per Windows Installer sono limitate ai seguenti formati.
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: Sintassi SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1b7d1179a8b6035186a9a5e78f46fdc857ac18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880861"
---
# <a name="sql-syntax"></a>Sintassi SQL

Le stringhe di query SQL per Windows Installer sono limitate ai seguenti formati.



| Azione                             | Query                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Seleziona un gruppo di record          | Selezionare \[ Distinct \] {Column-list} da {Table-List} \[ where {Operation-List} \] \[ Order by {column-List}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| Eliminare i record da una tabella        | Elimina da {Table} \[ dove {Operation-List}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Modificare i record esistenti in una tabella | AGGIORNAMENTO {Table-list} SET {Column} = {Constant} \[ , {Column} = {Constant} \] \[ ,... \] \[ Le query di aggiornamento {Operation-List} \] funzionano solo su colonne chiave non primarie.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Aggiungere record a una tabella             | INSERT INTO {TABLE} ({Column-List}) VALUEs ({Constant-List}) i \[ \] dati binari temporanei non possono essere inseriti in una tabella direttamente usando le query INSERT INTO o UPDATE SQL. Per altre informazioni, vedere [aggiunta di dati binari a una tabella con SQL](adding-binary-data-to-a-table-using-sql.md).<br/>                                                                                                                                                                                                       |
| Aggiungere una tabella                        | CREATE TABLE {Table} ({Column} {column type}) \[ \] è necessario specificare i tipi di colonna per ogni colonna durante l'aggiunta di una tabella. Per la creazione di una nuova tabella è necessario specificare almeno una colonna chiave primaria. Le sostituzioni possibili per {Column type} in precedenza sono: CHAR \[ ({Size}) \] \| character \[ ({Size}) \] \| LongChar \| short \| int \| integer \| Long \| Object \[ not null \] \[ Temporary \] \[ localizzable \] \[ , Column... \] \[ ,.. \] . Colonna chiave primaria \[ , colonna \] \[ . \] ..<br/> |
| Rimuovere una tabella                     | DROP TABLE {Table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Aggiungere una colonna                       | ALTER TABLE {TABLE} ADD {Column} {column type} il tipo di colonna deve essere specificato durante l'aggiunta di una colonna. Le sostituzioni possibili per {Column type} nella precedente sono: CHAR \[ ({Size}) \] \| character \[ ({Size}) \] \| LongChar \| short \| int \| integer \| Long \| Object \[ not null \] \[ Temporary \] \[ localizzable \] \[ \] .<br/>                                                                                                                                                                  |
| Mantieni e libera tabelle temporanee     | ALTER TABLE {nome tabella} HOLDALTER tabella {nome tabella} disponibile<br/> L'utente può usare i comandi tenendo sotto controllo la durata di una tabella temporanea o una colonna temporanea. Il numero di esenzioni in una tabella viene incrementato per ogni operazione SQL di attesa su tale tabella e decrementa per ogni operazione SQL gratuita nella tabella. Quando viene rilasciato l'ultimo conteggio delle esenzioni in una tabella, tutte le colonne temporanee diventano inaccessibili. Se tutte le colonne sono temporanee, la tabella diventa inaccessibile.<br/>     |



 

Per ulteriori informazioni, vedere [esempi di query sul database con SQL e script](examples-of-database-queries-using-sql-and-script.md).

### <a name="sql-grammar"></a>Grammatica SQL

I parametri facoltativi vengono visualizzati racchiusi tra parentesi quadre \[ \] . Quando vengono elencate diverse opzioni, i parametri facoltativi sono separati da una barra verticale.

Una {Constant} può essere una stringa o un Integer. Una stringa deve essere racchiusa tra virgolette singole "example". Un {Constant-list} è un elenco delimitato da virgole di una o più costanti.

L'opzione LOCALIZZAbile imposta un attributo di colonna che indica che la colonna deve essere localizzata.

Una {Column} è un riferimento a colonne a un valore in un campo di una tabella.

Un {marker} è un riferimento di parametro a un valore fornito da un record inviato con la query. Viene rappresentata nell'istruzione SQL da un punto interrogativo?. Per informazioni sull'uso dei parametri, vedere la funzione [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) o il metodo [**Execute**](view-execute.md) .

La sintassi di Windows Installer SQL non supporta l'escape delle virgolette singole (valore ASCII 39) in un valore letterale stringa. Tuttavia, è possibile recuperare o creare il record, impostare il campo con la proprietà [**StringData**](record-stringdata.md) o [**IntegerData**](record-integerdata.md) e quindi chiamare il metodo [**Modify**](view-modify.md) . In alternativa, è possibile creare un record e usare i marcatori di parametro (?) descritti in [**Execute**](view-execute.md) Method. Questa operazione può essere eseguita anche usando le funzioni di database [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute), [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)e [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa).

Una clausola WHERE {Operation-List} è facoltativa ed è un raggruppamento di operazioni da utilizzare per filtrare la selezione. Le operazioni devono essere dei seguenti tipi:

-   {Column} = {column}
-   {Column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {Constant}
-   {Column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {marker}
-   {Column} è null
-   {Column} non è null

Per i valori stringa sono possibili solo le operazioni = o <> . I confronti di valori oggetto sono limitati a IS NULL e IS NOT NULL.

Le singole operazioni possono essere raggruppate per operatore AND o or. L'ordinamento può essere imposto usando le parentesi ().

La clausola ORDER BY è facoltativa e causa un ritardo iniziale durante l'ordinamento. L'ordinamento in base alle stringhe consente di raggruppare stringhe identiche, ma non ordinare alfabeticamente le stringhe.

La clausola DISTINCT è facoltativa e non ripete record identici nel set di risultati restituito.

Un {Table-list} è un elenco delimitato da virgole di uno o più nomi di tabella definiti {table} nel join.

Un {Column-list} è un elenco delimitato da virgole di una o più colonne di tabella denominate {Column} selezionate. Le colonne ambigue possono essere qualificate ulteriormente come {TableName. Column}. Un asterisco può essere utilizzato come elenco di colonne in una query di selezione per rappresentare tutte le colonne nelle tabelle a cui si fa riferimento. Quando si fa riferimento ai campi in base alla posizione della colonna, selezionare le colonne in base al nome anziché utilizzare l'asterisco. Non è possibile usare un asterisco come elenco di colonne in una query INSERT INTO.

Per usare caratteri di escape per i nomi delle tabelle e delle colonne che si scontrano con le parole chiave di SQL, racchiudere il nome tra due contrassegni gravi \` \` (valore ASCII 96). Se il nome di una colonna deve essere preceduto da un carattere di escape e viene qualificato come {TableName. Column}, la tabella e la colonna devono essere sottoposte a escape singolarmente come { \` TableName \` . \` colonna \` }. È consigliabile che tutti i nomi di tabella e di colonna vengano preceduti da un carattere di escape in questo modo per evitare conflitti con parole riservate e ottenere prestazioni significative.

I nomi di tabella sono limitati a 31 caratteri. Per ulteriori informazioni, vedere [nomi di tabella](table-names.md). I nomi delle tabelle e delle colonne fanno distinzione tra maiuscole e minuscole. Le parole chiave SQL non fanno distinzione tra maiuscole e minuscole.

Il numero massimo di espressioni in una clausola WHERE di una query SQL è limitato a 32.

Sono supportati solo inner join e vengono specificati da un confronto di colonne di tabelle diverse. I join circolari non sono supportati. Un join circolare è una query SQL che collega tre o più tabelle in un circuito. Ad esempio, di seguito è riportato un join circolare:

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

Le colonne che fanno parte delle chiavi primarie per una tabella devono essere definite prima in ordine di priorità, seguite da eventuali colonne chiave non primarie. Le colonne permanenti devono essere definite prima delle colonne temporanee. La sequenza di ordinamento di una colonna di testo non è definita. Tuttavia, i valori di testo identici vengono sempre raggruppati insieme.

Si noti che quando si aggiunge o si crea una colonna, è necessario specificare il tipo di colonna.

Le tabelle non possono contenere più di una colonna di tipo ' Object '.

La dimensione massima che può essere specificata in modo esplicito per una colonna stringa in una query SQL è 255. Una colonna stringa di lunghezza infinita viene rappresentata con dimensioni pari a 0. Per altre informazioni, vedere [formato della definizione di colonna](column-definition-format.md).

Per eseguire qualsiasi istruzione SQL, è necessario creare una vista. Tuttavia, non è possibile utilizzare una vista che non crea un set di risultati, ad esempio CREATE TABLE o INSERT INTO, con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o con il metodo [**Modify**](view-modify.md) per aggiornare le tabelle tramite la vista.

Si noti che non è possibile recuperare un record contenente dati binari da un database e quindi usare tale record per inserire i dati in un database completamente diverso. Per spostare i dati binari da un database a un altro, è necessario esportare i dati in un file e quindi importarli nel nuovo database tramite una query e la funzione [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) . In questo modo si garantisce che ogni database disponga di una propria copia dei dati binari.

 

 




