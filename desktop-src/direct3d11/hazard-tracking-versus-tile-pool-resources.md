---
title: Verifica dei rischi e risorse pool di riquadri
description: Per le risorse non affiancate, Direct3D può impedire determinate condizioni di rischio durante il rendering, ma poiché il rilevamento dei rischi è a livello di riquadro per le risorse affiancate, il rilevamento delle condizioni di rischio durante il rendering delle risorse affiancate potrebbe essere troppo costoso.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395431"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a>Verifica dei rischi e risorse pool di riquadri

Per le risorse non affiancate, Direct3D può impedire determinate condizioni di rischio durante il rendering, ma poiché il rilevamento dei rischi è a livello di riquadro per le risorse affiancate, il rilevamento delle condizioni di rischio durante il rendering delle risorse affiancate potrebbe essere troppo costoso.

Per le risorse non affiancate, ad esempio, il runtime non consente l'associazione di una determinata sottorisorsa come input (ad esempio ShaderResourceView) e come output (ad esempio, RenderTargetView) allo stesso tempo. Se viene rilevato un caso di questo tipo, il runtime annulla l'associazione dell'input. Questo sovraccarico di rilevamento nel runtime è economico e viene eseguito a livello di sottorisorse. Uno dei vantaggi di questo sovraccarico di rilevamento consiste nel ridurre al minimo le probabilità che le applicazioni vengano accidentalmente a seconda dell'ordine di esecuzione dello shader. L'ordine di esecuzione dello shader hardware può variare in base a una determinata GPU (Graphics Processing Unit), quindi certamente tra le diverse GPU.

Il rilevamento delle risorse associate potrebbe essere troppo costoso per le risorse affiancate poiché il rilevamento è a livello di riquadro. Si verificano nuovi problemi, ad esempio la convalida dei tentativi di eseguire il rendering in un RenderTargetView con un riquadro mappato a più aree della superficie simultaneamente. Se questo rilevamento dei rischi per riquadro è troppo costoso per il runtime, idealmente questa sarebbe almeno un'opzione nel livello debug.

Un'applicazione deve informare il driver di visualizzazione quando ha emesso un'operazione di scrittura o lettura in una risorsa affiancata che fa riferimento alla memoria del pool di riquadri a cui verrà anche fatto riferimento da risorse affiancate separate nelle operazioni di lettura o scrittura imminenti che si prevede venga completata prima di poter iniziare le operazioni seguenti. Per altre informazioni su questa condizione, vedere [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) note.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping inclusi in un pool di riquadri](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




