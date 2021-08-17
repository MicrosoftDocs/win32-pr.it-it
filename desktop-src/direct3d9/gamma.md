---
description: Il contenuto della trama viene spesso archiviato in formato sRGB.
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: Gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ede077347d67c1657b86ad09b778625e22fd19a39c8333d7f11fec51be53b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523024"
---
# <a name="gamma-direct3d-9"></a>Gamma (Direct3D 9)

Il contenuto della trama viene spesso archiviato in formato sRGB. Tradizionalmente, le pipeline di pixel presupponevano che i colori fossero lineari, quindi le operazioni di fusione venivano eseguite nello spazio lineare. Tuttavia, poiché il contenuto sRGB è corretto in gamma, le operazioni di fusione nello spazio lineare produrranno risultati non corretti. Le schede video possono ora risolvere questo problema annullando la correzione gamma quando leggono qualsiasi contenuto sRGB e convertono i dati pixel nel formato sRGB durante la scrittura dei pixel. In questo caso, tutte le operazioni all'interno della pipeline di pixel vengono eseguite nello spazio lineare.

## <a name="gamma-correction"></a>Correzione gamma

Direct3D 9 può:

-   Indicare se una trama è gamma 2.2 corretta o meno (sRGB o meno). Il driver esegue la conversione in una gamma lineare per le operazioni di fusione al momento di SetTexture oppure il campionatore lo converte in dati lineari in fase di ricerca.
-   Indica se la pipeline di pixel deve correggere gamma nello spazio sRGB durante la scrittura nella destinazione di rendering.

Si presuppone che tutti gli altri colori (colore chiaro, colore materiale, colore vertice e così via) siano nello spazio lineare. Le applicazioni possono correggere in gamma i colori scritti nel buffer dei frame usando pixel shader istruzioni. La linearizzazione deve essere applicata solo ai canali RGB e non al canale alfa.

Non tutti i formati di superficie possono essere linearizzati. Solo i formati che [**passano CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ QUERY \_ SRGBREAD possono essere linearizzati. Lo stato del campionatore D3DSAMP \_ SRGBTEXTURE viene ignorato per il resto. È previsto che solo i formati di trama senza segno supportino questa conversione. I formati di trama senza segno includono solo componenti R, G, B e L. Se il canale alfa è presente, viene ignorato. Se i formati misti supportano la linearizzazione sRGB, vengono interessati solo i canali non firmati. Idealmente, l'hardware deve eseguire la linearizzazione prima del filtro, ma in Direct3D 9 l'hardware può eseguire la linearizzazione dopo il filtro.

Non tutti i formati di superficie possono essere scritti nello spazio sRGB. Solo i formati che passano [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con il flag di utilizzo D3DUSAGE \_ QUERY \_ SRGBWRITE possono essere linearizzati. Lo stato di rendering D3DRS \_ SRGBWRITEENABLE viene ignorato per il resto. È previsto che otto bit per canale I formati RGB senza segno esponga questa capacità.

Idealmente, l'hardware deve eseguire le operazioni di fusione del buffer dei frame nello spazio lineare, ma l'hardware può eseguirlo dopo il pixel shader ma prima del frullatore del buffer frame. Ciò significa che le operazioni di fusione del buffer dei frame eseguite nello spazio sRGB produrranno risultati non corretti. D3DRS SRGBWRITEENABLE viene rispettato durante l'esecuzione \_ di una cancellazione della destinazione di rendering. Per l'hardware che supporta più destinazioni di rendering [(Direct3D 9)](multiple-render-targets.md) o trame a più elementi [(Direct3D 9),](multiple-element-textures.md)viene scritta solo la prima destinazione o elemento di rendering.

### <a name="api-changes"></a>Modifiche all'API


```
// New sampler state (DWORD)
// If this is nonzero, the texture is linearized on lookup.
D3DSAMP_SRGBTEXTURE       // Default FALSE

// New render state (DWORD)
D3DRS_SRGBWRITEENABLE     // Default FALSE

// New usage flags
D3DUSAGE_QUERY_SRGBWRITE
D3DUSAGE_QUERY_SRGBREAD
```



### <a name="windowed-swap-chains"></a>Catene di scambio con finestre

È utile per le applicazioni mantenere i buffer indietro delle rispettive catene di scambio nello spazio lineare per consentire le operazioni di fusione corrette. Poiché il desktop in genere non si trova nello spazio lineare, è necessaria una correzione gamma prima di poter presentare il contenuto del buffer nascosto. L'applicazione può eseguire questa correzione allocando un buffer aggiuntivo ed eseguendo la propria copia di correzione dal buffer lineare al buffer nascosto. Ciò richiede una copia aggiuntiva che può essere evitata se il driver esegue la correzione gamma come parte del blit di presentazione.

In Direct3D 9 è disponibile un nuovo [flag, D3DPRESENT \_ LINEAR \_ CONTENT,](d3dpresent.md)che consente alla presentazione di eseguire la conversione implicita dallo spazio lineare a sRGB/gamma 2.2. [](/windows/desktop/api) Le applicazioni devono specificare questo flag se il formato backbuffer è a virgola mobile a 16 bit per far corrispondere la modalità finestra presente al comportamento gamma a schermo intero, purché D3DCAPS3 LINEAR TO SRGB PRESENTATION sia restituito per le funzionalità del dispositivo recuperate tramite \_ \_ \_ \_ [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Frame Buffer](frame-buffer.md)
</dt> </dl>

 

 
