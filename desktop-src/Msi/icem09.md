---
description: ICEM09 verifica che il modulo unione gestisca in modo sicuro le directory predefinite.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232446"
---
# <a name="icem09"></a>ICEM09

ICEM09 verifica che il modulo unione gestisca in modo sicuro le directory predefinite. Questa operazione viene eseguita verificando che nessun componente del modulo installi una directory in una directory di sistema predefinita, ad esempio "ProgramFilesFolder" o "dei". I moduli devono invece usare directory con nomi univoci (creati con la convenzione di denominazione del modulo merge) e usare azioni personalizzate per la directory di destinazione appropriata. Questo approccio impedisce ai moduli di entrare in conflitto con una struttura di directory esistente nel database finale. ICEM09 verifica che le azioni personalizzate necessarie per il funzionamento di questa tecnica non esistano (in modo che lo strumento di merge possa generarle) o esistano nel formato corretto (in modo che funzionino come previsto).

La mancata correzione di un avviso o di un errore segnalato da ICEM09 potrebbe causare problemi per i client del modulo merge. Le righe della tabella di directory con chiavi primarie, ad esempio ProgramFilesFolder, sono spesso presenti in un database. Se pertanto i componenti del modulo vengono installati direttamente in directory predefinite, ad esempio ProgramFilesFolder, è possibile che le voci di directory del modulo entrino in conflitto con le righe già esistenti. Questa condizione richiede che l'utente del modulo suddivida i file di origine dal modulo per poter corrispondere alla directory di origine esistente.

## <a name="result"></a>Risultato

ICEM09 segnala un errore o un avviso quando un componente del modulo installa una directory in una directory di sistema predefinita, causando un possibile conflitto di nomi con la struttura di directory esistente.

## <a name="example"></a>Esempio

ICEM09 invia gli avvisi seguenti per un modulo contenente le voci di database visualizzate.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

Rinominare la directory del modulo merge in modo che non corrisponda a una proprietà di Windows Installer e pertanto sia univoca. Impostare quindi una proprietà con lo stesso nome sul valore della directory Windows Installer. Quando si verifica la risoluzione della directory, la directory ha una proprietà con lo stesso nome, quindi il percorso di installazione della directory corrisponde al valore della proprietà. I file passano dalla posizione di origine distinta allo stesso percorso di destinazione. Questo processo dovrebbe rimuovere completamente i conflitti di Unione.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Se per l'azione non è presente il numero di sequenza 1, è possibile che non venga eseguito il merge del database di destinazione abbastanza presto nella sequenza per funzionare in modo efficace.

Per correggere il problema, impostare il numero di sequenza su 1. Si noti che la maggior parte degli strumenti di merge correnti (ma non alcune versioni precedenti) genera queste azioni personalizzate in fase di merge, pertanto non è sempre necessario creare esplicitamente le azioni nel modulo merge.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Poiché la colonna CustomAction è la chiave primaria della tabella CustomAction, alcuni strumenti di merge possono generare azioni duplicate poiché il nome dell'azione creato in precedenza è diverso.

Per correggere il problema, denominare l'azione come la directory di destinazione. Si noti che la maggior parte degli strumenti di merge correnti (ma non alcune versioni precedenti) genera queste azioni personalizzate in fase di merge, pertanto non è sempre necessario creare esplicitamente le azioni nel modulo merge.

[Tabella directory](directory-table.md)



| Directory          | \_Padre directory | DefaultDir |
|--------------------|-------------------|------------|
| ProgramFilesFolder | Directory1        | A          |
| Dei    | Directory2        | B:C        |
| CartellaDatiApp      | Directory3        | D          |
| MyPicturesFolder   | Directory4        | E          |



 

[Tabella componenti](component-table.md)



| Componente               | Directory          |
|-------------------------|--------------------|
| Component1.<GUID> | ProgramFilesFolder |
| Component2.<GUID> | Dei    |
| Component3.<GUID> | CartellaDatiApp      |
| Component4.<GUID> | MyPicturesFolder   |



 

[Tabella CustomAction](customaction-table.md)



| CustomAction                 | Tipo | Source (Sorgente)                       | Destinazione              |
|------------------------------|------|------------------------------|---------------------|
| Dei.<GUID> | 51   | Dei.<GUID> | \[Dei\] |
| MyAppDataFolderAction        | 51   | CartellaDatiApp.<GUID>   | \[CartellaDatiApp\]   |



 

[Tabella ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Azione                       | Sequenza | BaseAction | After | Condizione |
|------------------------------|----------|------------|-------|-----------|
| Dei.<GUID> | 100      |            |       |           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



