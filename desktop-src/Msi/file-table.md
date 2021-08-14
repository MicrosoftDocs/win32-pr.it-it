---
description: La tabella file contiene un elenco completo dei file di origine con i vari attributi, ordinati in base a un identificatore univoco, non localizzato.
ms.assetid: 31d0e727-a9eb-4cd2-a211-ea7b138d0173
title: Tabella file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde32fd6987555b29380a81e7691c50784346bfd360f35c3f147a778b7652c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119382801"
---
# <a name="file-table"></a>Tabella file

La tabella file contiene un elenco completo dei file di origine con i vari attributi, ordinati in base a un identificatore univoco, non localizzato. I file possono essere archiviati nel supporto di origine come singoli file o compressi all'interno di [*un file CAB.*](c-gly.md) Per altre informazioni, vedere [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

La tabella File include le colonne seguenti.



| Colonna      | Tipo                               | Chiave | Nullable |
|-------------|------------------------------------|-----|----------|
| File        | [Identificatore](identifier.md)       | S   | N        |
| Componente\_ | [Identificatore](identifier.md)       | N   | N        |
| FileName    | [Filename](filename.md)           | N   | N        |
| FileSize    | [DoubleInteger](doubleinteger.md) | N   | N        |
| Versione     | [Version](version.md)             | N   | S        |
| Linguaggio    | [Lingua](language.md)           | N   | S        |
| Attributi  | [Integer](integer.md)             | N   | S        |
| Sequenza    | [Integer](integer.md)             | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>File
</dt> <dd>

Token non localizzato che identifica in modo univoco il file. Questo campo non fa distinzione tra maiuscole e minuscole. Non assegnare identificatori a file diversi che differiscono solo per la distinzione tra maiuscole e minuscole.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md). Questo campo identifica il componente che controlla il file.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

Nome file utilizzato per l'installazione. Il nome può essere localizzato.

Poiché alcuni server Web possono fare distinzione tra maiuscole e minuscole, FileName deve corrispondere esattamente alla distinzione tra maiuscole e minuscole dei file di origine per garantire il supporto dei download Internet.

</dd> <dt>

<span id="FileSize"></span><span id="filesize"></span><span id="FILESIZE"></span>Dimensione
</dt> <dd>

Dimensioni del file, in byte. Deve essere un numero non negativo.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versione
</dt> <dd>

Questo campo è la stringa di versione per un file con controllo delle versioni. Questo campo è vuoto per i file senza controllo delle versioni. La versione del file immessa in questo campo deve essere identica alla versione del file inclusa nel pacchetto di installazione.

Il campo Versione può anche essere impostato in modo da contenere la chiave primaria di un altro record nella tabella File. Il file a cui si fa riferimento determina quindi la logica di controllo delle versioni per questo file. Per altre informazioni, vedere [File complementari](companion-files.md). Si noti che se questo file è il percorso della chiave per il relativo componente, non deve essere specificato come file complementare.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Lingua
</dt> <dd>

Elenco di ID lingua decimali separati da virgole.

I file dei tipi di carattere non devono essere creati con un ID lingua, perché i tipi di carattere non hanno una risorsa ID lingua incorporata. Questa colonna deve pertanto essere lasciata null per i file dei tipi di carattere.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Intero che contiene flag di bit che rappresentano gli attributi di file.

Nella tabella seguente viene illustrata la definizione del campo di bit.



| Costante                             | Valore esadecimale | Decimal | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbFileAttributesReadOnly**      | 0x000001    | 1       | Read-Only                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **msidbFileAttributesHidden**        | 0x000002    | 2       | Nascosto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **MsidbFileAttributesSystem**        | 0x000004    | 4       | Sistema                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesVital**         | 0x000200    | 512     | Il file è fondamentale per il funzionamento accurato del componente a cui appartiene. Se l'installazione di un file con l'attributo msidbFileAttributesVital ha esito negativo, l'installazione viene interrotta e viene eseguito il rollback. In questo caso, il programma di installazione visualizza una finestra di dialogo senza un pulsante Ignora. Se questo attributo non è impostato e l'installazione del file ha esito negativo, il programma di installazione visualizza una finestra di dialogo con un pulsante Ignora. In questo caso, l'utente può scegliere di ignorare l'errore di installazione del file e continuare. <br/> |
| **msidbFileAttributesChecksum**      | 0x000400    | 1024    | Il file contiene un [*checksum valido.*](c-gly.md) È necessario un checksum per ripristinare un file danneggiato.                                                                                                                                                                                                                                                                                                                                                                                           |
| **msidbFileAttributesPatchAdded**    | 0x001000    | 4096    | Questo bit deve essere aggiunto solo da una patch e se il file viene aggiunto dalla patch.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **msidbFileAttributesNoncompressed** | 0x002000    | 8192    | Il tipo di origine del file non è compresso. Se impostata, ignorare la [**proprietà Riepilogo conteggio**](word-count-summary.md) parole. Se né **msidbFileAttributesNoncompressed** né **msidbFileAttributesCompressed** sono impostati, lo stato di compressione del file viene specificato dalla **proprietà Riepilogo** conteggio parole. Non impostare sia **msidbFileAttributesNoncompressed** che **msidbFileAttributesCompressed**.                                                                                                                            |
| **msidbFileAttributesCompressed**    | 0x004000    | 16384   | Il tipo di origine del file è compresso. Se impostata, ignorare la [**proprietà Riepilogo conteggio**](word-count-summary.md) parole. Se né **msidbFileAttributesNoncompressed** né **msidbFileAttributesCompressed** sono impostati, lo stato di compressione del file viene specificato dalla **proprietà Riepilogo** conteggio parole. Non impostare sia **msidbFileAttributesNoncompressed** che **msidbFileAttributesCompressed**.                                                                                                                              |



 

Se il bit **msidbFileAttributesVital** all'interno della colonna Attributi è impostato e se il componente a cui appartiene il file è selezionato per l'installazione, il programma di installazione deve essere in grado di installare questo file per completare correttamente l'installazione. Se il programma di installazione non è in grado di installare il file per qualche motivo (ad esempio, se il file di origine non può trovarsi all'interno dell'immagine di origine), verrà visualizzata una finestra di dialogo di errore con le opzioni "Riprova" o "Annulla". Per un file per cui non è impostato **msidbFileAttributesVital,** le opzioni in caso di errore di installazione saranno "Abort", "Retry" e "Ignore", ovvero l'utente avrà la possibilità di completare l'installazione senza installare il file.

Il bit **msidbFileAttributesChecksum** all'interno della colonna Attributi deve essere impostato per ogni file eseguibile nell'installazione con [*un checksum*](c-gly.md) valido archiviato nell'intestazione del file eseguibile portabile (PE). Solo i file con questo bit impostato verranno verificati per verificare la validità del checksum durante una reinstallazione. Per altre informazioni, vedere [**REINSTALLMODE.**](reinstallmode.md)

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Posizione della sequenza di questo file nelle immagini multimediali. Questo ordine deve corrispondere all'ordine dei file nel file CAB se i file sono compressi. I numeri interi in questo campo devono essere uguali o maggiori di 1.

I numeri di sequenza nella colonna Sequenza vengono usati per specificare sia l'ordine di installazione per i file che il supporto di origine su cui si trova il file (in combinazione con [media table).](media-table.md) Si supponga, ad esempio, che un file abbia un numero di sequenza 92. Per determinare il disco di origine in cui si trova il file, cercare nella tabella Supporti la voce con il valore più piccolo Last Sequence maggiore di 92.

Anche se ai file compressi vengono assegnati numeri di sequenza interni all'interno di file CAB, questi numeri assoluti non devono corrispondere ai numeri di sequenza all'interno della tabella File. È tuttavia importante che la sequenza di file nella tabella File sia identica alla sequenza dei file all'interno degli archivi.

Per i file non compressi, i numeri di sequenza non devono essere univoci. Ad esempio, se tutti i file non sono compressi e si trovano tutti in un disco, è possibile assegnare a tutti i file lo stesso numero di sequenza.

Il limite massimo è 32767 file. Per creare un pacchetto Windows Installer con più file, vedere [Creazione di un pacchetto di grandi dimensioni.](authoring-a-large-package.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Le [azioni InstallFiles](installfiles-action.md) [e RemoveFiles](removefiles-action.md) nelle tabelle [*sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'uso *delle tabelle di sequenza,* vedere [Using a Sequence Table](using-a-sequence-table.md).

La tabella viene inizialmente generata dall'elenco di file, ma se si usa la compressione CABINET, la tabella viene rigenerata dall'output del motore di compressione. Per altre informazioni, vedere [File CAB.](cabinet-files.md)

Per spostare un file esistente nel computer dell'utente durante l'installazione, usare [l'azione MoveFiles](movefiles-action.md) e [moveFile Table](movefile-table.md). Per installare un file in più percorsi, usare [l'azione DuplicateFiles](duplicatefiles-action.md) e [la tabella DuplicateFile](duplicatefile-table.md).

Nella tabella seguente vengono riepilogate le possibili combinazioni di valori nella colonna Versione e nella colonna Lingua . Per altre informazioni, vedere [Regole di controllo delle versioni dei file.](file-versioning-rules.md)



| Versione | Linguaggio | Descrizione                                                                     |
|---------|----------|---------------------------------------------------------------------------------|
| 1.2.3.4 | 1033     | Versione e lingua.                                                       |
| 1.2.3.4 | (Null)   | Versione ma nessun linguaggio.                                                    |
| 1.2.3.4 | 0        | La versione e la lingua sono neutre.                                           |
| Testdb  | (Null)   | File complementare a cui non è associata alcuna lingua.                         |
| Testdb  | 1033     | File e lingua complementari.                                                |
| (Null)  | 1033     | Nessuna versione, ma a essa è associata una lingua, ovvero libreria dei tipi, file della Guida. |



 

Per altre informazioni, vedere La [tabella MsiLockPermissionsEx e](msilockpermissionsex-table.md) [la tabella LockPermissions.](lockpermissions-table.md)

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

 

 




