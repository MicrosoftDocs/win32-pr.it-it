---
title: Classe MediaRenderer
description: Implementa l'interfaccia IMediaRenderer che rappresenta un dispositivo ricevitore (Digital Media Renderer) DLNA.
ms.assetid: bac7898f-1334-4e28-92c7-6de464884eaf
keywords:
- API di streaming multimediale della classe MediaRenderer
- API di streaming multimediale della classe MediaRenderer, descritta
topic_type:
- apiref
api_name:
- MediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d14cdea89535fc680874905a9fb2b3358595baab
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516738"
---
# <a name="mediarenderer-class"></a>Classe MediaRenderer

Implementa l'interfaccia [**IMediaRenderer**](imediarenderer.md) che rappresenta un dispositivo ricevitore (Digital Media RENDERER) DLNA.

**MediaRenderer** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **MediaRenderer** dispone di questi metodi.



| Metodo                                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aggiungi \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828962(v=vs.85))        | Registra un gestore eventi per l'evento [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                       |
| [**Aggiungi \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828963(v=vs.85))        | Registra un gestore eventi per l'evento [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                       |
| [**GetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828964(v=vs.85))                                           | Esegue una query su ricevitore in modo asincrono per determinare se l'audio è attualmente disattivato o non disattivato.<br/>                                                                                                                                                                                                                                                                            |
| [**GetPositionInformationAsync**](/previous-versions/windows/desktop/legacy/hh828965(v=vs.85))             | Esegue una query su ricevitore in modo asincrono per recuperare le informazioni sulla posizione.<br/>                                                                                                                                                                                                                                                                                               |
| [**GetTransportInformationAsync**](/previous-versions/windows/desktop/legacy/hh828966(v=vs.85))           | Esegue una query su ricevitore in modo asincrono per recuperare le informazioni sul trasporto.<br/>                                                                                                                                                                                                                                                                                              |
| [**GetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828967(v=vs.85))                                       | Esegue una query su ricevitore in modo asincrono per il livello di volume audio corrente.<br/>                                                                                                                                                                                                                                                                                             |
| [**PauseAsync**](mediarenderer-pauseasync.md)                                               | Indica a ricevitore in modo asincrono di sospendere la riproduzione del contenuto corrente.<br/>                                                                                                                                                                                                                                                                                         |
| [**PlayAsync**](/previous-versions/windows/desktop/legacy/hh828972(v=vs.85))                                                 | Indica a ricevitore in modo asincrono di riprodurre il contenuto specificato chiamando il metodo [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))o [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) .<br/>                       |
| [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/legacy/hh828973(v=vs.85))                                   | Indica a ricevitore in modo asincrono di riprodurre il contenuto specificato chiamando il metodo [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))o [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) alla velocità specificata.<br/> |
| [**rimuovere \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828974(v=vs.85))  | Annulla la registrazione di un gestore eventi per l'evento [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                     |
| [**rimuovere \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828975(v=vs.85))  | Annulla la registrazione di un gestore eventi per l'evento [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                     |
| [**SeekAsync**](/previous-versions/windows/desktop/legacy/hh828976(v=vs.85))                                                 | Indica a ricevitore in modo asincrono di cercare un offset temporale particolare.<br/>                                                                                                                                                                                                                                                                                          |
| [**SetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828977(v=vs.85))                                           | Indica a ricevitore in modo asincrono di disattivare o disattivare l'audio.<br/>                                                                                                                                                                                                                                                                                           |
| [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828978(v=vs.85)) | Indica a ricevitore in modo asincrono di preparare il contenuto specificato per la riproduzione una volta terminata la riproduzione del contenuto corrente.<br/>                                                                                                                                                                                                                                   |
| [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828979(v=vs.85))           | Indica a ricevitore in modo asincrono di preparare il flusso multimediale specificato per la riproduzione una volta terminata la riproduzione del contenuto corrente.<br/>                                                                                                                                                                                                                              |
| [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828980(v=vs.85))                 | Indica a ricevitore in modo asincrono di preparare il contenuto identificato dall'URI specificato per la riproduzione al termine della riproduzione del contenuto corrente.<br/>                                                                                                                                                                                                             |
| [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85))         | Indica a ricevitore in modo asincrono di preparare il contenuto specificato per la riproduzione.<br/>                                                                                                                                                                                                                                                                                 |
| [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))                   | Indica a ricevitore in modo asincrono di preparare il flusso multimediale specificato per la riproduzione una volta terminata la riproduzione del contenuto corrente.<br/>                                                                                                                                                                                                                              |
| [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))                         | Indica a ricevitore in modo asincrono di preparare il contenuto identificato dall'URI specificato per la riproduzione.<br/>                                                                                                                                                                                                                                                           |
| [**SetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828984(v=vs.85))                                       | Imposta il livello di volume audio in ricevitore in modo asincrono sul valore specificato.<br/>                                                                                                                                                                                                                                                                                  |
| [**StopAsync**](mediarenderer-stopasync.md)                                                 | Indica a ricevitore in modo asincrono di arrestare la riproduzione del contenuto corrente.<br/>                                                                                                                                                                                                                                                                                          |



 

### <a name="properties"></a>Proprietà

La classe **MediaRenderer** dispone di queste proprietà.



| Proprietà                                                                | Tipo di accesso          | Descrizione                                                                                 |
|:------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------|
| [**ActionInformation**](mediarenderer-actioninformation.md)<br/> | Sola lettura<br/> | Ottiene informazioni sui metodi che possono essere attualmente richiamati in ricevitore.<br/>        |
| [**IsAudioSupported**](mediarenderer-isaudiosupported.md)<br/>   | Sola lettura<br/> | Ottiene un valore che indica se ricevitore è in grado di riprodurre contenuto audio.<br/> |
| [**IsImageSupported**](mediarenderer-isimagesupported.md)<br/>   | Sola lettura<br/> | Ottiene un valore che indica se ricevitore è in grado di visualizzare immagini.<br/>     |
| [**IsVideoSupported**](mediarenderer-isvideosupported.md)<br/>   | Sola lettura<br/> | Ottiene un valore che indica se ricevitore è in grado di riprodurre contenuto video.<br/> |



 

 

