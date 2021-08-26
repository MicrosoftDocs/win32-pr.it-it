---
description: Interfacce di streaming DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfacce di streaming DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11e7eec0ec7ad82c0046b8c052ff00093b496c05495ec38590d201724d7620e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983051"
---
# <a name="directdraw-streaming-interfaces"></a>Interfacce di streaming DirectDraw

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il [**filtro Grabber**](sample-grabber-filter.md) di esempio o implementare un filtro personalizzato per ottenere dati da un DirectShow di filtro.

 

Se si usano formati video supportati da DirectDraw nei flussi, le interfacce seguenti offrono un controllo più potente sui dati rispetto alle interfacce di base più generiche.



| Interfaccia                                                  | Descrizione                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Imposta e recupera il formato del flusso e l'oggetto DirectDraw associato al flusso multimediale. questa interfaccia deriva da [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream). È anche possibile usare questa interfaccia per creare esempi video. |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Consente di associare esempi video alle superfici DirectDraw. questa interfaccia deriva [**dall'interfaccia IStreamSample.**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) Ogni superficie collegata include un rettangolo di ritaglio per semplificare il rendering. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elenco di interfacce di streaming multimediale](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



