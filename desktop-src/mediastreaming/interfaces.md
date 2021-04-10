---
title: Interfacce di streaming multimediale
description: L'API di streaming multimediale fornisce le interfacce seguenti.
ms.assetid: 1E25B452-D23C-4A1D-BC39-A5B719DF2C5D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6cdb1893af3170ae9ec5989498a007230992361
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103963650"
---
# <a name="media-streaming-interfaces"></a>Interfacce di streaming multimediale

L' [API di streaming multimediale](media-streaming-api-portal.md) fornisce le interfacce seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                 | Descrizione                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice)<br/>                           | Rappresenta un [**IBasicDevice**](ibasicdevice.md) attivo associato a un dispositivo UPnP. <br/>                                                                                                                                          |
| [**IActiveBasicDeviceStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics)<br/>             | Fornisce metodi statici per la creazione di oggetti [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) . <br/>                                                                                                                                            |
| [**IBasicDevice**](ibasicdevice.md)<br/>                                       | Incapsula i metodi e gli eventi necessari per modellare un dispositivo DLNA.<br/>                                                                                                                                                                         |
| [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)<br/>                             | Incapsula i metodi e gli eventi necessari per recuperare un elenco di renderer multimediali digitali (DMRs) memorizzati nella cache (DMSs) e/o Digital Media Server () o per trovare in modo asincrono i DMRs e/o DMSs attualmente in rete.<br/>              |
| [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                         | Incapsula i metodi necessari per fornire informazioni sull'icona di un dispositivo DLNA.<br/>                                                                                                                                                    |
| [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair)<br/>                                         | Rappresenta una coppia di oggetti [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) che comprende un renderer e un server.<br/>                                                                                                                 |
| [**IMediaRenderer**](imediarenderer.md)<br/>                                   | Incapsula i metodi e gli eventi necessari per rappresentare un dispositivo ricevitore (Digital Media Renderer) DLNA.<br/>                                                                                                                                        |
| [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)<br/> | Incapsula i metodi necessari per fornire informazioni sui metodi che possono essere attualmente richiamati in ricevitore.<br/>                                                                                                                             |
| [**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)<br/>                     | Incapsula i metodi necessari per creare in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia [**IMediaRenderer**](imediarenderer.md) .<br/>                                                                               |
| [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics)<br/>                   | Incapsula i metodi necessari per selezionare in modo asincrono un flusso.<br/>                                                                                                                                                                         |
| [**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)<br/>                       | Incapsula i metodi necessari per fornire informazioni sulle impostazioni correnti relative al trasporto di ricevitore. Queste impostazioni includono lo stato di trasporto corrente e le informazioni sui metodi che possono essere richiamati in ricevitore.<br/> |



 

 

