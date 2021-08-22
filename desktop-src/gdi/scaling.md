---
description: La maggior parte delle applicazioni CAD e di disegno offre funzionalità che ridimensionano l'output creato dall'utente.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Scalabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf8cb7293be4083c08de1d104bb8349b3cd5003a0abddf77d41922cfb294cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965241"
---
# <a name="scaling"></a>Scalabilità

La maggior parte delle applicazioni CAD e di disegno offre funzionalità che ridimensionano l'output creato dall'utente. Le applicazioni che includono funzionalità di ridimensionamento (o zoom) chiamano la [**funzione SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare lo spazio globale appropriato per la trasformazione dello spazio della pagina. Questa funzione riceve un puntatore a una [**struttura XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) contenente i valori appropriati. I membri eM11 ed eM22 di XFORM specificano rispettivamente i componenti di scalabilità orizzontale e verticale.

Quando *si* verifica il ridimensionamento, le linee verticali e orizzontali (o vettori), che costituiscono un oggetto, vengono allungate o compresse rispetto all'asse x o y. La figura seguente mostra un rettangolo di 20 per 20 unità ridimensionato verticalmente fino al doppio dell'altezza originale quando viene copiato dallo spazio delle coordinate del mondo allo spazio delle coordinate di pagina.

![illustrazione che mostra un piccolo rettangolo nello spazio del mondo e uno più alto nello spazio della pagina](images/cstrn-10.png)

Nella figura precedente le linee verticali che definiscono il lato del rettangolo originale misurano 20 unità, mentre le linee verticali che definiscono i lati del rettangolo ridimensionato misurano 40 unità.

Il ridimensionamento verticale può essere rappresentato dall'algoritmo seguente.

``` syntax
y' = y * Dy 
```

Dove y' è la nuova lunghezza, y è la lunghezza originale e Dy è il fattore di scala verticale.

La scalabilità orizzontale può essere rappresentata dall'algoritmo seguente.

``` syntax
x' = x * Dx 
```

Dove x' è la nuova lunghezza, x è la lunghezza originale e Dx è il fattore di scala orizzontale.

Le trasformazioni di scalabilità verticale e orizzontale possono essere combinate in un'unica operazione usando una matrice 2 per 2.

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

La matrice 2 per 2 che ha prodotto la trasformazione di ridimensionamento contiene i valori seguenti.

``` syntax
|1    0| 
|0    2| 
```

 

 



