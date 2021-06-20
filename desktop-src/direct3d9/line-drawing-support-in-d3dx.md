---
description: Informazioni sul supporto del disegno a linee in D3DX. D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: Supporto del disegno linea in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cf15eae461d0dbe719e99cfac605a6c8b8d272
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407534"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>Supporto del disegno linea in D3DX (Direct3D 9)

D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.

D3DX supporta linee antialias a larghezza di pixel singolo. I modelli di linea non sono più supportati.

La libreria di disegno a linee emula le linee usando triangoli di trama e presuppone quanto segue:

-   L'hardware è disponibile tramite le interfacce Direct3D 9.
-   È disponibile almeno una fase di trama.
-   Vengono usate trame 64x64.
-   Sono disponibili le modalità seguenti:
    -   Filtraggio bilineare
    -   Modalità di chiusura dell'indirizzo
    -   Modalità di ritorno a capo degli indirizzi
    -   Opulate alfa
    -   Fusione alfa (SRCBLEND = SRC \_ ALPHA, DESTBLEND = INV \_ SRC \_ ALPHA)
    -   Test alfa se la fusione alfa non è disponibile; risultato di qualità inferiore

Per il rendering delle linee antialias nelle destinazioni di rendering multicampionamento, usare [**ID3DXLine**](id3dxline.md) che genera poligoni trame. I valori di copertura dei pixel, generati dalla rasterizzazione della linea antialias, modulano il valore alfa del pixel calcolato dall'pixel shader. Per disegnare una linea antialias, un'applicazione deve abilitare la fusione alfa e quindi deve impostare lo stato di rendering D3DRS \_ ANTIALIASEDLINEENABLE su **TRUE.**

## <a name="functionality-description"></a>Descrizione della funzionalità

La libreria supporta il disegno di strisce di linee colorate con le caratteristiche di linea seguenti, ognuna delle quali è indipendente da qualsiasi altra:

-   Spessore linea
-   Modello di linea con ripetizione (il contatore del modello di linea viene reimpostato con ogni [**chiamata ID3DXLine::D raw**](id3dxline--draw.md) o [**ID3DXLine::D rawTransform.**](id3dxline--drawtransform.md) Non viene reimpostato con ogni segmento della striscia di linea.
-   Antialias
-   Linee in stile OpenGL

> [!Note]  
> Non è supportato alcun mitering.

 

La libreria usa il supporto nativo per il disegno di linee hardware (se disponibile nel dispositivo) solo se:

-   Lo spessore della riga è 1.
-   Non è abilitato alcun modello di linea.

Le linee antialias a larghezza di singolo pixel sono supportate da alcuni componenti hardware, quindi la libreria lo usa, se disponibile. Il membro LineCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) enumera le funzionalità hardware per le primitive di disegno linea.

Quando si usa il disegno a linee software, ogni linea viene espansa in un rettangolo e quattro vertici vengono inviati al driver.

Ogni segmento di linea viene disegnato con due triangoli. La larghezza della primitiva è la larghezza specificata più 1,0, che può comportare una riga o una colonna aggiuntiva di pixel. Quando la linea diventa più ampia, la sfumatura antialias nella trama diventa più grosso modo e i texel completamente opachi vengono replicati intorno al centro. La sfumatura viene codificata nella direzione v della trama e in genere replicata lungo la direzione u. La modalità di indirizzamento della trama per v è clamp.

Ogni segmento di riga nell'elenco può essere considerato una riga separata che inizia dal punto finale precedente.

La qualità dell'antialiasing lungo i bordi parallelamente alla lunghezza della linea originale risente dell'estensione della linea. È previsto che le larghezze delle linee maggiori di 32,0 inizieranno a presentare artefatti lungo questi bordi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



