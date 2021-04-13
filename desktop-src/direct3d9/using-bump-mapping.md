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
# <a name="using-bump-mapping-direct3d-9"></a><span data-ttu-id="56140-103">Uso di bump mapping (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="56140-103">Using Bump Mapping (Direct3D 9)</span></span>

## <a name="detecting-support-for-bump-mapping"></a><span data-ttu-id="56140-104">Rilevamento del supporto per il mapping di Bump</span><span class="sxs-lookup"><span data-stu-id="56140-104">Detecting Support for Bump Mapping</span></span>

<span data-ttu-id="56140-105">Un dispositivo può eseguire il mapping di Bump se supporta l' \_ operazione D3DTOP BUMPENVMAP o D3DTOP \_ BUMPENVMAPLUMINANCE texture blending.</span><span class="sxs-lookup"><span data-stu-id="56140-105">A device can perform bump mapping if it supports either the D3DTOP\_BUMPENVMAP or D3DTOP\_BUMPENVMAPLUMINANCE texture blending operation.</span></span> <span data-ttu-id="56140-106">Usare [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ query \_ LEGACYBUMPMAP per verificare se un formato è supportato per il mapping di Bump.</span><span class="sxs-lookup"><span data-stu-id="56140-106">Use [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_LEGACYBUMPMAP to see if a format is supported for bump mapping.</span></span>

<span data-ttu-id="56140-107">Inoltre, le applicazioni devono controllare le funzionalità del dispositivo per assicurarsi che il dispositivo supporti un numero appropriato di fasi di fusione, in genere almeno tre ed espone almeno un formato pixel di mapping Bump.</span><span class="sxs-lookup"><span data-stu-id="56140-107">Additionally, applications should check the device capabilities to make sure the device supports an appropriate number of blending stages, usually at least three, and exposes at least one bump-mapping pixel format.</span></span>

<span data-ttu-id="56140-108">L'esempio di codice seguente controlla le funzionalità del dispositivo per rilevare il supporto per il mapping di bump nel dispositivo corrente, usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="56140-108">The following code example checks device capabilities to detect support for bump mapping in the current device, using the given criteria.</span></span>


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



## <a name="creating-a-bump-map-texture"></a><span data-ttu-id="56140-109">Creazione di una trama con mappa Bump</span><span class="sxs-lookup"><span data-stu-id="56140-109">Creating a Bump Map Texture</span></span>

<span data-ttu-id="56140-110">Si crea una trama con mappa Bump come qualsiasi altra trama.</span><span class="sxs-lookup"><span data-stu-id="56140-110">You create a bump map texture like any other texture.</span></span> <span data-ttu-id="56140-111">L'applicazione verifica il supporto per il mapping di bump e recupera un formato pixel valido, come descritto in rilevamento del supporto per il mapping di Bump.</span><span class="sxs-lookup"><span data-stu-id="56140-111">Your application verifies support for bump mapping and retrieves a valid pixel format, as discussed in Detecting Support for Bump Mapping.</span></span>

<span data-ttu-id="56140-112">Dopo aver creato la superficie, è possibile caricare ogni pixel con i valori Delta appropriati e la luminanza, se il formato della superficie include la luminanza.</span><span class="sxs-lookup"><span data-stu-id="56140-112">After the surface is created, you can load each pixel with the appropriate delta values, and luminance, if the surface format includes luminance.</span></span> <span data-ttu-id="56140-113">I valori per ogni componente pixel sono descritti in [formati di pixel della mappa Bump (Direct3D 9)](bump-map-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="56140-113">The values for each pixel component are described in [Bump Map Pixel Formats (Direct3D 9)](bump-map-pixel-formats.md).</span></span>

## <a name="configuring-bump-mapping-parameters"></a><span data-ttu-id="56140-114">Configurazione dei parametri di mapping di Bump</span><span class="sxs-lookup"><span data-stu-id="56140-114">Configuring Bump Mapping Parameters</span></span>

<span data-ttu-id="56140-115">Quando l'applicazione ha creato una mappa bump e impostato il contenuto di ogni pixel, è possibile prepararsi per il rendering configurando i parametri di mapping di Bump.</span><span class="sxs-lookup"><span data-stu-id="56140-115">When your application has created a bump map and set the contents of each pixel, you can prepare for rendering by configuring bump mapping parameters.</span></span> <span data-ttu-id="56140-116">I parametri di bump mapping includono l'impostazione delle trame richieste e delle relative operazioni di fusione, nonché i controlli di trasformazione e luminanza per la mappa Bump.</span><span class="sxs-lookup"><span data-stu-id="56140-116">Bump mapping parameters include setting the required textures and their blending operations, as well as the transformation and luminance controls for the bump map itself.</span></span>

1.  <span data-ttu-id="56140-117">Impostare la mappa della trama di base, se utilizzata, le trame di bump e la mappa dell'ambiente nelle fasi di combinazione delle trame.</span><span class="sxs-lookup"><span data-stu-id="56140-117">Set the base texture map if used, bump map, and environment map textures into texture blending stages.</span></span>
2.  <span data-ttu-id="56140-118">Impostare le operazioni relative al colore e alla fusione alfa per ogni fase della trama.</span><span class="sxs-lookup"><span data-stu-id="56140-118">Set the color and alpha blending operations for each texture stage.</span></span>
3.  <span data-ttu-id="56140-119">Imposta la matrice di trasformazione della mappa Bump.</span><span class="sxs-lookup"><span data-stu-id="56140-119">Set the bump map transformation matrix.</span></span>
4.  <span data-ttu-id="56140-120">Impostare i valori di offset e scala della luminanza in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="56140-120">Set the luminance scale and offset values as needed.</span></span>

<span data-ttu-id="56140-121">Nell'esempio di codice seguente vengono impostate tre trame, ovvero la mappa della trama di base, la mappa a urto e una mappa dell'ambiente speculare, alle fasi di combinazione delle trame appropriate.</span><span class="sxs-lookup"><span data-stu-id="56140-121">The following code example sets three textures (the base texture map, the bump map, and a specular environment map) to the appropriate texture blending stages.</span></span>


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



<span data-ttu-id="56140-122">Dopo aver impostato le trame sulle fasi di fusione, l'esempio di codice seguente prepara le operazioni di fusione e gli argomenti per ogni fase.</span><span class="sxs-lookup"><span data-stu-id="56140-122">After setting the textures to their blending stages, the following code example prepares the blending operations and arguments for each stage.</span></span>


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



<span data-ttu-id="56140-123">Quando si impostano le operazioni e gli argomenti di Blend, l'esempio di codice seguente imposta la matrice di mapping del bump 2x2 sulla matrice di identità impostando i \_ membri D3DTSS BUMPENVMAPMAT00 e D3DTSS \_ BUMPENVMAPMAT11 di [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) su 1,0.</span><span class="sxs-lookup"><span data-stu-id="56140-123">When the blending operations and arguments are set, the following code example sets the 2x2 bump mapping matrix to the identity matrix by setting the D3DTSS\_BUMPENVMAPMAT00 and the D3DTSS\_BUMPENVMAPMAT11 members of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) to 1.0.</span></span> <span data-ttu-id="56140-124">Impostando la matrice sull'identità, il sistema utilizzerà i valori Delta nella mappa Bump senza modifiche, ma non è un requisito.</span><span class="sxs-lookup"><span data-stu-id="56140-124">Setting the matrix to the identity causes the system to use the delta values in the bump map unmodified, but this is not a requirement.</span></span>


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



<span data-ttu-id="56140-125">Se si imposta l'operazione bump mapping per includere luminanza (D3DTOP \_ BUMPENVMAPLUMINANCE), è necessario impostare i controlli di luminanza.</span><span class="sxs-lookup"><span data-stu-id="56140-125">If you set the bump mapping operation to include luminance (D3DTOP\_BUMPENVMAPLUMINANCE), you must set the luminance controls.</span></span> <span data-ttu-id="56140-126">I controlli di luminanza configurano il modo in cui il sistema calcola la luminanza prima di modulare il colore dalla trama nella fase successiva.</span><span class="sxs-lookup"><span data-stu-id="56140-126">The luminance controls configure how the system computes luminance before modulating the color from the texture in the next stage.</span></span> <span data-ttu-id="56140-127">Per informazioni dettagliate, vedere le [formule di mapping di Bump (Direct3D 9)](bump-mapping-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="56140-127">For details, see [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md).</span></span>


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



<span data-ttu-id="56140-128">Dopo la configurazione dei parametri di bump mapping, l'applicazione può eseguire il rendering come di consueto e i poligoni sottoposti a rendering ricevono effetti di mapping Bump.</span><span class="sxs-lookup"><span data-stu-id="56140-128">After your application configures bump mapping parameters, it can render as normal, and the rendered polygons receive bump mapping effects.</span></span>

<span data-ttu-id="56140-129">Si noti che l'esempio precedente Mostra i parametri impostati per il mapping dell'ambiente speculare.</span><span class="sxs-lookup"><span data-stu-id="56140-129">Note that the preceding example shows parameters set for specular environment mapping.</span></span> <span data-ttu-id="56140-130">Quando si esegue il mapping della luce diffusa, le applicazioni impostano l'operazione di combinazione della trama per l'ultima fase di D3DTOP \_ Modulation.</span><span class="sxs-lookup"><span data-stu-id="56140-130">When performing diffuse light mapping, applications set the texture blending operation for the last stage to D3DTOP\_MODULATE.</span></span> <span data-ttu-id="56140-131">Per altre informazioni, vedere [Diffusion Light Maps (Direct3D 9)](diffuse-light-maps.md).</span><span class="sxs-lookup"><span data-stu-id="56140-131">For more information, see [Diffuse Light Maps (Direct3D 9)](diffuse-light-maps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56140-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56140-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56140-133">Bump mapping</span><span class="sxs-lookup"><span data-stu-id="56140-133">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 
