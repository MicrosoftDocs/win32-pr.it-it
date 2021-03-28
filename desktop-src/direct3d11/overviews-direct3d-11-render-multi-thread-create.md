---
title: Creazione di oggetti con multithreading
description: Utilizzare l'interfaccia ID3D11Device per creare risorse e oggetti, utilizzare sul ID3D11DeviceContext per il rendering.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955493"
---
# <a name="object-creation-with-multithreading"></a>Creazione di oggetti con multithreading

Utilizzare l'interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) per creare risorse e oggetti, utilizzare [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) per il [rendering](overviews-direct3d-11-render-multi-thread-render.md).

Di seguito sono riportati alcuni esempi di come creare le risorse:

-   [Procedura: creare un vertex buffer](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [Procedura: creare un buffer di indice](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [Procedura: creare un buffer costante](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [Procedura: inizializzare una trama da un file](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a>Considerazioni sul multithreading

La quantità di concorrenza della creazione e del rendering delle risorse che l'applicazione può ottenere dipende dal livello di supporto del multithreading implementato dal driver. Se il driver supporta le operazioni di creazione simultanea, l'applicazione dovrebbe presentare problemi di concorrenza molto inferiori. Tuttavia, se il driver non supporta la creazione di oggetti simultanei, la quantità di concorrenza è estremamente limitata. Per comprendere la quantità di supporto disponibile in un driver, eseguire una query sul driver per il valore del membro **DriverConcurrentCreates** della struttura di [**\_ \_ \_ Threading dei dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) . Per ulteriori informazioni sul controllo del supporto dei driver per il multithreading, vedere [procedura: verificare il supporto del driver](overviews-direct3d-11-render-multi-thread-support.md).

Le operazioni simultanee non portano necessariamente a prestazioni migliori. La creazione e il caricamento di una trama, ad esempio, è in genere limitata dalla larghezza di banda della memoria. Il tentativo di creare e caricare più trame potrebbe non essere più veloce rispetto a una trama alla volta, anche se questa operazione lascia inattivi più core CPU. Tuttavia, la creazione di più shader che usano più thread può migliorare le prestazioni perché questa operazione è meno dipendente dalle risorse di sistema, ad esempio la larghezza di banda della memoria.

Quando il driver e l'hardware grafico supportano il multithreading, è in genere possibile inizializzare in modo più efficiente le risorse appena create passando un puntatore ai dati iniziali nel parametro *pInitialData* , ad esempio in una chiamata al metodo [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




