---
description: Poiché la copia di file non necessaria rallenta un'installazione, il Windows Installer determina se il file di chiave del componente è già installato prima di tentare di installare i file di qualsiasi componente.
ms.assetid: 8be734c7-4f16-4f54-93db-bb8efb1ea6da
title: Sostituzione dei file esistenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b3908749e5496e4be9bf0ff68c7038a9ea6573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882717"
---
# <a name="replacing-existing-files"></a>Sostituzione dei file esistenti

Poiché la copia di file non necessaria rallenta un'installazione, il Windows Installer determina se il file di chiave del componente è già installato prima di tentare di installare i file di qualsiasi componente. Se il programma di installazione trova un file con lo stesso nome del file di chiave del componente installato nel percorso di destinazione, confronta la versione, la data e la lingua dei due file chiave e usa le regole di controllo delle versioni dei file per determinare se installare il componente fornito dal pacchetto. Se il programma di installazione stabilisce che è necessario sostituire la base del componente sul file di chiave, USA le regole di controllo delle versioni dei file per ogni file installato per determinare se sostituire il file.

Si noti che quando si crea un pacchetto di installazione con file con versione, la stringa di versione nella colonna versione della [tabella file](file-table.md) deve essere sempre identica alla versione del file inclusa nel pacchetto.

È possibile eseguire l'override o la modifica delle regole di controllo delle versioni dei file predefinite tramite la proprietà [**REINSTALLMODE**](reinstallmode.md) . Il programma di installazione usa le regole di controllo delle versioni dei file specificate dalla proprietà **REINSTALLMODE** durante l'installazione, la reinstallazione o il ripristino di un file. Nell'esempio seguente viene illustrato come il programma di installazione applica le [regole di controllo delle versioni dei file](file-versioning-rules.md)predefinite. Il valore predefinito della proprietà **REINSTALLMODE** è "omus".

I seguenti file di chiave del componente sono installati nel sistema prima che il componente venga reinstallato.



| File                                    | Versione  | Data di creazione | Data ultima modifica | Linguaggio    |
|-----------------------------------------|----------|-------------|---------------|-------------|
| FileA                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileB                                   | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileC                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| Campo                                   | 1.0.0000 | 1/1/99      | 1/2/99        | ENG         |
| File                                   | Nessuno     | 1/1/99      | 1/1/99        | Nessuno        |
| FileF (modificato > creare)<br/> | Nessuno     | 1/1/99      | 1/2/99        | Nessuno        |
| FileG                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileH                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| File                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN     |
| FileJ                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, GER, ITN |



 

I seguenti file di chiave del componente sono inclusi nel pacchetto del programma di installazione.



| File                               | Versione  | Data di creazione | Data ultima modifica | Linguaggio    |
|------------------------------------|----------|-------------|---------------|-------------|
| Filea (contrassegnato come uguale)<br/>     | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileB (versione precedente)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileC (versione successiva)<br/>   | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| Archiviato (versione successiva)<br/>   | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| File (contrassegnato come uguale)<br/>     | Nessuno     | 1/1/99      | 1/1/99        | Nessuno        |
| FileF (nuovo file)<br/>        | Nessuno     | 1/3/99      | 1/3/99        | Nessuno        |
| FileG (nuovo linguaggio)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (nuovo linguaggio)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | ITN, ITA, GER |
| Filei (altre lingue)<br/>  | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (meno lingue)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | GER         |



 

I seguenti file di chiave del componente sono rimasti nel sistema dopo la reinstallazione del componente. Lo stato del file di chiave determina lo stato di tutti gli altri file nel componente.



| File                | Versione  | Data di creazione | Data ultima modifica | Linguaggio    |
|---------------------|----------|-------------|---------------|-------------|
| Filea (originale)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileB (originale)    | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileC (sostituzione) | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| Archiviato (sostituzione) | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| File (sostituzione) | Nessuno     | 1/1/99      | 1/1/99        | Nessuno        |
| FileF (originale)    | Nessuno     | 1/1/99      | 1/2/99        | Nessuno        |
| FileG (sostituzione) | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (sostituzione) | 1.0.0000 | 1/1/99      | 1/1/99        | ITN, ITA, GER |
| Filei (sostituzione) | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (originale)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, GER, ITN |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica CRC durante un'installazione](crc-checking-during-an-installation.md)
</dt> </dl>

 

 




