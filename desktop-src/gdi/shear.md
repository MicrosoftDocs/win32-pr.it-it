---
description: Alcune applicazioni forniscono funzionalità che consentono di trasliare gli oggetti disegnati nell'area client.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Taglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32edb9484fd8bb2a9da15220b0acf39fd5c44c50091551205022c6458b50d4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092631"
---
# <a name="shear"></a>Taglio

Alcune applicazioni forniscono funzionalità che consentono di trasliare gli oggetti disegnati nell'area client. Le applicazioni che usano funzionalità di shear usano la [**funzione SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare i valori appropriati nello spazio globale per la trasformazione dello spazio della pagina. Questa funzione riceve un puntatore a una [**struttura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) contenente i valori appropriati. I membri eM12 ed eM21 di XFORM specificano rispettivamente le costanti di proporzionalità orizzontale e verticale.

Sono disponibili due componenti della *trasformazione della barra.* La prima modifica le linee verticali in un oggetto . il secondo modifica le linee orizzontali. La figura seguente mostra un rettangolo di 20 per 20 unità di cui è stata eseparata la sezione orizzontale quando viene copiato dallo spazio del mondo allo spazio della pagina.

![illustrazione che mostra un rettangolo nello spazio del mondo e un trapezio nello spazio della pagina](images/cstrn-13.png)

Una sezione orizzontale può essere rappresentata dall'algoritmo seguente:

``` syntax
x' = x + (Sx * y) 
```

dove x è la coordinata x originale, Sx è la costante di proporzionalità e x' è il risultato della trasformazione della barra.

Una sezione verticale può essere rappresentata dall'algoritmo seguente:

``` syntax
y' = y + (Sy * x) 
```

dove y è la coordinata y originale, Sy è la costante di proporzionalità e y' è il risultato della trasformazione della barra.

Le trasformazioni di sessazione orizzontale e verticale possono essere combinate in un'unica operazione usando una matrice 2 per 2.

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

La matrice 2 per 2 che ha prodotto la sezione contiene i valori seguenti:

``` syntax
|1    1| 
|0    1| 
```

 

 



