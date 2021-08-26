---
description: MsiViewGetColumnInfo e la proprietà ColumnInfo dell'oggetto View usano il formato seguente per descrivere le definizioni delle colonne di database.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Formato definizione colonna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f0fcad09d0c87b766022602b152c09f466b4d6cddc87467b89ff02793240b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077921"
---
# <a name="column-definition-format"></a>Formato definizione colonna

[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) e la [**proprietà ColumnInfo dell'oggetto**](view-columninfo.md) [**View**](view-object.md) usano il formato seguente per descrivere le definizioni delle colonne di database. Ogni colonna è descritta da una stringa nel campo di record corrispondente restituito dalla funzione o dalla proprietà . La stringa di definizione è costituita da una singola lettera che rappresenta il tipo di dati seguito dalla larghezza della colonna (in caratteri, se applicabile, byte in caso contrario). Una larghezza pari a zero definisce una larghezza illimitata, ad esempio flussi e campi di testo lunghi. Una lettera maiuscola indica che nella colonna sono consentiti valori Null.



| Descrittore di colonna | Stringa di definizione                 |
|-------------------|-----------------------------------|
| s?                | Stringa, lunghezza variabile (?=1-255) |
| s0                | Stringa, lunghezza variabile           |
| i2                | Short Integer                     |
| i4                | Long integer                      |
| v0                | Flusso binario                     |
| G?                | Stringa temporanea (?=0-255)        |
| J?                | Intero temporaneo (?=0,1,2,4)     |
| O0                | Oggetto temporaneo                  |



 

Le stringhe usate per descrivere le colonne hanno la relazione seguente con le SQL query usate da CREATE e ALTER. Per altre informazioni, vedere [Sintassi SQL.](sql-syntax.md)



| Valore restituito | Sintassi SQL                |
|----------------|---------------------------|
| s0             | LONGCHAR                  |
| l0             | LONGCHAR LOCALIZABLE      |
| s \#           | CHAR( \# )                  |
| s \#           | CHARACTER( \# )             |
| L \#           | CHAR( \# ) LOCALIZZABILE      |
| L \#           | CHARACTER( \# ) LOCALIZABLE |
| i2             | SHORT                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| v0             | OBJECT                    |



 

Se la lettera non viene scritta in maiuscolo, SQL'istruzione deve essere aggiunta con NOT NULL.



| Valore restituito | Sintassi SQL        |
|----------------|-------------------|
| s0             | LONGCHAR NOT NULL |



 

Il programma di installazione non limita internamente la lunghezza delle colonne al valore specificato dal formato di definizione della colonna. Se i dati immessi in un campo superano la lunghezza di colonna specificata, il pacchetto non riesce a superare la convalida [del pacchetto](package-validation.md). Per superare la convalida in questo caso, è necessario modificare i dati o lo schema del database. L'unico modo per modificare la lunghezza di colonna di una tabella standard è esportare la tabella usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), modificare il file con estensione idt esportato e quindi importare la tabella [**usando MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Gli autori non possono modificare i tipi di dati delle colonne, il supporto dei valori Null o gli attributi di localizzazione di qualsiasi colonna nelle tabelle standard. Gli autori possono creare tabelle personalizzate con colonne con attributi di colonna.

Quando si [**usa MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) per unire un database di riferimento in un database di destinazione, i nomi delle colonne, il numero di chiavi primarie e i tipi di dati delle colonne devono corrispondere. **MsiDatabaseMerge ignora** gli attributi di localizzazione e lunghezza della colonna. Se una colonna nel database di riferimento ha una lunghezza pari a 0 o maggiore della lunghezza della colonna nel database di destinazione, **MsiDatabaseMerge** aumenta la lunghezza della colonna nel database di destinazione fino alla lunghezza nel database di riferimento.

Quando si Mergmod.dll versione 2.0, l'applicazione di un modulo di merge a un file .msi non modifica mai la lunghezza delle colonne o i tipi di colonna di una tabella di database esistente. L'applicazione di un modulo unione può tuttavia modificare lo schema di una tabella di database esistente se il modulo aggiunge nuove colonne a una tabella per cui è possibile aggiungere colonne. Quando si usa una versione Mergemod.dll precedente alla versione 2.0, l'applicazione di un modulo di merge non modifica mai la lunghezza delle colonne e non modifica mai lo schema del database di destinazione.

 

 



