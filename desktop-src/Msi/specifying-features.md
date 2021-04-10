---
description: Microsoft Installer consente agli utenti di installare e rimuovere blocchi di funzionalità delle applicazioni definite Windows Installer funzionalità.
ms.assetid: 88268c5c-57c5-49f8-92df-1ad8f30a70c2
title: Specifica delle funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf7463b30247e921fb440ada1cd6f00f8e96a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231855"
---
# <a name="specifying-features"></a>Specifica delle funzionalità

Microsoft Installer consente agli utenti di installare e rimuovere blocchi di funzionalità delle applicazioni definite [Windows Installer funzionalità](windows-installer-features.md). In questa sezione vengono aggiunte al database di installazione informazioni sulle funzionalità disponibili per l'esempio del blocco note. Per ulteriori informazioni, vedere [Core tables Group](core-tables-group.md) e [Components and features](components-and-features.md).

Nell'esempio del blocco note vengono installate funzionalità in una gerarchia di funzionalità padre e figlio. Nell'elenco seguente, le funzionalità figlio vengono rientrate rispetto alla relativa funzionalità padre. Le funzionalità devono essere visualizzate in questo ordine nel [controllo SelectionTree](selectiontree-control.md) dell'interfaccia utente.

Blocco note

-   File Leggimi
-   Help

Cancello

-   January
    -   NewYears

Sport

-   Baseball
-   Calcio

Arti

-   Concerto
-   Danza

Usare un editor di database per aprire MNP2000.msi e immettere i dati seguenti nella [tabella delle funzionalità](feature-table.md)vuote.



| Funzionalità  | \_Elemento padre della funzionalità | Titolo         | Descrizione                | Visualizza | Level | Directory\_ | Attributi |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Arti     |                 | Arti          | Eventi Arts in Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Baseball | Sport           | Baseball      | Partite di baseball             | 17      | 3     | SPORTDIR    | 32         |
| Concerto  | Arti            | Concerto       | Eventi del concerto in Red Park | 21      | 3     | ARTSDIR     | 2          |
| Danza    | Arti            | Danza         | Eventi di danza nel Red Park   | 23      | 3     | ARTSDIR     | 2          |
| Calcio | Sport           | Calcio      | Partite di calcio             | 19      | 3     | SPORTDIR    | 2          |
| Cancello     |                 | Cancello          | Ricoveri del Red Park      | 6       | 3     | NOTEPADDIR  | 0          |
| Help     | Blocco note         | Help          | File della guida.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January  | Cancello            | January       | Ammissioni di gennaio         | 10      | 3     | MONDIno      | 2          |
| NewYears | January         | Giorno nuovo anno | Ricoveri nuovi anni   | 11      | 3     | HOLDIR      | 2          |
| Blocco note  |                 | Blocco note       | Editor blocco note             | 1       | 3     | NOTEPADDIR  | 0          |
| File Leggimi   | Blocco note         | File Leggimi        | File Leggimi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport    |                 | Eventi sportivi  | Eventi sportivi al Red Park   | 14      | 3     | NOTEPADDIR  | 0          |



 

[Continua](specifying-feature-component-relationships.md)

 

 



