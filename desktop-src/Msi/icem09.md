---
description: ICEM09 verifica che il modulo di merge gestisca in modo sicuro le directory predefinite.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4d2af38903d2e704d49b48f932818d8dfaeeb1e12588c007d4af05c297642c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894491"
---
# <a name="icem09"></a>ICEM09

ICEM09 verifica che il modulo di merge gestisca in modo sicuro le directory predefinite. A tale scopo, verificare che nessun componente nel modulo installi una directory in una directory di sistema predefinita, ad esempio "ProgramFilesFolder" o "StartMenuFolder". I moduli devono invece usare directory con nomi univoci (creati con la convenzione di denominazione del modulo unione) e usare azioni personalizzate per la destinazione della directory di destinazione appropriata. Questo approccio impedisce ai moduli di essere in conflitto con una struttura di directory esistente nel database finale. ICEM09 verifica che le azioni personalizzate necessarie per il funzionamento di questa tecnica non esistano (in modo che lo strumento di merge possa generarle) o esistano nel formato corretto (in modo che funzionino come previsto).

La mancata correzione di un avviso o di un errore segnalato da ICEM09 può causare problemi per i client del modulo unione. Le righe della tabella directory con chiavi primarie, ad esempio ProgramFilesFolder, sono spesso presenti in un database. Pertanto, se i componenti nel modulo vengono installati direttamente in directory predefinite, ad esempio ProgramFilesFolder, le voci di directory nel modulo potrebbero entrare in conflitto con le righe già esistenti. Questa condizione richiederebbe all'utente del modulo di dividere i file di origine dal modulo in modo che corrispondano alla directory di origine esistente.

## <a name="result"></a>Risultato

ICEM09 segnala un errore o un avviso quando un componente del modulo installa una directory in una directory di sistema predefinita, causando un possibile conflitto di nomi con la struttura di directory esistente.

## <a name="example"></a>Esempio

ICEM09 invia gli avvisi seguenti per un modulo contenente le voci di database visualizzate.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

Rinominare la directory del modulo unione in modo che non corrisponda a una Windows installer e pertanto è univoca. Impostare quindi una proprietà con lo stesso nome sul valore della directory Windows Installer. Quando viene verificata la risoluzione della directory, la directory ha lo stesso nome, quindi il percorso di installazione della directory è il valore della proprietà . I file vengono spostati dal percorso di origine distinto allo stesso percorso di destinazione. Questo processo deve rimuovere completamente i conflitti di merge.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Se l'azione non ha il numero di sequenza 1, potrebbe non eseguire il merge nel database di destinazione abbastanza presto nella sequenza per funzionare in modo efficace.

Per correggere questo avviso, impostare il numero di sequenza su 1. Si noti che la maggior parte degli strumenti di merge correnti (ma non alcune versioni precedenti) genererà queste azioni personalizzate in fase di unione, quindi non è sempre necessario creare in modo esplicito le azioni nel modulo unione.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Poiché la colonna CustomAction è la chiave primaria della tabella CustomAction, alcuni strumenti di merge possono generare azioni duplicate perché il nome dell'azione pre-creazione è diverso.

Per correggere questo avviso, assegnare all'azione lo stesso nome della directory di destinazione. Si noti che la maggior parte degli strumenti di merge correnti (ma non alcune versioni precedenti) generano queste azioni personalizzate in fase di unione, quindi non è sempre necessario creare in modo esplicito le azioni nel modulo unione.

[Tabella directory](directory-table.md)



| Directory          | Padre \_ della directory | DefaultDir |
|--------------------|-------------------|------------|
| Cartella ProgramFilesFolder | Directory1        | A          |
| StartMenuFolder    | Directory2        | B:C        |
| AppDataFolder      | Directory3        | D          |
| Cartella MyPictures   | Directory4        | E          |



 

[Tabella dei componenti](component-table.md)



| Componente               | Directory          |
|-------------------------|--------------------|
| Componente1.<GUID> | Cartella ProgramFilesFolder |
| Componente2.<GUID> | StartMenuFolder    |
| Componente3.<GUID> | AppDataFolder      |
| Componente4.<GUID> | Cartella MyPictures   |



 

[Tabella CustomAction](customaction-table.md)



| CustomAction                 | Tipo | Source (Sorgente)                       | Destinazione              |
|------------------------------|------|------------------------------|---------------------|
| StartMenuFolder.<GUID> | 51   | StartMenuFolder.<GUID> | \[StartMenuFolder\] |
| MyAppDataFolderAction        | 51   | AppDataFolder.<GUID>   | \[AppDataFolder\]   |



 

[Tabella ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Azione                       | Sequenza | BaseAction | After | Condition |
|------------------------------|----------|------------|-------|-----------|
| StartMenuFolder.<GUID> | 100      |            |       |           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul modulo di unione ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



