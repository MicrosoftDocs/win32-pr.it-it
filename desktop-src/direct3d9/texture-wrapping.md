---
description: In breve, il ritorno a capo delle trame modifica la modalità di base in cui Direct3D Rasterizza i poligoni con trama usando le coordinate di trama specificate per ogni vertice.
ms.assetid: 00683d3f-3e3c-4ee4-9aec-a0d7fd9c8941
title: Wrapping di trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7c0f8cb6d7793536999d5f3df128849572d3dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521418"
---
# <a name="texture-wrapping-direct3d-9"></a>Wrapping di trama (Direct3D 9)

In breve, il ritorno a capo delle trame modifica la modalità di base in cui Direct3D Rasterizza i poligoni con trama usando le coordinate di trama specificate per ogni vertice. Durante la rasterizzazione di un poligono, il sistema Interpola tra le coordinate di trama in ogni vertice del poligono per determinare i Texel da usare per ogni pixel del poligono. In genere, il sistema considera la trama come un piano 2D, interpolando i nuovi Texel prendendo la route più breve dal punto A all'interno di una trama al punto B. Se il punto A rappresenta la posizione u, v (0,8, 0,1) e il punto B è in corrispondenza di (0.1, 0.1), la riga di interpolazione è simile al diagramma seguente.

![diagramma di una linea di interpolazione tra due punti](images/interp1.png)

Si noti che la distanza più breve tra A e B in questa illustrazione viene eseguita approssimativamente al centro della trama. Abilitazione della trama u o della coordinata v-wrapping delle coordinate modifica il modo in cui Direct3D percepisce il percorso più breve tra le coordinate di trama nella direzione u e la direzione v. Per definizione, il wrapping della trama fa in modo che l'rasterizzatore prenda il percorso più breve tra i set di coordinate di trama, supponendo che 0,0 e 1,0 siano coincidenti. L'ultimo bit è la parte ingannevole: è possibile immaginare che l'abilitazione del wrapping della trama in una direzione induce il sistema a trattare una trama come se fosse stata avvolta intorno a un cilindro. Si consideri ad esempio il diagramma seguente.

![diagramma di una trama e due punti racchiusi intorno a un cilindro](images/interp2.png)

L'illustrazione precedente Mostra come il ritorno a capo nella direzione u influisca sulla modalità di interpolazione delle coordinate di trama da parte del sistema. Utilizzando gli stessi punti dell'esempio per le trame normali o non incapsulate, è possibile osservare che la route più breve tra i punti A e B non si trova più in mezzo alla trama; si trova ora oltre il bordo dove 0,0 e 1,0 sono presenti insieme. Il wrapping nella direzione v è simile, ad eccezione del fatto che esegue il wrapping della trama intorno a un cilindro che si trova sul lato. Il wrapping sia nella direzione u che nella direzione v è più complesso. In questa situazione, è possibile prevedere la trama come Torus o ad anello.

L'applicazione pratica più comune per il wrapping della trama consiste nell'eseguire il mapping dell'ambiente. In genere, un oggetto con trama con una mappa dell'ambiente viene visualizzato molto riflettente, mostrando un'immagine speculare dell'ambiente dell'oggetto nella scena. Ai fini di questa discussione, si immagini una stanza con quattro pareti, ciascuna dipinta con una lettera R, G, B, Y e i colori corrispondenti: rosso, verde, blu e giallo. La mappa dell'ambiente per una semplice stanza potrebbe avere un aspetto simile a quello illustrato nella figura seguente.

![illustrazione di strisce verticali di rosso, verde, blu e giallo](images/envmap.png)

Si supponga che il soffitto della stanza sia mantenuto da un pilastro perfettamente riflettente e a quattro lati. Il mapping della trama della mappa dell'ambiente al pilastro è semplice; l'aspetto del pilastro come se riflettesse le lettere e i colori non è altrettanto semplice. Nel diagramma seguente viene illustrata una cornice metallica del pilastro con le coordinate di trama applicabili elencate vicino ai vertici principali. La linea di giunzione in cui il wrapping attraverserà i bordi della trama viene visualizzata con una linea tratteggiata.

![diagramma di un rettangolo con una linea tratteggiata bisecante](images/seam.png)

Con il wrapping abilitato nell'u-Direction, la colonna con trama Mostra i colori e i simboli della mappa dell'ambiente in modo appropriato e, alla cucitura nella parte anteriore della trama, il rasterizzatore sceglie correttamente la route più breve tra le coordinate di trama, supponendo che le coordinate u 0,0 e 1,0 condividano la stessa posizione. Il pilastro con trama ha un aspetto simile a quello illustrato nella figura seguente.

![illustrazione di un pilastro costituito da quadranti rosso, verde, blu e giallo](images/tex-seam.png)

Se il wrapping della trama non è abilitato, il rasterizzatore non esegue l'interpolazione nella direzione necessaria per generare un'immagine riflessa credibile. Piuttosto, l'area nella parte anteriore del pilastro contiene una versione compressa orizzontalmente dei Texel tra le coordinate u 0,175 e 0,875, perché passano attraverso il centro della trama. L'effetto a capo è stato rovinato.

## <a name="using-texture-wrapping"></a>Uso del wrapping della trama

Per abilitare il wrapping della trama, chiamare il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) , come illustrato nell'esempio di codice riportato di seguito.


```
d3dDevice->SetRenderState(D3DRS_WRAP0, D3DWRAPCOORD_0);
```



Il primo parametro accettato da [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) è uno stato di rendering da impostare. Specificare uno dei WRAP0 D3DRS \_ tramite \_ i valori enumerati di D3DRS WRAP7 che specificano il livello di trama per cui impostare il wrapping. Specificare i flag D3DWRAPCOORD da \_ 0 a D3DWRAPCOORD \_ 3 nel secondo parametro per abilitare il wrapping della trama nella direzione corrispondente o combinarli per abilitare il wrapping in più direzioni. Se si omette un flag, il wrapping della trama nella direzione corrispondente è disabilitato. Per disabilitare il wrapping della trama per un set di coordinate di trama, impostare il valore dello stato di rendering corrispondente su 0.

Non confondere il wrapping della trama con le modalità di indirizzamento della trama con nome simile. Il wrapping della trama viene eseguito prima dell'indirizzamento della trama. Assicurarsi che i dati di wrapping della trama non contengano coordinate di trama non comprese nell'intervallo \[ 0,0, 1,0 \] perché verranno generati risultati non definiti. Per altre informazioni sull'indirizzamento delle trame, vedere [modalità di indirizzamento delle trame (Direct3D 9)](texture-addressing-modes.md).

## <a name="displacement-map-wrapping"></a>Wrapping della mappa di spostamento

Le mappe di spostamento vengono interpolate dal motore geometrica. Poiché non è possibile specificare la modalità wrap per il motore a mosaico, non è possibile eseguire il wrapping della trama con le mappe di spostamento. Un'applicazione è in grado di utilizzare un set di vertici che impone il wrapping dell'interpolazione in qualsiasi direzione. L'applicazione può inoltre specificare l'interpolazione da eseguire come un'interpolazione lineare semplice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
