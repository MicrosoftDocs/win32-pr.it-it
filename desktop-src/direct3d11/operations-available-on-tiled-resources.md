---
title: Operazioni disponibili sulle risorse affiancate
description: In questa sezione sono elencate le operazioni che è possibile eseguire sulle risorse affiancate.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045138"
---
# <a name="operations-available-on-tiled-resources"></a>Operazioni disponibili sulle risorse affiancate

In questa sezione sono elencate le operazioni che è possibile eseguire sulle risorse affiancate.

-   void [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) e [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations-questi punti del punto di operazioni in una risorsa affiancata alle posizioni nei pool di sezioni, o a null o a entrambi. Queste operazioni possono aggiornare un subset non contiguo dei puntatori a sezioni.
-   \*Operazioni Copy () e Update \* (): tutte le API in grado di copiare dati da e verso una superficie del pool predefinita (ad esempio, [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) e [**ID3D11DeviceContext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) funzionano per le risorse affiancate. La lettura da riquadri non mappati produce 0 e le scritture nei riquadri non mappati vengono rimosse.
-   Operazioni [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) : queste operazioni sono disponibili per copiare i riquadri con granularità 64KB da e verso qualsiasi risorsa affiancata e una risorsa buffer in un layout di memoria canonico. Il driver di visualizzazione e l'hardware eseguono qualsiasi memoria "swizzling" necessaria per la risorsa affiancata.
-   Le associazioni della pipeline Direct3D e le creazioni/associazioni di visualizzazione che funzionano su risorse non affiancate funzionano anche con le risorse affiancate.

I controlli riquadro sono disponibili in contesti immediati o posticipati (proprio come gli aggiornamenti alle risorse tipiche) e, al momento dell'esecuzione, gli accessi successivi ai riquadri (non le operazioni inviate in precedenza).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

 




