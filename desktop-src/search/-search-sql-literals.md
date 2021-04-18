---
description: Un valore letterale è una stringa di caratteri che rappresenta un valore in un'istruzione di query. Per confrontare i valori di colonna o per specificare i termini di ricerca, è possibile utilizzare valori letterali. Windows Search supporta i tipi di valori letterali seguenti.
ms.assetid: cc526174-3c91-402d-b7d0-69fc9a61c3f9
title: Valori letterali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e066f62a39bc46ec2ff7bf44c187d33f3832ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306122"
---
# <a name="literals"></a>Valori letterali

Un valore letterale è una stringa di caratteri che rappresenta un valore in un'istruzione di query. Per confrontare i valori di colonna o per specificare i termini di ricerca, è possibile utilizzare valori letterali. Windows Search supporta i tipi di valori letterali seguenti.


-   I **valori letterali stringa** possono essere di qualsiasi lunghezza e possono contenere caratteri ANSI o Unicode. È necessario racchiudere i valori letterali stringa tra virgolette singole ('). Per includere una virgoletta singola all'interno di un valore letterale stringa, usare due virgolette singole (''). Rappresenta una stringa vuota come due virgolette singole consecutive ('').
-   I **valori letterali numerici** possono contenere le cifre 0-9, un punto e la lettera e (o e). I valori letterali numerici rappresentano i numeri, inclusi i numeri interi positivi e negativi, i numeri decimali e i valori di valuta. I valori letterali numerici possono essere definiti utilizzando la notazione scientifica, ad esempio 2.3 E-05. Non racchiudere un valore letterale numerico tra virgolette singole o verrà interpretato come valore letterale stringa e confrontato con le tecniche di confronto delle stringhe. I valori di valuta non possono contenere simboli di valuta.
-   I **valori letterali esadecimali** possono contenere le cifre 0-9 e le lettere a-f e a-f. Un valore letterale esadecimale rappresenta un Unsigned Integer specificato in notazione esadecimale. I valori letterali esadecimali devono iniziare con 0x.
    > [!Note]  
    > Lo standard SQL-92 richiede che i valori letterali esadecimali siano racchiusi tra virgolette singole. Tuttavia, Windows Search non supporta tale notazione.

     

-   I valori **letterali booleani** rappresentano valori logici e possono essere **true** o **false**. Non racchiudere un valore letterale booleano tra virgolette singole oppure viene interpretato come valore letterale stringa.
-   I **valori letterali di data** rappresentano date specifiche, timestamp o ore relative e sono racchiusi tra virgolette singole. È necessario inserire le date nel formato anno/mese/giorno ore: minuti: secondi o anno-mese-giorno: minuti: secondi, in cui il mese, il giorno e l'anno sono numeri. Specificare l'anno con un valore a quattro cifre, ad esempio 2004. I valori temporali devono essere nel formato ore: minuti: secondi. La sintassi dell'ora relativa è basata sulla [funzione DateAdd](-search-sql-dateadd.md).

 

 



