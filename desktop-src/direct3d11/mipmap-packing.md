---
title: Compressione di mipmap
description: A seconda del livello di supporto per le risorse affiancate, mipmap con determinate dimensioni non seguono le forme standard del riquadro e sono considerate tutte raggruppate tra loro in modo che sia opaco per l'applicazione.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044424"
---
# <a name="mipmap-packing"></a>Compressione di mipmap

A seconda del [livello](tiled-resources-features-tiers.md) di supporto per le risorse affiancate, mipmap con determinate dimensioni non seguono le forme standard del riquadro e sono considerate tutte raggruppate tra loro in modo che sia opaco per l'applicazione. I livelli di supporto più elevati hanno garanzie più ampie sui tipi di dimensioni di superficie che si adattano alle forme di sezione standard (e possono quindi essere mappati singolarmente dalle applicazioni).

Ciò che può variare tra le implementazioni è che, date le dimensioni, il formato, il numero di mipmap e le sezioni di matrice di una risorsa affiancata, un numero di milioni di MIPS (per ogni sezione della matrice) può essere compresso in un numero N di riquadri. L'API [**ID3D11Device2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) esiste per consentire al driver di segnalare all'applicazione quali M e N sono, tra gli altri dettagli relativi alla superficie segnalata dall'API, che sono standard e non variano in base al fornitore dell'hardware. Il set di riquadri per i MIP compressi è ancora 64KB e può essere mappato singolarmente in posizioni diverse in un pool di sezioni. Tuttavia, la forma pixel dei riquadri e il modo in cui mipmap si adattano al set di riquadri sono specifici di un fornitore di hardware ed è troppo complesso da esporre. In questo modo, le applicazioni devono eseguire il mapping di tutti i riquadri designati come compressi o nessuno per volta. In caso contrario, il comportamento per l'accesso alla risorsa affiancata non è definito.

Per le superfici con matrici, il set di MIPS compresso e il numero di riquadri compressi che archiviano tali MIPS (M e N descritti in precedenza) si applica singolarmente per ogni sezione della matrice.

Le API dedicate per la copia dei riquadri ([**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) non possono accedere a MIPS compressi. Le applicazioni che vogliono copiare i dati da e verso i pacchetti MIPS possono eseguire questa operazione usando tutte le API specifiche delle risorse non affiancate per la copia e il rendering nelle superfici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come affiancare l'area di una risorsa affiancata](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




