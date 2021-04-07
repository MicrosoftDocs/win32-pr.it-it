---
description: Il tipo di dati del sensore primario per i sensori di luce di ambiente è illuminato in Lux (lumen per metro quadrato). I principi descritti in questo argomento si basano sull'assunzione di valori Lux come input e sulla reazione a tali dati in un programma.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Informazioni e interpretazione dei valori Lux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057870"
---
# <a name="understanding-and-interpreting-lux-values"></a>Informazioni e interpretazione dei valori Lux

Il tipo di dati del sensore primario per i sensori di luce di ambiente è illuminato in Lux (lumen per metro quadrato). I principi descritti in questo argomento si basano sull'assunzione di valori Lux come input e sulla reazione a tali dati in un programma.

Le letture Lux sono direttamente proporzionali all'energia per ogni metro quadrato assorbita al secondo. La percezione umana dei livelli di luce non è così semplice. La percezione umana della luce è complessa perché i nostri occhi sono costantemente regolabili e altri processi biologici influiscono sulla nostra percezione. Tuttavia, è possibile pensare a questa percezione da una prospettiva semplificata creando diversi intervalli di interesse con soglie note superiori e inferiori.

Il set di dati di esempio seguente rappresenta le soglie approssimative per le condizioni di illuminazione comuni e il passaggio di illuminazione corrispondente. In questo caso, ogni passaggio di illuminazione rappresenta una modifica nell'ambiente di illuminazione.

> [!Note]  
> Questo set di dati è a illustrazione e potrebbe non essere completamente accurato per tutti gli utenti o le situazioni.

 



| Condizione di illuminazione | Da (LUX) | A (LUX) | Valore medio (LUX) | Passaggio di illuminazione |
|--------------------|------------|----------|------------------|---------------|
| Pitch nero        | 0          | 10       | 5                | 1             |
| Molto scuro          | 11         | 50       | 30               | 2             |
| Interni scuri       | 51         | 200      | 125              | 3             |
| Dim-door        | 201        | 400      | 300              | 4             |
| Normale interno     | 401        | 1000     | 700              | 5             |
| Interni luminosi     | 1001       | 5000     | 3000             | 6             |
| Dim all'esterno       | 5001       | 10,000   | 7500             | 7             |
| Cloud all'esterno    | 10.001     | 30.000   | 20.000           | 8             |
| Luce solare diretta    | 30.001     | 100,000  | 65.000           | 9             |



 

Se si visualizzano questi dati usando i valori medi di questa tabella, si noterà che la relazione Lux-to-Lighting-Step non è lineare, come illustrato nel grafico seguente.

![grafico di illuminazione lineare](images/luxtostep.png)

Tuttavia, se si visualizzano questi dati utilizzando una scala logaritmica sull'asse x, è possibile notare che emerge una relazione approssimativamente lineare.

![grafico di illuminazione logaritmica](images/luxlogtostep.png)

### <a name="an-example-transform"></a>Trasformazione di esempio

In base al set di dati di esempio per i sensori di luce di ambiente forniti in precedenza, è possibile arrivare all'equazione seguente per eseguire il mapping dei valori Lux alla percezione umana. In questo esempio, i valori previsti variano da 0 Lux a 1 milione Lux.

![equazione valore LUX](images/sensor-lux-equation.jpg)

Questa equazione restituisce valori che variano in modo approssimativamente lineare tra 0,0 e 1,0. Questo risultato indica il modo in cui l'illuminazione percepita dall'uomo è cambiata in base al set di dati di esempio illustrato in precedenza.

 

 



