---
description: Creare una copia del pacchetto di installazione di esempio Windows Installer MNP2000.msi e rinominare il MNP2000t.msi di copia.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Personalizzazione di un database originale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3222ebce146e891c7b16c70eb78f0f26b95727c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307843"
---
# <a name="customizing-an-original-database"></a>Personalizzazione di un database originale

Creare una copia del pacchetto di installazione di esempio Windows Installer MNP2000.msi e rinominare il MNP2000t.msi di copia. Nei passaggi seguenti verrà personalizzato questo file usando un editor di tabelle di database, ad esempio ORCA, fornito con l'SDK o un altro editor di database.

Includere il nuovo file di risorse per l'elenco telefonico, Phone.txt, nella cartella blocco note con gli altri file di origine.



| File      | Descrizione                             | Percorso dell'origine                 | Percorso della destinazione                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | Risorsa per la \_ funzionalità elenco telefonico. | C: \\ \\ blocco note di esempio \\phone.txt | \[ProgramFilesFolder \] \\ Red \_ Park \\phone.txt |



 

Utilizzare l'editor di database per aggiungere un record alla [tabella file](file-table.md) di MNP2000t.msi per il nuovo file.

[Tabella file](file-table.md)



| File      | Componente\_ | FileName  | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Telefono       | Phone.txt | 1000     |         |          | 0          | 1        |



 

Come illustrato nella sezione Utilizzo delle [trasformazioni per aggiungere risorse](using-transforms-to-add-resources.md), la trasformazione deve aggiungere uno o più componenti nuovi al database di installazione per includere la nuova funzionalità elenco telefonico. Utilizzare l'editor di database per aggiungere il record seguente alla [tabella dei componenti](component-table.md) di MNP2000t.msi.

Il componente telefono deve essere identificato con un [GUID](guid.md)ID componente univoco. Se si sta riproducendo l'esempio, non riutilizzare lo stesso GUID ID componente della tabella seguente. Usare invece un'utilità, ad esempio Guidgen.exe per generare un nuovo GUID. Assicurarsi di usare una stringa GUID coerente con il tipo di dati [guid](guid.md) Windows Installer.

[Tabella componenti](component-table.md)



| Componente | ComponentId                            | Directory\_ | Attributi | Condizione | KeyPath   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Telefono     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

Utilizzare l'editor di database per modificare i dati nella [tabella delle funzionalità](feature-table.md) di MNP2000t.msi. Immettere 0 nella colonna livello del record della funzionalità Gate. In questo modo viene disabilitata la funzionalità di controllo e le relative funzionalità figlio e le funzionalità vengono nascoste dall'interfaccia utente. Si noti che poiché la proprietà [**INSTALLLEVEL**](installlevel.md) è impostata su 3 nella [tabella delle proprietà](property-table.md), il programma di installazione non installa le funzionalità con un livello pari a 0. Aggiungere un record per la nuova \_ funzionalità elenco telefonico.

[Tabella delle funzionalità](feature-table.md)



| Funzionalità     | \_Elemento padre della funzionalità | Titolo         | Descrizione                | Visualizza | Level | Directory\_ | Attributi |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Arti        |                 | Arti          | Eventi Arts in Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Baseball    | Sport           | Baseball      | Partite di baseball             | 17      | 3     | SPORTDIR    | 32         |
| Concerto     | Arti            | Concerto       | Eventi del concerto in Red Park | 21      | 3     | ARTSDIR     | 2          |
| Danza       | Arti            | Danza         | Eventi di danza nel Red Park   | 23      | 3     | ARTSDIR     | 2          |
| Calcio    | Sport           | Calcio      | Partite di calcio             | 19      | 3     | SPORTDIR    | 2          |
| Cancello        |                 | Cancello          | Ricoveri del Red Park      | 6       | 0     | NOTEPADDIR  | 0          |
| Help        | Blocco note         | Help          | File della guida.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January     | Cancello            | January       | Ammissioni di gennaio         | 10      | 3     | MONDIno      | 2          |
| NewYears    | January         | Giorno nuovo anno | Ricoveri nuovi anni   | 11      | 3     | HOLDIR      | 2          |
| Blocco note     |                 | Blocco note       | Editor blocco note             | 1       | 3     | NOTEPADDIR  | 0          |
| File Leggimi      | Blocco note         | File Leggimi        | File Leggimi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport       |                 | Eventi sportivi  | Eventi sportivi al Red Park   | 14      | 3     | NOTEPADDIR  | 0          |
| \_Elenco telefonico |                 | Elenco telefonico    | Elenco telefonico                 | 24      | 3     | NOTEPADDIR  | 0          |



 

Aggiungere il record seguente alla [tabella FeatureComponents](featurecomponents-table.md) di MNP2000t.msi.

[Tabella FeatureComponents](featurecomponents-table.md)



| Funzionalità\_   | Componente\_ |
|-------------|-------------|
| \_Elenco telefonico | Telefono       |



 

Aggiungere un nuovo record nella [tabella dei collegamenti](shortcut-table.md) per creare un collegamento alla \_ funzionalità elenco telefonico.

[Tabella di collegamento](shortcut-table.md)



| Tasto di scelta rapida | Directory\_ | Nome      | Componente\_ | Destinazione          | Argomenti | Descrizione | Tasto di scelta rapida | Icona\_ | IconIndex | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| sPhone   | MENUDIR     | Phone.txt | Telefono       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Continua](generating-a-customization-transform.md)

 

 



