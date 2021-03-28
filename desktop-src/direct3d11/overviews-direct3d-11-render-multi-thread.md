---
title: MultiThreading
description: Direct3D 11 implementa il supporto per la creazione e il rendering di oggetti usando più thread.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221749"
---
# <a name="multithreading"></a>MultiThreading

Direct3D 11 implementa il supporto per la creazione e il rendering di oggetti usando più thread.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                   | Descrizione                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introduzione al multithreading in Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | Il multithreading è progettato per migliorare le prestazioni eseguendo il lavoro utilizzando uno o più thread contemporaneamente. <br/>                                                                                                         |
| [Creazione di oggetti con multithreading](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | Utilizzare l'interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) per creare risorse e oggetti, utilizzare [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) per il [rendering](overviews-direct3d-11-render-multi-thread-render.md).<br/> |
| [Rendering immediato e posticipato](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | Direct3D 11 supporta due tipi di rendering: immediato e posticipato. Entrambe le implementazioni sono implementate tramite l'interfaccia [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .<br/>                                                      |
| [Elenco comandi](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | Un elenco di comandi è una sequenza di comandi GPU che possono essere registrati e riprodotti. Un elenco di comandi può migliorare le prestazioni riducendo la quantità di overhead generato dal runtime.<br/>                                    |
| [Differenze di threading tra le versioni di Direct3D](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | Molti modelli di programmazione multithread utilizzano le primitive di sincronizzazione (ad esempio, mutex) per creare sezioni critiche e impedire l'accesso al codice da parte di più thread alla volta.<br/>                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedura: verificare il supporto dei driver](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[Rendering](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





