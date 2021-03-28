---
description: La maggior parte delle applicazioni di disegno e CAD fornisce funzionalità per la scalabilità dell'output creato dall'utente.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Scalabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980303"
---
# <a name="scaling"></a>Scalabilità

La maggior parte delle applicazioni di disegno e CAD fornisce funzionalità per la scalabilità dell'output creato dall'utente. Le applicazioni che includono funzionalità di scalabilità (o zoom) chiamano la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare lo spazio globale appropriato sulla trasformazione dello spazio pagina. Questa funzione [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati. I membri eM11 e eM22 di l'oggetto di controllo di stato specificano rispettivamente i componenti di scalabilità orizzontale e verticale.

Quando si verifica il *ridimensionamento* , le linee verticali e orizzontali (o vettori), che costituiscono un oggetto, sono allungate o compresse rispetto all'asse x o y. La figura seguente mostra un rettangolo di 20 unità, ridimensionato verticalmente, al doppio dell'altezza originale quando viene copiato dallo spazio delle coordinate internazionali allo spazio delle coordinate di pagina.

![illustrazione che mostra un piccolo rettangolo nello spazio globale e uno più alto nello spazio della pagina](images/cstrn-10.png)

Nell'illustrazione precedente, le linee verticali che definiscono la misura laterale del rettangolo originale 20 unità, mentre le linee verticali che definiscono i lati del rettangolo ridimensionato misurano 40 unità.

La scalabilità verticale può essere rappresentata dall'algoritmo seguente.

``` syntax
y' = y * Dy 
```

Dove y è la nuova lunghezza, y è la lunghezza originale e dy è il fattore di scala verticale.

La scalabilità orizzontale può essere rappresentata dall'algoritmo seguente.

``` syntax
x' = x * Dx 
```

Dove x ' è la nuova lunghezza, x è la lunghezza originale e DX è il fattore di scala orizzontale.

Le trasformazioni di scala verticale e orizzontale possono essere combinate in una singola operazione usando una matrice 2 per 2.

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

La matrice 2 per 2 che ha prodotto la trasformazione di ridimensionamento contiene i valori seguenti.

``` syntax
|1    0| 
|0    2| 
```

 

 



