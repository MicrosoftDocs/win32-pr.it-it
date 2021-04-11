---
description: I dispositivi Direct3D possono trasformare le coordinate di trama per i vertici applicando una matrice 4x4.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Trasformazioni di coordinate di trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45b8107f609348ae2367b1171ae7913797f4558
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124467"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Trasformazioni di coordinate di trama (Direct3D 9)

I dispositivi Direct3D possono trasformare le coordinate di trama per i vertici applicando una matrice 4x4. Il sistema applica le trasformazioni alle coordinate di trama in modo analogo alla geometria. Qualsiasi trasformazione (scala, rotazione, traduzione, proiezione, taglio o qualsiasi combinazione di questi) può essere eseguita con una matrice 4x4.

> [!Note]  
> Direct3D non modifica i vertici trasformati e illuminati. Di conseguenza, un'applicazione che usa i vertici trasformati e illuminati non può usare Direct3D per trasformare le coordinate di trama dei vertici.

 

I dispositivi che supportano le operazioni di illuminazione e trasformazione con accelerazione hardware (T&L dispositivo HAL) accelerano anche la trasformazione delle coordinate di trama. Quando l'accelerazione hardware delle trasformazioni non è disponibile, le ottimizzazioni specifiche della piattaforma nella pipeline di geometria Direct3D si applicano alle trasformazioni di coordinate di trama.

Le trasformazioni di coordinate di trama sono utili per produrre effetti speciali evitando la necessità di modificare direttamente le coordinate di trama della geometria. È possibile usare matrici di traslazione o di rotazione semplici per animare trame in un oggetto oppure trasformare le coordinate di trama generate automaticamente da Direct3D per semplificare e probabilmente accelerare gli effetti avanzati, ad esempio trame proiettate e Dynamic Light-Mapping. Inoltre, è possibile usare le trasformazioni di coordinate di trama per riutilizzare un singolo set di coordinate di trama per più scopi, in più fasi di trama.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Impostazione e recupero di trasformazioni di coordinate di trama

Analogamente alle matrici utilizzate dall'applicazione per la geometria, è possibile impostare e recuperare le trasformazioni di coordinate di trama chiamando i metodi [**IDirect3DDevice9:: setransform**](/windows/desktop/api) e [**IDirect3DDevice9:: GetTransform**](/windows/desktop/api) . Questi metodi accettano il \_ TEXTURE0 D3DTS tramite i \_ membri D3DTS TEXTURE7 del tipo enumerato [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) per identificare le matrici di trasformazione per le fasi di trama da 0 a 7, rispettivamente.

Il codice seguente imposta una matrice da applicare alle coordinate di trama per la fase 0 della trama.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Abilitazione delle trasformazioni di coordinate di trama

Lo \_ stato della fase della trama D3DTSS TEXTURETRANSFORMFLAGS controlla l'applicazione delle trasformazioni di coordinate di trama. I valori per questo stato della fase trama sono definiti dal tipo enumerato [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) .

Le trasformazioni di coordinate di trama sono disabilitate quando D3DTSS \_ TEXTURETRANSFORMFLAGS è impostato su D3DTTFF \_ Disable (valore predefinito). Supponendo che siano state abilitate le trasformazioni di coordinate di trama per la fase 0, il codice seguente li Disabilita.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Gli altri valori definiti in [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) vengono usati per abilitare le trasformazioni di coordinate di trama e per controllare il numero di elementi delle coordinate di trama risultante passati al rasterizzatore. Ad esempio, eseguire il codice seguente.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



Il \_ valore COUNT2 di D3DTTFF indica al sistema di applicare il set di matrici di trasformazione per la fase di trama 0, quindi passare i primi due elementi delle coordinate di trama modificate al rasterizzatore.

Il \_ flag di trasformazione della trama D3DTTFF proiettata indica le coordinate per una trama proiettata. Quando si specifica questo flag, il rasterizzatore divide gli elementi passati in base all'ultimo elemento. Prendere ad esempio il codice seguente.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



Questo esempio informa il sistema di passare tre elementi coordinati di trama al rasterizzatore. Il rasterizzatore divide i primi due elementi per il terzo, producendo le coordinate di trama 2D necessarie per risolvere la trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elaborazione delle coordinate di trama](texture-coordinate-processing.md)
</dt> </dl>

 

 
