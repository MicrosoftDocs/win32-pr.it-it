---
title: Pipeline di trasformazione Direct3D
description: Questo articolo fornisce una spiegazione tecnica per gli sviluppatori di applicazioni Direct3D su come impostare i parametri della pipeline di trasformazione Direct3D mediante la manipolazione diretta delle matrici Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "103885890"
---
# <a name="the-direct3d-transformation-pipeline"></a>Pipeline di trasformazione Direct3D

Questo articolo fornisce una spiegazione tecnica per gli sviluppatori di applicazioni Direct3D su come impostare i parametri della pipeline di trasformazione Direct3D mediante la manipolazione diretta delle matrici Direct3D.

-   [Overview](#overview)
-   [Pipeline di trasformazione](#the-transformation-pipeline)
-   [Suggerimenti sull'utilizzo](#usage-tips)

## <a name="overview"></a>Panoramica

Direct3D usa tre trasformazioni per modificare le coordinate del modello 3D in coordinate pixel (spazio dello schermo). Queste trasformazioni sono trasformazione globale, trasformazione visualizzazione e trasformazione proiezione.

La trasformazione globale controlla il modo in cui le coordinate del modello vengono trasformate in coordinate internazionali. La trasformazione mondiale può includere traduzioni, rotazioni e scalabilità, ma non si applica alle luci. Per altre informazioni sull'uso delle trasformazioni internazionali, vedere [trasformazione globale](/windows/desktop/direct3d9/world-transform).

Visualizza trasformazione consente di controllare la transizione dalle coordinate internazionali allo "spazio della fotocamera", determinando la posizione della fotocamera nel mondo. Per un esempio di utilizzo delle trasformazioni di visualizzazione, vedere [visualizzazione della trasformazione](/windows/desktop/direct3d9/view-transform).

La trasformazione proiezione modifica la geometria dallo spazio della fotocamera in "spazio di ritaglio" e applica la distorsione della prospettiva. Il termine "spazio di ritaglio" indica il modo in cui la geometria viene ritagliata nel volume di visualizzazione durante questa trasformazione. Per un esempio di utilizzo delle trasformazioni di proiezione, vedere [trasformazione proiezione](/windows/desktop/direct3d9/projection-transform).

Infine, la geometria nello spazio di ritaglio viene trasformata in coordinate pixel (spazio dello schermo). Questa trasformazione è controllata dalle impostazioni del viewport.

Il ritaglio e la trasformazione dei vertici devono avvenire nello spazio omogeneo (semplicemente put, nello spazio in cui il sistema di coordinate include un quarto elemento), ma il risultato finale per la maggior parte delle applicazioni deve essere costituito da coordinate tridimensionali (3D) non omogenee definite nello "spazio dello schermo". Ciò significa che sia i vertici di input che il volume di ritaglio devono essere convertiti in uno spazio omogeneo per eseguire il ritaglio e quindi convertiti di nuovo nello spazio non omogeneo da visualizzare.

Le tre trasformazioni Direct3D-mondo, visualizzazione e trasformazione proiezione-sono definite dalle matrici Direct3D. Una matrice Direct3D è una matrice omogenea 4x4 definita da una struttura [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) . Sebbene le matrici Direct3D non siano oggetti standard, non sono rappresentate da un'interfaccia COM. è possibile crearle e impostarle esattamente come qualsiasi altro oggetto Direct3D. Per ulteriori informazioni sulle matrici Direct3D, vedere [trasformazioni](/windows/desktop/direct3d9/transforms).

## <a name="the-transformation-pipeline"></a>Pipeline di trasformazione

Se un vertice nella coordinata del modello viene fornito da PM = (XM, YM, ZM, 1), le trasformazioni mostrate nella figura seguente vengono applicate alle coordinate della schermata di calcolo PS = (XS, Ys, ZS, WS).

![spazio del modello per la trasformazione dello spazio dello schermo](images/d3dxfrm61.gif)

Di seguito sono riportate le descrizioni delle fasi illustrate nella figura precedente:

1.  MWorld della matrice mondiale trasforma i vertici dallo spazio del modello allo spazio globale. Questa matrice è impostata da:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    Nell'implementazione di Direct3D si presuppone che l'ultima colonna di questa matrice sia (0, 0, 0, 1). Non viene restituito alcun errore se l'utente specifica una matrice con un'ultima colonna diversa, ma l'illuminazione e la nebbia non saranno corrette.

2.  View Matrix mview trasforma i vertici dallo spazio globale allo spazio della fotocamera. Questa matrice è impostata da:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    Nell'implementazione di Direct3D si presuppone che l'ultima colonna di questa matrice sia (0, 0, 0, 1). Non viene restituito alcun errore se l'utente specifica una matrice con un'ultima colonna diversa, ma l'illuminazione e la nebbia non saranno corrette.

3.  La matrice di proiezione mproj trasforma i vertici dallo spazio della fotocamera allo spazio di proiezione. Questa matrice è impostata da:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    L'ultima colonna della matrice di proiezione deve essere (0, 0, 1, 0) o (0, 0, a,0) per gli effetti di nebbia e illuminazione corretti; (0, 0, 1, 0) il formato è preferibile.

    Il volume di ritaglio per tutti i punti XP = (XP, YP, ZP, WP) nello spazio di proiezione è definito come segue:

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    Tutti i punti che non soddisfano queste equazioni verranno ritagliati.

    Se un volume di visualizzazione è definito come segue:

    -   SW-Larghezza della finestra dello schermo nello spazio della fotocamera in prossimità del piano di ritaglio
    -   Altezza della finestra dello schermo SH nello spazio della fotocamera vicino al piano di ritaglio
    -   Zn-distanza dal piano di ritaglio vicino lungo gli assi Z nello spazio della fotocamera
    -   ZF-distanza dal piano di ritaglio lungo lungo gli assi Z nello spazio della fotocamera

    una matrice di proiezione prospettica potrebbe quindi essere scritta nel modo seguente:

    ![Mostra una matrice di proiezione prospettica.](images/d3dxfrm62.gif)

    dove mij sono membri di mproj.

    Per la proiezione ortogonale sono disponibili:

    ![proiezione ortogonale](images/d3dxfrm63.gif)

    Direct3D presuppone che la matrice di proiezione prospettica abbia il formato seguente:

    ![matrice di proiezione prospettica](images/d3dxfrm64.gif)

    Se la matrice di proiezione prospettica non presenta questo formato, saranno presenti alcuni artefatti. Ad esempio, la nebbia della tabella non funzionerà.

4.  Direct3D consente all'utente di modificare il volume di ritaglio come segue:

    ![modificare il volume di ritaglio](images/d3dxfrm65.gif)

    Questa operazione può essere riscritta come segue:

    ![modificare il volume di clip riscritto](images/d3dxfrm66.gif)

    dove:

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    Questa trasformazione può fornire maggiore precisione ed equivale a ridimensionare e spostare il volume di ritaglio.

    La matrice Mclip corrispondente è:

    ![matrice mclip](images/d3dxfrm67.gif)

    Un vertice viene trasformato da:

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    Se non si vuole ridimensionare il volume di ritaglio, è possibile impostare i parametri del viewport sui valori predefiniti:

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  La fase di ritaglio è facoltativa se l'utente specifica il \_ flag D3DDP DONOTCLIP in una chiamata DrawPrimitive. In questo caso, è possibile combinare tutte le matrici (incluso MVS).
6.  La matrice di scala del viewport MVS ridimensiona le coordinate in modo che si trovino all'interno della finestra del viewport e capovolge l'asse Y da un verso il basso:

    ![MVS della matrice di scala del viewport](images/d3dxfrm68.gif)

    dove:

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  Infine, le coordinate dello schermo vengono calcolate e passate al rasterizzatore:

    ![Coordinate dello schermo calcolate e passate al rasterizzatore](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>Suggerimenti sull'utilizzo

Ecco alcuni suggerimenti su come usare la pipeline di trasformazione Direct3D:

-   L'ultima colonna delle matrici World e View deve essere (0, 0, 0, 1) o l'illuminazione non sarà corretta.
-   Impostare i parametri del viewport per compilare una matrice Identity Mclip, a meno che non si conosca esattamente ciò che è necessario per.

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 