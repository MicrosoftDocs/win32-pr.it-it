---
description: Alcune applicazioni traducono o spostano oggetti disegnati nell'area client.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Traduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987655"
---
# <a name="translation"></a>Traduzione

Alcune applicazioni traducono o spostano oggetti disegnati nell'area client. chiamando la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare lo spazio globale appropriato sulla trasformazione dello spazio pagina. La funzione SetWorldTransform [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati. I membri di eDx e eDy del controllo di stato specificano rispettivamente i componenti di traduzione orizzontale e verticale.

Quando si verifica la *conversione* , ogni punto in un oggetto viene spostato verticalmente, orizzontalmente o entrambi, in base a una quantità specificata. Nella figura seguente viene illustrato un rettangolo di 20 unità che è stato convertito a destra di 10 unità quando viene copiato dallo spazio delle coordinate internazionali allo spazio delle coordinate di pagina.

![illustrazione che mostra un rettangolo in una posizione nello spazio globale e in una posizione diversa nello spazio della pagina](images/cstrn-09.png)

Nell'illustrazione precedente, la coordinata x di ogni punto nel rettangolo è 10 unità maggiore della coordinata x originale.

La traduzione orizzontale può essere rappresentata dall'algoritmo seguente.

``` syntax
x' = x + Dx 
```

Dove x è la nuova coordinata x, x è la coordinata x originale e DX è la distanza orizzontale spostata.

La conversione verticale può essere rappresentata dall'algoritmo seguente.

``` syntax
y' = y + Dy 
```

Dove y è la nuova coordinata y, y è la coordinata y originale e dy è la distanza verticale spostata.

Le trasformazioni di traslazione orizzontali e verticali possono essere combinate in una singola operazione usando una matrice 3 per 3.

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

(Regole dello stato di moltiplicazione della matrice in cui il numero di righe di una matrice deve essere uguale al numero di colonne nell'altro. Il numero intero 1 nella matrice \| x y 1 \| è un segnaposto che è stato aggiunto per soddisfare questo requisito.

La matrice 3 per 3 che ha prodotto la trasformazione di conversione illustrata contiene i valori seguenti.

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



