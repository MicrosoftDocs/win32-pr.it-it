---
description: L'installazione e la rimozione di ogni file è determinata dal componente Windows Installer che controlla il file.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Specifica di file e attributi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719dacbc434d47b4074a183e67edb02a88cb3c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310794"
---
# <a name="specifying-files-and-file-attributes"></a>Specifica di file e attributi di file

L'installazione e la rimozione di ogni file è determinata dal [componente Windows Installer](windows-installer-components.md) che controlla il file. Una volta specificato il raggruppamento di risorse in componenti, è possibile aggiungere informazioni sugli attributi di file al database di installazione. In questa sezione si aggiungono informazioni sul file al database di installazione per l'esempio del blocco note. Vedere il [gruppo di tabelle di file](file-tables-group.md).

I file nell'esempio del blocco note sono decompressi. Per informazioni su come aggiungere file CAB ai pacchetti, vedere [origini compresse e non compresse](compressed-and-uncompressed-sources.md) . Questo esempio non contiene informazioni sul controllo delle versioni dei file. Per ulteriori informazioni sul controllo delle versioni dei file, vedere [regole di controllo delle versioni](file-versioning-rules.md) dei file e [controllo delle versioni dei file predefiniti](default-file-versioning.md).

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella file vuota.

[Tabella file](file-table.md)



| File         | Componente\_ | FileName     | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Baseball    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Concerto     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Danza       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Calcio    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Help        | Help.txt     | 1000     |         |          | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Blocco note     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Blocco note     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Continua](specifying-source-media.md)

 

 



