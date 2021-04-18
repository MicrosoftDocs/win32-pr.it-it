---
description: ICE12 convalida le tabelle CustomAction, directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence e InstallUISequence del database Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314238"
---
# <a name="ice12"></a>ICE12

ICE12 esegue una query sulle tabelle [CustomAction](customaction-table.md), [directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [InstallUISequence](installuisequence-table.md) per convalidare quanto segue:

-   L' [azione CostFinalize secondo](costfinalize-action.md) si verifica in qualsiasi tabella di sequenza contenente azioni del tipo di [azione personalizzata 35](custom-action-type-35.md) o [tipo di azione personalizzata 51](custom-action-type-51.md).
-   Ogni [tipo di azione personalizzata 35](custom-action-type-35.md) viene eseguito dopo l' [azione CostFinalize secondo](costfinalize-action.md). nelle tabelle di sequenza.
-   Ogni [tipo di azione personalizzata 51](custom-action-type-51.md) che dispone di una chiave esterna per la tabella di directory nella colonna di origine della tabella CustomAction precede l' [azione CostFinalize secondo](costfinalize-action.md) nelle tabelle di sequenza.

Si noti che ICE12 non convalida il testo formattato nella colonna di destinazione della tabella CustomAction.

## <a name="result"></a>Risultato

ICE12 Invia un messaggio di errore se la convalida delle azioni personalizzate che impostano una proprietà della directory ha esito negativo.

## <a name="example"></a>Esempio

ICE12 avrebbe pubblicato tre errori per l'esempio illustrato.

-   Per CA1, la cartella ' fileFolder ' non è stata trovata nella tabella di directory
-   Per il CA2, la sequenza '80 ' precede CostFinalize secondo nella tabella InstallExecuteSequence. Deve essere successiva a ( CF@100 )
-   Per CA3, la sequenza ' 125' è successiva a CostFinalize secondo nella tabella InstallExecuteSequence. Deve precedere ( CF@100 )

[Tabella CustomAction](customaction-table.md) (parziale)



| Azione | Tipo | Source (Sorgente)        |
|--------|------|---------------|
| CA1    | 35   | MyFolder      |
| CA2    | 35   | WindowsFolder |
| CA3    | 51   | WindowsFolder |



 

[Tabella directory](directory-table.md)



| Directory     | \_Padre directory | DefaultDir    |
|---------------|-------------------|---------------|
| TARGETDIR     |                   | SourceDir     |
| WindowsFolder | TARGETDIR         | WindowsFolder |



 

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione       | Sequenza |
|--------------|----------|
| CostFinalize secondo | 100      |
| CA2          | 80       |
| CA3          | 125      |



 

Per correggere l'errore per CA1, modificare la voce della relativa colonna di origine nella tabella CustomAction con una voce esistente nella tabella directory o aggiungere la cartella alla tabella directory.

Per correggere l'errore per CA2, modificare la relativa sequenza nella tabella InstallExecuteSequence in modo che venga eseguita dopo l'azione CostFinalize secondo.

Per correggere l'errore per CA3, modificare la relativa sequenza nella tabella InstallExecuteSequence in modo che venga prima dell'azione CostFinalize secondo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



