---
description: È possibile considerare la trasformazione proiezione come il controllo degli elementi interni della fotocamera; è analogo alla scelta di una lente per la fotocamera.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Trasformazione proiezione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225421"
---
# <a name="projection-transform-direct3d-9"></a>Trasformazione proiezione (Direct3D 9)

È possibile considerare la trasformazione proiezione come il controllo degli elementi interni della fotocamera; è analogo alla scelta di una lente per la fotocamera. Questo è il più complesso dei tre tipi di trasformazione. Questa discussione sulla trasformazione proiezione è organizzata negli argomenti seguenti.

La matrice di proiezione è in genere una proiezione di scala e prospettiva. La trasformazione proiezione converte il tronco di visualizzazione in una forma Cuboid. Poiché la fine del tronco di visualizzazione è inferiore alla fine, questo ha l'effetto di espandere gli oggetti vicini alla fotocamera; Questo è il modo in cui la prospettiva viene applicata alla scena.

Nel [tronco di visualizzazione](viewports-and-clipping.md), la distanza tra la camera e l'origine dello spazio di trasformazione di visualizzazione è definita arbitrariamente come D, quindi la matrice di proiezione è simile alla figura seguente.

![illustrazione della matrice di proiezione](images/projmat1.png)

La matrice di visualizzazione converte la fotocamera nell'origine traducendo in z Direction by-D. La matrice di traslazione è simile alla figura seguente.

![illustrazione della matrice di traslazione](images/projmat2.png)

La moltiplicazione della matrice di traslazione da parte della matrice di proiezione (T \* P) fornisce la matrice di proiezione composita, come illustrato nella figura seguente.

![illustrazione della matrice di proiezione composita](images/projmat3.png)

La trasformazione prospettiva converte un tronco di visualizzazione in un nuovo spazio delle coordinate. Si noti che tronco diventa Cuboid e anche che l'origine si sposta dall'angolo superiore destro della scena al centro, come illustrato nel diagramma seguente.

![diagramma del modo in cui la trasformazione prospettiva modifica il tronco di visualizzazione in un nuovo spazio delle coordinate](images/cuboid.png)

Nella trasformazione prospettiva i limiti delle direzioni x e y sono-1 e 1. I limiti della direzione z sono 0 per il piano anteriore e 1 per il piano posteriore.

Questa matrice converte e ridimensiona gli oggetti in base a una distanza specificata dalla fotocamera al piano di ritaglio vicino, ma non considera il campo di visualizzazione (FOV) e i valori z che produce per gli oggetti nella distanza possono essere quasi identici, rendendo difficili i confronti di profondità. La matrice seguente risolve questi problemi e regola i vertici per tenere conto delle proporzioni del viewport, rendendola una scelta ottimale per la proiezione prospettica.

![illustrazione di una matrice per la proiezione prospettica](images/prjmatx1.png)

In questa matrice, Zn è il valore z del piano di ritaglio vicino. Le variabili w, h e Q hanno i significati seguenti. Si noti che FOV<sub>w</sub> e fovk rappresentano i campi di visualizzazione orizzontali e verticali del viewport, in radianti.

![equazioni del significato delle variabili](images/prjmatx2.png)

Per l'applicazione, l'uso di angoli di campo per la visualizzazione per definire i coefficienti di ridimensionamento x e y potrebbe non essere così comodo come usare le dimensioni orizzontali e verticali del viewport (nello spazio della fotocamera). Quando la matematica funziona, le due equazioni seguenti per w e h utilizzano le dimensioni del viewport e sono equivalenti alle equazioni precedenti.

![equazioni dei significati delle variabili w e h](images/prjmatx3.png)

In queste formule, Zn rappresenta la posizione del piano di ritaglio vicino e le variabili V<sub>w</sub> e VH rappresentano la larghezza e l'altezza del viewport, nello spazio fotocamera.

Per un'applicazione C++, queste due dimensioni corrispondono direttamente ai membri Width e Height della struttura [**D3DVIEWPORT9**](d3dviewport9.md) .

Indipendentemente dalla formula che si decide di usare, assicurarsi di impostare Zn sul valore più grande possibile, perché i valori z estremamente vicini alla fotocamera non variano molto. In questo modo si semplificano i confronti con i buffer z a 16 bit piuttosto complicati.

Come per le trasformazioni World e View, è possibile chiamare il metodo [**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) per impostare la trasformazione di proiezione.

## <a name="setting-up-a-projection-matrix"></a>Impostazione di una matrice di proiezione

La funzione di esempio ProjectionMatrix seguente imposta i piani di ritaglio anteriore e posteriore, nonché il campo orizzontale e verticale degli angoli di visualizzazione. I campi della visualizzazione devono essere minori di pi greco radianti.


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



Dopo aver creato la matrice, impostarla con [**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specificando la \_ proiezione D3DTS.

La libreria di utilità D3DX fornisce le funzioni seguenti che consentono di configurare la matrice di proiezione.

-   [**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
-   [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
-   [**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
-   [**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
-   [**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
-   [**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a>Matrice di proiezione facile da W

Direct3D può usare il componente w di un vertice che è stato trasformato dalle matrici World, View e Projection per eseguire calcoli basati sulla profondità negli effetti di nebbia o di buffer di profondità. I calcoli, ad esempio, richiedono che la matrice di proiezione normalizzare w sia equivalente allo spazio globale z. In breve, se la matrice di proiezione include un coefficiente (3, 4) diverso da 1, è necessario ridimensionare tutti i coefficienti in base all'inverso del coefficiente (3,4) per creare una matrice corretta. Se non si specifica una matrice conforme, gli effetti della nebbia e il buffer di profondità non vengono applicati correttamente.

Nella figura seguente è illustrata una matrice di proiezione non conforme e la stessa matrice è stata ridimensionata in modo da abilitare la nebbia relativa all'occhio.

![illustrazioni di una matrice di proiezione non conforme e una matrice con la nebbia relativa agli occhi](images/eyerlmx.png)

Nelle matrici precedenti, si presuppone che tutte le variabili siano diversi da zero. Per altre informazioni sulla nebbia relativa agli occhi, vedere [profondità basata sull'occhio](pixel-fog.md)rispetto alla Z. Per informazioni sul buffer di profondità basato su w, vedere [buffer di profondità (Direct3D 9)](depth-buffers.md).

Direct3D usa la matrice di proiezione attualmente impostata nei calcoli di profondità basati su w. Di conseguenza, le applicazioni devono impostare una matrice di proiezione conforme per ricevere le funzionalità basate su w desiderate, anche se non usano Direct3D per le trasformazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni](transforms.md)
</dt> </dl>

 

 
