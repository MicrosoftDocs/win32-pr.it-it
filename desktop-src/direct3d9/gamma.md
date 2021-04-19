---
description: Il contenuto della trama viene spesso archiviato in formato sRGB.
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: Gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cea4b3ba224452e1c3be8f96b7136f4e4f649c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303679"
---
# <a name="gamma-direct3d-9"></a>Gamma (Direct3D 9)

Il contenuto della trama viene spesso archiviato in formato sRGB. Tradizionalmente, le pipeline di pixel presumevano che i colori fossero lineari, quindi le operazioni di fusione venivano eseguite nello spazio lineare. Tuttavia, poiché il contenuto sRGB è con correzione gamma, le operazioni di fusione nello spazio lineare producono risultati non corretti. Le schede video possono ora risolvere questo problema annullando la correzione gamma quando leggono qualsiasi contenuto sRGB e convertono i dati dei pixel nel formato sRGB quando scrivono i pixel. In questo caso, tutte le operazioni all'interno della pipeline pixel vengono eseguite nello spazio lineare.

## <a name="gamma-correction"></a>Correzione gamma

Direct3D 9 può:

-   Indica se una trama è di gamma 2,2 con correzione o meno (sRGB o meno). Il driver eseguirà la conversione a una gamma lineare per le operazioni di fusione in fase di distrama oppure il campionatore lo convertirà in dati lineari al momento della ricerca.
-   Consente di indicare se la pipeline di pixel deve restituire una gamma di correzione allo spazio sRGB durante la scrittura nella destinazione di rendering.

Tutti gli altri colori (colore chiaro, colore del materiale, colore del vertice e così via) si presume siano nello spazio lineare. Le applicazioni possono correggere la gamma dei colori scritti nel buffer dei frame usando le istruzioni pixel shader. La linearizzazione deve essere applicata solo ai canali RGB e non al canale alfa.

Non è possibile linearizzare tutti i formati di superficie. È possibile linearizzare solo i formati che passano [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ query \_ SRGBREAD. Lo stato del campionatore D3DSAMP \_ SRGBTEXTURE viene ignorato per il resto. Per supportare questa conversione sono previsti solo formati di trama senza segno. I formati di trama senza segno includono solo i componenti R, G, B e L. Se il canale alfa è presente, viene ignorato. Se i formati misti supportano la linearizzazione sRGB, saranno interessati solo i canali senza segno. Idealmente, l'hardware deve eseguire la linearizzazione prima di filtrare, ma in Direct3D 9 l'hardware può eseguire la linearizzazione dopo il filtro.

Non tutti i formati di superficie possono essere scritti nello spazio sRGB. È possibile linearizzare solo i formati che passano il [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con il flag di utilizzo D3DUSAGE \_ query \_ SRGBWRITE. Lo stato di rendering D3DRS \_ SRGBWRITEENABLE viene ignorato per il resto. Per esporre questa possibilità, è previsto che i formati RGB non firmati di otto bit per canale siano esposte.

Idealmente, l'hardware deve eseguire le operazioni di fusione del buffer dei frame nello spazio lineare, ma l'hardware è autorizzato a eseguirlo dopo il pixel shader ma prima di frame buffer Blender. Ciò significa che le operazioni di fusione del buffer dei frame che avvengono nello spazio sRGB produrranno risultati non corretti. D3DRS \_ SRGBWRITEENABLE viene rispettato durante l'esecuzione di una cancellazione della destinazione di rendering. Per l'hardware che supporta [più destinazioni di rendering (Direct3D 9)](multiple-render-targets.md) o [trame a più elementi (Direct3D 9)](multiple-element-textures.md), viene scritta solo la prima destinazione di rendering o elemento.

### <a name="api-changes"></a>Modifiche API


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



### <a name="windowed-swap-chains"></a>Catene di scambio finestra

È importante che le applicazioni mantengano i buffer indietro delle catene di scambio nello spazio lineare per consentire le operazioni di fusione corrette. Poiché il desktop in genere non è nello spazio lineare, è necessaria una correzione gamma prima che sia possibile presentare il contenuto del buffer nascosto. L'applicazione può applicare questa correzione allocando un buffer aggiuntivo ed eseguendo la propria copia di correzione dal buffer lineare al buffer nascosto. Questa operazione richiede una copia aggiuntiva che può essere evitata se il driver esegue la correzione gamma come parte del blit di presentazione.

In Direct3D 9 è disponibile un nuovo flag, [D3DPRESENT \_ Linear \_ Content](d3dpresent.md) [**, che consente alla presentazione di eseguire**](/windows/desktop/api) la conversione implicita dallo spazio lineare a sRGB/gamma 2,2. Le applicazioni devono specificare questo flag se il formato backBuffer è a virgola mobile a 16 bit per abbinare la modalità a finestra presente al comportamento gamma a schermo intero, purché \_ \_ \_ venga restituita la presentazione D3DCAPS3 lineare a sRGB \_ per le funzionalità del dispositivo recuperate tramite [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer frame](frame-buffer.md)
</dt> </dl>

 

 
