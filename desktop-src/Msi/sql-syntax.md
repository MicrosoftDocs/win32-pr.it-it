---
description: Le SQL di query per Windows Installer sono limitate ai formati seguenti.
ms.assetid: badee528-fa69-43ab-965e-d9e6f2529b99
title: Sintassi SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6512f52ae687ee3f95a00f104c7cdfa251c878b649809faeb86c73bdcf82bf84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624675"
---
# <a name="sql-syntax"></a>Sintassi SQL

Le SQL di query per Windows Installer sono limitate ai formati seguenti.



| Azione                             | Query                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selezionare un gruppo di record          | SELECT \[ DISTINCT \] {column-list} FROM {table-list} \[ WHERE {operation-list} \] \[ ORDER BY {column-list}\]                                                                                                                                                                                                                                                                                                                                                                                                       |
| Eliminare record da una tabella        | DELETE FROM {table} \[ WHERE {operation-list}\]                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Modificare i record esistenti in una tabella | UPDATE {table-list} SET {column}= {constant}, \[ {column}= {constant} \] \[ , ... \] \[ Where {operation-list} UPDATE query work only on nonprimary key columns( WHERE {operation-list} \] UPDATE query work only on nonprimary key columns.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Aggiungere record a una tabella             | INSERT INTO {table} ({column-list}) VALUES ({constant-list}) TEMPORARY Binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL \[ \] query. Per altre informazioni, vedere [Aggiunta di dati binari a una tabella usando SQL](adding-binary-data-to-a-table-using-sql.md).<br/>                                                                                                                                                                                                       |
| Aggiungere una tabella                        | CREATE TABLE {table} ( {column} {column type}) Hold I tipi di colonna HOLD devono essere specificati per ogni colonna quando si \[ \] aggiunge una tabella. È necessario specificare almeno una colonna chiave primaria per la creazione di una nuova tabella. Le possibili sostituzioni per {tipo di colonna} in precedenza sono: CHAR \[ ( {size} ) \] \| CHARACTER ( \[ {size} ) \] \| LONGCHAR \| SHORT INT LONG OBJECT NOT NULL \| TEMPORARY \| \| \| \[ \] \[ \] \[ LOCALIZABLE \] \[ , column... \] \[ , ... \] Colonna PRIMARY \[ KEY, colonna \] \[ , ... \] .<br/> |
| Rimuovere una tabella                     | DROP TABLE {table}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Aggiungere una colonna                       | ALTER TABLE {table} ADD {column} {column type}Il tipo di colonna deve essere specificato quando si aggiunge una colonna. Le possibili sostituzioni per {tipo di colonna} in precedenza sono: CHAR \[ ( {size} ) \] \| CHARACTER ( \[ {size} ) \] \| LONGCHAR \| SHORT INT INTEGER LONG OBJECT NOT NULL \| TEMPORARY \| \| \| \[ \] \[ \] \[ LOCALIZABLE \] \[ HOLD \] .<br/>                                                                                                                                                                  |
| Contenere e liberare tabelle temporanee     | ALTER TABLE {nome tabella} HOLDALTER TABLE {nome tabella} FREE<br/> L'utente può usare i comandi HOLD e FREE per controllare l'intervallo di vita di una tabella temporanea o di una colonna temporanea. Il conteggio di blocco per una tabella viene incrementato per ogni operazione HOLD SQL tale tabella e decrementato per ogni SQL free sulla tabella. Quando viene rilasciato l'ultimo conteggio di blocco in una tabella, tutte le colonne temporanee diventano inaccessibili. Se tutte le colonne sono temporanee, la tabella diventa inaccessibile.<br/>     |



 

Per altre informazioni, vedere [Esempi di query di database con SQL e script](examples-of-database-queries-using-sql-and-script.md).

### <a name="sql-grammar"></a>Grammatica SQL

I parametri facoltativi vengono visualizzati racchiusi tra parentesi \[ \] quadre. Quando sono elencate diverse opzioni, i parametri facoltativi sono separati da una barra verticale.

{constant} è una stringa o un numero intero. Una stringa deve essere racchiusa tra virgolette singole 'example'. {constant-list} è un elenco delimitato da virgole di una o più costanti.

L'opzione LOCALIZABLE imposta un attributo di colonna che indica che la colonna deve essere localizzata.

{column} è un riferimento a colonne a un valore in un campo di una tabella.

{marker} è un riferimento di parametro a un valore fornito da un record inviato con la query. È rappresentato nell'istruzione SQL da un punto interrogativo ?. Per informazioni sull'uso dei parametri, vedere la [**funzione MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) o il [**metodo Execute.**](view-execute.md)

La Windows installer SQL non supporta l'escape delle virgolette singole (valore ASCII 39) in un valore letterale stringa. È tuttavia possibile recuperare o creare il record, impostare il campo con la [**proprietà StringData**](record-stringdata.md) o [**IntegerData**](record-integerdata.md) e quindi chiamare il [**metodo Modify.**](view-modify.md) In alternativa, è possibile creare un record e usare i marcatori di parametro (?) descritti nel [**metodo Execute.**](view-execute.md) A tale scopo, è anche possibile usare le funzioni di database [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute), [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)e [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa).

Una clausola WHERE {operation-list} è facoltativa ed è un raggruppamento di operazioni da usare per filtrare la selezione. Le operazioni devono essere dei tipi seguenti:

-   {column} = {column}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {constant}
-   {column} = \|  <>  \|  >  \|  <  \|  >=  \| <= {marker}
-   {column} è Null
-   {column} non è Null

Per i valori stringa, sono possibili solo le operazioni di <> = o . I confronti tra valori di oggetto sono limitati a IS NULL e IS NOT NULL.

Le singole operazioni possono essere raggruppate in base agli operatori AND o OR. L'ordinamento può essere imposto tramite parentesi ( ).

La clausola ORDER BY è facoltativa e causa un ritardo iniziale durante l'ordinamento. L'ordinamento in base alle stringhe raggruppa stringhe identiche, ma non le raggruppa in ordine alfabetico.

La clausola DISTINCT è facoltativa e non ripete record identici nel set di risultati restituito.

{table-list} è un elenco delimitato da virgole di uno o più nomi di tabella definiti {table} nel join.

{column-list} è un elenco delimitato da virgole di una o più colonne di tabella denominate {column} selezionate. Le colonne ambigue possono essere ulteriormente qualificate come {tablename.column}. Un asterisco può essere usato come elenco di colonne in una query SELECT per rappresentare tutte le colonne nelle tabelle di riferimento. Quando si fa riferimento ai campi in base alla posizione della colonna, selezionare le colonne in base al nome anziché usare l'asterisco. Non è possibile usare un asterisco come elenco di colonne in una query INSERT INTO.

Per eseguire l'escape dei nomi di tabella e dei nomi di colonna che SQL parole chiave, racchiudere il nome tra due accenti accentati gravi \` \` (valore ASCII 96). Se un nome di colonna deve essere preceduto da caratteri di escape ed è qualificato come {tablename.column}, la tabella e la colonna devono essere precedute singolarmente da { \` tablename \` . \` colonna \` }. È consigliabile utilizzare l'escape di tutti i nomi di tabella e di colonna in questo modo per evitare conflitti con parole riservate e ottenere prestazioni significative.

I nomi di tabella sono limitati a 31 caratteri. Per altre informazioni, vedere [Nomi di tabella](table-names.md). Per i nomi di tabella e colonna viene fatto distinzione tra maiuscole e minuscole. SQL parole chiave non fa distinzione tra maiuscole e minuscole.

Il numero massimo di espressioni in una clausola WHERE di una query SQL è limitato a 32.

Sono supportati solo inner join e vengono specificati da un confronto di colonne di tabelle diverse. I join circolari non sono supportati. Un join circolare è una SQL che collega tre o più tabelle in un circuito. Ad esempio, di seguito è riportato un join circolare:

``` syntax
WHERE Table1.Field1=Table2.Field1 AND Table2.Field2=Table3.Field1 AND Table3.Field2=Table1.Field2.
```

Le colonne che fanno parte delle chiavi primarie per una tabella devono essere definite per prime in ordine di priorità, seguite da eventuali colonne chiave non primaria. Le colonne persistenti devono essere definite prima delle colonne temporanee. La sequenza di ordinamento di una colonna di testo non è definita. Tuttavia, i valori di testo identici vengono sempre raggruppati.

Si noti che quando si aggiunge o si crea una colonna, è necessario specificare il tipo di colonna.

Le tabelle non possono contenere più di una colonna di tipo 'object'.

La dimensione massima che può essere specificata in modo esplicito per una colonna stringa in una SQL query è 255. Una colonna stringa di lunghezza infinita viene rappresentata con dimensioni 0. Per altre informazioni, vedere [Formato definizione colonna](column-definition-format.md).

Per eseguire qualsiasi SQL, è necessario creare una vista. Tuttavia, una vista che non crea un set di risultati, ad esempio CREATE TABLE o INSERT INTO, non può essere usata con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o il metodo [**Modify**](view-modify.md) per aggiornare le tabelle tramite la vista.

Si noti che non è possibile recuperare un record contenente dati binari da un database e quindi usarlo per inserire i dati in un database completamente diverso. Per spostare dati binari da un database a un altro, è necessario esportare i dati in un file e quindi importarlo nel nuovo database tramite una query e la [**funzione MsiRecordSetStream.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) Ciò garantisce che ogni database abbia una propria copia dei dati binari.

 

 




