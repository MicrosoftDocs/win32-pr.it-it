---
description: La tabella DuplicateFile contiene un elenco di file che devono essere duplicati, in una directory diversa rispetto al file originale o nella stessa directory, ma con un nome diverso. Il file originale deve essere un file installato dall'azione InstallFiles.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Tabella DuplicateFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050149"
---
# <a name="duplicatefile-table"></a>Tabella DuplicateFile

La tabella DuplicateFile contiene un elenco di file che devono essere duplicati, in una directory diversa rispetto al file originale o nella stessa directory, ma con un nome diverso. Il file originale deve essere un file installato dall' [azione InstallFiles](installfiles-action.md).

La tabella DuplicateFile include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| FileKey     | [Identificatore](identifier.md) | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | N   | N        |
| file\_      | [Identificatore](identifier.md) | N   | N        |
| DestName    | [Filename](filename.md)     | N   | S        |
| DestFolder  | [Identificatore](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey
</dt> <dd>

Una chiave primaria, un token non localizzato, che identifica un record DuplicateFile univoco.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna per la prima colonna della tabella dei [componenti](component-table.md). Se il componente identificato dalla chiave non è selezionato per l'installazione o la rimozione, non viene eseguita alcuna azione sul record DuplicateFile.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna nella [tabella file](file-table.md) che rappresenta il file originale che deve essere duplicato.

</dd> <dt>

<span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName
</dt> <dd>

Nome localizzabile da assegnare al file duplicato. Se questo campo è vuoto, al file di destinazione viene assegnato lo stesso nome del file originale.

</dd> <dt>

<span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder
</dt> <dd>

Nome di una proprietà che rappresenta il percorso completo in cui copiare il file duplicato. Se questa directory corrisponde alla directory che contiene il file originale e il nome del file duplicato proposto corrisponde a quello originale, non viene eseguita alcuna azione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La tabella viene elaborata dall' [azione DuplicateFiles](duplicatefiles-action.md) e dall' [azione RemoveDuplicateFiles](removeduplicatefiles-action.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
</dl>

 

 



