---
description: La tabella file contiene un elenco completo dei file di origine con i rispettivi attributi, ordinati in base a un identificatore univoco, non localizzato.
ms.assetid: 31d0e727-a9eb-4cd2-a211-ea7b138d0173
title: Tabella file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59838001101bbc65af50bff3f2b00b540976e4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883686"
---
# <a name="file-table"></a>Tabella file

La tabella file contiene un elenco completo dei file di origine con i rispettivi attributi, ordinati in base a un identificatore univoco, non localizzato. I file possono essere archiviati nel supporto di origine come singoli file o compressi in un [*file CAB*](c-gly.md). Per altre informazioni, vedere [uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md).

La tabella file contiene le colonne seguenti.



| Colonna      | Tipo                               | Chiave | Nullable |
|-------------|------------------------------------|-----|----------|
| File        | [Identificatore](identifier.md)       | S   | N        |
| Componente\_ | [Identificatore](identifier.md)       | N   | N        |
| FileName    | [Filename](filename.md)           | N   | N        |
| FileSize    | [DoubleInteger](doubleinteger.md) | N   | N        |
| Versione     | [Versione](version.md)             | N   | S        |
| Linguaggio    | [Lingua](language.md)           | N   | S        |
| Attributi  | [Integer](integer.md)             | N   | S        |
| Sequenza    | [Integer](integer.md)             | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>File
</dt> <dd>

Token non localizzato che identifica in modo univoco il file. Questo campo non è sensibile alla distinzione tra maiuscole e minuscole. Non assegnare identificatori a file diversi che differiscono solo per la loro distinzione tra maiuscole e minuscole.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md). Questo campo identifica il componente che controlla il file.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName
</dt> <dd>

Nome file utilizzato per l'installazione. Il nome può essere localizzato.

Poiché alcuni server Web possono fare distinzione tra maiuscole e minuscole, il nome file deve corrispondere esattamente al caso dei file di origine per garantire il supporto dei download in Internet.

</dd> <dt>

<span id="FileSize"></span><span id="filesize"></span><span id="FILESIZE"></span>FileSize
</dt> <dd>

Dimensioni del file, in byte. Deve essere un numero non negativo.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versione
</dt> <dd>

Questo campo è la stringa di versione per un file con versione. Questo campo è vuoto per i file senza versione. La versione del file immessa in questo campo deve essere identica alla versione del file inclusa nel pacchetto di installazione.

Il campo versione può essere impostato anche per contenere la chiave primaria di un altro record nella tabella file. Il file a cui si fa riferimento determina quindi la logica di controllo delle versioni per il file. Per ulteriori informazioni, vedere [file complementari](companion-files.md). Si noti che se questo file è il percorso della chiave per il componente, non deve essere specificato come file complementare.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio
</dt> <dd>

Elenco di ID di lingua decimali separati da virgole.

I file del tipo di carattere non devono essere creati con un ID lingua, perché i tipi di carattere non hanno una risorsa ID lingua incorporata. Questa colonna deve pertanto essere lasciata null per i file del tipo di carattere.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Intero contenente i flag di bit che rappresentano gli attributi del file.

Nella tabella seguente viene illustrata la definizione del campo di bit.



| Costante                             | Valore esadecimale | Decimal | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbFileAttributesReadOnly**      | 0x000001    | 1       | Read-Only                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **msidbFileAttributesHidden**        | 0x000002    | 2       | Nascosto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesSystem**        | 0x000004    | 4       | Sistema                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesVital**         | 0x000200    | 512     | Il file è essenziale per il corretto funzionamento del componente a cui appartiene. Se l'installazione di un file con l'attributo msidbFileAttributesVital ha esito negativo, l'installazione viene arrestata e ne viene eseguito il rollback. In questo caso, il programma di installazione visualizza una finestra di dialogo senza un pulsante Ignora. Se questo attributo non è impostato e l'installazione del file non riesce, il programma di installazione visualizza una finestra di dialogo con un pulsante Ignora. In questo caso, l'utente può scegliere di ignorare l'errore di installazione del file e continuare. <br/> |
| **msidbFileAttributesChecksum**      | 0x000400    | 1024    | Il file contiene un [*checksum*](c-gly.md)valido. Per ripristinare un file danneggiato, è necessario un checksum.                                                                                                                                                                                                                                                                                                                                                                                           |
| **msidbFileAttributesPatchAdded**    | 0x001000    | 4096    | Questo bit deve essere aggiunto solo da una patch e se il file viene aggiunto dalla patch.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **msidbFileAttributesNoncompressed** | 0x002000    | 8192    | Il tipo di origine del file non è compresso. Se impostato, ignorare la proprietà [**riepilogo Conteggio parole**](word-count-summary.md) . Se non è impostato né **msidbFileAttributesNoncompressed** né **msidbFileAttributesCompressed** , lo stato di compressione del file viene specificato dalla proprietà **riepilogo Conteggio parole** . Non impostare sia **msidbFileAttributesNoncompressed** che **msidbFileAttributesCompressed**.                                                                                                                            |
| **msidbFileAttributesCompressed**    | 0x004000    | 16384   | Il tipo di origine del file è compresso. Se impostato, ignorare la proprietà [**riepilogo Conteggio parole**](word-count-summary.md) . Se non è impostato né **msidbFileAttributesNoncompressed** né **msidbFileAttributesCompressed** , lo stato di compressione del file viene specificato dalla proprietà **riepilogo Conteggio parole** . Non impostare sia **msidbFileAttributesNoncompressed** che **msidbFileAttributesCompressed**.                                                                                                                              |



 

Se il bit **msidbFileAttributesVital** all'interno della colonna Attributes è impostato e se il componente a cui appartiene il file è selezionato per l'installazione, il programma di installazione deve essere in grado di installare il file affinché l'installazione venga completata correttamente. Se il programma di installazione non è in grado di installare il file per qualche motivo, ad esempio se non è possibile trovare il file di origine all'interno dell'immagine di origine, verrà visualizzata una finestra di dialogo di errore con le opzioni "Riprova" o "Annulla". Per un file in cui non è impostato **msidbFileAttributesVital** , le opzioni in caso di errore di installazione saranno "Abort", "Retry" e "ignore" (ovvero, l'utente avrà la possibilità di completare correttamente l'installazione senza installare il file).

È necessario impostare il bit **msidbFileAttributesChecksum** all'interno della colonna Attributes per ogni file eseguibile nell'installazione con un [*checksum*](c-gly.md) valido archiviato nell'intestazione del file eseguibile portabile (PE). Solo i file con questo set di bit saranno verificati per il checksum valido durante una reinstallazione. Per ulteriori informazioni, vedere [**REINSTALLMODE**](reinstallmode.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Posizione di sequenza del file nelle immagini del supporto. Questo ordine deve corrispondere all'ordine dei file nel file CAB se i file sono compressi. I numeri interi in questo campo devono essere uguali o maggiori di 1.

I numeri di sequenza nella colonna sequenza vengono utilizzati per specificare sia l'ordine di installazione per i file che il supporto di origine su cui si trova il file, insieme alla [tabella dei supporti](media-table.md). Si supponga, ad esempio, che un file disponga di un numero di sequenza pari a 92. Per determinare il disco di origine in cui si trova il file, cercare nella tabella dei supporti la voce con l'ultimo valore di sequenza più piccolo maggiore di 92.

Sebbene i file compressi siano assegnati ai numeri di sequenza interni all'interno dei cabinet, i numeri assoluti non devono corrispondere ai numeri di sequenza nella tabella file. È tuttavia importante che la sequenza di file nella tabella file sia identica alla sequenza dei file all'interno dei file CAB.

Per i file non compressi, i numeri di sequenza non devono essere univoci. Ad esempio, se tutti i file sono decompressi e tutti si trovano su un disco, è possibile assegnare a tutti i file lo stesso numero di sequenza.

Il limite massimo è 32767 file. Per creare un pacchetto di Windows Installer con più file, vedere la pagina relativa alla [creazione di un pacchetto di grandi dimensioni](authoring-a-large-package.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni [InstallFiles](installfiles-action.md) e [RemoveFiles](removefiles-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

La tabella viene inizialmente generata dall'elenco dei file, ma se si utilizza la compressione del cabinet, la tabella viene rigenerata dall'output del motore di compressione. Per ulteriori informazioni, vedere [file CAB](cabinet-files.md).

Per spostare un file esistente nel computer dell'utente durante l'installazione, usare l' [azione MoveFiles](movefiles-action.md) e la [tabella MoveFile](movefile-table.md). Per installare un file in più percorsi, usare l' [azione DuplicateFiles](duplicatefiles-action.md) e la [tabella DuplicateFile](duplicatefile-table.md).

Nella tabella seguente sono riepilogate le possibili combinazioni di valori nella colonna Version e nella colonna Language. Per altre informazioni, vedere [regole di controllo delle versioni dei file](file-versioning-rules.md).



| Versione | Linguaggio | Descrizione                                                                     |
|---------|----------|---------------------------------------------------------------------------------|
| 1.2.3.4 | 1033     | La versione e la lingua.                                                       |
| 1.2.3.4 | Null   | Versione ma nessuna lingua.                                                    |
| 1.2.3.4 | 0        | La versione e la lingua sono neutre.                                           |
| TestDB  | Null   | File complementare a cui non è associata alcuna lingua.                         |
| TestDB  | 1033     | Il file e la lingua complementari.                                                |
| Null  | 1033     | Nessuna versione, ma con un linguaggio associato (ovvero TypeLib, filelima). |



 

Per ulteriori informazioni, vedere la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) e la [tabella LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE39](ice39.md)  
[ICE42](ice42.md)  
[ICE45](ice45.md)  
[ICE50](ice50.md)  
[ICE51](ice51.md)  
[ICE54](ice54.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE60](ice60.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE76](ice76.md)  
[ICE91](ice91.md)  
</dl>

 

 




