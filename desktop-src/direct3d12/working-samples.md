---
title: Esempi funzionanti
description: Sono disponibili esempi funzionanti per il download, che mostrano l'utilizzo di alcune funzionalità di Direct3D 12.
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6f8bad1d20729f4caa78952feda22378ad37526b33b668e79260ef9658da53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631883"
---
# <a name="working-samples"></a>Esempi funzionanti

Sono disponibili esempi funzionanti per il download, che mostrano l'utilizzo di alcune funzionalità di Direct3D 12.

## <a name="working-samples"></a>Esempi funzionanti

Gli esempi funzionanti (sotto forma di Visual Studio 2015) possono essere scaricati [da GitHub/Microsoft/DirectX-Graphics-Samples.](https://github.com/Microsoft/DirectX-Graphics-Samples)

> [!Note]  
> L'elenco esatto degli esempi disponibili in questa posizione varia in base all'aggiunta e all'aggiornamento degli esempi.

 



<table>
<thead>
<tr class="header">
<th>Titolo di esempio</th>
<th>Descrizione</th>
<th>Desktop</th>
<th>UWP</th>
<th>Procedura dettagliata</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HelloWorld<dl> HelloWindow<br />
HelloTriangle<br />
HelloBundles<br />
HelloConstBuffers<br />
HelloTexture<br />
</dl></td>
<td>Il set di esempi HelloWorld contiene i semplici progetti seguenti che consentono di iniziare a usare Direct3D 12.<dl> Crea una finestra in preparazione del rendering del contenuto Direct3D 12.<br />
Esegue il rendering di un triangolo semplice usando Direct3D 12.<br />
Illustra l'uso di un bundle per il rendering con Direct3D 12.<br />
Illustra come usare buffer costanti per passare dati alla GPU usata per il rendering in Direct3D 12.<br />
Illustra come applicare una trama a un triangolo usando Direct3D 12.<br />
</dl></td>
<td>S</td>
<td>S</td>
<td><a href="creating-a-basic-direct3d-12-component.md">Creazione di un componente Direct3D 12 di base</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>Illustra le procedure consigliate per il buffering dei frame e la sincronizzazione, nonché il rendering di una mesh semplice tramite bundle.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>Esempio di come compilare un'applicazione con supporto multithreading.</td>
<td>S</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyGravity</td>
<td>Illustra come è possibile usare più motori per eseguire operazioni di calcolo asincrone insieme a operazioni 3D sulla stessa GPU.</td>
<td>S</td>
<td>S</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">Simulazione della gravità n-corpo multimotore</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>Illustra il culling dell'occlusione tramite heap di query e predicazione.</td>
<td>S</td>
<td>S</td>
<td><a href="predication-queries.md">Query di predicazione</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>Illustra le funzionalità di indicizzazione dinamica di DirectX 12 e HLSL.</td>
<td>S</td>
<td>S</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">Indicizzazione dinamica con HLSL 5.1</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>Illustra l'utilizzo di base del livello 11on12. Questo esempio esegue il rendering del testo usando D2D usando l'API Direct3D 11 in un dispositivo Direct3D 12 11on12.</td>
<td>S</td>
<td>S</td>
<td><a href="d2d-using-d3d11on12.md">D2D con D3D11on12</a></td>
</tr>
<tr class="even">
<td>D3D12ExecuteIndirect</td>
<td>Illustra il culling del motore di calcolo insieme alla funzionalità di esecuzione indiretta per eseguire solo il rendering degli oggetti che superano il test di culling.</td>
<td>S</td>
<td>S</td>
<td><a href="indirect-drawing-and-gpu-culling-.md">Disegno indiretto e culling della GPU</a></td>
</tr>
<tr class="odd">
<td>D3D12PipelineStateCache</td>
<td>Illustra la memorizzazione nella cache dell'oggetto di stato della pipeline (PSO).</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="even">
<td>D3D12Fullscreen</td>
<td>Illustra come gestire le transizioni a schermo intero e il ridimensionamento delle finestre in DirectX 12.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="odd">
<td>D3D12HeterogeneousMultiadapter</td>
<td>Illustra come condividere i carichi di lavoro tra più GPU eterogenee usando heap condivisi.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>Illustra l'uso di risorse riservate (affiancate). In questo esempio viene con trama un quad con una risorsa riservata contenente una catena mip completa.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>Si tratta di una soluzione a basso costo di integrazione per la gestione degli heap Direct3D 12 e delle risorse di cui è stato eseguito il commit, usando le tecniche di gestione della memoria di Direct3D 11.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>Illustra l'uso di risorse di piccole dimensioni, che mostrano i potenziali risparmi di memoria ottenuti usando le risorse posizionate (con un allineamento di 4 KB) rispetto alle risorse riservate e di cui è stato eseguito il commit (con un allineamento di 64 KB).</td>
<td>S</td>
<td>S</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Procedura per il codice D3D12](d3d12-code-walk-throughs.md)
</dt> </dl>

 

 




