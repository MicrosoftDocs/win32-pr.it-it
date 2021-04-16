---
description: Questa sezione illustra come usare le primitive di ordine superiore nell'applicazione.
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: Uso di Higher-Order primitive (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8d1447635c38e5e5df3d16ebca5ee3ee142020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551420"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>Uso di Higher-Order primitive (Direct3D 9)

Questa sezione illustra come usare le primitive di ordine superiore nell'applicazione.

-   [Determinazione del supporto di Higher-Order primitive](#determining-higher-order-primitive-support)
-   [Disegno di patch](#drawing-patches)
-   [Generazione di normali e coordinate di trama](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>Determinazione del supporto di Higher-Order primitive

È possibile eseguire una query sul membro DevCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per determinare il livello di supporto per le operazioni che coinvolgono primitive di ordine superiore. La tabella seguente elenca le funzionalità del dispositivo correlate alle primitive di ordine superiore in Direct3D 9.



| Funzionalità di dispositivo             | Descrizione                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_NPATCHES D3DDEVCAPS          | Il dispositivo supporta N-patch ed è basato su [triangoli PN curvi](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (un tipo speciale di triangoli di Bézier cubici). |
| \_QUINTICRTPATCHES D3DDEVCAPS  | Il dispositivo supporta le curve di Bézier quinte e le spline B-spline.                                                                                                         |
| \_RTPATCHES D3DDEVCAPS         | Il dispositivo supporta le patch rettangolari e triangolari (RT-patches).                                                                                             |
| \_RTPATCHHANDLEZERO D3DDEVCAPS | RT: le patch possono essere disegnate in modo efficiente usando l'handle zero.                                                                                                     |



 

Si noti che D3DDEVCAPS \_ RTPATCHHANDLEZERO non significa che è possibile disegnare una patch con handle zero. Una patch con handle zero può essere sempre disegnata, indipendentemente dal fatto che questa funzionalità del dispositivo sia impostata o meno. Quando questa funzionalità è impostata, l'architettura hardware non richiede la memorizzazione nella cache di tutte le informazioni e le patch non memorizzate nella cache (handle zero) devono essere disegnate in modo efficiente come quelle memorizzate nella cache.

## <a name="drawing-patches"></a>Disegno di patch

Direct3D 9 supporta due tipi di primitive o patch di ordine superiore. Queste sono denominate N-patch e patch Rect/Tri. È possibile eseguire il rendering di n-patch usando qualsiasi chiamata di rendering del triangolo abilitando N-patch tramite la chiamata a [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)(nSegments) con un valore nSegments maggiore di 1,0. È necessario eseguire il rendering delle patch Rect/Tri usando i punti di ingresso espliciti seguenti.

È possibile utilizzare i metodi seguenti per creare le patch.

-   [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch). Per comprendere meglio il modo in cui viene fatto riferimento ai dati della patch nel buffer dei vertici, vedere [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).
-   [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api). Per comprendere meglio il modo in cui viene fatto riferimento ai dati della patch nel buffer dei vertici, vedere [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

[**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) disegna una patch di ordine superiore rettangolare specificata dal parametro pRectPatchInfo usando i flussi attualmente impostati. Il parametro handle viene usato per associare la patch a un handle, in modo che la volta successiva che viene disegnata la patch non sia necessario specificare nuovamente pRectPatchInfo. In questo modo è possibile pre-calcolare e memorizzare nella cache i coefficienti di differenza in avanti o altre informazioni, che a loro volta Abilita le chiamate successive a **IDirect3DDevice9::D rawrectpatch** usando lo stesso handle per un'esecuzione efficiente.

Per le patch statiche, un'applicazione deve impostare il vertex shader e i flussi appropriati, fornire le informazioni sulle patch nel parametro pRectPatchInfo e specificare un handle in modo che Direct3D possa acquisire e memorizzare nella cache le informazioni. L'applicazione può quindi chiamare [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) successivamente con pRectPatchInfo impostato su **null** per creare in modo efficiente la patch. Quando si disegna una patch memorizzata nella cache, i flussi attualmente impostati vengono ignorati. Tuttavia, è possibile eseguire l'override del pNumSegs memorizzato nella cache specificando i nuovi valori per pNumSegs. Inoltre, è necessario impostare lo stesso vertex shader quando viene eseguito il rendering di una patch memorizzata nella cache come è stato impostato al momento dell'acquisizione.

Per le patch dinamiche, i dati della patch cambiano per ogni rendering della patch, quindi non è efficiente memorizzare nella cache le informazioni. L'applicazione può comunicarla a Direct3D impostando handle su 0. In questo caso, Direct3D disegna la patch usando i flussi attualmente impostati e i valori di pNumSegs e non memorizza nella cache le informazioni. Non è possibile impostare contemporaneamente handle su 0 e pPatch su **null**.

Con la rispecificazione di pRectPatchInfo per lo stesso handle, l'applicazione può sovrascrivere le informazioni memorizzate nella cache in precedenza.

[**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) è simile a [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) , ad eccezione del fatto che disegna una patch di ordine superiore triangolare.

## <a name="generating-normals-and-texture-coordinates"></a>Generazione di normali e coordinate di trama

Se si usa uno shader FVF (Flexible Vertex Format), non è possibile generare automaticamente le normali e le coordinate di trama.

Per le normali, è possibile specificarle direttamente o fare in modo che Direct3D le calcoli automaticamente.

Le coordinate generate per le patch rettangolari sono coordinate basate su spline, come illustrato nelle illustrazioni seguenti.

![illustrazione di una trama originale e della trama con coordinate basate su spline](images/texturespline.png)

Le coordinate generate per le patch triangolari sono coordinate basate su spline baricentrica, come illustrato nelle illustrazioni seguenti.

![illustrazione di una trama originale e della trama con coordinate basate su spline baricentrica](images/texturebarycentricspline.png)

Se un'applicazione deve modificare l'intervallo delle coordinate di trama generate, è possibile eseguire questa operazione usando le trasformazioni di trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitive di ordine superiore](higher-order-primitives.md)
</dt> </dl>

 

 
