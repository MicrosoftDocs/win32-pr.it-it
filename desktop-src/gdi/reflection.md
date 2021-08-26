---
description: Alcune applicazioni forniscono funzionalità che riflettono (o rispecchiano) gli oggetti disegnati nell'area client.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Reflection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03d872273e7d0b9f23d9ffb31c6304c8b59b59eda80c7181802120f89c0d764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092701"
---
# <a name="reflection"></a>Reflection

Alcune applicazioni forniscono funzionalità che riflettono (o rispecchiano) gli oggetti disegnati nell'area client. Le applicazioni che contengono funzionalità di reflection usano la [**funzione SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare i valori appropriati nello spazio globale sulla trasformazione dello spazio della pagina. Questa funzione riceve un puntatore a una [**struttura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) contenente i valori appropriati. I membri eM11 ed eM22 di XFORM specificano rispettivamente i componenti di reflection orizzontale e verticale.

La *trasformazione reflection* crea un'immagine speculare di un oggetto rispetto all'asse x o y. In breve, la reflection è semplicemente un ridimensionamento negativo. Per produrre una reflection orizzontale, le coordinate x vengono moltiplicate per 1. Per produrre una reflection verticale, le coordinate y vengono moltiplicate per 1.

La reflection orizzontale può essere rappresentata dall'algoritmo seguente:

``` syntax
x' = -x 
```

dove x è la coordinata x e x' è il risultato della reflection.

La matrice 2 per 2 che ha prodotto la reflection orizzontale contiene i valori seguenti:

``` syntax
|-1    0| 
|0     1| 
```

La reflection verticale può essere rappresentata dall'algoritmo seguente:

``` syntax
y' = -y 
```

dove y è la coordinata y e y' è il risultato della reflection.

La matrice 2 per 2 che ha prodotto la reflection verticale contiene i valori seguenti:

``` syntax
|1    0| 
|0   -1| 
```

Le operazioni di reflection orizzontale e reflection verticale possono essere combinate in un'unica operazione usando la matrice 2 per 2 seguente:

``` syntax
|-1    0| 
|0    -1| 
```

 

 



