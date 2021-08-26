---
description: Quando si crea un pacchetto di installazione, è possibile usare la funzione MsiViewModify o il metodo View.Modify per assicurarsi che i dati immessi siano sintatticamente corretti.
ms.assetid: c960e9df-dcd6-44d2-8662-40a1dea81f45
title: Convalida interna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44184a87f7d8bd28b3603d81bb83ae28ec68471e6c9c849bf9322dc5e968c886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043301"
---
# <a name="internal-validation"></a>Convalida interna

Quando si crea un pacchetto di installazione, è possibile usare la funzione [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o il metodo View.Modify per assicurarsi che i dati immessi siano sintatticamente corretti. Per altre informazioni, vedere [**Metodo Modify**](view-modify.md). Al livello più basso, la colonna di una tabella di database può archiviare numeri interi (brevi o lunghi), stringhe o dati binari. Tuttavia, un pacchetto di installazione richiede stringhe o numeri interi specifici in determinate tabelle. Queste specifiche vengono mantenute nella [ \_ tabella Di convalida](-validation-table.md). Ad esempio, la colonna FileName della tabella [File](file-table.md) è una colonna stringa, ma archivia in modo specifico un nome file. Pertanto, non solo la voce deve essere una stringa, ma deve anche seguire i requisiti per la denominazione dei file.

I vari valori di enumerazione di convalida usati con la [**funzione MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) consentono la convalida immediata a livelli diversi. L'enumerazione MSIMODIFY VALIDATE FIELD può essere usata \_ \_ per convalidare singoli campi di un record. Non convalida le chiavi esterne. L'enumerazione MSIMODIFY \_ VALIDATE convalida un'intera riga e include la convalida della chiave esterna. Se si inserisce una nuova riga in una tabella, usare l'enumerazione MSIMODIFY VALIDATE NEW per verificare l'aggiunta di dati validi e l'uso di \_ \_ chiavi primarie univoche. Un inserimento non riesce se le chiavi primarie non sono univoche. Se una chiamata a **MsiViewModify** con una delle enumerazioni di convalida restituisce un errore, è possibile effettuare chiamate ripetute a [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) per diagnosticare il problema. **MsiViewGetError** indica la colonna in cui si è verificato l'errore e il valore di enumerazione per risolvere il problema. Per altre informazioni, vedere [**Metodo GetError**](view-geterror.md).

È anche possibile usare la convalida interna per assicurarsi che altri autori immissione dei dati correttamente nella tabella personalizzata. Aggiungere ogni colonna della tabella personalizzata alla tabella Validation usando il nome della tabella personalizzata e il nome \_ della colonna come chiave primaria. Specificare una descrizione o uno scopo di ogni colonna nella colonna Descrizione della \_ tabella Convalida. Immettere i requisiti applicabili per ogni colonna usando le colonne Nullable, MinValue, MaxValue, KeyTable, KeyColumn, Category e Set:

-   Se la colonna ammette valori Null, immettere "Y". In caso contrario, immettere "N".
-   Se la colonna è una colonna integer e può contenere un intervallo di numeri interi, immettere tale intervallo usando le colonne MinValue e MaxValue.
-   Le colonne chiave esterna vengono identificate usando le colonne KeyTable e KeyColumn.
-   Per le colonne stringa, specificare una categoria, ad esempio Nome file, GUID o Identificatore. Per altre informazioni, vedere Tipi [di dati delle colonne](column-data-types.md).
-   Se i dati possono riguardare solo un numero specifico di valori (stringa o integer), usare la colonna Imposta per elencare i valori accettabili.

Di seguito è riportato un elenco delle colonne (oltre a Table, Column e Description) nella tabella Validation che possono essere compilate se la colonna è \_ del tipo specificato. Si noti che non è necessario compilare tutte le colonne.



| Tipo    | Colonne                                                          |
|---------|------------------------------------------------------------------|
| Intero | Nullable, MinValue, MaxValue, KeyTable, KeyColumn, Set           |
| string  | Nullable, KeyTable, KeyColumn, Category, Set, MinValue, MaxValue |
| Binary  | Nullable, Category (Category deve essere "Binary")                   |



 

Gli ambienti di creazione possono usare MSIMODIFY \_ VALIDATE \_ DELETE. Questa enumerazione presuppone che si voglia eliminare la riga. Non viene eseguita alcuna convalida di campo o chiave esterna. Questa enumerazione esegue effettivamente una convalida di chiave esterna inversa. Controlla la tabella validation per i riferimenti nelle colonne KeyTable e KeyColumn per la tabella a cui appartiene la \_ riga "deleted". Se sono presenti colonne che elencano la tabella che contiene la riga "deleted" come chiave esterna potenziale, scorre la colonna per verificare se uno dei valori fa riferimento ai valori nella riga "deleted". Un errore restituito significa che si interrompe l'integrità relazionale del database eliminando la riga.

 

 



