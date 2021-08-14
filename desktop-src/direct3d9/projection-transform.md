---
description: È possibile pensare alla trasformazione della proiezione come al controllo degli elementi interni della fotocamera. è analogo alla scelta di una lente per la fotocamera.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Trasformazione proiezione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad15ee0f4d23401563a9a51b8767be3da6e47dfee9dc76d580154ef1d524d02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092689"
---
# <a name="projection-transform-direct3d-9"></a>Trasformazione proiezione (Direct3D 9)

È possibile pensare alla trasformazione della proiezione come al controllo degli elementi interni della fotocamera. è analogo alla scelta di una lente per la fotocamera. Si tratta del tipo di trasformazione più complesso tra i tre. Questa discussione sulla trasformazione della proiezione è organizzata negli argomenti seguenti.

La matrice di proiezione è in genere una proiezione di scala e prospettiva. La trasformazione di proiezione converte il frustum di visualizzazione in una forma cuboide. Poiché l'estremità più vicina del frustum di visualizzazione è più piccola dell'estremità più distante, ciò ha l'effetto di espandere gli oggetti che si avvicinano alla fotocamera; questa è la modalità di applicazione della prospettiva alla scena.

Nel [frustum](viewports-and-clipping.md)di visualizzazione la distanza tra la fotocamera e l'origine dello spazio di trasformazione di visualizzazione è definita arbitrariamente come D, quindi la matrice di proiezione è simile alla figura seguente.

![illustrazione della matrice di proiezione](images/projmat1.png)

La matrice di visualizzazione trasla la fotocamera nell'origine traslando nella direzione z di - D. La matrice di traslazione è simile alla figura seguente.

![illustrazione della matrice di traslazione](images/projmat2.png)

La moltiplicazione della matrice di traslazione per la matrice di proiezione (T P) fornisce la matrice di \* proiezione composita, come illustrato nella figura seguente.

![illustrazione della matrice di proiezione composita](images/projmat3.png)

La trasformazione prospettica converte un frustum di visualizzazione in un nuovo spazio delle coordinate. Si noti che il frustum diventa cuboide e che l'origine si sposta dall'angolo superiore destro della scena al centro, come illustrato nel diagramma seguente.

![diagramma del modo in cui la trasformazione della prospettiva modifica il frustum di visualizzazione in un nuovo spazio delle coordinate](images/cuboid.png)

Nella trasformazione prospettica i limiti delle direzioni x e y sono -1 e 1. I limiti della direzione z sono 0 per il piano anteriore e 1 per il piano posteriore.

Questa matrice trasla e ridimensiona gli oggetti in base a una distanza specificata dalla fotocamera al piano di ritaglio vicino, ma non considera il campo di visualizzazione (fov) e i valori z prodotti per gli oggetti in distanza possono essere quasi identici, rendendo difficili i confronti di profondità. La matrice seguente risolve questi problemi e regola i vertici per prendere in considerazione le proporzioni del viewport, rendendolo una scelta ottimale per la proiezione prospettica.

![illustrazione di una matrice per la proiezione prospettica](images/prjmatx1.png)

In questa matrice Zn è il valore z del piano di ritaglio vicino. Le variabili w, h e Q hanno i significati seguenti. Si noti che fov<sub>w</sub> e fovk rappresentano i campi di visualizzazione orizzontale e verticale del viewport, in radianti.

![equazioni dei significati delle variabili](images/prjmatx2.png)

Per l'applicazione, l'uso degli angoli del campo di visualizzazione per definire i coefficienti di ridimensionamento x e y potrebbe non essere pratico come l'uso delle dimensioni orizzontali e verticali del viewport (nello spazio della fotocamera). Mentre la matematica funziona, le due equazioni seguenti per w e h usano le dimensioni del viewport e sono equivalenti alle equazioni precedenti.

![equazioni dei significati delle variabili w e h](images/prjmatx3.png)

In queste formule Zn rappresenta la posizione del piano di ritaglio vicino e le variabili V<sub>w</sub> e Vh rappresentano la larghezza e l'altezza del viewport, nello spazio della fotocamera.

Per un'applicazione C++, queste due dimensioni corrispondono direttamente ai membri Width e Height della [**struttura D3DVIEWPORT9.**](d3dviewport9.md)

Indipendentemente dalla formula che si decide di usare, assicurarsi di impostare Zn su un valore il più grande possibile, perché i valori z molto vicini alla fotocamera non variano di molto. In questo modo i confronti di profondità con z buffer a 16 bit sono piuttosto complicati.

Come per le trasformazioni world e view, chiami il metodo [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) per impostare la trasformazione di proiezione.

## <a name="setting-up-a-projection-matrix"></a>Impostazione di una matrice di proiezione

La funzione di esempio ProjectionMatrix seguente imposta i piani di ritaglio anteriore e posteriore, nonché il campo orizzontale e verticale degli angoli di visualizzazione. I campi di visualizzazione devono essere minori di pi greco radianti.


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



Dopo aver creato la matrice, impostarla con [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specificando D3DTS \_ PROJECTION.

La libreria di utilità D3DX fornisce le funzioni seguenti che consentono di configurare la matrice di proiezione.

-   [**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
-   [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
-   [**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
-   [**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
-   [**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
-   [**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a>Matrice di proiezione di tipo W

Direct3D può usare il componente w di un vertice che è stato trasformato dalle matrici di mondo, visualizzazione e proiezione per eseguire calcoli basati sulla profondità in effetti di buffer di profondità o di effetto effetto di effetto effetto di effetto di profondità buffer o di proiezione. Calcoli come questi richiedono che la matrice di proiezione normalizzi w in modo che sia equivalente allo spazio globale z. In breve, se la matrice di proiezione include un coefficiente (3,4) che non è 1, è necessario ridimensionare tutti i coefficienti in base all'inverso del coefficiente (3,4) per creare una matrice appropriata. Se non si specifica una matrice conforme, gli effetti e il buffering della profondità non vengono applicati correttamente.

Nella figura seguente viene illustrata una matrice di proiezione non conforme e la stessa matrice ridimensionata in modo che sia abilitata l'icona relativa agli occhi.

![illustrazioni di una matrice di proiezione non conforme e di una matrice con coordinate relative agli occhi](images/eyerlmx.png)

Nelle matrici precedenti si presuppone che tutte le variabili siano diverse da zero. Per altre informazioni sulla profondità relativa agli occhi, vedere Confronto tra profondità relativa [agli occhi e profondità basata su Z.](pixel-fog.md) Per informazioni sul buffer di profondità basato su W, vedere [Buffer di profondità (Direct3D 9).](depth-buffers.md)

Direct3D usa la matrice di proiezione attualmente impostata nei calcoli di profondità basati su w. Di conseguenza, le applicazioni devono impostare una matrice di proiezione conforme per ricevere le funzionalità basate su W desiderate, anche se non usano Direct3D per le trasformazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni](transforms.md)
</dt> </dl>

 

 
