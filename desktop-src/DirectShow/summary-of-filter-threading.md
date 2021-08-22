---
description: Riepilogo del threading del filtro
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: Riepilogo del threading del filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 048c151ed5fe69eea4cb0c81d01f43e97790b7223970791d3717adb9e15bea41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951740"
---
# <a name="summary-of-filter-threading"></a>Riepilogo del threading del filtro

Nel thread di streaming vengono chiamati i metodi seguenti:

-   [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

Nel thread dell'applicazione vengono chiamati i metodi seguenti:

-   Modifiche dello stato: [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).
-   Orologio di riferimento: [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).
-   Operazioni di aggiunta: [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin::Connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).
-   Funzioni allocatore: [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).
-   Flushing: [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).

L'elenco non è completo. Quando si implementa un filtro, è necessario considerare quali metodi modificano lo stato del filtro e quali metodi eseguono operazioni di streaming.

 

 



