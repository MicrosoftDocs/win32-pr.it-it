---
description: Il pacchetto di aggiornamento Windows Installer di esempio aggiunge nuove funzionalità al prodotto originale.
ms.assetid: cbc4c2ff-e08b-4ebb-a306-a80f9a6e4360
title: Aggiornamento delle funzionalità per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af072618bd0a2ba16a7f098d6b1129ba17c27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314768"
---
# <a name="updating-features-for-an-upgrade"></a>Aggiornamento delle funzionalità per un aggiornamento

Il pacchetto di aggiornamento di esempio aggiunge tre nuove funzionalità al prodotto originale:

-   Basket, una nuova funzionalità figlio della funzionalità sport.
-   Opera, una nuova funzionalità figlio della funzionalità Arts.
-   Memorial, una nuova funzionalità figlio della funzionalità Gate.

Utilizzare l'editor di database per aprire MNP2001.msi e immettere i dati seguenti nella [tabella delle funzionalità](feature-table.md).

[Tabella delle funzionalità](feature-table.md)



| Funzionalità    | \_Elemento padre della funzionalità | Titolo         | Descrizione                | Visualizza | Level | Directory\_ | Attributi |
|------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Arti       |                 | Arti          | Eventi Arts in Red Park.   | 18      | 3     | NOTEPADDIR  | 0          |
| Baseball   | Sport           | Baseball      | Partite di baseball             | 17      | 3     | SPORTDIR    | 32         |
| Concerto    | Arti            | Concerto       | Eventi del concerto in Red Park | 19      | 3     | ARTSDIR     | 2          |
| Danza      | Arti            | Danza         | Eventi di danza nel Red Park   | 21      | 3     | ARTSDIR     | 2          |
| Calcio   | Sport           | Calcio      | Partite di calcio             | 13      | 3     | SPORTDIR    | 2          |
| Cancello       |                 | Cancello          | Ricoveri del Red Park      | 6       | 3     | NOTEPADDIR  | 0          |
| Help       | Blocco note         | Help          | File della guida.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January    | Cancello            | January       | Ammissioni di gennaio         | 7       | 3     | MONDIno      | 2          |
| NewYears   | January         | Giorno nuovo anno | Ricoveri nuovi anni   | 9       | 3     | HOLDIR      | 2          |
| Blocco note    |                 | Blocco note       | Editor blocco note             | 1       | 3     | NOTEPADDIR  | 0          |
| File Leggimi     | Blocco note         | File Leggimi        | File Leggimi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport      |                 | Eventi sportivi  | Eventi sportivi al Red Park   | 12      | 3     | NOTEPADDIR  | 0          |
| Basket | Sport           | Basket    | Giochi Basket           | 15      | 3     | SPORTDIR    | 2          |
| Opera      | Arti            | Opera         | Prestazioni dell'opera         | 23      | 3     | ARTSDIR     | 2          |
| Memorial   | Cancello            | Giorno Memorial  | Ricoveri per giorni commemorativi    | 11      | 3     | HOLDIR      | 2          |



 

Utilizzare l'editor di database per aprire MNP2001.msi e immettere i dati seguenti nella [tabella FeatureComponents](featurecomponents-table.md)vuota.



| Funzionalità\_  | Componente\_ |
|------------|-------------|
| Baseball   | Baseball    |
| Concerto    | Concerto     |
| Danza      | Danza       |
| Calcio   | Calcio    |
| Help       | Help        |
| January    | January     |
| NewYears   | NewYears    |
| Blocco note    | Blocco note     |
| File Leggimi     | Blocco note     |
| Basket | Basket  |
| Opera      | Opera       |
| Memorial   | Memorial    |



 

[Continua](updating-shortcuts-for-an-upgrade.md)

 

 



