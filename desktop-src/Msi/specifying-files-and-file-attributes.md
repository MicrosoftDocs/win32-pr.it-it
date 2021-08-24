---
description: L'installazione e la rimozione di ogni file sono determinate dal Windows programma di installazione che controlla il file.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Specifica di file e attributi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdb63bf2779ddc5730013bad06b382c168a62bab5e897d5d621f7a65644e445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893731"
---
# <a name="specifying-files-and-file-attributes"></a>Specifica di file e attributi di file

L'installazione e la rimozione di ogni file sono determinate dal [Windows programma](windows-installer-components.md) di installazione che controlla il file. Dopo aver specificato il raggruppamento delle risorse in componenti, è possibile aggiungere le informazioni sull'attributo del file al database di installazione. In questa sezione si aggiungono informazioni sul file al database di installazione per l'Blocco note esempio. Vedere file [tables group](file-tables-group.md).

I file nell'esempio Blocco note sono decompressi. Per [informazioni su come aggiungere file CAB ai](compressed-and-uncompressed-sources.md) pacchetti, vedere Origini compresse e non compresse. Questo esempio non contiene informazioni sul controllo delle versioni dei file. Per altre informazioni sul controllo delle versioni dei file, vedere [Regole di controllo delle versioni dei file](file-versioning-rules.md) e Controllo delle versioni dei file [predefinito.](default-file-versioning.md)

Usare l'editor di database per MNP2000.msi e immettere i dati seguenti nella tabella File vuota.

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

 

 



