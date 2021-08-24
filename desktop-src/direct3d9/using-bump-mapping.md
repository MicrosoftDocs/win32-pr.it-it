---
description: Uso di Bump Mapping (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Uso di Bump Mapping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195a99ffaa29d416aea93c5599f1fb461cd78a9961bd9c69f3f02ae3e8fe4719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025831"
---
# <a name="using-bump-mapping-direct3d-9"></a>Uso di Bump Mapping (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Rilevamento del supporto per il mapping di urti

Un dispositivo può eseguire il bump mapping se supporta l'operazione di fusione della trama D3DTOP \_ BUMPENVMAP o D3DTOP \_ BUMPENVMAPLUMINANCE. Usare [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE QUERY LEGACYBUMPMAP per verificare se è supportato un formato per \_ \_ il mapping di urti.

Inoltre, le applicazioni devono controllare le funzionalità del dispositivo per assicurarsi che il dispositivo supporti un numero appropriato di fasi di fusione, in genere almeno tre, ed espone almeno un formato pixel di bump mapping.

L'esempio di codice seguente controlla le funzionalità del dispositivo per rilevare il supporto per il mapping di urti nel dispositivo corrente, usando i criteri specificati.


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a>Creazione di una trama mappa a rilievo

Si crea una trama mappa a rilievo come qualsiasi altra trama. L'applicazione verifica il supporto per il bump mapping e recupera un formato pixel valido, come descritto in Rilevamento del supporto per il mapping di urti.

Dopo aver creato la superficie, è possibile caricare ogni pixel con i valori differenziali appropriati e la luminanza, se il formato della superficie include la luminanza. I valori per ogni componente pixel sono descritti in [Bump Map Pixel Formats (Direct3D 9)](bump-map-pixel-formats.md).

## <a name="configuring-bump-mapping-parameters"></a>Configurazione dei parametri di bump mapping

Dopo che l'applicazione ha creato una mappa di rilievo e impostato il contenuto di ogni pixel, è possibile prepararsi per il rendering configurando i parametri di bump mapping. I parametri di mapping di rilievo includono l'impostazione delle trame necessarie e delle relative operazioni di fusione, nonché i controlli di trasformazione e luminanza per la mappa di rilievo stessa.

1.  Impostare la mappa trama di base, se usata, la mappa a rilievo e le trame della mappa dell'ambiente nelle fasi di fusione delle trame.
2.  Impostare le operazioni di fusione di colore e alfa per ogni fase della trama.
3.  Impostare la matrice di trasformazione della mappa di rilievo.
4.  Impostare i valori di scala di luminance e offset in base alle esigenze.

Nell'esempio di codice seguente vengono impostate tre trame (mappa di trama di base, mappa di rilievo e mappa dell'ambiente speculare) nelle fasi di fusione della trama appropriate.


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



Dopo aver impostato le trame sulle rispettive fasi di fusione, l'esempio di codice seguente prepara le operazioni di fusione e gli argomenti per ogni fase.


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



Quando le operazioni di fusione e gli argomenti sono impostati, l'esempio di codice seguente imposta la matrice di mapping di rilievo 2x2 sulla matrice di identità impostando i membri D3DTSS \_ BUMPENVMAPMAT00 e \_ D3DTSS BUMPENVMAPMAT11 [**di D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) su 1.0. L'impostazione della matrice sull'identità fa sì che il sistema usi i valori differenziali nella mappa a rilievo senza modifiche, ma questo non è un requisito.


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



Se si imposta l'operazione di bump mapping in modo da includere la luminance (D3DTOP \_ BUMPENVMAPLUMINANCE), è necessario impostare i controlli di luminance. I controlli di luminanza configurano il modo in cui il sistema calcola la luminanza prima di modulare il colore dalla trama nella fase successiva. Per informazioni dettagliate, vedere [Formule di bump mapping (Direct3D 9).](bump-mapping-formulas.md)


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



Dopo che l'applicazione ha configurato i parametri di bump mapping, può eseguire il rendering come di consueto e i poligoni sottoposti a rendering ricevono effetti di bump mapping.

Si noti che l'esempio precedente mostra i parametri impostati per il mapping dell'ambiente speculare. Quando si esegue il mapping della luce diffusa, le applicazioni impostano l'operazione di fusione della trama per l'ultima fase su D3DTOP \_ MODULATE. Per altre informazioni, vedere [Diffuse Light Mappe (Direct3D 9)](diffuse-light-maps.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bump Mapping](bump-mapping.md)
</dt> </dl>

 

 
