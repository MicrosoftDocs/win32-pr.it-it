---
description: 'Questo esempio illustra il layout di un file con estensione cub contenente due ICE. Il programma di installazione esegue le azioni personalizzate nella sequenza: ICE01 e ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: File con estensione cub di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7aadbaca8bde7091f38d5ce8ccc39926ec6c595aa33e65e488136e89cccfc81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039661"
---
# <a name="sample-cub-file"></a>File con estensione cub di esempio

In questo esempio viene illustrato il layout di un file con estensione cub contenente due [ICE.](internal-consistency-evaluators-ices.md) Il programma di installazione esegue le azioni personalizzate nella sequenza: ICE01 e ICE08.

L'azione personalizzata ICE01 è [un'azione personalizzata di tipo 1.](custom-action-type-1.md) Si tratta di un punto di ingresso a una DLL archiviata come flusso nel file con estensione cub. Questo flusso è elencato nella tabella binaria ice.dll.

L'azione personalizzata ICE08 è [un'azione personalizzata di tipo 6.](custom-action-type-6.md) Si tratta di un punto di ingresso a una funzione in VBScript archiviata come flusso nel file con estensione cub. Questo flusso è elencato nella tabella binaria come ice.vbs.

[Tabella binaria](binary-table.md)



| Nome    | Dati                               |
|---------|------------------------------------|
| ice.vbs | Dati binari non formattati di ice.vbs |
| ice.dll | Dati binari non formattati di ice.dll |



 

[Tabella CustomAction](customaction-table.md)



| Azione | Tipo | Source (Sorgente)  | Destinazione |
|--------|------|---------|--------|
| ICE01  | 1    | ice.dll | ICE01  |
| ICE08  | 6    | ice.vbs | ICE02  |



 

\_Tabella ICESequence



| Azione | Condition | Sequenza |
|--------|-----------|----------|
| ICE01  |           | 10       |
| ICE08  |           | 20       |



 

\_Tabella speciale

ICE01 e ICE08 non richiedono l'inclusione di tabelle di elaborazione speciali. Quando il file con estensione cub contiene tabelle speciali, devono essere incluse anche nella \_ tabella di convalida.

[\_Tabella di convalida](-validation-table.md)



| Tabella         | Colonna    | Nullable | Minvalue | MaxValue | KeyTable | KeyColumn | Category                         | Impostazione | Descrizione |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binary        | Nome      | N        |          |          |          |           | [Identificatore](identifier.md)     |     |             |
| Binary        | Dati      | N        |          |          |          |           | [Binario](binary.md)             |     |             |
| CustomAction  | Azione    | N        |          |          |          |           | [Identificatore](identifier.md)     |     |             |
| CustomAction  | Tipo      | N        |          |          |          |           | [Integer](integer.md)           |     |             |
| CustomAction  | Source (Sorgente)    | S        |          |          |          |           | [CustomSource](customsource.md) |     |             |
| CustomAction  | Destinazione    | S        |          |          |          |           | [Formattato](formatted.md)       |     |             |
| \_ICESequence | Azione    | N        |          |          |          |           | [Identificatore](identifier.md)     |     |             |
| \_ICESequence | Condition | S        |          |          |          |           | [Condition](condition.md)       |     |             |
| \_ICESequence | Sequenza  | S        |          |          |          |           | [Integer](integer.md)           |     |             |



 

 

 



