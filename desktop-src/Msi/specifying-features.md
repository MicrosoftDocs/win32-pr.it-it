---
description: Il programma di installazione Microsoft consente agli utenti di installare e rimuovere blocchi di funzionalità dell'applicazione definiti Windows funzionalità del programma di installazione.
ms.assetid: 88268c5c-57c5-49f8-92df-1ad8f30a70c2
title: Specifica delle funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8356020ce79881948b0886cfb83f634789f1ec9cfa55e7b150eb275ea1b81fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624695"
---
# <a name="specifying-features"></a>Specifica delle funzionalità

Microsoft Installer consente agli utenti di installare e rimuovere blocchi di funzionalità dell'applicazione definiti Windows [funzionalità del programma di installazione.](windows-installer-features.md) In questa sezione si aggiungono informazioni al database di installazione sulle funzionalità disponibili per l'Blocco note esempio. Per altre informazioni, vedere [Gruppo](core-tables-group.md) e componenti e funzionalità delle [tabelle principali](components-and-features.md).

L Blocco note di esempio installa le funzionalità in una gerarchia di funzionalità padre e figlio. Nell'elenco seguente le funzionalità figlio vengono rientrate rispetto alla relativa funzionalità padre. Le funzionalità devono essere visualizzate in questo ordine nel [controllo SelectionTree dell'interfaccia](selectiontree-control.md) utente.

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

Usare un editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella [delle funzionalità vuota.](feature-table.md)



| Funzionalità  | Elemento \_ padre della funzionalità | Titolo         | Descrizione                | Visualizza | Level | Directory\_ | Attributi |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Arti     |                 | Arti          | Eventi di arti a Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Baseball | Sport           | Baseball      | Giochi di baseball             | 17      | 3     | SPORTDIR    | 32         |
| Concerto  | Arti            | Concerto       | Eventi di concerto a Red Park | 21      | 3     | ARTODIR     | 2          |
| Danza    | Arti            | Danza         | Eventi di danze a Red Park   | 23      | 3     | ARTODIR     | 2          |
| Calcio | Sport           | Calcio      | Giochi di calcio             | 19      | 3     | SPORTDIR    | 2          |
| Cancello     |                 | Cancello          | Ammissioni di Red Park      | 6       | 3     | NOTEPADDIR  | 0          |
| Help     | Blocco note         | Help          | File della Guida.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January  | Cancello            | January       | Ammissioni di gennaio         | 10      | 3     | MONDIR      | 2          |
| NewYears | January         | Giorno del nuovo anno | Ammissioni per il giorno del nuovo anno   | 11      | 3     | HOLDIR      | 2          |
| Blocco note  |                 | Blocco note       | Blocco note Editore             | 1       | 3     | NOTEPADDIR  | 0          |
| File Leggimi   | Blocco note         | File Leggimi        | File Leggimi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport    |                 | Eventi di sport  | Eventi sport al Red Park   | 14      | 3     | NOTEPADDIR  | 0          |



 

[Continua](specifying-feature-component-relationships.md)

 

 



