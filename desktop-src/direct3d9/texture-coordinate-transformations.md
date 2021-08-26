---
description: I dispositivi Direct3D possono trasformare le coordinate della trama per i vertici applicando una matrice 4x4.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Trasformazioni delle coordinate di trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755af38c6c58fc2f19297b056e3e9f35ce2559a6a7a2d52e8a23c94f93f4fbaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984791"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Trasformazioni delle coordinate di trama (Direct3D 9)

I dispositivi Direct3D possono trasformare le coordinate della trama per i vertici applicando una matrice 4x4. Il sistema applica le trasformazioni alle coordinate della trama nello stesso modo della geometria. Qualsiasi trasformazione (scala, rotazione, traslazione, proiezione, traslazione o qualsiasi combinazione di questi elementi) può essere eseguita con una matrice 4x4.

> [!Note]  
> Direct3D non modifica i vertici trasformati e accesi. Di conseguenza, un'applicazione che usa vertici trasformati e illuminati non può usare Direct3D per trasformare le coordinate di trama dei vertici.

 

Anche i dispositivi che supportano operazioni di trasformazione e illuminazione con accelerazione hardware (T&L HAL Device) accelerano la trasformazione delle coordinate della trama. Quando l'accelerazione hardware delle trasformazioni non è disponibile, le ottimizzazioni specifiche della piattaforma nella pipeline di geometria Direct3D si applicano alle trasformazioni delle coordinate di trama.

Le trasformazioni delle coordinate di trama sono utili per produrre effetti speciali evitando la necessità di modificare direttamente le coordinate della trama della geometria. È possibile usare matrici di traslazione o rotazione semplici per animare trame su un oggetto oppure trasformare le coordinate della trama generate automaticamente da Direct3D per semplificare e forse accelerare gli effetti avanzati, ad esempio trame proiettate e mapping dinamico della luce. È anche possibile usare le trasformazioni delle coordinate di trama per riutilizzare un singolo set di coordinate di trama per più scopi, in più fasi di trama.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Impostazione e recupero delle trasformazioni delle coordinate di trama

Analogamente alle matrici utilizzate dall'applicazione per la geometria, è possibile impostare e recuperare le trasformazioni delle coordinate di trama chiamando i metodi [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) e [**IDirect3DDevice9::GetTransform.**](/windows/desktop/api) Questi metodi accettano i membri da D3DTS TEXTURE0 a D3DTS TEXTURE7 del tipo enumerato \_ \_ [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) per identificare rispettivamente le matrici di trasformazione per le fasi di trama da 0 a 7.

Il codice seguente imposta una matrice da applicare alle coordinate della trama per la fase della trama 0.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Abilitazione delle trasformazioni delle coordinate di trama

Lo stato della fase della \_ trama TEXTURETRANSFORMFLAGS D3DTSS controlla l'applicazione delle trasformazioni delle coordinate di trama. I valori per questo stato della fase di trama sono definiti dal [**tipo enumerato D3DTEXTURETRANSFORMFLAGS.**](./d3dtexturetransformflags.md)

Le trasformazioni delle coordinate di trama sono disabilitate quando \_ TEXTURETRANSFORMFLAGS D3DTSS è impostato su D3DTTFF \_ DISABLE (valore predefinito). Supponendo che le trasformazioni delle coordinate di trama siano state abilitate per la fase 0, il codice seguente le disabilita.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Gli altri valori definiti in [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) vengono usati per abilitare le trasformazioni delle coordinate di trama e per controllare il numero di elementi delle coordinate di trama risultanti passati al rasterizzatore. Ad esempio, prendere il codice seguente.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



Il valore D3DTTFF COUNT2 indica al sistema di applicare il set di matrici di trasformazione per la fase di trama 0 e quindi passa i primi due elementi delle coordinate della trama modificate al \_ rasterizzatore.

Il flag di trasformazione trama PROIETTATA D3DTTFF \_ indica le coordinate per una trama proiettata. Quando viene specificato questo flag, il rasterizzatore divide gli elementi passati per l'ultimo elemento. Si consideri il codice seguente, ad esempio.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



Questo esempio informa il sistema di passare tre elementi delle coordinate di trama al rasterizzatore. Il rasterizzatore divide i primi due elementi per il terzo, producendo le coordinate della trama 2D necessarie per affrontare la trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elaborazione delle coordinate di trama](texture-coordinate-processing.md)
</dt> </dl>

 

 
