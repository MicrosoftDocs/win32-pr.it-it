---
title: Walk-Throughs Codice D3D12
description: In questa sezione viene fornito il codice per gli scenari di esempio. Molti dei passaggi forniscono informazioni dettagliate su quale codifica è necessario aggiungere a un esempio di base, per evitare di ripetere il codice componente di base per ogni scenario.
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdea9b519e2a0adac9dc346d6bee455af0018da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104473"
---
# <a name="d3d12-code-walk-throughs"></a>Walk-Throughs Codice D3D12

In questa sezione viene fornito il codice per gli scenari di esempio. Molti dei passaggi forniscono informazioni dettagliate su quale codifica è necessario aggiungere a un esempio di base, per evitare di ripetere il codice componente di base per ogni scenario.

Per il componente più semplice, vedere la sezione [creazione di un componente Direct3D 12 di base](creating-a-basic-direct3d-12-component.md) . I passaggi seguenti descrivono scenari più avanzati.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [D2D con D3D11on12](d2d-using-d3d11on12.md)<br/>                                       | L'esempio **D3D1211on12** illustra come eseguire il rendering del contenuto di D2D sul contenuto di D3D12 condividendo le risorse tra un dispositivo basato su 11 e un dispositivo basato su 12. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Simulazione della gravità del corpo a più motori](multi-engine-n-body-gravity-simulation.md)<br/> | L'esempio **D3D12nBodyGravity** illustra come eseguire il lavoro di calcolo in modo asincrono. L'esempio avvia un numero di thread ciascuno con una coda di comandi di calcolo e pianifica il lavoro di calcolo sulla GPU che esegue una simulazione di gravità n corpo. Ogni thread opera su due buffer pieni di dati sulla posizione e sulla velocità. Con ogni iterazione, compute shader legge i dati della posizione e della velocità correnti da un buffer e scrive l'iterazione successiva nell'altro buffer. Al termine dell'iterazione, compute shader scambia quale buffer è il SRV per la lettura dei dati di posizione/velocità e che è il UAV per la scrittura di aggiornamenti della posizione/velocità modificando lo stato della risorsa in ogni buffer.<br/> |
| [Query predicazione](predication-queries.md)<br/>                                       | L'esempio **D3D12PredicationQueries** illustra l'abbattimento delle occlusioni usando gli heap di query DirectX 12 e predicazione. Nella procedura dettagliata viene descritto il codice aggiuntivo necessario per estendere l'esempio **HelloConstBuffer** per la gestione delle query predicazione. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Indicizzazione dinamica con HLSL 5,1](dynamic-indexing-using-hlsl-5-1.md)<br/>               | L'esempio **D3D12DynamicIndexing** illustra alcune delle nuove funzionalità di HLSL disponibili nel modello di shader 5,1, in particolare l'indicizzazione dinamica e le matrici non associate, per eseguire il rendering dello stesso mesh più volte, ogni volta che viene eseguito il rendering con un materiale selezionato dinamicamente. Con l'indicizzazione dinamica, è ora possibile indicizzare gli shader in una matrice senza conoscere il valore dell'indice in fase di compilazione. In combinazione con matrici non vincolate, viene aggiunto un altro livello di riferimento indiretto e flessibilità per gli autori dello shader e le pipeline di grafica.<br/>                                                                                                                                                                                  |
| [Disegno indiretto e eliminazione della GPU](indirect-drawing-and-gpu-culling-.md)<br/>            | Nell'esempio D3D12ExecuteIndirect viene illustrato come utilizzare i comandi indiretti per creare il contenuto. Viene inoltre illustrato come questi comandi possono essere modificati sulla GPU in un compute shader prima che vengano emessi. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Esercitazioni video su DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
</dt> <dt>

[Codice di esempio nel riferimento D3D12](notes-on-example-code.md)
</dt> <dt>

[Esempi di lavoro](working-samples.md)
</dt> </dl>

 

 





