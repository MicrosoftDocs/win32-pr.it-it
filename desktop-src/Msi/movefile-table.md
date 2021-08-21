---
description: Questa tabella contiene un elenco di file da spostare o copiare da una directory di origine specificata a una directory di destinazione specificata.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Tabella MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d90afe8a5fb950f2e6fdb96ba0f8af4f8969226a5dc219bc9cd0598481beb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945096"
---
# <a name="movefile-table"></a>Tabella MoveFile

Questa tabella contiene un elenco di file da spostare o copiare da una directory di origine specificata a una directory di destinazione specificata.

La tabella MoveFile include le colonne seguenti.



| Colonna       | Tipo                         | Chiave | Nullable |
|--------------|------------------------------|-----|----------|
| FileKey      | [Identificatore](identifier.md) | S   | N        |
| Componente\_  | [Identificatore](identifier.md) | N   | N        |
| SourceName   | [Text](text.md)             | N   | S        |
| DestName     | [Filename](filename.md)     | N   | S        |
| SourceFolder | [Identificatore](identifier.md) | N   | S        |
| DestFolder   | [Identificatore](identifier.md) | N   | N        |
| Opzioni      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Chiave primaria che identifica in modo univoco un record MoveFile specifico.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella [tabella Component](component-table.md). Se il componente a cui fa riferimento questa chiave non è selezionato per l'installazione o la rimozione, non viene eseguita alcuna azione su questa voce MoveFile.

</dd> <dt>

<span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName
</dt> <dd>

Questa colonna contiene il nome localizzabile dei file di origine da spostare o copiare. Questa colonna può essere lasciata vuota. Vedere la descrizione della colonna SourceFolder. Questo campo deve contenere un nome file lungo e può contenere caratteri jolly ( \* e ?).

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

Questa colonna contiene il nome localizzabile da assegnare al file originale dopo lo spostamento o la copia. Se questo campo è vuoto, al file di destinazione viene assegnato lo stesso nome del file di origine.

</dd> <dt>

<span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder
</dt> <dd>

Questa colonna contiene il nome di una proprietà con un valore che viene risolto nel percorso completo della directory di origine. Se la colonna SourceName viene lasciata vuota, si presuppone che la proprietà denominata nella colonna SourceFolder contenga il percorso completo del file di origine (incluso il nome del file).

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>CartellaDest
</dt> <dd>

Nome di una proprietà il cui valore viene risolto nel percorso completo della directory di destinazione.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opzioni
</dt> <dd>

Valore intero che specifica la modalità operativa.



| Costante                     | Valore esadecimale | Decimal | Significato               |
|------------------------------|-------------|---------|-----------------------|
| (nessuna)                       | 0x000       | 0       | Copiare il file di origine. |
| **msidbMoveFileOptionsMove** | 0x001       | 1       | Spostare il file di origine. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se viene immesso un carattere jolly " " nella colonna SourceName della tabella MoveFile e viene specificato un nome di file di destinazione nella colonna DestName, tutti i file spostati o copiati mantengono i nomi nelle \* origini.

Questa tabella viene elaborata [dall'azione MoveFiles](movefiles-action.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE85](ice85.md)  
</dl>

 

 



