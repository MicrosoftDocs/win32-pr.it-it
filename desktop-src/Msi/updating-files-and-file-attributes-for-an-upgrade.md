---
description: Poiché l'aggiornamento aggiorna i file utilizzati dall'applicazione, è necessario modificare la tabella dei file del database.
ms.assetid: 65a7ae86-b426-4dd4-8cf5-f905dc2a1727
title: Aggiornamento di file e attributi di file per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c1d749a61376d38e8c7793ba5766dd63133bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319954"
---
# <a name="updating-files-and-file-attributes-for-an-upgrade"></a>Aggiornamento di file e attributi di file per un aggiornamento

Poiché l'aggiornamento aggiorna i file utilizzati dall'applicazione, è necessario modificare la [tabella dei file](file-table.md) del database. Usare l'editor di database Orca fornito con l'SDK o un altro editor per aprire MNP2001.msi e immettere i dati seguenti nella [tabella file](file-table.md).

[Tabella file](file-table.md)



| File         | Componente\_ | FileName     | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseba01.txt | Baseball    | Baseba01.txt | 1000     |         |          | 0          | 1        |
| Concer01.txt | Concerto     | Concer01.txt | 1000     |         |          | 0          | 1        |
| Dance01.txt  | Danza       | Dance01.txt  | 1000     |         |          | 0          | 1        |
| Opera01.txt  | Opera       | Opera01.txt  | 1000     |         |          | 0          | 1        |
| Footba01.txt | Calcio    | Footba01.txt | 1000     |         |          | 0          | 1        |
| Basket01.txt | Basket  | Basket01.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Help        | Help.txt     | 1000     |         |          | 0          | 1        |
| Januar01.txt | January     | Januar01.txt | 1000     |         |          | 0          | 1        |
| NewYea01.txt | NewYears    | NewYea01.txt | 1000     |         |          | 0          | 1        |
| Memori01.txt | Memorial    | Memori01.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Blocco note     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Blocco note     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Continua](updating-components-for-an-upgrade.md)

 

 



