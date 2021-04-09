---
description: Quando si crea un pacchetto di installazione, è possibile usare la funzione MsiViewModify o il metodo View. Modify per assicurarsi che i dati immessi siano sintatticamente corretti.
ms.assetid: c960e9df-dcd6-44d2-8662-40a1dea81f45
title: Convalida interna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3c1a9e6f7b7e35b4d7d91287af64eff7812de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128375"
---
# <a name="internal-validation"></a>Convalida interna

Quando si crea un pacchetto di installazione, è possibile usare la funzione [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o il metodo View. Modify per assicurarsi che i dati immessi siano sintatticamente corretti. Per ulteriori informazioni, vedere [**modifica del metodo**](view-modify.md). Al livello più basso, la colonna di una tabella di database può archiviare interi (short o Long), stringhe o dati binari. Tuttavia, un pacchetto di installazione richiede interi o stringhe specifiche in determinate tabelle. Queste specifiche vengono mantenute nella [ \_ tabella di convalida](-validation-table.md). Ad esempio, la colonna FileName della [tabella file](file-table.md) è una colonna stringa, ma archivia in modo specifico un nome file. Pertanto, non solo la voce deve essere una stringa, ma deve anche seguire i requisiti per la denominazione dei file.

I vari valori enum di convalida usati con la funzione [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) consentono la convalida immediata a livelli diversi. L' \_ enumerazione del \_ Campo Validate MSIMODIFY può essere usata per convalidare i singoli campi di un record. Non convalida le chiavi esterne. L' \_ enumerazione MSIMODIFY Validate convalida un'intera riga e include la convalida della chiave esterna. Se si inserisce una nuova riga in una tabella, usare l' \_ enumerazione MSIMODIFY Validate \_ New per verificare che si stiano aggiungendo dati validi e usando chiavi primarie univoche. Un inserimento ha esito negativo se le chiavi primarie non sono univoche. Se una chiamata a **MsiViewModify** con una delle enumerazioni di convalida restituisce un errore, è possibile eseguire chiamate ripetute a [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) per la diagnosi del problema. **MsiViewGetError** indica la colonna in cui si è verificato l'errore e il valore enum per facilitare la risoluzione del problema. Per ulteriori informazioni, vedere [**metodo getError**](view-geterror.md).

È anche possibile usare la convalida interna per assicurarsi che altri autori immettano correttamente i dati nella tabella personalizzata. Aggiungere tutte le colonne della tabella personalizzata alla \_ tabella di convalida usando il nome della tabella e il nome della colonna personalizzati come chiave primaria. Fornire una descrizione o uno scopo di ogni colonna nella colonna Descrizione della \_ tabella di convalida. Immettere i requisiti applicabili per ogni colonna usando le colonne nullable, MinValue, MaxValue, DataTable, DataColumn, Category e set:

-   Se la colonna ammette valori null, immettere una "Y". In caso contrario, immettere ' n'.
-   Se la colonna è una colonna di tipo integer e può contenere un intervallo di numeri interi, immettere tale intervallo utilizzando le colonne MinValue e MaxValue.
-   Le colonne chiave esterna vengono identificate tramite le colonne chiave e colonna chiave.
-   Per le colonne di tipo stringa, specificare una categoria, ad esempio filename, GUID o Identifier. Per altre informazioni, vedere [tipi di dati di colonna](column-data-types.md).
-   Se i dati possono essere correlati solo a un numero specifico di valori (stringa o Integer), utilizzare la colonna set per elencare i valori accettabili.

Di seguito è riportato un elenco delle colonne (oltre a tabella, colonna e descrizione) nella \_ tabella di convalida che è possibile compilare se la colonna è del tipo specificato. (Si noti che non è necessario compilare tutte le colonne).



| Tipo    | Colonne                                                          |
|---------|------------------------------------------------------------------|
| Integer | Nullable, MinValue, MaxValue, tabella di tabella, colonna di colonne, set           |
| string  | Nullable, DataTable, colonna di colonna, categoria, set, MinValue, MaxValue |
| Binary  | Nullable, Category (la categoria deve essere "binary")                   |



 

Gli ambienti di creazione possono usare MSIMODIFY \_ Validate \_ Delete. Questa enumerazione presuppone che si voglia eliminare la riga. Non viene eseguita alcuna convalida del campo o della chiave esterna. Questa enumerazione esegue effettivamente una convalida della chiave esterna inversa. Consente di controllare la \_ tabella di convalida per i riferimenti nelle colonne della tabella e della colonna della tabella per la tabella a cui appartiene la riga "Deleted". Se sono presenti colonne in cui è elencata la tabella contenente la riga "eliminata" come potenziale chiave esterna, il ciclo passa a tale colonna per verificare se uno dei valori fa riferimento ai valori nella riga "eliminato". Un errore restituito indica che si interrompe l'integrità relazionale del database eliminando la riga.

 

 



