---
title: Interfacce di streaming multimediale
description: L'API Streaming multimediale fornisce le interfacce seguenti.
ms.assetid: 1E25B452-D23C-4A1D-BC39-A5B719DF2C5D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb21c5c17502c887f78fa223ec2a2f8f814d3998bb75b81812eb4de9919f7342
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972190"
---
# <a name="media-streaming-interfaces"></a>Interfacce di streaming multimediale

[L'API Streaming](media-streaming-api-portal.md) multimediale fornisce le interfacce seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                 | Descrizione                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice)<br/>                           | Rappresenta un [**oggetto IBasicDevice**](ibasicdevice.md) attivo associato a un dispositivo UPnP. <br/>                                                                                                                                          |
| [**IActiveBasicDeviceStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics)<br/>             | Fornisce metodi statici per la creazione [**di oggetti IActiveBasicDevice.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) <br/>                                                                                                                                            |
| [**IBasicDevice**](ibasicdevice.md)<br/>                                       | Incapsula i metodi e gli eventi necessari per modellare un dispositivo DLNA.<br/>                                                                                                                                                                         |
| [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)<br/>                             | Incapsula i metodi e gli eventi necessari per recuperare un elenco di dmr (Digital Media Renderer) e/o server multimediali digitali (DMS) memorizzati nella cache o per trovare in modo asincrono le dmr e/o i dms attualmente in rete.<br/>              |
| [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                         | Incapsula i metodi necessari per fornire informazioni sull'icona di un dispositivo DLNA.<br/>                                                                                                                                                    |
| [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair)<br/>                                         | Rappresenta una coppia [**di oggetti ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) costituita da un renderer e un server.<br/>                                                                                                                 |
| [**IMediaRenderer**](imediarenderer.md)<br/>                                   | Incapsula i metodi e gli eventi necessari per rappresentare un dispositivo DLNA Digital Media Renderer (DMR).<br/>                                                                                                                                        |
| [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)<br/> | Incapsula i metodi necessari per fornire informazioni sui metodi che possono essere attualmente richiamati nella dmr.<br/>                                                                                                                             |
| [**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)<br/>                     | Incapsula i metodi necessari per creare in modo asincrono una nuova istanza di un oggetto che implementa [**l'interfaccia IMediaRenderer.**](imediarenderer.md)<br/>                                                                               |
| [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics)<br/>                   | Incapsula i metodi necessari per selezionare in modo asincrono un flusso.<br/>                                                                                                                                                                         |
| [**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)<br/>                       | Incapsula i metodi necessari per fornire informazioni sulle impostazioni correnti relative al trasporto della dmr. Queste impostazioni includono lo stato del trasporto corrente e informazioni sui metodi che possono essere attualmente richiamati nella dmr.<br/> |



 

 

