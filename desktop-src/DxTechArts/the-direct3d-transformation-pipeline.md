---
title: Pipeline di trasformazione Direct3D
description: Questo articolo fornisce una spiegazione tecnica per gli sviluppatori di applicazioni Direct3D su come impostare i parametri della pipeline di trasformazione Direct3D tramite la manipolazione diretta delle matrici Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6377e3b17cfb4ceb6eda1f4cf59a93c12fd3e6b2f7e43f29f622ed6ee12c271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152335"
---
# <a name="the-direct3d-transformation-pipeline"></a>Pipeline di trasformazione Direct3D

Questo articolo fornisce una spiegazione tecnica per gli sviluppatori di applicazioni Direct3D su come impostare i parametri della pipeline di trasformazione Direct3D tramite la manipolazione diretta delle matrici Direct3D.

-   [Overview](#overview)
-   [Pipeline di trasformazione](#the-transformation-pipeline)
-   [Utilizzo Suggerimenti](#usage-tips)

## <a name="overview"></a>Panoramica

Direct3D usa tre trasformazioni per modificare le coordinate del modello 3D in coordinate pixel (spazio dello schermo). Queste trasformazioni sono trasformazione globale, trasformazione di visualizzazione e trasformazione di proiezione.

La trasformazione del mondo controlla il modo in cui le coordinate del modello vengono trasformate in coordinate globali. La trasformazione del mondo può includere traslazioni, rotazioni e ridimensionamenti, ma non si applica alle luci. Per altre informazioni sull'uso delle trasformazioni world, vedere [World Transform](/windows/desktop/direct3d9/world-transform).

La trasformazione della visualizzazione controlla la transizione dalle coordinate del mondo allo "spazio della fotocamera", determinando la posizione della fotocamera nel mondo. Per un esempio di utilizzo delle trasformazioni di visualizzazione, vedere [Trasformazione di visualizzazione](/windows/desktop/direct3d9/view-transform).

La trasformazione proiezione modifica la geometria dallo spazio della fotocamera allo "spazio di ritaglio" e applica la distorsione della prospettiva. Il termine "spazio di ritaglio" si riferisce al modo in cui la geometria viene ritagliata al volume di visualizzazione durante questa trasformazione. Per un esempio di utilizzo delle trasformazioni di proiezione, vedere [Trasformazione proiezione](/windows/desktop/direct3d9/projection-transform).

Infine, la geometria nello spazio clip viene trasformata in coordinate pixel (spazio dello schermo). Questa trasformazione è controllata dalle impostazioni del viewport.

Il ritaglio e la trasformazione dei vertici devono avere luogo in uno spazio omogeneo (in parole semplici, spazio in cui il sistema di coordinate include un quarto elemento), ma il risultato finale per la maggior parte delle applicazioni deve essere coordinate tridimensionali (3D) non omogenee definite nello "spazio dello schermo". Ciò significa che sia i vertici di input che il volume di ritaglio devono essere convertiti in uno spazio omogeneo per eseguire il ritaglio e quindi traslati nuovamente in uno spazio non omogeneo da visualizzare.

Le tre trasformazioni Direct3D world, view e projection transform-sono definite dalle matrici Direct3D. Una matrice Direct3D è una matrice omogenea 4x4 definita da una [**struttura D3DMATRIX.**](/windows/desktop/direct3d9/d3dmatrix) Anche se le matrici Direct3D non sono oggetti standard, non sono rappresentate da un'interfaccia COM. È possibile crearle e impostarle come qualsiasi altro oggetto Direct3D. Per altre informazioni sulle matrici Direct3D, vedere [Trasformazioni](/windows/desktop/direct3d9/transforms).

## <a name="the-transformation-pipeline"></a>Pipeline di trasformazione

Se un vertice nella coordinata del modello viene specificato da Pm = (Xm, Ym, Zm, 1), le trasformazioni illustrate nella figura seguente vengono applicate alle coordinate dello schermo di calcolo Ps = (Xs, Ys, Zs, Ws).

![trasformazione dello spazio del modello nello spazio dello schermo](images/d3dxfrm61.gif)

Di seguito sono riportate le descrizioni delle fasi illustrate nella figura precedente:

1.  La matrice globale Mworld trasforma i vertici dallo spazio del modello allo spazio globale. Questa matrice è impostata da:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    L'implementazione Direct3D presuppone che l'ultima colonna di questa matrice sia (0, 0, 0, 1). Non viene restituito alcun errore se l'utente specifica una matrice con un'ultima colonna diversa, ma l'illuminazione e la nebbia non saranno corrette.

2.  View matrix Mview trasforma i vertici dallo spazio globale allo spazio della fotocamera. Questa matrice è impostata da:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    L'implementazione Direct3D presuppone che l'ultima colonna di questa matrice sia (0, 0, 0, 1). Non viene restituito alcun errore se l'utente specifica una matrice con l'ultima colonna diversa, ma l'illuminazione e la nebbia non saranno corrette.

3.  La matrice di proiezione Mproj trasforma i vertici dallo spazio della fotocamera allo spazio di proiezione. Questa matrice è impostata da:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    L'ultima colonna della matrice di proiezione deve essere (0, 0, 1, 0) o (0, 0, a, 0) per gli effetti corretti di nebbia e illuminazione; (0, 0, 1, 0) è preferibile.

    Il volume di ritaglio per tutti i punti Xp = (Xp, Yp, Zp, Wp) nello spazio di proiezione è definito come:

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    Tutti i punti che non soddisfano queste equazioni verranno ritagliati.

    Se un volume di visualizzazione è definito come:

    -   Larghezza della finestra dello schermo sw nello spazio della fotocamera vicino al piano di ritaglio
    -   Altezza della finestra sh-screen nello spazio della fotocamera in prossimità del piano di ritaglio
    -   Distanza Zn dal piano di ritaglio vicino lungo gli assi Z nello spazio della fotocamera
    -   Distanza Zf dal piano di ritaglio lontano lungo gli assi Z nello spazio della fotocamera

    quindi una matrice di proiezione prospettica può essere scritta come segue:

    ![Mostra una matrice di proiezione prospettica.](images/d3dxfrm62.gif)

    dove Mij è membro di Mproj.

    Per la proiezione ortogonale sono stati:

    ![proiezione ortogonale](images/d3dxfrm63.gif)

    Direct3D presuppone che la matrice di proiezione prospettica abbia il formato seguente:

    ![matrice di proiezione prospettica](images/d3dxfrm64.gif)

    Se la matrice di proiezione prospettica non ha questo formato, saranno presenti alcuni elementi. Ad esempio, la tabella #a0 non funzionerà.

4.  Direct3D consente all'utente di modificare il volume della clip nel modo seguente:

    ![modificare il volume del clip](images/d3dxfrm65.gif)

    Questa operazione può essere riscritta come:

    ![modificare il volume del clip riscritto](images/d3dxfrm66.gif)

    dove:

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    Questa trasformazione può fornire una maggiore precisione ed equivale a ridimensionare e spostare il volume di ritaglio.

    La matrice Mclip corrispondente è:

    ![Matrice mclip](images/d3dxfrm67.gif)

    Un vertice viene trasformato da:

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    Se non si vuole ridimensionare il volume della clip, è possibile impostare i parametri del viewport sui valori predefiniti:

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  La fase di ritaglio è facoltativa se l'utente specifica il flag DONOTCLIP D3DDP \_ in una chiamata DrawPrimitive. In questo caso, è possibile combinare tutte le matrici (incluso Mvs).
6.  La matrice di scala del viewport ridimensiona le coordinate per essere all'interno della finestra del viewport e capovolge l'asse Y dall'alto verso il basso:

    ![viewport scale matrix mvs](images/d3dxfrm68.gif)

    dove:

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  Infine, le coordinate dello schermo vengono calcolate e passate al rasterizzatore:

    ![coordinate dello schermo calcolate e passate al rasterizzatore](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>Utilizzo Suggerimenti

Ecco alcuni suggerimenti per l'uso della pipeline di trasformazione Direct3D:

-   L'ultima colonna delle matrici world e view deve essere (0, 0, 0, 1) o l'illuminazione non sarà corretta.
-   Impostare i parametri del viewport per compilare una matrice di Mclip di identità, a meno che non si comprendi esattamente per cosa è necessario.

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 