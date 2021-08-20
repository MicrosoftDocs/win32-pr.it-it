---
description: Un file di archivio di testo per un database Windows Installer contiene un'estensione di file con estensione idt.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Formato file di archivio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72c7fe21b547bb5469af00dc9202d90dba3873a7ed86a6db6261a4228097a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145834"
---
# <a name="archive-file-format"></a>Formato file di archivio

Un [file di archivio di testo](text-archive-files.md) per un database Windows Installer contiene un'estensione di file con estensione idt. Quando un intero database viene esportato in file di archivio, ogni tabella del database include un file con estensione idt separato. Se una tabella contiene una colonna di flusso, ogni flusso nella tabella è rappresentato da un file con estensione ibd. I file con estensione ibd vengono archiviati in una cartella con lo stesso nome della tabella.

## <a name="idt-file-format"></a>Formato di file con estensione idt

Il file con estensione idt di una tabella di database esportata che contiene solo caratteri ASCII ha il formato di base seguente.

-   La prima riga contiene i nomi delle colonne della tabella separati da tabulazioni.
-   La seconda riga contiene le definizioni di colonna separate da tabulazioni.
-   Se il file contiene solo dati ASCII, la terza riga è il nome della tabella e i nomi delle colonne chiave primaria separati da tabulazioni.
-   Le righe rimanenti del file rappresentano le righe della tabella, con colonne separate da tabulazioni.

> [!Note]  
> Se il file contiene dati non ASCII, la terza riga è la tabella codici numerica seguita dal nome della tabella e dai nomi delle colonne chiave primaria separati da tabulazioni. Un file con estensione idt che contiene informazioni non ASCII deve essere salvato in formato ASCII. Ad esempio, un file di archivio di testo può contenere i nomi di colonna e tabella codificati come UTF-8, ma il file di archivio stesso deve essere ASCII. Vedere la sezione [Dati ASCII nei file di archivio di testo](ascii-data-in-text-archive-files.md).

 

> [!Note]  
> I file con estensione idt [ \_ ForceCodepage](-forcecodepage.md) e [ \_ SummaryInformation](-summaryinformation.md) speciali usano formati estesi. Per le descrizioni dei formati, vedere le sezioni \_ ForceCodepage e \_ SummaryInformation.

 

## <a name="column-definitions"></a>Definizioni di colonna

Le definizioni di colonna sono indicate da caratteri.

-   Il primo carattere indica il tipo di colonna. Una lettera minuscola indica una colonna non nullable e una lettera maiuscola indica che la colonna può contenere valori Null.

    | Carattere | Significato                   |
    |-----------|---------------------------|
    | s, S      | Colonna stringa             |
    | l, L      | Colonna stringa localizzabile |
    | v, V      | Colonna binaria             |
    | i, I      | Colonna Integer            |

    

     

-   Il secondo carattere indica le dimensioni dei dati della colonna.

    > [!Note]  
    > Il Windows Installer non usa effettivamente le dimensioni della colonna specificate per limitare le dimensioni della stringa che può essere immessa in un campo di colonna stringa. Tuttavia, alcuni strumenti di creazione usano le dimensioni di colonna specificate per limitare le dimensioni di una stringa valida. È consigliabile che le stringhe immesse in qualsiasi colonna soddisfino i requisiti di dimensione specificati.

     

    

    | Definizione di colonna | Significato                                    |
    |-------------------|--------------------------------------------|
    | s255              | Colonna stringa non nullable lunga 255        |
    | L50               | Colonna stringa localizzabile nullable lunga 50 |
    | i2, I2            | Colonna Short Integer                       |
    | i4, I4            | Colonna Long Integer                        |

    

     

## <a name="control-character-translation"></a>Conversione dei caratteri di controllo

L'esportazione di una tabella in un file di archivio di testo converte i caratteri di controllo per evitare conflitti con i delimitatori di file. Durante la scrittura nel file con estensione idt, i caratteri di controllo vengono convertiti come indicato di seguito.



| Carattere di controllo | Traduzione in .idt | Significato         |
|-------------------|---------------------|-----------------|
| NULL              | 21                  | Null            |
| BS                | 27                  | Spazio indietro      |
| HT                | 16                  | Scheda             |
| Se                | 25                  | avanzamento riga       |
| FF                | 24                  | Feed modulo       |
| CR                | 17                  | ritorno a capo |



 

 

 



