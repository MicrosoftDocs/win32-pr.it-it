---
description: Il Windows Installer installa e rimuove i blocchi di risorse denominati Windows Installer componenti di. Per ulteriori informazioni, vedere Core tables Group e Components and features.
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: Specifica di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98cb254498236b85ab5c2bc0df3bd32892227b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879554"
---
# <a name="specifying-components"></a>Specifica di componenti

Il Windows Installer installa e rimuove i blocchi di risorse denominati [Windows Installer componenti](windows-installer-components.md)di. Per ulteriori informazioni, vedere [Core tables Group](core-tables-group.md) e [Components and features](components-and-features.md).

In questa sezione vengono aggiunte informazioni sui componenti utilizzati dall'esempio di blocco note alla [tabella dei componenti](component-table.md) creata durante l' [importazione di un database vuoto](importing-a-blank-database.md). Per ulteriori informazioni, vedere [organizzazione di applicazioni in componenti](organizing-applications-into-components.md) e [definizione di componenti del programma di installazione](defining-installer-components.md).

Nell'esempio del blocco note vengono utilizzati otto componenti per controllare le risorse.



| Componente | Risorse                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| Baseball  | Baseball.txt, sBaseball                                                                                               |
| Concerto   | Concert.txt, sConcert                                                                                                 |
| Danza     | Dance.txt, sDance                                                                                                     |
| Calcio  | Football.txt, sFootball                                                                                               |
| Help      | Help.txt, sHelp                                                                                                       |
| January   | January.txt, sJanuary                                                                                                 |
| NewYears  | NewYears.txt, sNewYears                                                                                               |
| Blocco note   | Redpark.exe, Readme.txt, sReadme, sNotepad, **HKEY \_ \_ computer locale** \\ **software** \\ **Microsoft** \\ **notepad Sample** |



 

Ogni componente deve essere identificato con un [GUID](guid.md)ID componente univoco. Se si sta riproducendo l'esempio, non riutilizzare gli stessi GUID di ID componente nella tabella seguente. Usare invece un'utilità, ad esempio Guidgen.exe per generare nuovi GUID per i componenti.

Assicurarsi di usare una stringa GUID coerente con il tipo di dati GUID Windows Installer. Per altre informazioni, vedere [modifica del codice del componente](changing-the-component-code.md) e [cosa accade se le regole dei componenti sono interrotte?](what-happens-if-the-component-rules-are-broken.md)

Utilizzare Orca o un altro editor di database per immettere i dati seguenti nella [tabella dei componenti](component-table.md) vuota di MNP2000.msi. Non riutilizzare i GUID indicati di seguito nella colonna ComponentId dell'esempio.



| Componente | ComponentId                            | Directory\_ | Attributi | Condizione | KeyPath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Baseball  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concerto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Concert.txt  |
| Danza     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Dance.txt    |
| Calcio  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Help      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIno      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Blocco note   | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

Le directory di origine e di destinazione per ogni componente sono specificate dal valore immesso nella \_ colonna directory. Il programma di installazione risolve il percorso di questa directory usando le informazioni nella tabella directory. Il programma di installazione usa i file di percorso della chiave specificati nella colonna percorso chiave per rilevare ogni componente. Gli attributi di esecuzione remota vengono impostati nell'esempio in modo che i componenti possano essere eseguiti dall'origine o eseguiti localmente.

[Continua](specifying-files-and-file-attributes.md)

 

 



