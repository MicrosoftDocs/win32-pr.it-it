---
description: Per fare in modo che un'applicazione esegua il rendering realistico di una scena 3D, è necessario tenere in considerazione l'effetto delle fonti di luce sull'aspetto della scena.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Mapping chiaro con trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304096"
---
# <a name="light-mapping-with-textures-direct3d-9"></a>Mapping chiaro con trame (Direct3D 9)

Per fare in modo che un'applicazione esegua il rendering realistico di una scena 3D, è necessario tenere in considerazione l'effetto delle fonti di luce sull'aspetto della scena. Sebbene le tecniche, ad esempio l'ombreggiatura flat e Gouraud, siano strumenti preziosi in questo senso, possono essere insufficienti per le proprie esigenze. Direct3D supporta il Multipass e la combinazione di più trame. Queste funzionalità consentono all'applicazione di eseguire il rendering di scene con un aspetto più realistico rispetto alle scene sottoposte a rendering solo con tecniche di ombreggiatura. Applicando una o più mappe chiare, l'applicazione può mappare le aree di luce e ombreggiatura alle relative primitive.

Una mappa leggera è una trama o un gruppo di trame che contiene informazioni sull'illuminazione in una scena 3D. È possibile archiviare le informazioni sull'illuminazione nei valori alfa della mappa chiara, nei valori dei colori o in entrambi.

Se si implementa il mapping chiaro con la combinazione di trame MultiPASS, l'applicazione deve eseguire il rendering della mappa chiara sulle primitive al primo passaggio. Deve usare un secondo passaggio per eseguire il rendering della trama di base. L'eccezione è rappresentata dal mapping chiaro speculare. In tal caso, eseguire prima il rendering della trama di base; quindi aggiungere la mappa chiara.

La combinazione di più trame consente all'applicazione di eseguire il rendering della mappa chiara e della trama di base in un unico passaggio. Se l'hardware dell'utente fornisce la combinazione di più trame, l'applicazione deve sfruttarla quando esegue il mapping chiaro. Ciò migliora significativamente le prestazioni dell'applicazione.

Con le mappe leggere, un'applicazione Direct3D può ottenere un'ampia gamma di effetti di illuminazione quando esegue il rendering delle primitive. Consente di eseguire il mapping non solo di luci monocromatiche e colorate in una scena, ma anche di aggiungere dettagli come evidenziazioni speculari e illuminazione diffusa.

Per informazioni sull'uso della combinazione di trame Direct3D per eseguire il mapping chiaro, vedere gli argomenti seguenti.

-   [Mappe chiare monocromatiche (Direct3D 9)](monochrome-light-maps.md)
-   [Mappe per la luce del colore (Direct3D 9)](color-light-maps.md)
-   [Mappe chiare speculari (Direct3D 9)](specular-light-maps.md)
-   [Mappe chiare diffuse (Direct3D 9)](diffuse-light-maps.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazione di trame](texture-blending.md)
</dt> </dl>

 

 



