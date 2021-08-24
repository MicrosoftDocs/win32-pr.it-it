---
title: MultiThreading
description: Direct3D 11 implementa il supporto per la creazione e il rendering di oggetti usando più thread.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 718d80d9b70db0d6102d746168f338ddd8099339cee349724d87036714b16580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124326"
---
# <a name="multithreading"></a>MultiThreading

Direct3D 11 implementa il supporto per la creazione e il rendering di oggetti usando più thread.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                   | Descrizione                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introduzione al multithreading in Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | Il multithreading è progettato per migliorare le prestazioni eseguendo il lavoro usando uno o più thread contemporaneamente. <br/>                                                                                                         |
| [Creazione di oggetti con multithreading](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | Usare [**l'interfaccia ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) per creare risorse e oggetti, usare [**ID3D11DeviceContext per**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) il [rendering.](overviews-direct3d-11-render-multi-thread-render.md)<br/> |
| [Rendering immediato e posticipato](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | Direct3D 11 supporta due tipi di rendering: immediato e posticipato. Entrambi vengono implementati usando [**l'interfaccia ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/>                                                      |
| [Elenco comandi](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | Un elenco di comandi è una sequenza di comandi GPU che possono essere registrati e riprodotti. Un elenco di comandi può migliorare le prestazioni riducendo la quantità di overhead generato dal runtime.<br/>                                    |
| [Differenze di threading tra le versioni direct3D](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | Molti modelli di programmazione multi-thread usano primitive di sincronizzazione (ad esempio mutex) per creare sezioni critiche e impedire l'accesso al codice da più thread alla volta.<br/>                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedura: Controllare il supporto dei driver](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[Rendering](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





