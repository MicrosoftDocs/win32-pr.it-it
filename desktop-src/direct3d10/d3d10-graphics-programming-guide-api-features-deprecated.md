---
description: Un elenco delle funzionalità disponibili in Direct3D 10 è disponibile qui. Questa pagina elenca le funzionalità di Direct3D 9 che non sono più supportate in Direct3D 10.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Funzionalità deprecate (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66b6fe5092427cd66876ab5f6e1d7aaf83f0880
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126699"
---
# <a name="deprecated-features-direct3d-10"></a>Funzionalità deprecate (Direct3D 10)

Un elenco delle funzionalità disponibili in Direct3D 10 è disponibile [qui](d3d10-graphics-programming-guide-api-features.md). Questa pagina elenca le funzionalità di Direct3D 9 che non sono più supportate in Direct3D 10.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le principali modifiche alle funzionalità in Direct3D 10 sono:<br/> Direct3D 10 non supporta più la pipeline di trasformazione e illuminazione a funzione fissa.<br/> Direct3D 10 non supporta più il Blender di trama a funzione fissa (talvolta denominato pixel shader a funzione fissa).<br/> Direct3D 10 implementa nuove regole di rasterizzazione, più semplici e più pulite rispetto alle regole GDI legacy implementate in Direct3D 9. Ad esempio, il controllo Last-pixel per le linee non è più supportato.<br/> |



 

Di seguito è riportato un elenco completo delle funzionalità di Direct3D 9 deprecate in Direct3D 10.

-   **Blend alfa**. Alpha Blend è ora programmato indipendentemente dalla combinazione di colori. Direct3D 10 aggiunge un interruttore Alpha-Blend-Enable che è abilitato per impostazione predefinita. Per ulteriori informazioni, vedere [oggetti stato (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) .
-   **Test alfa**. Il test alfa è un comportamento in pixel a funzione fissa per Direct3D 9. Il test alfa è stato spostato in pixel shader programmabili per Direct3D 10 e versioni successive. Per informazioni sull'emulazione della funzionalità di test alfa Direct3D 9 in Direct3D 10 e versioni successive, vedere l'esempio FixedFuncEMU in [DirectX SDK per il 2010 giugno](https://www.microsoft.com/download/en/details.aspx?id=6812).
-   **Opzioni della modalità Blend**. BOTHSRCALPHA è stato rimosso da D3D10 \_ Blend perché è ridondante con BOTHINVSRCALPHA. Per ulteriori informazioni, vedere [**D3D10 \_ Blend**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend) .
-   **Formati di compressione dei blocchi**. Non esiste alcuna distinzione tra Alpha pre-moltiplicato o alfa non premoltiplicato in Direct3D 10. Questi formati Direct3D 9 sono mappati a questi formati Direct3D 10: 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2,DXT3  | RB2\*       |
    | DXT4, DXT5  | BC3\*       |

    

     

    Per ulteriori informazioni, vedere [compressione dei blocchi (Direct3D 10)](d3d10-graphics-programming-guide-resources-block-compression.md) .

-   **Ritagliare i piani**. Invece di usare i piani di ritaglio, Direct3D 10 implementa le distanze di ritaglio e le distanze di selezione, con un massimo di 8 componenti ciascuno in un massimo di 2 elementi di attributi vertice. Per ulteriori informazioni, vedere [semantica (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-semantics.md) . L' [esempio FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornisce un esempio di emulazione di piani di ritaglio in Direct3D 10.
-   **Rethering**. Direct3D 10 non supporta la scrittura di dati reindirizzati in una destinazione di rendering.
-   La **pipeline di trasformazione e illuminazione a funzione fissa non è disponibile**. È invece necessario utilizzare gli shader. Per ulteriori informazioni, vedere [fasi dello shader (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   Funzione **fixed Blend Blender (denominata anche funzione fixed pixel shader)**. È invece necessario utilizzare gli shader. Per ulteriori informazioni, vedere [fasi dello shader (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   Le **modalità di riempimento** sono state modificate. Direct3D 10 implementa modalità di riempimento solide e wireframe. Il punto di D3DFILLMODE è stato rimosso. se necessario, usare un geometry shader per emulare la modalità punto. L' [esempio FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornisce un esempio di emulazione del punto D3DFILLMODE in Direct3D 10. Per ulteriori informazioni, vedere [**\_ \_ modalità di riempimento D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) e [fasi dello shader (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   **Formati**. L'hardware può usare i formati esposti dall'API. I formati di luminanza non sono più implementati.
-   **Filtro mipmap**. È stata rimossa l'opzione per la selezione della modalità senza filtro. Usare invece una trama con una sola mipmap o impostare lo stato del campionatore MaxLOD su 0. Per ulteriori informazioni, vedere [oggetti stato (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) .
-   **Tavolozze**. Le applicazioni devono invece usare una trama di lettura dipendente.
-   **Modelli di pixel e vertex shader**: 1 \_ x, 2 \_ x e 3 \_ 0. Direct3D 10 supporta il modello di Shader 4. Per ulteriori informazioni, vedere il [modello di Shader 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md) .
-   **Sprite punto**. Usare invece un geometry shader. Per ulteriori informazioni, vedere [fasi dello shader (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   **Regole di rasterizzazione**. Le regole di rasterizzazione di linee GDI legacy vengono sostituite con regole più semplici e pulite. Il controllo Last-pixel per le linee non è più supportato. Per ulteriori informazioni, vedere [regole di rasterizzazione (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md) .
-   **Modalità ombreggiatura**. D3DSHADEMODE (che supportano l'ombreggiatura flat/Gouraud/Phong) è stato rimosso. Direct3D 10 implementa due modificatori di interpolazione per gli output di vertex shader. Vedere l' [esempio FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) per un esempio di emulazione di Direct3D 9 Gouraud e modalità flat shader in Direct3D 10.
-   istruzione **texldp** . Un'applicazione deve implementare un carico di trama proiettato con istruzioni HLSL aggiuntive. Per ulteriori informazioni, vedere il [riferimento per HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) . L' [esempio FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornisce un esempio di emulazione di Texldp in Direct3D 10.
-   Lo stato della fase della trama della **coordinata di trama** (TCI) (D3DTSS \_ TEXCOORDINDEX) non è più supportato.
-   **Ventilatori di triangolo**. Un'applicazione deve convertire le ventole triangolo esistenti in elenchi di triangolo o strisce di triangolo. Per emulare alcuni comportamenti usando DrawPrimitive nelle API precedenti, provare a usare DrawIndexed in Direct3D 10. Per ulteriori informazioni, vedere [topologie primitive (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) .
-   **Buffering W**. Il supporto hardware non è garantito. è consigliabile che un'applicazione utilizzi invece buffer di profondità ad alta precisione. Per ulteriori informazioni, vedere [configurazione della funzionalità Depth-Stencil (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) .
-   **Modalità a capo** (wrapping delle coordinate di trama). Il wrapping degli indirizzi di trama, ad esempio wrap, mirror, Clamp e così via, esiste ancora. Vedere [**D3D10 \_ Sampler \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) e [**D3D10 \_ texture \_ Address \_ mode**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
