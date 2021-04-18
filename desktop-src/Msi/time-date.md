---
description: Il tipo di dati data/ora include l'ora e la data archiviate singolarmente, usando interi senza segno come campi di bit, compressi come indicato di seguito.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Data/ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313326"
---
# <a name="timedate"></a>Data/ora

Il tipo di dati data/ora include l'ora e la data archiviate singolarmente, usando interi senza segno come campi di bit, compressi come indicato di seguito.

## <a name="time"></a>Tempo

L'ora è codificata in un intero senza segno a 2 byte con i seguenti campi di bit.



| Contenuto           | BITS        | Intervallo di valori |
|--------------------|-------------|-------------|
| ore              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| intervalli di 2 secondi | B C D E F   | 0 – 29        |



 

## <a name="date"></a>Data

La data è codificata in un intero senza segno a 2 byte con i campi di bit seguenti.



| Contenuto | BITS          | Intervallo di valori              |
|----------|---------------|--------------------------|
| anno     | 0 1 2 3 4 5 6 | 0 – 119 (relativo a 1980) |
| month    | 7 8 9 A       | 1–12                     |
| day      | B C D E F     | 1–31                     |



 

 

 



