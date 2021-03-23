---
title: Esempi di lavoro
description: Gli esempi operativi sono disponibili per il download, mostrando l'utilizzo di una serie di funzionalità di Direct3D 12.
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1b61ec374e21c9173797121ee90ec72e789de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104069"
---
# <a name="working-samples"></a>Esempi di lavoro

Gli esempi operativi sono disponibili per il download, mostrando l'utilizzo di una serie di funzionalità di Direct3D 12.

## <a name="working-samples"></a>Esempi di lavoro

Gli esempi funzionanti (sotto forma di progetti Visual Studio 2015) possono essere scaricati da [GitHub/Microsoft/DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples).

> [!Note]  
> L'elenco esatto degli esempi disponibili in questo percorso varia a seconda che gli esempi vengano aggiunti e aggiornati.

 



<table>
<thead>
<tr class="header">
<th>Titolo di esempio</th>
<th>Descrizione</th>
<th>Desktop</th>
<th>Piattaforma UWP</th>
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
<td>Il set di esempi HelloWorld contiene i seguenti progetti semplici che consentono di iniziare a usare Direct3D 12.<dl> Crea una finestra per preparare il rendering del contenuto Direct3D 12.<br />
Esegue il rendering di un triangolo semplice usando Direct3D 12.<br />
Viene illustrato l'utilizzo di un bundle per il rendering con Direct3D 12.<br />
Viene illustrato come utilizzare i buffer costanti per passare dati alla GPU utilizzata per il rendering in Direct3D 12.<br />
Viene illustrato come applicare una trama a un triangolo usando Direct3D 12.<br />
</dl></td>
<td>S</td>
<td>S</td>
<td><a href="creating-a-basic-direct3d-12-component.md">Creazione di un componente Direct3D 12 di base</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>Illustra le procedure consigliate per la memorizzazione nel buffer e la sincronizzazione dei frame, nonché il rendering di una rete semplice con bundle.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>Esempio di compilazione di un'applicazione con supporto multithreading.</td>
<td>S</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyGravity</td>
<td>Viene illustrato come usare più motori per eseguire operazioni di calcolo asincrone insieme a un lavoro 3D sulla stessa GPU.</td>
<td>S</td>
<td>S</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">Simulazione della gravità del corpo a più motori</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>Illustra l'abbattimento di occlusione usando heap di query e predicazione.</td>
<td>S</td>
<td>S</td>
<td><a href="predication-queries.md">Query predicazione</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>Illustra le funzionalità di indicizzazione dinamica di DirectX 12 e HLSL.</td>
<td>S</td>
<td>S</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">Indicizzazione dinamica con HLSL 5,1</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>Viene illustrato l'utilizzo di base del livello 11on12. Questo esempio esegue il rendering del testo usando D2D usando l'API Direct3D 11 in un dispositivo Direct3D 12 11on12.</td>
<td>S</td>
<td>S</td>
<td><a href="d2d-using-d3d11on12.md">D2D con D3D11on12</a></td>
</tr>
<tr class="even">
<td>D3D12ExecuteIndirect</td>
<td>Viene illustrata l'eliminazione del motore di calcolo insieme alla funzionalità Esegui indirect per eseguire il rendering solo degli oggetti che superano il test di eliminazione.</td>
<td>S</td>
<td>S</td>
<td><a href="indirect-drawing-and-gpu-culling-.md">Disegno indiretto e eliminazione della GPU</a></td>
</tr>
<tr class="odd">
<td>D3D12PipelineStateCache</td>
<td>Viene illustrata la memorizzazione nella cache dell'oggetto di stato della pipeline.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="even">
<td>D3D12Fullscreen</td>
<td>Viene illustrato come gestire le transizioni da schermo intero a finestra e il ridimensionamento delle finestre in DirectX 12.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="odd">
<td>D3D12HeterogeneousMultiadapter</td>
<td>Illustra come condividere i carichi di lavoro tra più GPU eterogeneo usando gli heap condivisi.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>Viene illustrato l'utilizzo delle risorse riservate (affiancate). In questo esempio un quad è tramato con una risorsa riservata contenente una catena MIP completa.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>Si tratta di una soluzione con costi di integrazione ridotta per gestire gli heap e le risorse di cui è stato eseguito il commit in Direct3D 12, usando le tecniche di gestione della memoria di Direct3D 11.</td>
<td>S</td>
<td>S</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>Viene illustrato l'uso di piccole risorse posizionate, mostrando i potenziali risparmi di memoria ottenuti usando le risorse posizionate (con un allineamento 4K) sulle risorse sottoposte a commit e riservate (con un allineamento 64K).</td>
<td>S</td>
<td>S</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Procedure dettagliate per il codice D3D12](d3d12-code-walk-throughs.md)
</dt> </dl>

 

 




