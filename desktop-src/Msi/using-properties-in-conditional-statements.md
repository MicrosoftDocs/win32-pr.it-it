---
description: Il valore logico di una proprietà impostata è True.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Uso delle proprietà nelle istruzioni condizionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5dcee5c2d657b8014ac98c0d4d1ce5b56f0f3614a597cd63611ae965e30720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499211"
---
# <a name="using-properties-in-conditional-statements"></a>Uso delle proprietà nelle istruzioni condizionali

Il valore logico di una proprietà impostata è True. Per determinare se una proprietà viene impostata senza ottenere effettivamente il relativo valore, testare l'espressione logica "MyProperty" o "Not MyProperty". Quando la proprietà MyProperty è impostata, la prima restituisce True e la seconda come False.

Una o più proprietà possono essere combinate con operatori per formare espressioni logiche usate in istruzioni condizionali. Per altre informazioni sugli operatori che possono essere usati nelle istruzioni condizionali, vedere [Sintassi delle istruzioni condizionali.](conditional-statement-syntax.md)

Un'istruzione condizionale che usa le proprietà può essere immessa nella colonna Condizione della tabella [Condizione](condition-table.md) per modificare lo stato di selezione di qualsiasi voce nella [tabella Funzionalità](feature-table.md).

Le istruzioni condizionali con una o più proprietà vengono comunemente usate nella colonna Condizione delle tabelle di database.

Le tabelle seguenti hanno ognuna una colonna per le espressioni condizionali:

-   [Tabella delle condizioni](condition-table.md)
-   [Tabella ControlEvent](controlevent-table.md)
-   [Tabella LaunchCondition](launchcondition-table.md)
-   [Tabella InstallUISequence](installuisequence-table.md)
-   [Tabella InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabella ControlCondition](controlcondition-table.md)
-   [Tabella AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabella AdvtExecuteSequence](advtexecutesequence-table.md)
-   [Tabella AdminUISequence](adminuisequence-table.md)

Si noti che le sei tabelle della sequenza di azioni hanno campi per una condizione. Se l'espressione condizionale in questo campo restituisce False, il programma di installazione ignora tale azione.

Se si imposta una [proprietà](private-properties.md) privata nella sequenza dell'interfaccia utente mediante la creazione di un'azione personalizzata in una delle tabelle di sequenza dell'interfaccia utente, tale proprietà non viene impostata nella sequenza di esecuzione. Per impostare la proprietà nella sequenza di esecuzione, è necessario inserire anche un'azione personalizzata in una tabella della sequenza di esecuzione. In alternativa, è possibile impostare la proprietà come [proprietà pubblica](public-properties.md) e includerla nella [**proprietà SecureCustomProperties.**](securecustomproperties.md)

Per altre informazioni, vedere [Uso di una tabella di sequenze](using-a-sequence-table.md) o Uso di [proprietà.](using-properties.md)

 

 



