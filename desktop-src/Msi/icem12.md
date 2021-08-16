---
description: ICEM12 verifica che in una tabella ModuleSequence le azioni standard presentino numeri di sequenza e le azioni personalizzate hanno valori BaseAction e After.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53e6f83b9ffccf6595719815ec4bd44cc8ff3774b989b682751dd9be1bbe5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634944"
---
# <a name="icem12"></a>ICEM12

ICEM12 verifica che in una tabella ModuleSequence le azioni standard presentino numeri di sequenza e le azioni personalizzate hanno valori BaseAction e After.

Questo icem è disponibile nel file Mergemod.cub disponibile in Windows Installer 2.0 SDK e versioni successive. Per informazioni dettagliate, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Risultato

ICEM12 invia un errore nei casi seguenti:

-   Trova che il modulo contiene [un'azione standard](standard-actions.md) senza un numero di sequenza.
-   Viene rilevato che per un'azione standard sono stati immessi valori nei campi BaseAction o After della tabella [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md)o [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)table .
-   Trova che il [](custom-actions.md) modulo contiene un'azione personalizzata senza valori immessi nei campi Sequence, BaseAction o After della tabella [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)table , [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md)o [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)table .

ICEM12 invia un avviso se trova un'azione personalizzata con un numero di sequenza specificato, ma nessun valore nei campi BaseAction o After.

Si noti che tutte le azioni trovate [nella tabella CustomAction](customaction-table.md) sono considerate azioni personalizzate. Tutte le altre azioni sono considerate azioni standard.

## <a name="example"></a>Esempio

ICEM12 invia i messaggi di errore e di avviso seguenti per un modulo che contiene le voci di database illustrate di seguito:

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
| Action1 | 30   | source1 | target1 |
| Action3 | 30   | source3 | target3 |



 

[ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)



| Azione  | Sequenza | BaseAction | After | Condition |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1    | 1     | true      |
| Action3 |          |            |       | true      |



 

[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Azione  | Sequenza | BaseAction | After | Condition |
|---------|----------|------------|-------|-----------|
| Action1 | 1        |            |       | true      |



 

Per correggere questi errori, provare a eseguire le operazioni seguenti:

-   Rimuovere il numero di sequenza per l'azione personalizzata Action1 e usare invece i campi BaseAction e After.
-   Immettere i valori nei campi Sequence, BaseAction o After per l'azione personalizzata Action3. Lasciare vuoti i campi BaseAction e After per l'azione standard Action2.
-   Non lasciare vuoto il campo Sequenza per l'azione standard Action2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul modulo di unione ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



