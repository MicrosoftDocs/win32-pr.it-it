---
description: Questa sezione illustra come usare primitive di ordine superiore nell'applicazione.
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: Uso Higher-Order primitive (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7d7a7b7f619c033665f8cb9894db5d60d5d6ecf9116de4ada230accc476c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797296"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>Uso Higher-Order primitive (Direct3D 9)

Questa sezione illustra come usare primitive di ordine superiore nell'applicazione.

-   [Determinazione del Higher-Order primitive](#determining-higher-order-primitive-support)
-   [Patch di disegno](#drawing-patches)
-   [Generazione di normali e coordinate di trama](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>Determinazione del Higher-Order primitive

È possibile eseguire query sul membro DevCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per determinare il livello di supporto per le operazioni che coinvolgono primitive di ordine superiore. La tabella seguente elenca le funzionalità del dispositivo correlate alle primitive di ordine superiore in Direct3D 9.



| Funzionalità di dispositivo             | Descrizione                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS \_ NPATCHES          | Il dispositivo supporta n-patch ed è basato su [triangoli PN](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) curvi (uno speciale tipo di triangoli di Bézier cubici). |
| D3DDEVCAPS \_ QUINTICRTPATCHES  | Il dispositivo supporta curve bezier quintiche e B-spline.                                                                                                         |
| D3DDEVCAPS \_ RTPATCHES         | Il dispositivo supporta patch rettangolari e triangolari (patch RT).                                                                                             |
| D3DDEVCAPS \_ RTPATCHHANDLEZERO | Le patch RT possono essere disegnate in modo efficiente usando l'handle zero.                                                                                                     |



 

Si noti che D3DDEVCAPS RTPATCHHANDLEZERO non significa che è possibile disegnare una patch con \_ handle zero. È sempre possibile disegnare una patch handle zero, indipendentemente dal fatto che questa funzionalità del dispositivo sia impostata o meno. Quando questa funzionalità è impostata, l'architettura hardware non richiede la memorizzazione nella cache delle informazioni e le patch non memorizzate nella cache (handle zero) vengono disegnate in modo efficiente come quelle memorizzate nella cache.

## <a name="drawing-patches"></a>Patch di disegno

Direct3D 9 supporta due tipi di primitive di ordine superiore, o patch. Queste sono definite patch N e patch Rect/Tri. È possibile eseguire il rendering delle patch N usando qualsiasi chiamata di rendering triangolare abilitando N-patch tramite la chiamata a [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)( nSegments ) con valore nSegments maggiore di 1,0. È necessario eseguire il rendering delle patch Rect/Tri usando i punti di ingresso espliciti seguenti.

È possibile usare i metodi seguenti per disegnare le patch.

-   [**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch). Per comprendere meglio come viene fatto riferimento ai dati della patch nel vertex buffer, vedere [**D3DRECTPATCH \_ INFO**](d3drectpatch-info.md).
-   [**IDirect3DDevice9::D rawTriPatch**](/windows/desktop/api). Per comprendere meglio come viene fatto riferimento ai dati della patch nel vertex buffer, vedere [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

[**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) disegna una patch rettangolare di ordine elevato specificata dal parametro pRectPatchInfo usando i flussi attualmente impostati. Il parametro Handle viene usato per associare la patch a un handle, in modo che la prossima volta che viene disegnata la patch non sia necessario specificare nuovamente pRectPatchInfo. In questo modo è possibile precompilare e memorizzare nella cache coefficienti di differenza in avanti o altre informazioni, che a sua volta consente chiamate successive a **IDirect3DDevice9::D rawRectPatch** usando lo stesso handle per l'esecuzione efficiente.

Per le patch statiche, un'applicazione imposta il vertex shader e i flussi appropriati, fornisce informazioni sulla patch nel parametro pRectPatchInfo e specifica un handle in modo che Direct3D possa acquisire e memorizzare nella cache le informazioni. L'applicazione può quindi chiamare [**IDirect3DDevice9::D rawRectPatch successivamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) con pRectPatchInfo impostato su **NULL** per disegnare in modo efficiente la patch. Quando si disegna una patch memorizzata nella cache, i flussi attualmente impostati vengono ignorati. Tuttavia, è possibile eseguire l'override di pNumSegs memorizzati nella cache specificando nuovi valori per pNumSegs. Inoltre, è necessario impostare lo stesso vertex shader durante il rendering di una patch memorizzata nella cache impostata al momento dell'acquisizione.

Per le patch dinamiche, i dati delle patch cambiano per ogni rendering della patch, quindi non è efficiente memorizzare nella cache le informazioni. L'applicazione può trasmetterlo a Direct3D impostando Handle su 0. In questo caso, Direct3D disegna la patch usando i flussi attualmente impostati e i valori pNumSegs e non memorizza nella cache le informazioni. Non è valido impostare contemporaneamente Handle su 0 e pPatch su **NULL.**

Se si specifica nuovamente pRectPatchInfo per lo stesso handle, l'applicazione può sovrascrivere le informazioni memorizzate in precedenza nella cache.

[**IDirect3DDevice9::D rawTriPatch**](/windows/desktop/api) è simile a [**IDirect3DDevice9::D rawRectPatch,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) ad eccezione del fatto che disegna una patch triangolare di alto ordine.

## <a name="generating-normals-and-texture-coordinates"></a>Generazione di normali e coordinate di trama

Se si usa uno shader FVF (Flexible Vertex Format), la generazione automatica di normali e coordinate di trama non è possibile.

Per le normali, è possibile specificarle direttamente o fare in modo che Direct3D le calcoli automaticamente.

Le coordinate generate per le patch rettangolari sono coordinate basate su spline, come illustrato nelle illustrazioni seguenti.

![illustrazione di una trama originale e della trama con coordinate basate su spline](images/texturespline.png)

Le coordinate generate per le patch triangolari sono coordinate baricentriche basate su spline, come illustrato nelle illustrazioni seguenti.

![illustrazione di una trama originale e della trama con coordinate basate su spline barycentriche](images/texturebarycentricspline.png)

Se un'applicazione deve modificare l'intervallo delle coordinate di trama generate, questa operazione può essere eseguita usando trasformazioni di trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitive di ordine superiore](higher-order-primitives.md)
</dt> </dl>

 

 
