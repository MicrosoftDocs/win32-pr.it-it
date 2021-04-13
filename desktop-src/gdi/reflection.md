---
description: Alcune applicazioni forniscono funzionalità che riflettono gli oggetti (o mirror) disegnati nell'area client.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Reflection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978354"
---
# <a name="reflection"></a>Reflection

Alcune applicazioni forniscono funzionalità che riflettono gli oggetti (o mirror) disegnati nell'area client. Le applicazioni che contengono funzionalità di Reflection usano la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare i valori appropriati nello spazio globale sulla trasformazione dello spazio pagina. Questa funzione [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati. I membri eM11 e eM22 di l'oggetto di controllo di stato specificano rispettivamente i componenti di Reflection orizzontale e verticale.

La *trasformazione Reflection* crea un'immagine speculare di un oggetto in relazione all'asse x o y. In breve, la reflection è solo una scala negativa. Per produrre una reflection orizzontale, le coordinate x vengono moltiplicate per 1. Per produrre una reflection verticale, le coordinate y vengono moltiplicate per 1.

La reflection orizzontale può essere rappresentata dall'algoritmo seguente:

``` syntax
x' = -x 
```

dove x è la coordinata x e x ' è il risultato della reflection.

La matrice 2 per 2 che ha prodotto la reflection orizzontale contiene i valori seguenti:

``` syntax
|-1    0| 
|0     1| 
```

La reflection verticale può essere rappresentata dall'algoritmo seguente:

``` syntax
y' = -y 
```

dove y è la coordinata y e y "è il risultato della reflection.

La matrice 2 per 2 che ha prodotto la reflection verticale contiene i valori seguenti:

``` syntax
|1    0| 
|0   -1| 
```

Le operazioni di Reflection orizzontale e verticale possono essere combinate in una singola operazione usando la matrice 2-by-2 seguente:

``` syntax
|-1    0| 
|0    -1| 
```

 

 



