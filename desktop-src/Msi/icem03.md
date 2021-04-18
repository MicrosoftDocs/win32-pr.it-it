---
description: ICEM03 verifica che tutte le azioni del modulo siano azioni di base o derivano da un'azione di base valida.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313345"
---
# <a name="icem03"></a>ICEM03

ICEM03 verifica che tutte le azioni del modulo siano azioni di base o derivano da un'azione di base valida.

I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.

## <a name="result"></a>Risultato

ICEM03 invia i messaggi di errore per un modulo contenente azioni in una tabella di sequenza che non è un'azione di base o derivata da un'azione di base valida.

## <a name="example"></a>Esempio

ICEM03 invia i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[Tabella ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Azione  | Sequenza | BaseAction | After | Condizione |
|---------|----------|------------|-------|-----------|
| Action1 |          | Action2    | 0     |           |
| Action2 |          | Action1    | 0     |           |



 

ICEM03 Invia errori per queste due azioni perché fanno riferimento l'uno all'altro come azioni di base nella tabella ModuleInstallExecuteSequence. Tutte le azioni nelle tabelle [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md)e [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) devono essere azioni di base o derivare la posizione dalla combinazione di un'altra azione e un flag before e After.

Per correggere l'errore, determinare le azioni di base per le due azioni. Aggiungere un record per le azioni di base con un numero di sequenza predefinito. Per action1 e Action2 immettere i nomi delle azioni di base nella colonna BaseAction e 0 o 1 nella colonna after.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



