---
description: Il modello Direct3D Light copre l'illuminazione ambientale, diffusa, speculare e emissivo.
ms.assetid: cf870c89-4be0-4b95-92aa-ec7bcdc6d9dd
title: Matematica dell'illuminazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683e320788d720883702ebfa56941b1a3a5cf090
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481093"
---
# <a name="mathematics-of-lighting-direct3d-9"></a>Matematica dell'illuminazione (Direct3D 9)

Il modello Direct3D Light copre l'illuminazione ambientale, diffusa, speculare e emissivo. Si tratta di una flessibilità sufficiente per la risoluzione di un'ampia gamma di situazioni di illuminazione. Si fa riferimento alla quantità totale di luce in una scena come illuminazione globale e la si calcola usando la seguente equazione.


```
Global Illumination = Ambient Light + Diffuse Light + Specular Light + Emissive Light 
```



[Illuminazione ambiente (Direct3D 9)](ambient-lighting.md) è un'illuminazione costante. È costante in tutte le direzioni e colora tutti i pixel di un oggetto lo stesso. Il calcolo è rapido, ma lascia gli oggetti più semplici e non realistici. Per vedere come viene calcolata l'illuminazione ambientale da Direct3D, vedere illuminazione ambiente (Direct3D 9).

[Illuminazione diffusa (Direct3D 9)](diffuse-lighting.md) dipende sia dalla direzione della luce che dalla normale della superficie dell'oggetto. Varia a seconda della superficie di un oggetto in seguito alla modifica della direzione della luce e al vettore numerico della superficie di modifica. È necessario più tempo per calcolare l'illuminazione diffusa perché cambia per ogni vertice dell'oggetto. Tuttavia, il vantaggio derivante dall'uso di questo approccio consiste nel fatto che applica una sfumatura agli oggetti e fornisce una profondità tridimensionale (3D). Per vedere come viene calcolata l'illuminazione diffusa in Direct3D, vedere illuminazione diffusa (Direct3D 9).

[Illuminazione speculare (Direct3D 9)](specular-lighting.md) identifica le evidenziazioni speculari brillanti che si verificano quando la luce raggiunge la superficie di un oggetto e la riflette verso la fotocamera. È più intenso della luce diffusa e si abbassa più rapidamente sulla superficie dell'oggetto. È necessario più tempo per calcolare l'illuminazione speculare rispetto all'illuminazione diffusa. Tuttavia, il vantaggio derivante dall'utilizzo di questa funzione è la possibilità di aggiungere dettagli significativi a una superficie. Per vedere come viene calcolata l'illuminazione speculare in Direct3D, vedere illuminazione speculare (Direct3D 9).

[Emissivo Lighting (Direct3D 9)](emissive-lighting.md) è una luce emessa da un oggetto; ad esempio, un bagliore. Per vedere come viene calcolata l'illuminazione emissivo in Direct3D, vedere illuminazione emissivo (Direct3D 9).

L'illuminazione realistica può essere eseguita applicando ognuno di questi tipi di illuminazione a una scena 3D. I valori calcolati per i componenti ambient, emissivo e Diffusion sono restituiti come colore del vertice diffuso; il valore per il componente illuminazione speculare viene restituito come colore del vertice speculare. I valori di ambiente, diffusione e luce speculare possono essere influenzati da un'attenuazione e da un fattore Spotlight della luce specificata. Per altre informazioni sul funzionamento dell'attenuazione, vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).

Per ottenere un effetto di illuminazione più realistico, è possibile aggiungere altre luci; Tuttavia, la scena richiede più tempo per il rendering. Per ottenere tutti gli effetti desiderati da una finestra di progettazione, alcuni giochi usano più energia della CPU rispetto a quella disponibile in genere. In questo caso, è tipico ridurre al minimo il numero di calcoli di illuminazione usando mappe di illuminazione e mappe dell'ambiente per aggiungere illuminazione a una scena quando si usano mappe di trame.

L'illuminazione viene calcolata nello spazio della fotocamera. Per vedere come vengono calcolate le trasformazioni di illuminazione, vedere la pagina relativa alle [trasformazioni dello spazio della fotocamera (Direct3D 9)](camera-space-transformations.md). L'illuminazione ottimizzata può essere calcolata nello spazio del modello, quando esistono condizioni speciali: i vettori normali sono già normalizzati (D3DRS \_ NORMALIZENORMALS è true), la fusione del vertex non è necessaria, le matrici di trasformazione sono ortogonali e così via.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Luci e materiali](lights-and-materials.md)
</dt> </dl>

 

 



