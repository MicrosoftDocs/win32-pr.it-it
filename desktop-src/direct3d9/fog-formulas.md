---
description: Le applicazioni C++ possono controllare in che modo la nebbia influisce sul colore degli oggetti in una scena modificando il modo in cui Microsoft Direct3D calcola gli effetti della nebbia sulla distanza.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Formule di osanna (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac92b6d00ff5f4d4ec03dbe7bb40365917f8b835fd121cdc934c470c45c38814
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027001"
---
# <a name="fog-formulas-direct3d-9"></a>Formule di osanna (Direct3D 9)

Le applicazioni C++ possono controllare in che modo la nebbia influisce sul colore degli oggetti in una scena modificando il modo in cui Microsoft Direct3D calcola gli effetti della nebbia sulla distanza. Il [**tipo enumerato D3DFOGMODE**](./d3dfogmode.md) contiene membri che identificano le tre formule della nebbia. Tutte le formule calcolano un fattore di nebbia come funzione della distanza, dati i parametri che l'applicazione imposta.

## <a name="linear-fog"></a>Sfumatura lineare

Questa opzione viene impostata con l'equazione D3DFOG \_ LINEAR seguente.

![equazione di direct3d linear osa](images/fogliner.png)

dove

-   start è la distanza da cui iniziano gli effetti della nebbia.
-   end è la distanza alla quale gli effetti della nebbia non aumentano più.
-   d rappresenta la profondità o la distanza dal punto di vista. Per la nebbia basata sull'intervallo, il valore di d è la distanza tra la posizione della fotocamera e un vertice. Per la nebbia non basata sull'intervallo, il valore di d è il valore assoluto della coordinata Z nello spazio della fotocamera.

## <a name="exponential-fog"></a>Nebbiosa esponenziale

Le formule lineari ed esponenziali sono supportate sia per la nebbia pixel che per la nebbia dei vertici.

Questa opzione viene impostata con l'equazione D3DFOG \_ EXP seguente.

![equazione di direct3d exponential osa](images/fogexp.png)

dove

-   e è la base dei logaritmi naturali (circa 2,71828).
-   densità è una densità di nebbia arbitraria che può variare da 0,0 a 1,0.
-   d rappresenta la profondità o la distanza dal punto di vista, come indicato in precedenza.

Questo valore viene impostato con l'equazione D3DFOG \_ EXP2 seguente.

![equazione di direct3d esponenziale 2 osa](images/fogexp2.png)

dove

-   e è la base dei logaritmi naturali, come indicato in precedenza.
-   densità è una densità di nebbia arbitraria che può variare da 0,0 a 1,0, come indicato in precedenza.
-   d rappresenta la profondità o la distanza dal punto di vista, come indicato in precedenza.

> [!Note]  
> Il sistema archivia il fattore di nebbia nel componente alfa del colore speculare per un vertice. Se l'applicazione esegue la propria trasformazione e illuminazione, è possibile inserire manualmente i valori dei fattori di nebbia, che devono essere applicati dal sistema durante il rendering.

 

Il grafico seguente mostra queste formule, usando valori comuni come nei parametri della formula.

![grafico delle formule della nebbia su distanza e quantità di colore](images/foggraph.png)

D3DFOG \_ LINEAR è 1.0 all'inizio e 0.0 alla fine. Non viene misurata rispetto ai piani vicini o lontani.

Quando Direct3D calcola gli effetti della fusa, usa il fattore nebbia di una delle equazioni precedenti nell'equazione di fusione seguente.

![equazione degli effetti della nebbia per direct3d](images/fogcalc.png)

Questa formula ridimensiona in modo efficace il colore del poligono C corrente in base al fattore nebbia f e aggiunge il prodotto al colore della nebbia C, ridimensionato in base all'inverso bit per bit del fattore di nebbia. Il valore del colore risultante è una combinazione del colore della nebbia e del colore originale, come fattore di distanza. La formula si applica a tutti i dispositivi supportati in Microsoft DirectX 7.0 e versioni successive. Per il dispositivo di rampa legacy, il fattore di nebbia ridimensiona i componenti di colore diffusi e speculari, con un'estensione compresa tra 0,0 e 1,0, inclusi. Il fattore di nebbia inizia in genere da 1,0 per il piano vicino e diminuisce a 0,0 nel piano lontano.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di nebbia](fog-types.md)
</dt> </dl>

 

 
