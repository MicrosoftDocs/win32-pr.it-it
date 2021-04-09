---
description: Un file di archivio di testo per un database di Windows Installer contiene un'estensione del nome di file. IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Formato file di archivio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881114"
---
# <a name="archive-file-format"></a>Formato file di archivio

Un [file di archivio di testo](text-archive-files.md) per un database di Windows Installer contiene un'estensione del nome di file. IDT. Quando viene esportato un intero database nei file di archivio, ogni tabella nel database dispone di un file con estensione IDT separato. Se una tabella contiene una colonna di flusso, ogni flusso della tabella è rappresentato da un file con estensione IBD. I file con estensione IBD vengono archiviati in una cartella con lo stesso nome della tabella.

## <a name="idt-file-format"></a>Formato file. IDT

Il file con estensione IDT di una tabella di database esportata contenente solo caratteri ASCII presenta il formato di base seguente.

-   La prima riga contiene i nomi delle colonne di tabella separati da tabulazioni.
-   La seconda riga contiene le definizioni di colonna separate da tabulazioni.
-   Se il file contiene solo dati ASCII, la terza riga è il nome della tabella e i nomi delle colonne chiave primaria separati da tabulazioni.
-   Le righe rimanenti nel file rappresentano le righe della tabella, con colonne separate da tabulazioni.

> [!Note]  
> Se il file contiene dati non ASCII, la terza riga è la tabella codici numerica seguita dal nome della tabella e dai nomi delle colonne di chiave primaria separati da tabulazioni. Un file con estensione IDT che contiene informazioni non ASCII deve essere salvato nel formato ASCII. Un file di archivio di testo, ad esempio, può contenere i nomi di colonna e di tabella codificati come UTF-8, ma il file di archivio deve essere ASCII. Vedere la sezione [dati ASCII in file di archivio di testo](ascii-data-in-text-archive-files.md).

 

> [!Note]  
> I file [ \_ ForceCodepage](-forcecodepage.md) e [ \_ SummaryInformation](-summaryinformation.md) . IDT speciali utilizzano i formati estesi. Per le \_ \_ descrizioni dei formati, vedere le sezioni ForceCodepage e SummaryInformation.

 

## <a name="column-definitions"></a>Definizioni di colonna

Le definizioni delle colonne sono indicate da caratteri.

-   Il primo carattere indica il tipo di colonna. Una lettera minuscola indica una colonna che non ammette i valori null e una lettera maiuscola indica che la colonna può contenere valori null.

    | Carattere | Significato                   |
    |-----------|---------------------------|
    | s, S      | Colonna stringa             |
    | l, L      | Colonna stringa localizzabile |
    | v, V      | Colonna binaria             |
    | i,      | Colonna integer            |

    

     

-   Il secondo carattere indica le dimensioni dei dati della colonna.

    > [!Note]  
    > Il Windows Installer non utilizza effettivamente la dimensione della colonna specificata per limitare le dimensioni della stringa che è possibile immettere in un campo di colonna stringa. Tuttavia, alcuni strumenti di creazione utilizzano le dimensioni di colonna specificate per limitare le dimensioni di una stringa valida. È consigliabile che le stringhe immesse in una colonna soddisfino il requisito di dimensione specificato.

     

    

    | Definizione di colonna | Significato                                    |
    |-------------------|--------------------------------------------|
    | s255              | Lunghezza della colonna stringa non nullable 255        |
    | L50               | Lunghezza della colonna stringa localizzabile Nullable 50 |
    | I2, I2            | Colonna short Integer                       |
    | I4, I4            | Colonna Long Integer                        |

    

     

## <a name="control-character-translation"></a>Conversione di caratteri di controllo

L'esportazione di una tabella in un file di archivio di testo converte i caratteri di controllo in modo da evitare conflitti con i delimitatori di file. Durante la scrittura nel file con estensione IDT, i caratteri di controllo vengono convertiti come indicato di seguito.



| Carattere di controllo | Traduzione in. IDT | Significato         |
|-------------------|---------------------|-----------------|
| NULL              | 21                  | Null            |
| BS                | 27                  | Spazio indietro      |
| HT                | 16                  | Scheda             |
| Se                | 25                  | avanzamento riga       |
| FF                | 24                  | Feed form       |
| CR                | 17                  | ritorno a capo |



 

 

 



