---
description: Interfacce di streaming multimediali
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Interfacce di streaming multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d654bae73ee822f553a1494e3b374cf35b8ac4a1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530559"
---
# <a name="multimedia-streaming-interfaces"></a>Interfacce di streaming multimediali

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.

 

Questa sezione contiene le voci di riferimento per tutte le interfacce di streaming multimediali e i relativi metodi, inclusi quelli supportati da Microsoft DirectShow.



| Interfaccia                                                  | Descrizione                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | Gestisce le connessioni interne tra i filtri DirectShow e i grafici di filtro nelle applicazioni che usano lo streaming multimediale.                            |
| [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Contiene i metodi per modificare gli esempi di flusso con tipi di supporto arbitrari.                                                                            |
| [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Contiene i metodi per la creazione di flussi multimediali con tipi di supporto arbitrari.                                                                            |
| [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | Espone la funzionalità DirectShow agli sviluppatori di flussi multimediali.                                                                                       |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | Fornisce metodi che consentono alle applicazioni di impostare e ottenere i dati audio sottostanti a cui faranno riferimento i flussi audio.                                   |
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | Controlla i flussi multimediali audio fornendo metodi che impostano e ottengono il formato del flusso.                                                                 |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | Recupera le informazioni dagli oggetti dati [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) sottostanti.                                                                |
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Controlla i flussi multimediali visualizzati in Microsoft® DirectDraw® surfaces.                                                                                  |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Fornisce metodi per l'impostazione e il recupero di puntatori alla superficie DirectDraw associata all'esempio di flusso corrente.                                    |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | Consente di accedere alle caratteristiche di un flusso multimediale, ad esempio il tipo di supporto e l'ID scopo del flusso. Dispone inoltre di metodi che creano esempi di dati. |
| [**IMediaStreamFilter**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | Supportato dal filtro del flusso multimediale, usato internamente dall'oggetto flusso multimediale. .                                                       |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | Contiene metodi che impostano e recuperano i dati di memoria sugli oggetti dati audio.                                                                               |
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | Fornisce metodi che controllano un flusso multimediale e forniscono l'accesso ai flussi multimediali sottostanti.                                                   |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | Fornisce il controllo sul comportamento degli esempi di flusso.                                                                                                   |



 

 

 



