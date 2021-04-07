---
description: Interfacce di streaming di DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfacce di streaming di DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048973"
---
# <a name="directdraw-streaming-interfaces"></a>Interfacce di streaming di DirectDraw

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.

 

Se nei flussi si utilizzano formati video supportati da DirectDraw, le interfacce seguenti consentono un controllo più efficace sui dati rispetto alle interfacce di base più generiche.



| Interfaccia                                                  | Descrizione                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Imposta e recupera il formato del flusso e l'oggetto DirectDraw associato al flusso multimediale; Questa interfaccia deriva da [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream). È anche possibile usare questa interfaccia per creare esempi video. |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Consente di alleghi gli esempi video alle superfici DirectDraw; Questa interfaccia deriva dall'interfaccia [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) . Ogni superficie collegata include un rettangolo di ridimensionamento per semplificare il rendering. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elenco di interfacce di streaming multimediali](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



