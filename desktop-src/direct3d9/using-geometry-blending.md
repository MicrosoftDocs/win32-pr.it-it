---
description: La struttura definita dall'utente seguente può essere usata per i vertici che verranno combinati tra due matrici.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Uso della combinazione di geometria (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303797"
---
# <a name="using-geometry-blending-direct3d-9"></a>Uso della combinazione di geometria (Direct3D 9)

La struttura definita dall'utente seguente può essere usata per i vertici che verranno combinati tra due matrici.


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



Il peso della Blend deve essere visualizzato dopo i dati position e RHW in FVF e prima della normale del vertice.

Si noti che il formato Vertex precedente contiene solo un valore di peso di fusione. Ciò è dovuto al fatto che saranno presenti due matrici internazionali, definite negli Stati di trasformazione [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)(0) e **D3DTS \_ WORLDMATRIX**(1). Il sistema combina ogni vertice tra queste due matrici usando il valore del peso singolo. Per tre matrici sono necessari solo due pesi e così via.

> [!Note]
>
> La definizione di pesi dell'interfaccia è facile. L'uso di una funzione lineare della distanza tra le giunzioni è un inizio positivo, ma una funzione Sigma più liscia sembra migliore. La scelta di una funzione di distribuzione di peso cutaneo può comportare grinze acute alle articolazioni, se lo si desidera, usando una variazione grande del peso della pelle per una breve distanza.

 

## <a name="setting-blending-matrices"></a>Impostazione di matrici di Blend

È possibile impostare le matrici di trasformazione tra le quali il sistema esegue la fusione chiamando il metodo [**IDirect3DDevice9:: setransform**](/windows/desktop/api) . Impostare il primo parametro su un valore definito dalla macro [**\_ WORLDMATRIX D3DTS**](d3dts-worldmatrix.md) e impostare il secondo parametro sull'indirizzo della matrice da impostare.

Nell'esempio di codice C++ riportato di seguito vengono impostate due matrici internazionali, tra cui la geometria viene fusa per creare l'illusione di un ARM combinato.


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



Impostando una matrice di Blend, il sistema memorizza nella cache la matrice per un uso successivo. non indica al sistema di iniziare la fusione dei vertici.

## <a name="enabling-geometry-blending"></a>Abilitazione della fusione Geometry

Per impostazione predefinita, la combinazione di geometria è disabilitata. Per abilitare la combinazione di geometria, chiamare il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) per impostare lo \_ stato di rendering VERTEXBLEND di D3DRS su un valore del tipo enumerato [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Nell'esempio di codice seguente viene illustrato l'aspetto di questa chiamata quando si imposta lo stato di rendering di una blend tra due matrici internazionali.


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



Quando D3DRS \_ VERTEXBLEND è impostato su un valore diverso da D3DVBF \_ Disable, il sistema presuppone che il numero appropriato di pesi di fusione venga incluso nel formato del vertice. È responsabilità dell'utente fornire un formato di vertice conforme e fornire una descrizione corretta del formato ai metodi di rendering Direct3D.

Se abilitata, il sistema esegue la fusione geometrica per tutti gli oggetti sottoposti a rendering dai metodi di rendering DrawPrimitive.

## <a name="see-also"></a>Vedere anche

[Codici FVF della funzione fissa (Direct3D 9)](fixed-function-fvf-codes.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Blending Geometry](geometry-blending.md)
</dt> </dl>

 

 
