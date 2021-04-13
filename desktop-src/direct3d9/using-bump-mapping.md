---
description: Uso di bump mapping (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Uso di bump mapping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482676"
---
# <a name="using-bump-mapping-direct3d-9"></a>Uso di bump mapping (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Rilevamento del supporto per il mapping di Bump

Un dispositivo può eseguire il mapping di Bump se supporta l' \_ operazione D3DTOP BUMPENVMAP o D3DTOP \_ BUMPENVMAPLUMINANCE texture blending. Usare [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ query \_ LEGACYBUMPMAP per verificare se un formato è supportato per il mapping di Bump.

Inoltre, le applicazioni devono controllare le funzionalità del dispositivo per assicurarsi che il dispositivo supporti un numero appropriato di fasi di fusione, in genere almeno tre ed espone almeno un formato pixel di mapping Bump.

L'esempio di codice seguente controlla le funzionalità del dispositivo per rilevare il supporto per il mapping di bump nel dispositivo corrente, usando i criteri specificati.


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



## <a name="creating-a-bump-map-texture"></a>Creazione di una trama con mappa Bump

Si crea una trama con mappa Bump come qualsiasi altra trama. L'applicazione verifica il supporto per il mapping di bump e recupera un formato pixel valido, come descritto in rilevamento del supporto per il mapping di Bump.

Dopo aver creato la superficie, è possibile caricare ogni pixel con i valori Delta appropriati e la luminanza, se il formato della superficie include la luminanza. I valori per ogni componente pixel sono descritti in [formati di pixel della mappa Bump (Direct3D 9)](bump-map-pixel-formats.md).

## <a name="configuring-bump-mapping-parameters"></a>Configurazione dei parametri di mapping di Bump

Quando l'applicazione ha creato una mappa bump e impostato il contenuto di ogni pixel, è possibile prepararsi per il rendering configurando i parametri di mapping di Bump. I parametri di bump mapping includono l'impostazione delle trame richieste e delle relative operazioni di fusione, nonché i controlli di trasformazione e luminanza per la mappa Bump.

1.  Impostare la mappa della trama di base, se utilizzata, le trame di bump e la mappa dell'ambiente nelle fasi di combinazione delle trame.
2.  Impostare le operazioni relative al colore e alla fusione alfa per ogni fase della trama.
3.  Imposta la matrice di trasformazione della mappa Bump.
4.  Impostare i valori di offset e scala della luminanza in base alle esigenze.

Nell'esempio di codice seguente vengono impostate tre trame, ovvero la mappa della trama di base, la mappa a urto e una mappa dell'ambiente speculare, alle fasi di combinazione delle trame appropriate.


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



Dopo aver impostato le trame sulle fasi di fusione, l'esempio di codice seguente prepara le operazioni di fusione e gli argomenti per ogni fase.


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



Quando si impostano le operazioni e gli argomenti di Blend, l'esempio di codice seguente imposta la matrice di mapping del bump 2x2 sulla matrice di identità impostando i \_ membri D3DTSS BUMPENVMAPMAT00 e D3DTSS \_ BUMPENVMAPMAT11 di [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) su 1,0. Impostando la matrice sull'identità, il sistema utilizzerà i valori Delta nella mappa Bump senza modifiche, ma non è un requisito.


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



Se si imposta l'operazione bump mapping per includere luminanza (D3DTOP \_ BUMPENVMAPLUMINANCE), è necessario impostare i controlli di luminanza. I controlli di luminanza configurano il modo in cui il sistema calcola la luminanza prima di modulare il colore dalla trama nella fase successiva. Per informazioni dettagliate, vedere le [formule di mapping di Bump (Direct3D 9)](bump-mapping-formulas.md).


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



Dopo la configurazione dei parametri di bump mapping, l'applicazione può eseguire il rendering come di consueto e i poligoni sottoposti a rendering ricevono effetti di mapping Bump.

Si noti che l'esempio precedente Mostra i parametri impostati per il mapping dell'ambiente speculare. Quando si esegue il mapping della luce diffusa, le applicazioni impostano l'operazione di combinazione della trama per l'ultima fase di D3DTOP \_ Modulation. Per altre informazioni, vedere [Diffusion Light Maps (Direct3D 9)](diffuse-light-maps.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bump mapping](bump-mapping.md)
</dt> </dl>

 

 
