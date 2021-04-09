---
description: ICEM12 verifica che in una tabella ModuleSequence le azioni standard includano numeri di sequenza e azioni personalizzate hanno BaseAction e After values.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049626"
---
# <a name="icem12"></a>ICEM12

ICEM12 verifica che in una tabella ModuleSequence le azioni standard includano numeri di sequenza e azioni personalizzate hanno BaseAction e After values.

Questo ICEM è disponibile nel file Mergemod. cub fornito in Windows Installer SDK 2,0 e versioni successive. Per informazioni dettagliate, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Risultato

ICEM12 Invia un errore nei casi seguenti:

-   Trova il modulo che contiene un' [azione standard](standard-actions.md) senza un numero di sequenza.
-   Rileva che un'azione standard contiene valori immessi nei campi BaseAction o After della tabella [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence Table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence Table](moduleinstalluisequence-table.md)o [ModuleInstallExecuteSequence Table](moduleinstallexecutesequence-table.md).
-   Trova il modulo che contiene un' [azione personalizzata](custom-actions.md) senza i valori immessi nei campi Sequence, BaseAction o After della [tabella ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence Table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence Table](moduleinstalluisequence-table.md)o [ModuleInstallExecuteSequence Table](moduleinstallexecutesequence-table.md).

ICEM12 Invia un avviso se trova un'azione personalizzata con un numero di sequenza specificato, ma nessun valore nei campi BaseAction o After.

Si noti che tutte le azioni trovate nella [tabella CustomAction](customaction-table.md) sono considerate azioni personalizzate. Tutte le altre azioni sono considerate azioni standard.

## <a name="example"></a>Esempio

ICEM12 invia i messaggi di avviso e di errore seguenti per un modulo che contiene le voci del database indicate di seguito:

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[CustomAction](customaction-table.md)



| Azione  | Tipo | Source (Sorgente)  | Destinazione  |
|---------|------|---------|---------|
| Action1 | 30   | source1 | Target1 |
| Action3 | 30   | source3 | Target3 |



 

[ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)



| Azione  | Sequenza | BaseAction | After | Condizione |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1    | 1     | true      |
| Action3 |          |            |       | true      |



 

[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Azione  | Sequenza | BaseAction | After | Condizione |
|---------|----------|------------|-------|-----------|
| Action1 | 1        |            |       | true      |



 

Per correggere questi errori, provare a eseguire le operazioni seguenti:

-   Rimuovere il numero di sequenza per l'azione personalizzata action1 e usare invece i campi BaseAction e After.
-   Immettere i valori nei campi Sequence, BaseAction o After per l'azione personalizzata Action3. Lasciare vuoti i campi BaseAction e After per l'azione standard Action2.
-   Non lasciare vuoto il campo sequenza per l'azione standard Action2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



