---
description: Un elenco delle funzionalità disponibili in Direct3D 10 è disponibile qui. Questa pagina elenca le funzionalità di Direct3D 9 che non sono più supportate in Direct3D 10.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Funzionalità deprecate (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ce1750e6d8f98785bf87fb92169e56f0b4ca4e8a6dfdd34c6174a8c3087eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852771"
---
# <a name="deprecated-features-direct3d-10"></a>Funzionalità deprecate (Direct3D 10)

Un elenco delle funzionalità disponibili in Direct3D 10 è [disponibile qui.](d3d10-graphics-programming-guide-api-features.md) Questa pagina elenca le funzionalità di Direct3D 9 che non sono più supportate in Direct3D 10.

Le principali modifiche alle funzionalità in Direct3D 10 sono:

- Direct3D 10 non supporta più la pipeline di trasformazione e illuminazione a funzione fissa.
- Direct3D 10 non supporta più il blender di trama a funzione fissa (talvolta denominato pixel shader).
- Direct3D 10 implementa nuove regole di rasterizzazione, più semplici e più pulite rispetto alle regole GDI legacy implementate in Direct3D 9. Ad esempio, il controllo dell'ultimo pixel per le linee non è più supportato.

Di seguito è riportato un elenco completo delle funzionalità di Direct3D 9 deprecate in Direct3D 10.

- **Alpha blend**. La fusione alfa è ora programmata indipendentemente dalla combinazione di colori. Direct3D 10 aggiunge un interruttore alpha-blend-enable, che è abilitato per impostazione predefinita. Per altre informazioni, vedere Oggetti di stato [(Direct3D 10).](d3d10-graphics-programming-guide-api-features-state-objects.md)
- **Test alfa**. Il test alfa è un comportamento in pixel a funzione fissa per Direct3D 9. Il test alfa viene spostato in pixel shader programmabili per Direct3D 10 e versioni successive. Per informazioni sull'emulazione della funzionalità di test alfa Direct3D 9 in Direct3D 10 e versioni successive, vedere l'esempio FixedFuncEMU in DirectX SDK per giugno [2010.](https://www.microsoft.com/download/en/details.aspx?id=6812)
- **Opzioni della modalità blend**. BOTHSRCALPHA è stato rimosso da D3D10 \_ BLEND perché è ridondante con BOTHINVSRCALPHA. Per [**altre informazioni, vedere D3D10 \_ BLEND.**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend)
- **Formati di compressione a blocchi**. Non esiste alcuna distinzione tra alfa premoltiplicati o alfa non premoltiplicati in Direct3D 10. Questi formati Direct3D 9 sono mappati a questi formati Direct3D 10: 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2, DXT3  | RB2\*       |
    | DXT4, DXT5  | BC3\*       |

    

     

    Per altre informazioni, vedere Compressione a blocchi [(Direct3D 10).](d3d10-graphics-programming-guide-resources-block-compression.md)

-   **Piani di ritaglio**. Invece di usare i piani di ritaglio, Direct3D 10 implementa le distanze delle clip e le distanze di taglio, con un massimo di 8 componenti ognuno in un massimo di 2 elementi di attributi vertice. Per [altre informazioni, vedere Semantica (DirectX HLSL).](../direct3dhlsl/dx-graphics-hlsl-semantics.md) [L'esempio FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornisce un esempio di emulazione dei piani di ritaglio in Direct3D 10.
-   **Dithering di**. Direct3D 10 non supporta la scrittura di dati dithering in una destinazione di rendering.
-   **Pipeline di trasformazione e illuminazione a funzione fissa in non disponibile.** È invece necessario usare gli shader. Per altre informazioni, vedere Fasi shader [(Direct3D 10).](/previous-versions//bb205146(v=vs.85))
-   **Blender di trama a funzione fissa (detto anche funzione fissa pixel shader).** È invece necessario usare gli shader. Per altre informazioni, vedere Fasi shader [(Direct3D 10).](/previous-versions//bb205146(v=vs.85))
-   **Le modalità di** riempimento sono state modificate. Direct3D 10 implementa le modalità di riempimento a tinta unita e wireframe. Il punto D3DFILLMODE è stato rimosso. Se necessario, usare uno shader geometry per emulare la modalità punto. [L'esempio FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornisce un esempio di emulazione del punto D3DFILLMODE in Direct3D 10. Per altre informazioni, vedere [**D3D10 \_ FILL \_ MODE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) (MODALITÀ RIEMPIMENTO [D3D10) e Shader Stages (Direct3D 10) (Fasi shader - Direct3D 10).](/previous-versions//bb205146(v=vs.85))
-   **Formatta**. L'hardware può usare formati esposti dall'API. I formati di luminance non sono più implementati.
-   **Filtro Mipmap**. Rimozione dell'opzione per la selezione della modalità senza filtro. Usare invece una trama con un solo mipmap o impostare lo stato del campionatore MaxLOD su 0. Per altre informazioni, vedere Oggetti di stato [(Direct3D 10).](d3d10-graphics-programming-guide-api-features-state-objects.md)
-   **Tavolozze**. Le applicazioni devono invece usare una trama dipendente letta.
-   **Modelli di pixel shader e vertex shader:** 1 \_ x, 2 \_ x e 3 \_ 0. Direct3D 10 supporta il modello shader 4. Per [altre informazioni, vedere Shader Model 4 (Modello shader 4).](../direct3dhlsl/dx-graphics-hlsl-sm4.md)
-   **Point sprites**. In alternativa, usare uno shader geometrico. Per altre informazioni, vedere Fasi shader [(Direct3D 10).](/previous-versions//bb205146(v=vs.85))
-   **Regole di rasterizzazione**. Le regole di rasterizzazione della riga GDI legacy vengono sostituite con regole più semplici e più semplici. Il controllo dell'ultimo pixel per le linee non è più supportato. Per [altre informazioni, vedere Regole di rasterizzazione (Direct3D 10).](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md)
-   **Modalità ombreggiatura**. D3DSHADEMODE (che supporta l'ombreggiatura flat/gouraud/phong) è stato rimosso. Direct3D 10 implementa invece due modificatori di interpolazione per gli output del vertex shader. Vedere [l'esempio FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) per un esempio di emulazione delle modalità gouraud e flat shade di Direct3D 9 in Direct3D 10.
-   **Istruzione texldp.** Un'applicazione deve implementare un carico di trama proiettato con istruzioni HLSL aggiuntive. Per altre informazioni, vedere Informazioni di riferimento per [HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md) [L'esempio FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornisce un esempio di emulazione di texldp in Direct3D 10.
-   **Lo stato della fase della** trama dell'indice delle coordinate di trama (D3DTSS \_ TEXCOORDINDEX) non è più supportato.
-   **Ventole triangolare**. Un'applicazione deve convertire le ventole triangolo esistenti in elenchi di triangoli o strisce di triangoli. Per emulare alcuni comportamenti usando DrawPrimitive nelle API precedenti, provare a usare DrawIndexed in Direct3D 10. Per [altre informazioni, vedere Topologie primitive (Direct3D 10).](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md)
-   **W buffering**. Il supporto hardware non è garantito; È consigliabile che un'applicazione usi invece buffer di profondità ad alta precisione. Per [altre informazioni, Depth-Stencil configuring Depth-Stencil Functionality (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) (Configurazione della funzionalità di Depth-Stencil (Direct3D 10).
-   **Modalità di ritorno a capo** (ritorno a capo delle coordinate della trama). L'incapsulamento degli indirizzi della trama (ad esempio wrap, mirror, clamp e così via) esiste ancora. Vedere [**D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) e [**D3D10 \_ TEXTURE ADDRESS \_ \_ MODE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
