---
description: ICE12 convalida le tabelle CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence e InstallUISequence del database Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef427ca1567680aa9a9f2a598f5a94cb8dee545487afcf3eb1fbb8d1f350fd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262261"
---
# <a name="ice12"></a>ICE12

ICE12 esegue query sulle tabelle [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [InstallUISequence](installuisequence-table.md) per convalidare quanto segue:

-   [L'azione CostFinalize](costfinalize-action.md) si verifica in qualsiasi tabella di sequenza contenente azioni di tipo [Custom Action Type 35](custom-action-type-35.md) o [Custom Action Type 51.](custom-action-type-51.md)
-   Ogni tipo [di azione personalizzata 35](custom-action-type-35.md) viene dopo l'azione [CostFinalize](costfinalize-action.md). nelle tabelle di sequenza.
-   Ogni tipo di azione personalizzata [51](custom-action-type-51.md) con chiave esterna per la tabella Directory nella colonna Origine della tabella CustomAction viene eseguita prima dell'azione [CostFinalize](costfinalize-action.md) nelle tabelle di sequenza.

Si noti che ICE12 non convalida il testo formattato nella colonna Target della tabella CustomAction.

## <a name="result"></a>Risultato

ICE12 invia un messaggio di errore se la convalida delle azioni personalizzate che impostano una proprietà della directory ha esito negativo.

## <a name="example"></a>Esempio

ICE12 potrebbe inviare tre errori per l'esempio illustrato.

-   Per CA1, cartella 'MyFolder' non trovata nella tabella Directory
-   Per CA2, la sequenza '80' viene prima di CostFinalize nella tabella InstallExecuteSequence. Deve essere dopo ( CF@100 )
-   Per CA3, la sequenza '125' segue CostFinalize nella tabella InstallExecuteSequence. Deve essere prima di ( CF@100 )

[Tabella CustomAction](customaction-table.md) (parziale)



| Azione | Tipo | Source (Sorgente)        |
|--------|------|---------------|
| CA1    | 35   | Cartella      |
| CA2    | 35   | Cartella Windows |
| CA3    | 51   | Cartella Windows |



 

[Tabella directory](directory-table.md)



| Directory     | Padre \_ della directory | DefaultDir    |
|---------------|-------------------|---------------|
| Targetdir     |                   | SourceDir     |
| Cartella Windows | Targetdir         | Cartella Windows |



 

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione       | Sequenza |
|--------------|----------|
| CostFinalize | 100      |
| CA2          | 80       |
| CA3          | 125      |



 

Per correggere l'errore per CA1, modificare la voce nella colonna Source nella tabella CustomAction in una voce esistente nella tabella Directory o aggiungere MyFolder alla tabella Directory.

Per correggere l'errore per CA2, modificarne la sequenza nella tabella InstallExecuteSequence in modo che venga eseguita dopo l'azione CostFinalize.

Per correggere l'errore per CA3, modificarne la sequenza nella tabella InstallExecuteSequence in modo che venga eseguita prima dell'azione CostFinalize.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



