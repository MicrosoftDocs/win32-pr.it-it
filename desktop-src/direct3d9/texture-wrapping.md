---
description: In breve, il wrapping della trama cambia il modo di base in cui Direct3D rasterizza i poligoni trame usando le coordinate di trama specificate per ogni vertice.
ms.assetid: 00683d3f-3e3c-4ee4-9aec-a0d7fd9c8941
title: Wrapping della trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c29ebe78bcfa237f46eacb247432185adedd1e53ae0774e767807269bb3bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984763"
---
# <a name="texture-wrapping-direct3d-9"></a>Wrapping della trama (Direct3D 9)

In breve, il wrapping della trama cambia il modo di base in cui Direct3D rasterizza i poligoni trame usando le coordinate di trama specificate per ogni vertice. Durante l'rasterizzazione di un poligono, il sistema interpola le coordinate della trama in corrispondenza di ognuno dei vertici del poligono per determinare i texel da usare per ogni pixel del poligono. In genere, il sistema considera la trama come un piano 2D, interpolando nuovi texel prendendo il percorso più breve dal punto A all'interno di una trama al punto B. Se il punto A rappresenta la posizione u, v (0.8, 0.1) e il punto B è in corrispondenza di (0.1,0.1), la riga di interpolazione sarà simile al diagramma seguente.

![diagramma di una linea di interpolazione tra due punti](images/interp1.png)

Si noti che la distanza più breve tra A e B in questa illustrazione viene eseguita approssimativamente attraverso il centro della trama. L'abilitazione del wrapping delle coordinate u-texture o v-texture cambia il modo in cui Direct3D percepirà il percorso più breve tra le coordinate della trama nella direzione u e nella direzione v. Per definizione, il wrapping della trama fa sì che il rasterizzatore prenda il percorso più breve tra i set di coordinate della trama, presupponendo che 0,0 e 1,0 siano coincidenti. L'ultimo bit è la parte difficile: è possibile immaginare che l'abilitazione del wrapping della trama in una direzione fa sì che il sistema tratti una trama come se fosse racchiusa in un cilindro. Si consideri ad esempio il diagramma seguente.

![diagramma di una trama e di due punti incapsulati intorno a un cilindro](images/interp2.png)

La figura precedente mostra come il ritorno a capo nella direzione u - influisce sul modo in cui il sistema interpola le coordinate della trama. Usando gli stessi punti dell'esempio per trame normali o non incapsulate, è possibile vedere che il percorso più breve tra i punti A e B non si trova più al centro della trama; ora si trova oltre il bordo in cui 0.0 e 1.0 sono presenti insieme. Il ritorno a capo nella direzione v è simile, ad eccezione del fatto che esegue il wrapping della trama intorno a un cilindro che si trova sul lato. Il wrapping in entrambe le direzioni u e v è più complesso. In questo caso, è possibile immaginare la trama come un torus o un anello.

L'applicazione pratica più comune per il wrapping delle trame consiste nell'eseguire il mapping dell'ambiente. In genere, un oggetto con trama con una mappa dell'ambiente appare molto riflettente, mostrando un'immagine speculare dell'ambiente circostante dell'oggetto nella scena. Ai fini di questa discussione, si immagini una stanza con quattro pareti, ognuna disegnata con una lettera R, G, B, Y e i colori corrispondenti: rosso, verde, blu e giallo. La mappa dell'ambiente per una stanza così semplice potrebbe essere simile alla figura seguente.

![illustrazione di strisce verticali di rosso, verde, blu e giallo](images/envmap.png)

Imagine che il limite massimo della stanza sia mantenuto da un pilastro perfettamente riflettente, a quattro lati. Il mapping della trama della mappa dell'ambiente al pilastro è semplice. fare in modo che il pilastro rifletta le lettere e i colori non è così semplice. Il diagramma seguente mostra un frame di collegamento del pilastro con le coordinate di trama applicabili elencate vicino ai vertici superiori. La linea di punteggiatura in cui il ritorno a capo attraversa i bordi della trama viene visualizzata con una linea tratteggiata.

![diagramma di un rettangolo con una linea punteggiata biecting](images/seam.png)

Con il ritorno a capo abilitato nella direzione u, il pilastro con trama mostra i colori e i simboli della mappa dell'ambiente in modo appropriato e, nella parte anteriore della trama, il rasterizzatore sceglie correttamente l'itinerario più breve tra le coordinate della trama, presupponendo che le coordinate u 0.0 e 1.0 concivano la stessa posizione. Il pilastro con trama è simile alla figura seguente.

![illustrazione di un pilastro costituito da quadranti rosso, verde, blu e giallo](images/tex-seam.png)

Se il wrapping della trama non è abilitato, il rasterizzatore non esegue l'interpolazione nella direzione necessaria per generare un'immagine riflessa e dispersibile. L'area all'inizio del pilastro contiene invece una versione compressa orizzontalmente dei texel tra le coordinate u 0,175 e 0,875, mentre passano attraverso il centro della trama. L'effetto wrap viene insodd distorsi.

## <a name="using-texture-wrapping"></a>Uso della disposizione testo con trama

Per abilitare il wrapping delle trame, chiamare il metodo [**IDirect3DDevice9::SetRenderState,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) come illustrato nell'esempio di codice seguente.


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



Il primo parametro accettato da [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) è uno stato di rendering da impostare. Specificare uno dei valori enumerati da \_ D3DRS WRAP0 a D3DRS WRAP7 che specificano il livello di trama per cui impostare \_ il ritorno a capo. Specificare i flag da D3DWRAPCOORD 0 a \_ D3DWRAPCOORD 3 nel secondo parametro per abilitare il wrapping della trama nella direzione corrispondente oppure combinarli per abilitare il ritorno a capo in più \_ direzioni. Se si omette un flag, il ritorno a capo della trama nella direzione corrispondente è disabilitato. Per disabilitare il wrapping della trama per un set di coordinate di trama, impostare il valore per lo stato di rendering corrispondente su 0.

Non confondere il wrapping della trama con le modalità di indirizzamento della trama con lo stesso nome. Il wrapping della trama viene eseguito prima dell'indirizzamento della trama. Assicurarsi che i dati di wrapping delle trame non contengano coordinate di trama al di fuori dell'intervallo \[ 0.0, 1.0 perché questo \] produrrà risultati indefiniti. Per altre informazioni sull'indirizzamento delle trame, vedere [Modalità di indirizzamento delle trame (Direct3D 9).](texture-addressing-modes.md)

## <a name="displacement-map-wrapping"></a>Wrapping della mappa di spostamento

Le mappe di spostamento vengono interpolate dal motore a tesselation. Poiché non è possibile specificare la modalità di ritorno a capo per il motore a trama, non è possibile eseguire il wrapping della trama con mappe di spostamento. Un'applicazione è in grado di usare un set di vertici che forza l'interpolazione a eseguire il wrapping in qualsiasi direzione. L'applicazione può anche specificare l'interpolazione da eseguire come semplice interpolazione lineare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
