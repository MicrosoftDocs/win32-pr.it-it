---
description: 'Impostando il parametro FVF del metodo IDirect3DDevice9:: CreateVertexBuffer su un valore diverso da zero, che deve essere un codice FVF valido, viene indicato che il contenuto del buffer deve essere caratterizzato da un codice FVF.'
ms.assetid: 7cab559f-3e9d-46bd-b00f-439e0922aeeb
title: Buffer vertex FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86201c3ddc1cab6d492539caccc61c1430b3a2c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303804"
---
# <a name="fvf-vertex-buffers-direct3d-9"></a>Buffer vertex FVF (Direct3D 9)

Impostando il parametro FVF del metodo [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/desktop/api) su un valore diverso da zero, che deve essere un codice FVF valido, viene indicato che il contenuto del buffer deve essere caratterizzato da un codice FVF. Un buffer di vertici creato con un codice FVF viene definito buffer dei vertici FVF. Alcuni metodi o usi di [**IDirect3DDevice9**](/windows/desktop/api) richiedono buffer dei vertici FVF e altri richiedono buffer di Vertex non FVF. I buffer vertex FVF sono obbligatori come argomento del buffer dei vertici di destinazione per [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).

I buffer vertex FVF possono essere associati a un flusso di dati di origine per qualsiasi numero di flusso.

La presenza del componente D3DFVF \_ XYZRHW nei buffer dei vertici FVF indica che i vertici nel buffer sono stati elaborati. Buffer vertex usati per [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) i buffer del vertice di destinazione devono essere post-elaborati. I buffer vertex usati per gli input di shader con funzioni fisse possono essere pre-elaborati o postelaborati. Se il buffer dei vertici è post-elaborazione, lo shader viene effettivamente ignorato e i dati vengono passati direttamente al modulo di ritaglio e configurazione primitivi.

I buffer vertex FVF possono essere usati con i vertex shader. Inoltre, i flussi di vertici possono rappresentare gli stessi formati di vertice che possono essere presenti nei buffer dei vertici non FVF. Non è necessario utilizzarli per inserire dati da buffer di vertici distinti. La flessibilità aggiuntiva dei nuovi flussi di vertici consente alle applicazioni che devono garantire la separazione dei dati per un funzionamento migliore, ma non è obbligatorio. Se l'applicazione è in grado di gestire i dati con interfoliazione in anticipo, si tratta di un incremento delle prestazioni. Se l'applicazione eseguirà l'interleave solo dei dati prima di ogni chiamata di rendering, deve abilitare l'API o l'hardware per eseguire questa operazione con più flussi.

Gli elementi più importanti con le prestazioni dei vertici sono l'uso di un vertice a 32 byte e la gestione di un corretto ordinamento della cache.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer vertici](vertex-buffers.md)
</dt> </dl>

 

 
