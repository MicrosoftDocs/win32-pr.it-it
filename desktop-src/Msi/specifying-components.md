---
description: Il Windows installer installa e rimuove blocchi di risorse a cui si fa riferimento Windows componenti del programma di installazione. Per altre informazioni, vedere Gruppo e componenti e funzionalità delle tabelle principali.
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: Specifica dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2264784d3edaad5b46017e3d337f8abfec66e1b60d18ba54388b03beddb13b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628001"
---
# <a name="specifying-components"></a>Specifica dei componenti

Il Windows installer installa e rimuove blocchi di risorse definiti Windows [componenti del programma di installazione.](windows-installer-components.md) Per altre informazioni, vedere [Gruppo](core-tables-group.md) e componenti e funzionalità delle [tabelle principali](components-and-features.md).

In questa sezione si aggiungono informazioni sui componenti usati [](component-table.md) dall'esempio Blocco note alla tabella dei componenti creata in [Importazione di un database vuoto](importing-a-blank-database.md). Per altre informazioni, vedere [Organizzazione di applicazioni in componenti e](organizing-applications-into-components.md) Definizione dei componenti del programma di [installazione](defining-installer-components.md).

L Blocco note di esempio usa otto componenti per controllare le risorse.



| Componente | Risorse                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| Baseball  | Baseball.txt, sBaseball                                                                                               |
| Concerto   | Concert.txt, sConcert                                                                                                 |
| Danza     | Dance.txt, sDance                                                                                                     |
| Calcio  | Football.txt, sFootball                                                                                               |
| Help      | Help.txt, sHelp                                                                                                       |
| January   | January.txt, sJanuary                                                                                                 |
| NewYears  | NewYears.txt, sNewYears                                                                                               |
| Blocco note   | Redpark.exe, Readme.txt, sReadme, sNotepad, **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Blocco note Sample** |



 

Ogni componente deve essere identificato con un ID componente [univoco GUID](guid.md). Se si sta riproduendo l'esempio, non riutilizzare gli stessi GUID id componente nella tabella seguente. Usare invece un'utilità come Guidgen.exe per generare nuovi GUID per i componenti.

Assicurarsi di usare una stringa GUID coerente con il tipo di dati GUID Windows installer. Per altre informazioni, vedere [Modifica del codice del componente](changing-the-component-code.md) e Cosa accade se le regole del componente vengono [interrotte?](what-happens-if-the-component-rules-are-broken.md)

Usare Orca o un altro editor di database per immettere i dati seguenti nella tabella dei componenti [vuota](component-table.md) MNP2000.msi. Non riutilizzare i GUID illustrati di seguito nella colonna ComponentId dell'esempio.



| Componente | Componentid                            | Directory\_ | Attributi | Condition | Percorso chiave      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Baseball  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concerto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTODIR     | 2          |           | Concert.txt  |
| Danza     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTODIR     | 2          |           | Dance.txt    |
| Calcio  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Help      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Blocco note   | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

Le directory di origine e di destinazione per ogni componente vengono specificate dal valore immesso nella colonna \_ Directory. Il programma di installazione risolve il percorso di questa directory usando le informazioni nella tabella Directory. Il programma di installazione usa i file del percorso della chiave specificati nella colonna KeyPath per rilevare ogni componente. Gli attributi di esecuzione remota vengono impostati nell'esempio in modo che i componenti possano essere eseguiti dall'origine o in locale.

[Continua](specifying-files-and-file-attributes.md)

 

 



