---
description: 'Questo esempio illustra il layout di un file con estensione cub contenente due CIEM. Il programma di installazione esegue le azioni personalizzate nella sequenza: ICE01 e ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: File Sample. cub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966637"
---
# <a name="sample-cub-file"></a>File Sample. cub

Questo esempio illustra il layout di un file con estensione cub contenente due [CIEM](internal-consistency-evaluators-ices.md). Il programma di installazione esegue le azioni personalizzate nella sequenza: ICE01 e ICE08.

L'azione personalizzata ICE01 è un' [azione personalizzata di tipo 1](custom-action-type-1.md). Si tratta di un punto di ingresso per una DLL archiviata come flusso nel file con estensione cub. Questo flusso è elencato nella tabella binaria ice.dll.

L'azione personalizzata ICE08 è un [tipo di azione personalizzata 6](custom-action-type-6.md). Si tratta di un punto di ingresso di una funzione in VBScript archiviato come flusso nel file con estensione cub. Questo flusso è elencato nella tabella binaria come ice.vbs.

[Tabella binaria](binary-table.md)



| Nome    | Data                               |
|---------|------------------------------------|
| ice.vbs | Dati binari non formattati di ice.vbs |
| ice.dll | Dati binari non formattati di ice.dll |



 

[Tabella CustomAction](customaction-table.md)



| Azione | Tipo | Source (Sorgente)  | Destinazione |
|--------|------|---------|--------|
| ICE01  | 1    | ice.dll | ICE01  |
| ICE08  | 6    | ice.vbs | ICE02  |



 

\_Tabella ICESequence



| Azione | Condizione | Sequenza |
|--------|-----------|----------|
| ICE01  |           | 10       |
| ICE08  |           | 20       |



 

\_Tabella speciale

ICE01 e ICE08 non richiedono l'inclusione di tabelle di elaborazione speciali. Quando il file con estensione cub contiene tabelle speciali, è necessario includerle anche nella \_ tabella di convalida.

[\_Tabella di convalida](-validation-table.md)



| Tabella         | Colonna    | Nullable | MinValue | MaxValue | KeyTable | KeyColumn | Category                         | Set | Descrizione |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binary        | Nome      | N        |          |          |          |           | [Identificatore](identifier.md)     |     |             |
| Binary        | Data      | N        |          |          |          |           | [Binario](binary.md)             |     |             |
| CustomAction  | Azione    | N        |          |          |          |           | [Identificatore](identifier.md)     |     |             |
| CustomAction  | Tipo      | N        |          |          |          |           | [Integer](integer.md)           |     |             |
| CustomAction  | Source (Sorgente)    | S        |          |          |          |           | [CustomSource](customsource.md) |     |             |
| CustomAction  | Destinazione    | S        |          |          |          |           | [Formattato](formatted.md)       |     |             |
| \_ICESequence | Azione    | N        |          |          |          |           | [Identificatore](identifier.md)     |     |             |
| \_ICESequence | Condizione | S        |          |          |          |           | [Condition](condition.md)       |     |             |
| \_ICESequence | Sequenza  | S        |          |          |          |           | [Integer](integer.md)           |     |             |



 

 

 



