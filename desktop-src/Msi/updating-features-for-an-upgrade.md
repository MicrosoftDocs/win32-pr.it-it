---
description: Il pacchetto di Windows di aggiornamento del programma di installazione di esempio aggiunge nuove funzionalità al prodotto originale.
ms.assetid: cbc4c2ff-e08b-4ebb-a306-a80f9a6e4360
title: Aggiornamento delle funzionalità per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a6febda0c13101cc7c0615526514ebe3fee24e2aa14bac1d07794206f2de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809907"
---
# <a name="updating-features-for-an-upgrade"></a>Aggiornamento delle funzionalità per un aggiornamento

Il pacchetto di aggiornamento di esempio aggiunge tre nuove funzionalità al prodotto originale:

-   Basket, una nuova funzionalità figlio della funzionalità Sport.
-   Opera, una nuova funzionalità figlio della funzionalità Arti.
-   Una nuova funzionalità figlio della funzionalità Gate.

Usare l'editor di database per aprire MNP2001.msi e immettere i dati seguenti nella [tabella Funzionalità](feature-table.md).

[Tabella delle funzionalità](feature-table.md)



| Funzionalità    | Elemento \_ padre della funzionalità | Titolo         | Descrizione                | Visualizza | Level | Directory\_ | Attributi |
|------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Arti       |                 | Arti          | Eventi di arti a Red Park.   | 18      | 3     | NOTEPADDIR  | 0          |
| Baseball   | Sport           | Baseball      | Giochi di baseball             | 17      | 3     | SPORTDIR    | 32         |
| Concerto    | Arti            | Concerto       | Eventi di concerto a Red Park | 19      | 3     | ARTODIR     | 2          |
| Danza      | Arti            | Danza         | Eventi di danze a Red Park   | 21      | 3     | ARTODIR     | 2          |
| Calcio   | Sport           | Calcio      | Giochi di calcio             | 13      | 3     | SPORTDIR    | 2          |
| Cancello       |                 | Cancello          | Ammissioni di Red Park      | 6       | 3     | NOTEPADDIR  | 0          |
| Help       | Blocco note         | Help          | File della Guida.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January    | Cancello            | January       | Ammissioni di gennaio         | 7       | 3     | MONDIR      | 2          |
| NewYears   | January         | Giorno del nuovo anno | Ammissioni per il giorno del nuovo anno   | 9       | 3     | HOLDIR      | 2          |
| Blocco note    |                 | Blocco note       | Blocco note Editore             | 1       | 3     | NOTEPADDIR  | 0          |
| File Leggimi     | Blocco note         | File Leggimi        | File Leggimi                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport      |                 | Eventi di sport  | Eventi sport al Red Park   | 12      | 3     | NOTEPADDIR  | 0          |
| Basket | Sport           | Basket    | Giochi di basket           | 15      | 3     | SPORTDIR    | 2          |
| Opera      | Arti            | Opera         | Prestazioni dell'opera         | 23      | 3     | DIRDIR     | 2          |
| memoriale   | Cancello            | Giorno della memoria  | Ammissioni giornaliere    | 11      | 3     | HOLDIR      | 2          |



 

Usare l'editor di database per MNP2001.msi e immettere i dati seguenti nella tabella [FeatureComponents vuota.](featurecomponents-table.md)



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
| memoriale   | memoriale    |



 

[Continua](updating-shortcuts-for-an-upgrade.md)

 

 



