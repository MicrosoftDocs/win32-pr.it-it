---
description: Il valore logico di una proprietà impostata è true.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Uso delle proprietà nelle istruzioni condizionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307240"
---
# <a name="using-properties-in-conditional-statements"></a>Uso delle proprietà nelle istruzioni condizionali

Il valore logico di una proprietà impostata è true. Per determinare se una proprietà è impostata senza ottenere effettivamente il relativo valore, testare l'espressione logica "SetProperty" o "not SetProperty". Quando viene impostata la proprietà Property, il primo restituisce true e il secondo come false.

Una o più proprietà possono essere combinate con operatori per formare espressioni logiche utilizzate in un'istruzione condizionale. Per ulteriori informazioni sugli operatori che possono essere utilizzati nelle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

È possibile immettere un'istruzione condizionale che utilizza proprietà nella colonna condizione della [tabella Condition](condition-table.md) per modificare lo stato di selezione di qualsiasi voce nella [tabella Feature](feature-table.md).

Le istruzioni condizionali con una o più proprietà vengono comunemente utilizzate nella colonna condizione delle tabelle di database.

Le tabelle seguenti includono ognuna una colonna per le espressioni condizionali:

-   [Tabella Condition](condition-table.md)
-   [Tabella ControlEvent](controlevent-table.md)
-   [Tabella LaunchCondition](launchcondition-table.md)
-   [Tabella InstallUISequence](installuisequence-table.md)
-   [Tabella InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabella ControlCondition](controlcondition-table.md)
-   [Tabella AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabella AdvtExecuteSequence](advtexecutesequence-table.md)
-   [Tabella AdminUISequence](adminuisequence-table.md)

Si noti che le sei tabelle di sequenza delle azioni hanno campi per una condizione. Se l'espressione condizionale in questo campo restituisce false, l'azione verrà ignorata dal programma di installazione.

Se si imposta una [proprietà privata](private-properties.md) nella sequenza dell'interfaccia utente creando un'azione personalizzata in una delle tabelle di sequenza dell'interfaccia utente, tale proprietà non viene impostata nella sequenza di esecuzione. Per impostare la proprietà nella sequenza di esecuzione, è inoltre necessario inserire un'azione personalizzata in una tabella della sequenza di esecuzione. In alternativa, è possibile rendere la proprietà una [proprietà pubblica](public-properties.md) e includerla nella proprietà [**SecureCustomProperties**](securecustomproperties.md) .

Per ulteriori informazioni, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md) o [utilizzo delle proprietà](using-properties.md).

 

 



