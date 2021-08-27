---
description: Questa sezione presenta i concetti di base della trasformazione visualizzazione e fornisce informazioni dettagliate su come configurare una matrice di trasformazione della visualizzazione in un'applicazione Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Trasformazione Visualizzazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb184cb75f84a1d28ed6f03f2e65113ea65292fd6ca1871d517d472614f64a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118533"
---
# <a name="view-transform-direct3d-9"></a>Trasformazione Visualizzazione (Direct3D 9)

Questa sezione presenta i concetti di base della trasformazione visualizzazione e fornisce informazioni dettagliate su come configurare una matrice di trasformazione della visualizzazione in un'applicazione Direct3D.

La trasformazione della visualizzazione individua il visualizzatore nello spazio del mondo, trasformando i vertici nello spazio della fotocamera. Nello spazio della fotocamera, la fotocamera o il visualizzatore si trova all'origine, osservando la direzione z positiva. Si ricordi che Direct3D usa un sistema di coordinate mancino, quindi z è positivo in una scena. La matrice di visualizzazione riloca gli oggetti nel mondo intorno alla posizione di una fotocamera, l'origine dello spazio della fotocamera, e all'orientamento.

Esistono diversi modi per creare una matrice di visualizzazione. In tutti i casi, la fotocamera ha una posizione logica e un orientamento nello spazio globale che viene usato come punto di partenza per creare una matrice di visualizzazione che verrà applicata ai modelli in una scena. La matrice di visualizzazione trasla e ruota gli oggetti per posizionarli nello spazio della fotocamera, dove la fotocamera si trova all'origine. Un modo per creare una matrice di visualizzazione è combinare una matrice di traslazione con matrici di rotazione per ogni asse. In questo approccio si applica l'equazione di matrice generale seguente.

![equazione della trasformazione della visualizzazione](images/viewtran.png)

In questa formula V è la matrice di visualizzazione da creare, T è una matrice di traslazione che riposiziona gli oggetti nel mondo e Rₓ tramite R<sub>z</sub> sono matrici di rotazione che ruotano gli oggetti lungo gli assi x, y e z. Le matrici di traslazione e rotazione si basano sulla posizione logica e sull'orientamento della fotocamera nello spazio del mondo. Pertanto, se la posizione logica della fotocamera nel mondo è <10.20.100>, l'obiettivo della matrice di traslazione è spostare gli oggetti -10 unità lungo l'asse x, -20 unità lungo l'asse y e -100 unità lungo l'asse z. Le matrici di rotazione nella formula sono basate sull'orientamento della fotocamera, in termini di quanto gli assi dello spazio della fotocamera vengono ruotati all'esterno dell'allineamento con lo spazio del mondo. Ad esempio, se la fotocamera citata in precedenza è diretta verso il basso, l'asse z è di 90 gradi (pi greco/2 radianti) non allineato all'asse z dello spazio del mondo, come illustrato nella figura seguente.

![illustrazione dello spazio di visualizzazione della fotocamera rispetto allo spazio del mondo](images/camtop.png)

Le matrici di rotazione applicano rotazioni di grandezza uguale, ma opposta, ai modelli nella scena. La matrice di visualizzazione per questa fotocamera include una rotazione di -90 gradi intorno all'asse x. La matrice di rotazione viene combinata con la matrice di traslazione per creare una matrice di visualizzazione che regola la posizione e l'orientamento degli oggetti nella scena in modo che la parte superiore sia rivolta verso la fotocamera, dando l'aspetto che la fotocamera si trova sopra il modello.

## <a name="setting-up-a-view-matrix"></a>Impostazione di una matrice di visualizzazione

Le funzioni helper [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) e [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) creano una matrice di visualizzazione in base alla posizione della fotocamera e a un punto di sguardo.

Nell'esempio seguente viene creata una matrice di visualizzazione per le coordinate mancino.


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



Direct3D usa le matrici world e view per configurare diverse strutture di dati interne. Ogni volta che si imposta una nuova matrice globale o di visualizzazione, il sistema ricalcola le strutture interne associate. L'impostazione frequente di queste matrici richiede molto tempo a livello di calcolo. È possibile ridurre al minimo il numero di calcoli necessari concatenando il mondo e visualizzando le matrici in una matrice di visualizzazione globale impostata come matrice globale e quindi impostando la matrice di visualizzazione sull'identità. Conservare le copie memorizzate nella cache di singole matrici di mondo e visualizzare le matrici che è possibile modificare, concatenare e reimpostare la matrice globale in base alle esigenze. Per maggiore chiarezza, gli esempi raramente utilizzano questa ottimizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni](transforms.md)
</dt> </dl>

 

 



