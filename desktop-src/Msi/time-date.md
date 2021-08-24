---
description: Il tipo di dati Time/Date contiene l'ora e la data archiviate singolarmente, usando interi senza segno come campi di bit, come indicato di seguito.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Ora/Data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3c5cccc2f1211918b52008f0d81a7e4693dfd14766696b77cd184d75f4309d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810741"
---
# <a name="timedate"></a>Ora/Data

Il tipo di dati Time/Date contiene l'ora e la data archiviate singolarmente, usando interi senza segno come campi di bit, come indicato di seguito.

## <a name="time"></a>Ora

L'ora viene codificata in un intero senza segno a 2 byte con i campi di bit seguenti.



| Contenuto           | BITS        | Intervallo di valori |
|--------------------|-------------|-------------|
| ore              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| Intervalli di 2 secondi | B C D E F   | 0–29        |



 

## <a name="date"></a>Data

La data viene codificata in un intero senza segno a 2 byte con i campi di bit seguenti.



| Contenuto | BITS          | Intervallo di valori              |
|----------|---------------|--------------------------|
| anno     | 0 1 2 3 4 5 6 | 0-119 (relativo al 1980) |
| month    | 7 8 9 A       | 1–12                     |
| day      | B C D E F     | 1–31                     |



 

 

 



