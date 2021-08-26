---
description: Il tipo di dati principale del sensore per i sensori di luce ambientale è l'illuminazione in lume per metro quadrato. I principi descritti in questo argomento si basano sull'assunzione di valori di lusso come input e sulla reazione a tali dati in un programma.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Comprensione e interpretazione dei valori di Lusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05b4bc9c3efa73f91d54a9c88231180ec2807964b753e175bc13755b54c2743
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126537"
---
# <a name="understanding-and-interpreting-lux-values"></a>Comprensione e interpretazione dei valori di Lusso

Il tipo di dati principale del sensore per i sensori di luce ambientale è l'illuminazione in lume per metro quadrato. I principi descritti in questo argomento si basano sull'assunzione di valori di lusso come input e sulla reazione a tali dati in un programma.

Le letture di Lusso sono direttamente proporzionali all'energia per metro quadrato che viene consumata al secondo. La percezione umana dei livelli di luce non è così semplice. La percezione umana della luce è complessa perché gli occhi si regolano costantemente e altri processi biologico influiscono sulla percezione. È tuttavia possibile pensare a questa percezione da una prospettiva semplificata creando diversi intervalli di interesse con soglie superiori e inferiori note.

Il set di dati di esempio seguente rappresenta soglie approssimative per le condizioni di illuminazione comuni e il passaggio di illuminazione corrispondente. In questo caso, ogni passaggio di illuminazione rappresenta un cambiamento nell'ambiente di illuminazione.

> [!Note]  
> Questo set di dati è a scopo illustrativo e potrebbe non essere completamente accurato per tutti gli utenti o le situazioni.

 



| Condizione di illuminazione | Da (lux) | A (lusso) | Valore medio (lusso) | Passaggio di illuminazione |
|--------------------|------------|----------|------------------|---------------|
| Pitch Black        | 0          | 10       | 5                | 1             |
| Molto scuro          | 11         | 50       | 30               | 2             |
| Interni scuro       | 51         | 200      | 125              | 3             |
| Dim Indoors        | 201        | 400      | 300              | 4             |
| Normale all'interno     | 401        | 1000     | 700              | 5             |
| Bright Indoors     | 1001       | 5000     | 3000             | 6             |
| Dim Outdoors       | 5001       | 10,000   | 7500             | 7             |
| Cloudy Outdoors    | 10,001     | 30.000   | 20.000           | 8             |
| Luce solare diretta    | 30,001     | 100,000  | 65,000           | 9             |



 

Se si visualizzano questi dati usando i valori medio di questa tabella, si noterrà che la relazione tra lusso e illuminazione non è lineare, come illustrato nel grafico seguente.

![Grafico dell'illuminazione lineare](images/luxtostep.png)

Tuttavia, se si visualizzano questi dati usando una scala logaritmica sull'asse x, si può vedere che emerge una relazione approssimativamente lineare.

![grafico di illuminazione logaritmica](images/luxlogtostep.png)

### <a name="an-example-transform"></a>Trasformazione di esempio

In base al set di dati di esempio per i sensori di luce ambientale forniti in precedenza, è possibile arrivare all'equazione seguente per eseguire il mapping dei valori di lusso alla percezione umana. In questo esempio, i valori previsti sono da 0 a 1.000.000.000.

![Equazione del valore di lusso](images/sensor-lux-equation.jpg)

Questa equazione determina valori che variano in modo approssimativamente lineare tra 0,0 e 1,0. Questo risultato indica il modo in cui l'illuminazione percepita dall'utente è cambiata in base al set di dati di esempio mostrato in precedenza.

 

 



