---
title: Codice D3D12 Walk-Throughs
description: In questa sezione viene fornito il codice per scenari di esempio. Molte delle operazioni dettagliate forniscono informazioni dettagliate sul codice che è necessario aggiungere a un esempio di base, per evitare di ripetere il codice del componente di base per ogni scenario.
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fc076657d8a9096d1206adc9c61b6dc16fc95792dc0c0da2fcd636377b7ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497201"
---
# <a name="d3d12-code-walk-throughs"></a>Codice D3D12 Walk-Throughs

In questa sezione viene fornito il codice per scenari di esempio. Molte delle operazioni dettagliate forniscono informazioni dettagliate sul codice che è necessario aggiungere a un esempio di base, per evitare di ripetere il codice del componente di base per ogni scenario.

Per il componente più semplice, vedere la sezione Creazione di un componente [Direct3D 12 di](creating-a-basic-direct3d-12-component.md) base. Le procedure guidate seguenti descrivono scenari più avanzati.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [D2D con D3D11on12](d2d-using-d3d11on12.md)<br/>                                       | **L'esempio D3D1211on12** illustra come eseguire il rendering del contenuto D2D sul contenuto D3D12 condividendo le risorse tra un dispositivo basato su 11 e un dispositivo basato su 12. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Simulazione della gravità n-corpo a più motori](multi-engine-n-body-gravity-simulation.md)<br/> | **L'esempio D3D12nBodyGravity** illustra come eseguire operazioni di calcolo in modo asincrono. L'esempio ruota un numero di thread ognuno con una coda di comandi di calcolo e pianifica il lavoro di calcolo sulla GPU che esegue una simulazione della gravità n-body. Ogni thread opera su due buffer con dati relativi a posizione e velocità. A ogni iterazione, lo shader di calcolo legge i dati di posizione e velocità correnti da un buffer e scrive l'iterazione successiva nell'altro buffer. Al termine dell'iterazione, il compute shader scambia quale buffer è il valore SRV per la lettura dei dati di posizione/velocità e che è l'UAV per la scrittura di aggiornamenti di posizione/velocità modificando lo stato della risorsa in ogni buffer.<br/> |
| [Query di predicazione](predication-queries.md)<br/>                                       | **L'esempio D3D12PredicationQueries** illustra l'eliminazione dell'occlusione tramite heap di query e predicazione DirectX 12. La procedura dettagliata descrive il codice aggiuntivo necessario per estendere **l'esempio HelloConstBuffer** per gestire le query di predicazione. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Indicizzazione dinamica con HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)<br/>               | L'esempio **D3D12DynamicIndexing** illustra alcune delle nuove funzionalità HLSL disponibili in Shader Model 5.1, in particolare l'indicizzazione dinamica e le matrici non associate, per eseguire il rendering della stessa mesh più volte, ogni volta che ne viene eseguito il rendering con un materiale selezionato dinamicamente. Con l'indicizzazione dinamica, gli shader possono ora indicizzare in una matrice senza conoscere il valore dell'indice in fase di compilazione. In combinazione con matrici non associate, questo aggiunge un altro livello di riferimento indiretto e flessibilità per gli autori di shader e le pipeline di grafica.<br/>                                                                                                                                                                                  |
| [Disegno indiretto ed culling GPU](indirect-drawing-and-gpu-culling-.md)<br/>            | L'esempio D3D12ExecuteIndirect illustra come usare i comandi indiretti per disegnare contenuto. Illustra anche come questi comandi possono essere manipolati nella GPU in un compute shader prima che siano emessi. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Esercitazioni video sull'apprendimento avanzato di DirectX](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
</dt> <dt>

[Codice di esempio nel riferimento D3D12](notes-on-example-code.md)
</dt> <dt>

[Esempi di lavoro](working-samples.md)
</dt> </dl>

 

 





