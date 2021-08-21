---
description: Interfacce di streaming multimediale
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Interfacce di streaming multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b38200d98b0f01b7260508cbf7bd19c6e65efdfb3af78f2efff77be38294e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152957"
---
# <a name="multimedia-streaming-interfaces"></a>Interfacce di streaming multimediale

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il [**filtro Sample Grabber**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico DirectShow filtro personalizzato.

 

Questa sezione contiene voci di riferimento per tutte le interfacce di streaming multimediale e i relativi metodi, inclusi quelli supportati da Microsoft DirectShow.



| Interfaccia                                                  | Descrizione                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | Gestisce le connessioni interne tra i DirectShow e i grafici dei filtri nelle applicazioni che usano lo streaming multimediale.                            |
| [**Esempio IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Contiene metodi per la modifica di esempi di flussi con tipi di supporti arbitrari.                                                                            |
| [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Contiene metodi per la creazione di flussi multimediali con tipi di elementi multimediali arbitrari.                                                                            |
| [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | Espone DirectShow funzionalità agli sviluppatori di flussi multimediali.                                                                                       |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | Fornisce metodi che consentono alle applicazioni di impostare e ottenere i dati audio sottostanti a cui farà riferimento i flussi audio.                                   |
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | Controlla i flussi multimediali audio fornendo metodi che impostano e ottengono il formato del flusso.                                                                 |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | Recupera informazioni dagli oggetti dati [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) sottostanti.                                                                |
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Controlla i flussi multimediali visualizzati nelle superfici ® Microsoft® DirectDraw.                                                                                  |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Fornisce metodi che impostano e recuperano puntatori alla superficie DirectDraw associata all'esempio di flusso corrente.                                    |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | Fornisce l'accesso alle caratteristiche di un flusso multimediale, ad esempio il tipo di supporto e l'ID scopo del flusso. Include anche metodi che creano esempi di dati. |
| [**IMediaStreamFilter**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | Supportato dal filtro Media Stream, che viene usato internamente dall'oggetto flusso multimediale. .                                                       |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | Contiene metodi che impostano e recuperano dati di memoria su oggetti dati audio.                                                                               |
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | Fornisce metodi che controllano un flusso multimediale e forniscono l'accesso ai flussi multimediali sottostanti.                                                   |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | Fornisce il controllo sul comportamento degli esempi di flusso.                                                                                                   |



 

 

 



