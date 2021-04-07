---
description: Quando una tabella che contiene solo caratteri ASCII viene esportata in un file di archivio di testo, il file con estensione IDT rispetta il formato di file di archivio di base.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Dati ASCII nei file di archivio di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881109"
---
# <a name="ascii-data-in-text-archive-files"></a>Dati ASCII nei file di archivio di testo

Quando una tabella che contiene solo caratteri ASCII viene esportata in un [file di archivio di testo](text-archive-files.md), il file con estensione IDT rispetta il formato di file di [Archivio](archive-file-format.md)di base. Se la tabella contiene informazioni non ASCII, il formato del file di archivio viene esteso per includere le informazioni sulla tabella codici.

## <a name="text-archive-files-that-contain-only-ascii-characters"></a>File di archivio di testo che contengono solo caratteri ASCII

Quando una tabella che contiene solo caratteri ASCII viene esportata in un file di archivio, il file con estensione IDT si trova nel [formato di file di archivio](archive-file-format.md)di base. Ogni flusso della tabella viene esportato come file con estensione IBD. I file con estensione IBD vengono archiviati in una cartella con lo stesso nome della tabella. Si consideri, ad esempio, l'esportazione della seguente tabella [binaria](binary-table.md) .



| Nome  | Data      |
|-------|-----------|
| Libri | Libri. IBD |
| Cars  | Automobili. IBD  |



 

La struttura di directory dopo l'esportazione della tabella è la seguente. Le informazioni nella tabella di database vengono esportate in Binary. IDT. I due flussi di dati binari vengono esportati in book. IBD e Cars. IBD salvati nella cartella denominata Binary.

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

Il file di archivio Binary. IDT è nel [formato di file di archivio](archive-file-format.md) di base e avrà un aspetto simile al seguente.

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a>File di archivio di testo che contengono caratteri non ASCII

Se il file contiene dati non ASCII, il formato del [file di archivio](archive-file-format.md) di base del file con estensione IDT viene esteso per includere le informazioni sulla tabella codici. La terza riga della tabella. IDT è la tabella codici numerica seguita dal nome della tabella e dai nomi delle colonne chiave primaria separati da tabulazioni.

> [!Note]  
> Un file con estensione IDT che contiene informazioni non ASCII deve essere salvato nel formato ASCII. Un file di archivio di testo, ad esempio, può contenere i nomi di colonna e di tabella codificati come UTF-8, ma il file di archivio deve essere ASCII.

 

La tabella ActionText seguente localizzata in francese conterrebbe informazioni non ASCII. La tabella codici numerica utilizzata per le stringhe francesi è 1252.



| Azione    | Descrizione                                  | Modello |
|-----------|----------------------------------------------|----------|
| PUBBLICIZZA | Pubblicazione d'informations sur l'applicazione |          |



 

Il file di archivio esportato, ActionText. IDT, sarà il seguente.

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> Se un file di archivio di testo contiene dati non ASCII, il file di archivio include informazioni sulla tabella codici. I file di archivio con le informazioni sulla tabella codici possono essere importati di nuovo solo in un database di tale tabella codici esatta oppure in un database indipendente dalla lingua. Nel caso di un database indipendente dalla lingua, la tabella codici viene impostata sulla tabella codici del file di archivio. Per ulteriori informazioni sul modo in cui Windows Installer gestisce le tabelle codici, vedere la sezione [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md).

 

 

 



