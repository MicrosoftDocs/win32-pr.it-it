---
description: Informazioni sul supporto del disegno di linee in D3DX. D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: Supporto per il disegno di linee in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9cf107615410da6dcfba02d6f708129429e31586360183277fb8f669653d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799682"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>Supporto per il disegno di linee in D3DX (Direct3D 9)

D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.

D3DX supporta linee antialias a livello di singolo pixel. I modelli di linea non sono più supportati.

La libreria di disegno linee emula le linee usando triangoli di trama e presuppone quanto segue:

-   L'hardware è disponibile tramite le interfacce Direct3D 9.
-   È disponibile almeno una fase della trama.
-   Vengono usate trame 64x64.
-   Sono disponibili le modalità seguenti:
    -   Filtraggio bilineare
    -   Modalità indirizzo di chiusura
    -   Modalità di wrapping degli indirizzi
    -   Alpha op modulate
    -   Fusione alfa (SRCBLEND = SRC \_ ALPHA, DESTBLEND = INV \_ SRC \_ ALPHA)
    -   Test alfa se la fusione alfa non è disponibile; risultato di qualità inferiore

Per il rendering di linee con antialias nelle destinazioni di rendering multicampionamento, [**usa ID3DXLine**](id3dxline.md) che genera poligoni con trama. I valori di copertura in pixel, generati dalla rasterizzazione delle linee con antialias, modulano il valore alfa del pixel calcolato dal pixel shader. Per disegnare una linea antialias, un'applicazione deve abilitare la fusione alfa e quindi deve impostare lo stato di rendering D3DRS \_ ANTIALIASEDLINEENABLE su **TRUE.**

## <a name="functionality-description"></a>Descrizione della funzionalità

La libreria supporta il disegno di strisce di linee colorate con le caratteristiche di linea seguenti, ognuna delle quali è indipendente da qualsiasi altra:

-   Spessore linea
-   Modello di linea con ripetizione (il contatore del modello di linea viene reimpostato con ogni [**chiamata ID3DXLine::D raw**](id3dxline--draw.md) o [**ID3DXLine::D rawTransform.**](id3dxline--drawtransform.md) Non viene reimpostata con ogni segmento della striscia di linee.
-   Antialias
-   Linee in stile OpenGL

> [!Note]  
> Non è supportato alcun mitering.

 

La libreria usa il supporto nativo per il disegno di linee hardware (se disponibile nel dispositivo) solo se:

-   Lo spessore della riga è 1.
-   Non è abilitato alcun modello di linea.

Le linee antialias a livello di singolo pixel sono supportate da alcuni componenti hardware, quindi la libreria lo usa, se disponibile. Il membro LineCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) enumera le funzionalità hardware per le primitive di disegno linea.

Quando si usa il disegno di linee software, ogni linea viene espansa in un rettangolo e quattro vertici vengono inviati al driver.

Ogni segmento di linea viene disegnato con due triangoli. La larghezza della primitiva è la larghezza specificata più 1,0, che può comportare una riga o una colonna di pixel aggiuntiva. Quando la linea si amplia, la sfumatura antialias nella trama diventa più grosso modo e i texel completamente opachi vengono replicati intorno al centro. La sfumatura viene codificata nella direzione v della trama e in genere replicata lungo la direzione u. La modalità di indirizzamento della trama per v è clamp.

Ogni segmento di riga nell'elenco può essere considerato una linea separata che inizia dal punto finale precedente.

La qualità dell'anti-aliasing lungo i bordi paralleli alla lunghezza della linea originale ne risentirà man appena la linea si largherà. È previsto che la larghezza delle linee maggiore di 32,0 inizierà a mostrare artefatti lungo questi bordi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



