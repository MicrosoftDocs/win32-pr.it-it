---
description: Quando una tabella che contiene solo caratteri ASCII viene esportata in un file di archivio di testo, il file con estensione idt è conforme al formato di file di archivio di base.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Dati ASCII nei file di archivio di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7fa327d19b59793862bd2c06ce814b17979e8e8a6f72d41b1af677b715b4ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078071"
---
# <a name="ascii-data-in-text-archive-files"></a>Dati ASCII nei file di archivio di testo

Quando una tabella che contiene solo caratteri ASCII viene esportata in un file di archivio di testo, il [file](text-archive-files.md)con estensione idt è conforme al formato di [file di archivio di base](archive-file-format.md). Se la tabella contiene informazioni non ASCII, il formato del file di archivio viene esteso per includere le informazioni della tabella codici.

## <a name="text-archive-files-that-contain-only-ascii-characters"></a>File di archivio di testo che contengono solo caratteri ASCII

Quando una tabella che contiene solo caratteri ASCII viene esportata in un file di archivio, il file con estensione idt è nel formato di [file di archivio di base](archive-file-format.md). Ogni flusso nella tabella viene esportato come file con estensione ibd. I file con estensione ibd vengono archiviati in una cartella con lo stesso nome della tabella. Si consideri ad esempio l'esportazione della [tabella Binaria](binary-table.md) seguente.



| Nome  | Dati      |
|-------|-----------|
| Libri | Books.ibd |
| Cars  | Cars.ibd  |



 

La struttura di directory dopo l'esportazione di questa tabella è la seguente. Le informazioni nella tabella di database vengono esportate in Binary.idt. I due flussi di dati binari vengono esportati in Book.ibd e Cars.ibd salvati nella cartella denominata Binary.

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

Il file di archivio Binary.idt è nel formato di [file di archivio di base](archive-file-format.md) e sarà simile al seguente.

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a>File di archivio di testo contenenti caratteri non ASCII

Se il file contiene dati non ASCII, il formato di file di [archivio](archive-file-format.md) di base del file con estensione idt viene esteso per includere informazioni sulla tabella codici. La terza riga della tabella con estensione idt è la tabella codici numerica seguita dal nome della tabella e dai nomi delle colonne chiave primaria separati da tabulazioni.

> [!Note]  
> Un file con estensione idt che contiene informazioni non ASCII deve essere salvato in formato ASCII. Ad esempio, un file di archivio di testo può contenere i nomi di colonna e tabella codificati come UTF-8, ma il file di archivio stesso deve essere ASCII.

 

La tabella ActionText seguente localizzata in francese conterrà informazioni non ASCII. La tabella codici numerica usata per le stringhe in francese è 1252.



| Azione    | Descrizione                                  | Modello |
|-----------|----------------------------------------------|----------|
| PUBBLICIZZA | Pubblicazione d'informations sur l'application |          |



 

Il file di archivio esportato, ActionText.idt, sarà il seguente.

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> Se un file di archivio di testo contiene dati non ASCII, il file di archivio include informazioni sulla tabella codici. I file di archivio con informazioni sulla tabella codici possono essere importati solo in un database di tale tabella codici esatta o in un database indipendente dal linguaggio. Nel caso di un database indipendente dal linguaggio, la tabella codici viene impostata sulla tabella codici del file di archivio. Per altre informazioni sul modo in cui Windows installer gestisce le code pages, vedere la sezione [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).

 

 

 



