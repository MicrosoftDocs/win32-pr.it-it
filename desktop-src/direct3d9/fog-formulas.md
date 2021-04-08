---
description: Le applicazioni C++ possono controllare il modo in cui la nebbia influisce sul colore degli oggetti in una scena modificando il modo in cui Microsoft Direct3D calcola gli effetti della nebbia rispetto alla distanza.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Formule Fog (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876402"
---
# <a name="fog-formulas-direct3d-9"></a>Formule Fog (Direct3D 9)

Le applicazioni C++ possono controllare il modo in cui la nebbia influisce sul colore degli oggetti in una scena modificando il modo in cui Microsoft Direct3D calcola gli effetti della nebbia rispetto alla distanza. Il tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) contiene membri che identificano le tre formule di nebbia. Tutte le formule calcolano un fattore di nebbia come funzione di distanza, dati i parametri impostati dall'applicazione.

## <a name="linear-fog"></a>Nebbia lineare

Viene impostato con l' \_ equazione lineare D3DFOG seguente.

![equazione della nebbia lineare Direct3D](images/fogliner.png)

dove

-   Start è la distanza con cui iniziano gli effetti di nebbia.
-   End è la distanza con cui gli effetti della nebbia non aumentano più.
-   d rappresenta la profondità o la distanza dal punto di vista. Per la nebbia basata sull'intervallo, il valore di d è la distanza tra la posizione della fotocamera e un vertice. Per la nebbia non basata sull'intervallo, il valore di d è il valore assoluto della coordinata Z nello spazio della fotocamera.

## <a name="exponential-fog"></a>Nebbia esponenziale

Le formule lineare ed esponenziale sono supportate sia per la nebbia dei pixel che per il vertice.

Questa impostazione viene impostata con l' \_ equazione exp D3DFOG seguente.

![equazione della nebbia esponenziale Direct3D](images/fogexp.png)

dove

-   e è la base dei logaritmi naturali (approssimativamente 2,71828).
-   la densità è una densità di nebbia arbitraria che può variare da 0,0 a 1,0.
-   d rappresenta la profondità o la distanza dal punto di vista, come indicato in precedenza.

Questa impostazione viene impostata con l' \_ equazione D3DFOG exp2 seguente.

![equazione di Direct3D esponenziale 2 Fog](images/fogexp2.png)

dove

-   e è la base dei logaritmi naturali come indicato sopra.
-   la densità è una densità di nebbia arbitraria che può variare da 0,0 a 1,0 come indicato sopra.
-   d rappresenta la profondità o la distanza dal punto di vista, come indicato sopra.

> [!Note]  
> Il sistema archivia il fattore di nebbia nel componente alfa del colore speculare per un vertice. Se l'applicazione esegue una trasformazione e un'illuminazione proprie, è possibile inserire manualmente i valori del fattore di nebbia, che verranno applicati dal sistema durante il rendering.

 

Il grafico seguente mostra queste formule, usando i valori comuni come nei parametri della formula.

![grafico delle formule di nebbia rispetto alla distanza e alla quantità di colore](images/foggraph.png)

D3DFOG \_ Linear è 1,0 all'inizio e 0,0 alla fine. Non viene misurato in relazione ai piani vicini o lontani.

Quando Direct3D calcola gli effetti di nebbia, usa il fattore di nebbia di una delle equazioni precedenti nell'equazione di fusione seguente.

![equazione degli effetti di nebbia per Direct3D](images/fogcalc.png)

Questa formula ridimensiona in modo efficace il colore del poligono corrente C per il fattore di nebbia f e aggiunge il prodotto al colore di nebbia C, ridimensionato dall'inverso bit per bit del fattore di nebbia. Il valore di colore risultante è una combinazione del colore di nebbia e del colore originale, come fattore di distanza. La formula si applica a tutti i dispositivi supportati in Microsoft DirectX 7,0 e versioni successive. Per il dispositivo ramp legacy, il fattore di nebbia ridimensiona i componenti del colore speculare e diffuso, che vengono fissati nell'intervallo tra 0,0 e 1,0 inclusi. Il fattore di nebbia inizia in genere a 1,0 per il piano vicino e viene ridotto a 0,0 sul piano lontano.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di nebbia](fog-types.md)
</dt> </dl>

 

 
