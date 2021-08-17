---
description: Il modello di luce Direct3D copre l'illuminazione ambientale, diffusa, speculare ed emissiva.
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: Matematica dell'illuminazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1c6ffa8a1142c1be40993dcd8130b4708f2b509c8a5a1f05e234d0231c3bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728336"
---
# <a name="mathematics-of-lighting-direct3d-9"></a>Matematica dell'illuminazione (Direct3D 9)

Il modello di luce Direct3D copre l'illuminazione ambientale, diffusa, speculare ed emissiva. Questa flessibilità è sufficiente per risolvere un'ampia gamma di situazioni di illuminazione. Si fa riferimento alla quantità totale di luce in una scena come illuminazione globale e la si calcola usando l'equazione seguente.


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



[L'illuminazione ambientale (Direct3D 9) è](ambient-lighting.md) un'illuminazione costante. È costante in tutte le direzioni e colora tutti i pixel di un oggetto allo stesso modo. È veloce da calcolare, ma lascia gli oggetti appiattiti e non realistici. Per vedere come l'illuminazione ambientale viene calcolata da Direct3D, vedere Ambient Lighting (Direct3D 9) (Illuminazione ambientale (Direct3D 9).

[L'illuminazione diffusa (Direct3D 9)](diffuse-lighting.md) dipende sia dalla direzione della luce che dalla normale superficie dell'oggetto. Varia attraverso la superficie di un oggetto in seguito alla modifica della direzione della luce e del vettore numerico della superficie che cambia. Il calcolo dell'illuminazione diffusa richiede più tempo perché cambia per ogni vertice dell'oggetto, tuttavia il vantaggio di usarlo è la sfumatura degli oggetti e la profondità tridimensionale (3D). Per vedere come viene calcolata l'illuminazione diffusa in Direct3D, vedere Illuminazione diffusa (Direct3D 9).

[L'illuminazione speculare (Direct3D 9)](specular-lighting.md) identifica le evidenziazioni speculari luminosi che si verificano quando la luce raggiunge la superficie di un oggetto e si riflette di nuovo verso la fotocamera. È più intenso della luce diffusa e si spegne più rapidamente sulla superficie dell'oggetto. Il calcolo dell'illuminazione speculare rispetto all'illuminazione diffusa richiede più tempo, tuttavia il vantaggio di usarla è che aggiunge dettagli significativi a una superficie. Per vedere come viene calcolata l'illuminazione speculare in Direct3D, vedere Illuminazione speculare (Direct3D 9).

[L'illuminazione emissiva (Direct3D 9)](emissive-lighting.md) è una luce emessa da un oggetto. ad esempio un alone. Per informazioni su come viene calcolata l'illuminazione emissiva in Direct3D, vedere Emissive Lighting (Direct3D 9) (Illuminazione emissiva (Direct3D 9).

L'illuminazione realistica può essere eseguita applicando ognuno di questi tipi di illuminazione a una scena 3D. I valori calcolati per i componenti di ambiente, emissivi e diffusi vengono restituiti come colore del vertice diffuso. Il valore per il componente di illuminazione speculare viene restituito come colore del vertice speculare. I valori di luce ambientale, diffusa e speculare possono essere influenzati dall'attenuazione e dal fattore in evidenza di una determinata luce. Per altre informazioni sul funzionamento dell'attenuazione, vedere [Attenuazione e fattore spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)

Per ottenere un effetto di illuminazione più realistico, si aggiungono più luci; Tuttavia, il rendering della scena richiede più tempo. Per ottenere tutti gli effetti desiderati da un progettista, alcuni giochi usano una potenza della CPU maggiore di quella disponibile comunemente. In questo caso, è tipico ridurre al minimo il numero di calcoli di illuminazione usando le mappe di illuminazione e le mappe dell'ambiente per aggiungere illuminazione a una scena mentre si usano le mappe di trama.

L'illuminazione viene calcolata nello spazio della fotocamera. Per informazioni su come vengono calcolate le trasformazioni di illuminazione, vedere Trasformazioni dello spazio [della fotocamera (Direct3D 9).](camera-space-transformations.md) L'illuminazione ottimizzata può essere calcolata nello spazio del modello, quando esistono condizioni speciali: i vettori normali sono già normalizzati (D3DRS NORMALIZENORMALS è True), la fusione dei vertici non è necessaria, le matrici di trasformazione \_ sono ortogonali e così via.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Luci e materiali](lights-and-materials.md)
</dt> </dl>

 

 



