---
description: MsiViewGetColumnInfo e la Proprietà ColumnInfo dell'oggetto View utilizzano il formato seguente per descrivere le definizioni delle colonne del database.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Formato della definizione di colonna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231885"
---
# <a name="column-definition-format"></a>Formato della definizione di colonna

[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) e la [**Proprietà ColumnInfo**](view-columninfo.md) dell'oggetto [**View**](view-object.md) utilizzano il formato seguente per descrivere le definizioni delle colonne del database. Ogni colonna è descritta da una stringa nel campo record corrispondente restituito dalla funzione o dalla proprietà. La stringa di definizione è costituita da una singola lettera che rappresenta il tipo di dati seguito dalla larghezza della colonna (in caratteri se applicabile, in caso contrario, byte). Uno spessore pari a zero indica una larghezza senza limiti (ad esempio, campi di testo lunghi e flussi). Una lettera maiuscola indica che nella colonna sono consentiti valori null.



| Descrittore di colonna | Stringa di definizione                 |
|-------------------|-----------------------------------|
| s?                | Stringa, lunghezza variabile (? = 1-255) |
| S0                | Stringa, lunghezza variabile           |
| i2                | Valore short Integer                     |
| i4                | Long integer                      |
| V0                | Flusso binario                     |
| g?                | Stringa temporanea (? = 0-255)        |
| j?                | Integer temporaneo (? = 0, 1, 2, 4)     |
| O0                | Oggetto temporaneo                  |



 

Le stringhe utilizzate per descrivere le colonne hanno la seguente relazione con le stringhe di query SQL utilizzate da CREATE e ALTER. Per altre informazioni, vedere [sintassi SQL](sql-syntax.md).



| Valore restituito | Sintassi SQL                |
|----------------|---------------------------|
| S0             | LONGCHAR                  |
| L0             | LONGCHAR LOCALIZZABILE      |
| s \#           | CHAR ( \# )                  |
| s \#           | CARATTERE ( \# )             |
| l \#           | CHAR ( \# ) localizzabile      |
| l \#           | CHARACTER ( \# ) localizzabile |
| i2             | SHORT                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| V0             | OBJECT                    |



 

Se la lettera non è in maiuscolo, l'istruzione SQL deve essere aggiunta con NOT NULL.



| Valore restituito | Sintassi SQL        |
|----------------|-------------------|
| S0             | LONGCHAR NOT NULL |



 

Il programma di installazione non limita internamente la lunghezza delle colonne al valore specificato dal formato di definizione della colonna. Se i dati immessi in un campo superano la lunghezza della colonna specificata, il pacchetto non supera la [convalida del pacchetto](package-validation.md). Per passare la convalida in questo caso, è necessario modificare i dati o lo schema del database. Per modificare la lunghezza di colonna di una tabella standard è sufficiente esportare la tabella utilizzando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), modificare il file IDT esportato e quindi importare la tabella utilizzando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Gli autori non possono modificare i tipi di dati delle colonne, i valori null o gli attributi di localizzazione di tutte le colonne nelle tabelle standard. Gli autori possono creare tabelle personalizzate con colonne con qualsiasi attributo di colonna.

Quando si utilizza [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) per unire un database di riferimento in un database di destinazione, i nomi delle colonne, il numero di chiavi primarie e i tipi di dati di colonna devono corrispondere. **MsiDatabaseMerge** ignora gli attributi di localizzazione e di lunghezza della colonna. Se una colonna nel database di riferimento ha una lunghezza maggiore o uguale a 0 rispetto alla lunghezza della colonna nel database di destinazione, **MsiDatabaseMerge** aumenta la lunghezza della colonna nel database di destinazione fino alla lunghezza del database di riferimento.

Quando si usa Mergmod.dll versione 2,0, l'applicazione di un modulo merge a un file con estensione msi non modifica mai la lunghezza delle colonne o i tipi di colonna di una tabella di database esistente. L'applicazione di un modulo merge può tuttavia modificare lo schema di una tabella di database esistente se il modulo aggiunge nuove colonne a una tabella per cui è valida aggiungere colonne. Quando si utilizza una versione di Mergemod.dll inferiore alla versione 2,0, l'applicazione di un modulo merge non modifica mai la lunghezza delle colonne e non modifica mai lo schema del database di destinazione.

 

 



