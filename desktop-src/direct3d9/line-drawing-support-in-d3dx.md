---
description: D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: Supporto per disegno linee in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974a0fdeb24dad1107f85e6c79603368776bce15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401244"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>Supporto per disegno linee in D3DX (Direct3D 9)

D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.

D3DX supporta linee con antialias a livello di singolo pixel. I modelli di linea non sono più supportati.

La libreria di disegno a linee emula le linee usando triangoli di trama e presuppone quanto segue:

-   L'hardware è disponibile tramite le interfacce Direct3D 9.
-   È disponibile almeno una fase della trama.
-   vengono usate le trame 64x64.
-   Sono disponibili le modalità seguenti:
    -   Filtraggio bilineare
    -   Modalità di indirizzo del morsetto
    -   Modalità indirizzo a capo
    -   Alpha modulazione op
    -   Fusione alfa (SRCBLEND = SRC \_ Alpha, DESTBLEND = inv \_ src \_ Alpha)
    -   Test alfa se la fusione alfa non è disponibile; risultato di qualità inferiore

Per il rendering di linee con antialias nelle destinazioni di rendering multicampionamento, usare [**ID3DXLine**](id3dxline.md) che genera poligoni con trama. I valori di copertura dei pixel, generati dalla rasterizzazione di linee con antialias, modulano il valore alfa del pixel calcolato dal pixel shader. Per disegnare una linea con antialias, un'applicazione deve abilitare la fusione alfa e quindi impostare lo \_ stato di rendering ANTIALIASEDLINEENABLE di D3DRS su **true**.

## <a name="functionality-description"></a>Descrizione della funzionalità

La libreria supporta il disegno di strisce di linea colorate con le funzionalità di riga seguenti, ognuna delle quali è indipendente da qualsiasi altra:

-   Spessore linea
-   Modello di linea con ripetizione (il contatore del pattern di riga viene reimpostato con ogni chiamata a [**ID3DXLine::D RAW**](id3dxline--draw.md) o [**ID3DXLine::D rawtransform**](id3dxline--drawtransform.md) . Non viene reimpostato con ogni segmento della striscia di linea.
-   Anti-aliasing
-   Linee di tipo OpenGL

> [!Note]  
> Non sono supportati AUGNATURA.

 

La libreria utilizza il supporto nativo per la creazione di linee hardware (se disponibile nel dispositivo) solo se:

-   La lunghezza riga è 1.
-   Non è abilitato alcun pattern di linea.

Le linee con anti-aliasing a livello di singolo pixel sono supportate da alcuni componenti hardware, quindi la libreria lo usa, se disponibile. Il membro LineCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) enumera le funzionalità hardware per le primitive di disegno di riga.

Quando si usa il disegno della linea di software, ogni riga viene espansa in un rettangolo e quattro vertici vengono inviati al driver.

Ogni segmento di linea viene disegnato con due triangoli. La larghezza della primitiva è la larghezza specificata più 1,0, che può comportare una riga o una colonna di pixel aggiuntiva. Man volta che la linea diventa più ampia, la sfumatura di antialias nella trama diventa più grossolana e i Texel più completamente opachi vengono replicati al centro. La sfumatura è codificata nella direzione v della trama e viene in genere replicata lungo la direzione u. La modalità di indirizzamento della trama per v è Clamp.

Ogni segmento di riga nell'elenco può essere considerato come una riga separata che si avvia dall'endpoint precedente.

La qualità dell'anti-aliasing lungo i bordi paralleli alla lunghezza della riga originale è soggetta a una maggiore larghezza della riga. Si prevede che le larghezze di riga maggiori di 32,0 inizieranno a presentare elementi lungo questi bordi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



