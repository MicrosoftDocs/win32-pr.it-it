---
description: L'aggiunta di una nebbia a una scena 3D può migliorare il realismo, fornire un ambiente o impostare un mood e nascondere gli artefatti a volte quando viene visualizzata la geometria distanti.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303806"
---
# <a name="fog-direct3d-9"></a>Nebbia (Direct3D 9)

L'aggiunta di una nebbia a una scena 3D può migliorare il realismo, fornire un ambiente o impostare un mood e nascondere gli artefatti a volte quando viene visualizzata la geometria distanti. Direct3D supporta due modelli di nebbia, la nebbia dei pixel e la nebbia dei vertici, ognuno con funzionalità e interfaccia di programmazione personalizzate.

In sostanza, la nebbia viene implementata combinando il colore degli oggetti in una scena con un colore di nebbia scelto in base alla profondità di un oggetto in una scena o la relativa distanza dal punto di vista. Man mano che gli oggetti crescono più distanti, il colore originale si mescola sempre più con il colore di nebbia scelto, creando l'illusione che l'oggetto sia sempre più nascosto da piccole particelle fluttuanti nella scena. Nella figura seguente viene mostrata una scena di cui viene eseguito il rendering senza nebbia e viene visualizzata una scena simile con la nebbia abilitata.

![illustrazione della stessa scena con e senza nebbia](images/fogcomp.png)

In questa illustrazione, la scena a sinistra ha un orizzonte chiaro, oltre il quale non è visibile alcuno scenario, anche se sarebbe visibile nel mondo reale. La scena a destra nasconde l'orizzonte usando un colore di nebbia identico al colore di sfondo, facendo in modo che i poligoni sembrino dissolversi nella distanza. Combinando gli effetti di nebbia discreti con la progettazione della scena creativa è possibile aggiungere umore e ammorbidire il colore degli oggetti in una scena.

Direct3D offre due modi per aggiungere la nebbia a una scena: la nebbia dei pixel e la nebbia del vertice, denominate per la modalità di applicazione degli effetti di nebbia. Per informazioni dettagliate, vedere [pixel Fog (Direct3D 9)](pixel-fog.md) e [Vertex Fog (Direct3D 9)](vertex-fog.md). In breve, la nebbia dei pixel, detta anche nebbia della tabella, è implementata nel driver di dispositivo e la nebbia del vertice viene implementata nel motore di illuminazione Direct3D. Un'applicazione può implementare la nebbia con un vertex shader e contemporaneamente la nebbia pixel, se lo si desidera.

> [!Note]  
> Indipendentemente dal fatto che si usi la nebbia pixel o vertex, l'applicazione deve fornire una matrice di proiezione conforme per assicurarsi che gli effetti di nebbia siano applicati correttamente. Questa restrizione si applica anche alle applicazioni che non utilizzano il motore di trasformazione e illuminazione Direct3D. Per ulteriori informazioni su come fornire una matrice appropriata, vedere [proiezione Transform (Direct3D 9)](projection-transform.md).

 

Gli argomenti seguenti introducono la nebbia e presentano informazioni sull'uso di varie funzionalità di nebbia nelle applicazioni Direct3D.

-   [Formule Fog (Direct3D 9)](fog-formulas.md)
-   [Parametri di nebbia (Direct3D 9)](fog-parameters.md)
-   [Blending di nebbia (Direct3D 9)](fog-blending.md)
-   [Colore nebbia (Direct3D 9)](fog-color.md)
-   [Nebbia vertice (Direct3D 9)](vertex-fog.md)
-   [Nebbia pixel (Direct3D 9)](pixel-fog.md)

La fusione di nebbia è controllata dagli Stati di rendering; non fa parte della pipeline di pixel programmabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



