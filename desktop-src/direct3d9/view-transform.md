---
description: In questa sezione vengono introdotti i concetti di base della trasformazione visualizzazione e vengono fornite informazioni dettagliate su come configurare una matrice di trasformazione visualizzazione in un'applicazione Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Visualizzazione trasformazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521906"
---
# <a name="view-transform-direct3d-9"></a>Visualizzazione trasformazione (Direct3D 9)

In questa sezione vengono introdotti i concetti di base della trasformazione visualizzazione e vengono fornite informazioni dettagliate su come configurare una matrice di trasformazione visualizzazione in un'applicazione Direct3D.

La trasformazione visualizzazione individua il visualizzatore nello spazio globale, trasformando i vertici nello spazio della fotocamera. Nello spazio della fotocamera, la fotocamera o il visualizzatore si trova all'origine, osservando la direzione della z positiva. Si ricordi che Direct3D usa un sistema di coordinate a sinistra, quindi la z è positiva in una scena. La matrice di visualizzazione Riloca gli oggetti nel mondo intorno alla posizione della fotocamera, ovvero l'origine dello spazio della fotocamera e l'orientamento.

Esistono diversi modi per creare una matrice di viste. In tutti i casi, la fotocamera ha una posizione e un orientamento logici nello spazio globale usato come punto di partenza per creare una matrice di visualizzazione che verrà applicata ai modelli in una scena. La matrice di visualizzazione converte e ruota gli oggetti in modo da posizionarli nello spazio della fotocamera, in cui la fotocamera è all'origine. Un modo per creare una matrice di viste consiste nel combinare una matrice di traslazione con matrici di rotazione per ogni asse. In questo approccio viene applicata la seguente equazione della matrice generale.

![equazione della trasformazione visualizzazione](images/viewtran.png)

In questa formula, V è la matrice di visualizzazione da creare, T è una matrice di traslazione che riposiziona gli oggetti nel mondo e R ₓ tramite R<sub>z</sub> sono matrici di rotazione che ruotano gli oggetti lungo l'asse x, y e z. Le matrici di traslazione e rotazione sono basate sulla posizione logica e sull'orientamento della fotocamera nello spazio globale. Quindi, se la posizione logica della fotocamera nel mondo è <10, 20100>, l'obiettivo della matrice di traslazione è spostare gli oggetti-10 unità lungo l'asse x,-20 unità lungo l'asse y e-100 unità lungo l'asse z. Le matrici di rotazione nella formula sono basate sull'orientamento della fotocamera, in termini di quanto gli assi dello spazio della fotocamera vengono ruotati dall'allineamento allo spazio globale. Ad esempio, se la fotocamera indicata in precedenza punta verso il basso, l'asse z è 90 gradi (pi/2 radianti) dall'allineamento con l'asse z dello spazio globale, come illustrato nella figura seguente.

![illustrazione dello spazio di visualizzazione della fotocamera rispetto allo spazio globale](images/camtop.png)

Le matrici di rotazione applicano le rotazioni di uguale, ma opposto, alla grandezza dei modelli nella scena. La matrice di visualizzazione per questa fotocamera include una rotazione di-90 gradi intorno all'asse x. La matrice di rotazione viene combinata con la matrice di traslazione per creare una matrice di visualizzazione che consente di regolare la posizione e l'orientamento degli oggetti nella scena in modo che la parte superiore si trovi davanti alla fotocamera, fornendo l'aspetto che la fotocamera è sopra il modello.

## <a name="setting-up-a-view-matrix"></a>Impostazione di una matrice di visualizzazione

Le funzioni di supporto [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) e [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) creano una matrice di viste basata sulla posizione della fotocamera e un punto di ricerca.

Nell'esempio seguente viene creata una matrice di viste per le coordinate di sinistra.


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



Direct3D usa le matrici World e View per configurare diverse strutture di dati interne. Ogni volta che si imposta una nuova matrice World o View, il sistema ricalcola le strutture interne associate. L'impostazione frequente di queste matrici è un calcolo che richiede molto tempo. È possibile ridurre al minimo il numero di calcoli necessari concatenando il mondo e visualizzare le matrici in una matrice di visualizzazione globale impostata come matrice globale e quindi impostando la matrice di visualizzazione sull'identità. Mantieni le copie memorizzate nella cache di singole matrici di mondo e di visualizzazione che puoi modificare, concatenare e reimpostare la matrice globale in base alle esigenze. Per maggiore chiarezza, i campioni utilizzano raramente questa ottimizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni](transforms.md)
</dt> </dl>

 

 



