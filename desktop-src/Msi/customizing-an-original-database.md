---
description: Creare una copia del pacchetto di installazione del Windows di esempio MNP2000.msi e rinominare questa copia MNP2000t.msi.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Personalizzazione di un database originale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f02f176bb24b1792d9184ebc662a45c9dbfdb8df385b3fb481967c9c8a099a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075041"
---
# <a name="customizing-an-original-database"></a>Personalizzazione di un database originale

Creare una copia del pacchetto di installazione del Windows di esempio MNP2000.msi e rinominare questa copia MNP2000t.msi. Nei passaggi seguenti questo file verrà personalizzato usando un editor di tabelle di database come Orca, fornito con l'SDK, o un altro editor di database.

Includere il nuovo file di risorse per l'elenco Phone.txt telefono nella cartella Blocco note con gli altri file di origine.



| File      | Descrizione                             | Percorso dell'origine                 | Percorso della destinazione                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | Una risorsa per la Telefono \_ list. | C: \\ Esempi \\ Blocco note \\phone.txt | \[ProgramFilesFolder \] \\ Red Park \_ \\phone.txt |



 

Usare l'editor di database per aggiungere un record alla tabella [File](file-table.md) MNP2000t.msi per il nuovo file.

[Tabella file](file-table.md)



| File      | Componente\_ | FileName  | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Telefono       | Phone.txt | 1000     |         |          | 0          | 1        |



 

Come illustrato nella sezione [Uso](using-transforms-to-add-resources.md)delle trasformazioni per aggiungere risorse , la trasformazione deve aggiungere uno o più nuovi componenti al database di installazione per contenere la nuova funzionalità elenco telefonici. Usare l'editor di database per aggiungere il record seguente alla [tabella Component](component-table.md) di MNP2000t.msi.

Il Telefono deve essere identificato con un [ID](guid.md)componente univoco GUID . Se si sta riproduendo l'esempio, non riutilizzare lo stesso GUID id componente della tabella seguente. Usare invece un'utilità come Guidgen.exe per generare un nuovo GUID. Assicurarsi di usare una stringa GUID coerente con il tipo di dati GUID Windows [Installer.](guid.md)

[Tabella dei componenti](component-table.md)



| Componente | Componentid                            | Directory\_ | Attributi | Condition | Percorso chiave   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Telefono     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

Usare l'editor di database per modificare i dati nella [tabella Funzionalità](feature-table.md) di MNP2000t.msi. Immettere 0 nella colonna Livello del record della funzionalità Gate. In questo modo la funzionalità Gate e le relative funzionalità figlio vengono disabilitate e queste funzionalità vengono disattivate dall'interfaccia utente. Si noti che poiché la [**proprietà INSTALLLEVEL**](installlevel.md) è impostata su 3 nella tabella [Property](property-table.md), il programma di installazione non installa le funzionalità con un livello 0. Aggiungere un record per la nuova Telefono \_ funzionalità Elenco.

[Tabella delle funzionalità](feature-table.md)



| Funzionalità     | Elemento padre \_ della funzionalità | Titolo         | Descrizione                | Visualizza | Level | Directory\_ | Attributi |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Arti        |                 | Arti          | Eventi di rito al Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Baseball    | Sport           | Baseball      | Baseball Games             | 17      | 3     | SPORTDIR    | 32         |
| Concerto     | Arti            | Concerto       | Eventi di concertare al Red Park | 21      | 3     | DIRDIR     | 2          |
| Danza       | Arti            | Danza         | Eventi di musica classica al Red Park   | 23      | 3     | DIRDIR     | 2          |
| Calcio    | Sport           | Calcio      | Giochi di football             | 19      | 3     | SPORTDIR    | 2          |
| Cancello        |                 | Cancello          | Ammissioni di Red Park      | 6       | 0     | NOTEPADDIR  | 0          |
| Help        | Blocco note         | Help          | File della Guida.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January     | Cancello            | January       | Ammissioni di gennaio         | 10      | 3     | CHER      | 2          |
| NewYears    | January         | New Years Day | New Years Day Admissions   | 11      | 3     | HOLDIR      | 2          |
| Blocco note     |                 | Blocco note       | Blocco note Editore             | 1       | 3     | NOTEPADDIR  | 0          |
| File Leggimi      | Blocco note         | File Leggimi        | File Leggimi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport       |                 | Eventi di sport  | Eventi sport al Red Park   | 14      | 3     | NOTEPADDIR  | 0          |
| \_Telefono Elenco |                 | Telefono Elenco    | Telefono Elenco                 | 24      | 3     | NOTEPADDIR  | 0          |



 

Aggiungere il record seguente alla [tabella FeatureComponents di](featurecomponents-table.md) MNP2000t.msi.

[Tabella FeatureComponents](featurecomponents-table.md)



| Funzionalità\_   | Componente\_ |
|-------------|-------------|
| \_Telefono Elenco | Telefono       |



 

Aggiungere un nuovo record nella tabella [Collegamento per](shortcut-table.md) creare un collegamento alla Telefono \_ funzionalità Elenco.

[Tabella dei collegamenti](shortcut-table.md)



| Tasto di scelta rapida | Directory\_ | Nome      | Componente\_ | Destinazione          | Argomenti | Descrizione | Tasto di scelta rapida | Icona\_ | IconIndex | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| sPhone   | MENUDIR     | Phone.txt | Telefono       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Continua](generating-a-customization-transform.md)

 

 



