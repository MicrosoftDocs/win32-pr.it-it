---
description: Poiché la copia di file non necessaria rallenta un'installazione, il programma di installazione Windows determina se il file di chiave del componente è già installato prima di tentare di installare i file di qualsiasi componente.
ms.assetid: 8be734c7-4f16-4f54-93db-bb8efb1ea6da
title: Sostituzione di file esistenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fb8075aae2c7e217235eb8c84607106efe839bcbfd12ed4b658f4ed5df6182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990576"
---
# <a name="replacing-existing-files"></a>Sostituzione di file esistenti

Poiché la copia di file non necessaria rallenta un'installazione, il programma di installazione Windows determina se il file di chiave del componente è già installato prima di tentare di installare i file di qualsiasi componente. Se il programma di installazione trova un file con lo stesso nome del file di chiave del componente installato nel percorso di destinazione, confronta la versione, la data e la lingua dei due file chiave e usa le regole di controllo delle versioni dei file per determinare se installare il componente fornito dal pacchetto. Se il programma di installazione determina che deve sostituire la base del componente sul file di chiave, usa le regole di controllo delle versioni dei file in ogni file installato per determinare se sostituire il file.

Si noti che quando si crea un pacchetto di installazione con file con versione, la stringa di versione nella colonna Versione della tabella [File](file-table.md) deve essere sempre identica alla versione del file incluso nel pacchetto.

Le regole di controllo delle versioni dei file predefinite possono essere sostituite o modificate usando la [**proprietà REINSTALLMODE.**](reinstallmode.md) Il programma di installazione usa le regole di controllo delle versioni dei file specificate dalla **proprietà REINSTALLMODE** durante l'installazione, la reinstallazione o il ripristino di un file. Nell'esempio seguente viene illustrato come il programma di installazione applica le regole [di controllo delle versioni dei file predefinite.](file-versioning-rules.md) Il valore predefinito della proprietà **REINSTALLMODE** è "omus".

I file di chiave del componente seguenti vengono installati nel sistema prima della reinstallazione del componente.



| File                                    | Versione  | Data di creazione | Data ultima modifica | Linguaggio    |
|-----------------------------------------|----------|-------------|---------------|-------------|
| FileA                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileB                                   | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileC                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| Archiviato                                   | 1.0.0000 | 1/1/99      | 1/2/99        | ENG         |
| FileE                                   | Nessuno     | 1/1/99      | 1/1/99        | Nessuno        |
| FileF (> creazione)<br/> | Nessuno     | 1/1/99      | 1/2/99        | Nessuno        |
| FileG                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileH                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileI                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN     |
| FileJ                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, GER, ITN |



 

I file di chiave del componente seguenti sono inclusi nel pacchetto del programma di installazione.



| File                               | Versione  | Data di creazione | Data ultima modifica | Linguaggio    |
|------------------------------------|----------|-------------|---------------|-------------|
| FileA (contrassegnato come uguale)<br/>     | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileB (versione precedente)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileC (versione successiva)<br/>   | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileD (versione successiva)<br/>   | 2.0.0000 | 12/31/98    | 1/10/99       | Frn         |
| FileE (contrassegnato come uguale)<br/>     | Nessuno     | 1/1/99      | 1/1/99        | Nessuno        |
| FileF (nuovo file)<br/>        | Nessuno     | 1/3/99      | 1/3/99        | Nessuno        |
| FileG (nuova lingua)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | Frn         |
| FileH (nuova lingua)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | ITN, ENG, GER |
| FileI (altre lingue)<br/>  | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (meno lingue)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | Ger         |



 

I file di chiave del componente seguenti rimangono nel sistema dopo la reinstallazione del componente. Lo stato del file di chiave determina lo stato di qualsiasi altro file nel componente.



| File                | Versione  | Data di creazione | Data ultima modifica | Linguaggio    |
|---------------------|----------|-------------|---------------|-------------|
| FileA (originale)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileB (originale)    | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileC (sostituzione) | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileD (sostituzione) | 2.0.0000 | 12/31/98    | 1/10/99       | Frn         |
| FileE (sostituzione) | Nessuno     | 1/1/99      | 1/1/99        | Nessuno        |
| FileF (originale)    | Nessuno     | 1/1/99      | 1/2/99        | Nessuno        |
| FileG (sostituzione) | 1.0.0000 | 1/1/99      | 1/1/99        | Frn         |
| FileH (sostituzione) | 1.0.0000 | 1/1/99      | 1/1/99        | ITN, ENG, GER |
| FileI (sostituzione) | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (originale)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, GER, ITN |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo CRC durante un'installazione](crc-checking-during-an-installation.md)
</dt> </dl>

 

 




